---
tags:
- documentation
title: 安装
weight: 1
---


## 在R中安装

用户可以从使用`devtools` 或者 [`pak`](https://pak.r-lib.org/) 从[GitHub](https://github.com/obenno/scSpotlight)上安装, 
或者直接使用r-universe作为安装源. 我们推荐使用`pak`作为安装工具, 速度
相对传统方式快很多, 两者都需要先从CRAN上安装相应的package.

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
devtools::install_github("obenno/scSpotlight@v0.0.2")
```
{{% /tab %}}
{{% tab title="pak from github" %}}
```r
# install.packages("pak")
pak::pkg_install("obenno/scSpotlight@v0.0.2")
```
{{% /tab %}}
{{< /tabs >}}


## Docker

用户如果有安装docker, 也可以选择使用我们准备好的docker image. 拉取image使用如下命令:

```
docker pull registry-intl.cn-hangzhou.aliyuncs.com/thunderbio/scspotlight:0.0.2
```

在特定的端口(如`8081`端口)运行app, 请使用如下命令:

```
docker run -p 8081:8081 registry-intl.cn-hangzhou.aliyuncs.com/thunderbio/scspotlight:0.0.2 Rscript -e 'scSpotlight::run_app(options = list(port=8081, host="0.0.0.0", launch.browser = FALSE), runningMode="processing")'
```
    