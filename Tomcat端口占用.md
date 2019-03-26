# Tomcat 端口被占用

## 概述

> Tomcat不正常关闭，经常会导致再启动端口时，显示端口被占用

## 解决方法

### 查询占用8080端口的线程
> netstat -ano

### 找到占用端口的进程ID
> netstat -aon|findstr 端口号

### 查询出占用程序名称
> tasklist|findstr 进程ID

### 杀死应用程序
> taskkill /f/t/im 应用程序名称