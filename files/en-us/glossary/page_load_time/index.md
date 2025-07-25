---
title: Page load time
slug: Glossary/Page_load_time
page-type: glossary-definition
sidebar: glossarysidebar
---

**Page load time** is the time it takes for a page to load, measured from [navigation start](/en-US/docs/Web/API/PerformanceTiming/navigationStart) to the [start of the load event](/en-US/docs/Web/API/PerformanceTiming/loadEventStart).

```js
let time = performance.timing;

let pageloadTime = time.loadEventStart - time.navigationStart;
```

While page load time 'sounds' like the perfect web performance metric, it isn't. Load times can vary greatly between users depending on device capabilities, network conditions, and, to a lesser extent, distance from the server. The development environment, where page load time is measured, is likely an optimal experience, not reflective of your users' reality. In addition, web performance isn't just about when the load event happens. It's also about {{Glossary("perceived performance")}}, responsiveness, {{Glossary("jank")}} and jitter.

## See also

- [Navigation and resource timing](/en-US/docs/Web/Performance/Guides/Navigation_and_resource_timings)
- {{domxref("PerformanceNavigationTiming")}}
- {{domxref("PerformanceResourceTiming")}},
