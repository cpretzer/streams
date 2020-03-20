# Episode 002
# Episode 002

## Intro and Overview
1. Welcome to the Stream
2. Topic
  - Canary Deployments with SMI, Flagger, and Linkerd
3. Resources
  - Outline: This document
  - Example files: Canary Deployments in [Demo Repository](https://github.com/cpretzer/demos)
    - `git clone git@github.com:cpretzer/demos`
    - `cd canary-deployments`

## The Main Show
  - Pre-Deployed Components
    - [Linkerd](https://linkerd.io/getting-started)
      - Includes API Resources for [SMI](https://smi-spec.io)
    - [Flagger](https://docs.flagger.app/tutorials/linkerd-progressive-delivery)
    - [Cheatsheet](https://github.com/cpretzer/demos/)
  - Cluster provided by [Digital Ocean](https://www.digitalocean.com/products/kubernetes/)
    - This can just as easily be run locally, but I like having a public endpoint

### Linkerd
  - Control Plane
  - Injection
  - mTLS

### Flagger
  - View Flagger component and logs
  - Canary resource
    - Review definition

 ### Traffic Split
   - SMI
   - Review TrafficSplit resource
     - Apex
     - Leaf

### Watch a rollout

### Putting it all together
   - Prometheus metrics from Linkerd proxies
   - Flagger deplpoyment


## Wrap Up
* Q & A?
* [Streams Repository](https://github.com/cpretzer/streams)
  * [This Episode](https://github.com/cpretzer/streams/Episode_002)
  * Create Issues/PRs for Feedback
  * Find me on [Slack](https://linkerd.slack.io) @charles
