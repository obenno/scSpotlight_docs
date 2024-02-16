---
title: Installation
tags: ["documentation", "installation"]
categories: ["Introduciton"]
weight: 1
---


## Installation via R

One can install scSpotlight from [GitHub](https://github.com/obenno/scSpotlight) with `devtools`
or from [r-universe](https://r-universe.dev).  We recommend to use [`pak`](https://pak.r-lib.org/) 
instead of traditional way, as it's much faster.

{{< tabs >}}
{{% tab title="traditional way from r-universe" %}}
```r
# Install scSpotlight in R:
install.packages('scSpotlight', repos = c('https://obenno.r-universe.dev', 'https://cloud.r-project.org'))
```
{{% /tab %}}
{{% tab title="pak from r-universe" %}}
```r
# install.packages('pak')
pak::repo_add(scSpotlight = "https://obenno.r-universe.dev")
pak::pkg_install("scSpotlight")
```
{{% /tab %}}
{{% tab title="devtools from github" %}}
```r
# install.packages("devtools")
devtools::install_github("obenno/scSpotlight@v0.0.3")
```
{{% /tab %}}
{{% tab title="pak from github" %}}
```r
# install.packages("pak")
pak::pkg_install("obenno/scSpotlight@v0.0.3")
```
{{% /tab %}}
{{< /tabs >}}


## Docker

To pull the latest image from the command line

```
docker pull registry-intl.cn-hangzhou.aliyuncs.com/thunderbio/scspotlight:0.0.2
```

To run the app on specific port (e.g. `port:8081`), please use the command below:

```
docker run -p 8081:8081 registry-intl.cn-hangzhou.aliyuncs.com/thunderbio/scspotlight:0.0.2 Rscript -e 'scSpotlight::run_app(options = list(port=8081, host="0.0.0.0", launch.browser = FALSE), runningMode="processing")'
```
