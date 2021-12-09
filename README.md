 ![Repo](https://ee2c-109-252-71-113.ngrok.io/zpm-shields/repo/mode?module=sergeymi37%2Fappmsw-zpm-shields&color=gold)
 ![Registry](https://ee2c-109-252-71-113.ngrok.io/zpm-shields/registry/mode?project=zpm-shields&color=F4A460)
 
 ![Repo+Registry](https://ee2c-109-252-71-113.ngrok.io/zpm-shields/both/mode?module=sergeymi37%2Fappmsw-zpm-shields&project=zpm-shields)
## zpm-shields
 
 [![Quality Gate Status](https://community.objectscriptquality.com/api/project_badges/measure?project=intersystems_iris_community%2Fappmsw-zpm-shields&metric=alert_status)](https://community.objectscriptquality.com/dashboard?id=intersystems_iris_community%2Fappmsw-zpm-shields)
 <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/SergeyMi37/appmsw-zpm-shields">
 
 Service for displaying version numbers of ZPM and OEX registry in badges.
 I always wanted to know what version of the project is in the repository without looking at the module file. Hml and how it relates to the public repository version. Is it time to update the release or not?

## Installation with ZPM

If ZPM the current instance is not installed, then in one line you can install the latest version of ZPM.
```
zn "%SYS" d ##class(Security.SSLConfigs).Create("z") s r=##class(%Net.HttpRequest).%New(),r.Server="pm.community.intersystems.com",r.SSLConfiguration="z" d r.Get("/packages/zpm/latest/installer"),$system.OBJ.LoadStream(r.HttpResponse.Data,"c")
```
If ZPM is installed, then `zpm-shields` can be set with the command
```
zpm:USER>install zpm-shields
```
## Installation with Docker

## Prerequisites
Make sure you have [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [Docker desktop](https://www.docker.com/products/docker-desktop) installed.

## Installation 
Clone/git pull the repo into any local directory

```
git clone https://github.com/SergeyMi37/appmsw-zpm-shields
```

Open the terminal in this directory and run:

```
docker-compose build
```

3. Run the IRIS container with your project:

```
docker-compose up -d
```
After installation, you will have a service to which you need to provide access without authentication.
## Using these links you can get a svg file that can be inserted into README.MD
```
![Repo](http://localhost:52773/zpm-shields/repo/mode?module=https:%2F%2Fgithub.com%2FSergeyMi37%2Fzapm&color=blue)
```
![](https://raw.githubusercontent.com/SergeyMi37/appmsw-zpm-shields/master/doc/Screenshot_1.png)
```
![Registry](http://localhost:52773/zpm-shields/registry/mode?project=appmsw-dbdeploy&color=gold)
```
![](https://raw.githubusercontent.com/SergeyMi37/appmsw-zpm-shields/master/doc/Screenshot_2.png)
```
![Repo+Registry](http://localhost:52773/zpm-shields/both/mode?module=sergeymi37%2Fappmsw-dbdeploy&project=appmsw-dbdeploy&color=FFA07A)
```
![](https://raw.githubusercontent.com/SergeyMi37/appmsw-zpm-shields/master/doc/Screenshot_3.png)

You can forward your local address outside with the [`ngrok`](https://ngrok.com/) utility for test.
