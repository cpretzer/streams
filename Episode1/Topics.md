# Episode 1
## Intro and Overview
1. Why I'm streaming
  1. [LinkedIn](https://www.linkedin.com/in/charlespretzer/)
2. Initial setup and asking for recommendations
  1. Really basic
     1. MacBook Pro
     2. [OBS](https://obsproject.com/)
     3. [Azure Clusters and VMs](https://azure.microsoft.com/en-us/)
## Main Content     
1. Walk through [Prometheus Federation](https://prometheus.io/docs/prometheus/latest/federation/)
  1. What is [Prometheus](https://prometheus.io/)
    1. Why does it matter?
        * Becoming accepted as the standard for consuming telemetry
        * Relatively easy entrypoint
        * [Mature software](https://en.wikipedia.org/wiki/Prometheus_(software))
  2. What is federation
    * Using one prometheus to scrape metrics from another instance of prometheus
    * Gives the "suits" the "single pane of glass" that they like
  3. Example
    * k8s cluster running a demo application
    * [Linkerd Service Mesh](https://linkerd.io)
      * Deploys with a short-term Prometheus instance
        * Stores 6 hours of data
        * Meant to be federated with a production-grade Prometheus installation in order to get meaningful long-term metrics
    * [NGINX Ingress](https://kubernetes.github.io/ingress-nginx/) to provide an entry point to the `linkerd-prometheus` pod
    * `kubectl port-forward svc/web-svc -n emojivoto 8080:80`
      * [Application UI](http://localhost:8080)
    * `kubectl port-forward svc/linkerd-prometheus -n linkerd 9099:9090`
      * [Prometheus UI](http://localhost:9099)
    * Azure VM running a prometheus process: [UI](http://episode1-prom.pretzer.dev:9090)
      * start command `prometheus --config.file=linkerd-prometheus.yml --log.level=debug`
      * Look at the config file
## Wrap Up
* Q & A?
* [Streams Repository](https://github.com/cpretzer/streams)
  * [This Episode](https://github.com/cpretzer/streams/Episode1)
  * Create Issues/PRs for Feedback
  * Find me on [Slack](https://linkerd.slack.io)
