---
layout: '../../layouts/MarkdownPost.astro'
title: 'Basic commands of Anaconda '
pubDate: 2023-07-05
description: ''
author: 'Space Cat'
cover:
    url: ''
    square: ''
    alt: ''
tags: ["Code"]
theme: 'light'
featured: true
---
1.Listing packages and environments
conda info -e
conda list
conda list --name <env name>
conda list -p <env path>

2.Delete packages and environments
conda remove -n <env name> packages
conda remove -n <env nanme> --all