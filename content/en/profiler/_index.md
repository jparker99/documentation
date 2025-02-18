---
title: Continuous Profiler
kind: Documentation
aliases:
    - /tracing/profiling/
    - /tracing/profiler/
further_reading:
    - link: '/profiler/enabling'
      tag: 'Documentation'
      text: 'Enable continuous profiler for your application'
    - link: 'getting_started/profiler'
      tag: 'Documentation'
      text: 'Getting Started with Continuous Profiler'
    - link: 'profiler/search_profiles'
      tag: 'Documentation'
      text: 'Learn more about available profile types'
    - link: '/developers/guide/data-collection-resolution-retention/'
      tag: 'Documentation'
      text: 'Data collection, resolution, and retention'
    - link: 'https://www.datadoghq.com/blog/introducing-datadog-profiling/'
      tag: 'Blog'
      text: 'Introducing always-on production profiling in Datadog'
    - link: 'https://www.datadoghq.com/blog/datadog-github-action-vulnerability-analysis/'
      tag: 'Blog'
      text: 'Datadog GitHub Action for continuous vulnerability analysis'
    - link: 'https://www.datadoghq.com/blog/code-optimization-datadog-profile-comparison/'
      tag: 'Blog'
      text: 'Compare and optimize your code with Datadog Profile Comparison.'
    - link: 'https://www.datadoghq.com/blog/engineering/how-we-optimized-our-akka-application-using-datadogs-continuous-profiler/'
      tag: 'Blog'
      text: 'How we optimized our Akka application using Datadog’s Continuous Profiler'
    - link: 'https://www.datadoghq.com/blog/ruby-profiling-datadog-continuous-profiler/'
      tag: 'Blog'
      text: 'Analyze Ruby code performance with Datadog Continuous Profiler'

---

{{< vimeo 441865141 >}}

</br>

Find CPU, memory, and IO bottlenecks, broken down by method name, class name, and line number, to significantly reduce end-user latency and infrastructure costs.

### Low impact in production

Continuous profiler runs in production across all services by leveraging technologies such as JDK Flight Recorder to have minimal impact on your host's CPU and memory usage.

## Getting started

Profiling your service to visualize all your stack traces in one place takes just minutes.

### Instrument your application

{{< partial name="profiling/profiling-languages.html" >}}

## Guide to using the profiler

The [Getting Started with Profiler][1] guide takes a sample service with a performance problem and shows you how to use Continuous Profiler to understand and fix the problem.

## Explore Datadog profiler

After you've configured your application to send profiles to Datadog, start getting insights into your code performance. By default, profiles are retained for 7 days, and metrics generated from profile data are retained for 1 month.

### Search profiles by tags

[Use tags to search profiles][2] across any dimension—whether it’s a specific host, service, version, or any combination.

{{< img src="profiler/search_profiles.mp4" alt="Search profiles by tags" video=true >}}

### Track function performance over deployments

Obtain key profiling metrics from services such as top CPU usage by method, top memory allocations by thread, and CPU usage by version to visualize in your dashboards.

{{< img src="profiler/profiling-metric-dashboard.mp4" alt="Add profiling metrics to your dashboards." video=true >}}

### Connect traces to profiling data

Application processes that have both [APM distributed tracing][3] and continuous profiler enabled are automatically linked, so you can move directly from span information to profiling data on the [Code Hotspots tab][4] to find specific lines of code related to performance issues.

{{< img src="profiler/code_hotspots_tab.mp4" alt="Code Hotspots tab shows profiling information for a APM trace span" video=true >}}

### Find changes in performance by comparing profiles

Comparing similar profiles from different times, environments, or deployments can help you understand the possible causes of and solutions to performance problems. The Datadog profiler offers [comparison visualizations][5] to make sense of why profiles are different based on time frames or tags that you scope by. 

## Further Reading

{{< partial name="whats-next/whats-next.html" >}}

[1]: /getting_started/profiler/
[2]: /profiler/search_profiles
[3]: /tracing/
[4]: /profiler/connect_traces_and_profiles/
[5]: /profiler/compare_profiles/
