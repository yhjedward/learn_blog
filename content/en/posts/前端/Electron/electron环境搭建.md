---
title: "Electron环境搭建"
date: 2023-12-02T10:34:56+08:00
categories: ["前端"]
tags: ["Electron"]
draft: false
---

# 概述

## 配置安装 electron

1. nodejs官网下载安装 nodejs.js.
2. 使用 npm 安装 pnpm
```shell
npm install -g pnpm
```
3. 创建目标项目文件夹
```shell
mkdir electron_Project
```
4. 在当前文件夹下使用 pnpm 快速生成 package.json 默认配置
```shell
pnpm init
``` 
5. 使用 pnpm 安装 electron
```shell
pnpm add -D electron
```

## 配置 main.js 文件
