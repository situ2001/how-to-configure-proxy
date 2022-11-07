# How to configure proxy for

The goal of this repo is to free yourself from endless search on Google for guides and docs that tell you how to configure proxy for dev tools like github, npm and so on.
PRs and issues are welcomed.

## My environment

App clash opens port 7890 for http and socks proxy. This may be a common proxy env in mainland China.

## git

Basic form. Just globally configured once.

```shell
git config --global http.proxy http://<proxy.server>:<port> # without username and password
git config --global http.proxy http://<proxy_username:proxy_password>@<proxy.server>:<port> # with username and password
```

Used by myself (App Clash that opens port 7890 for http and socks proxy)

```shell
git config --global http.proxy http://127.0.0.1:7890
```

## npm

```shell
npm --proxy http://<proxy_username:proxy_password>@<proxy.server>:<port> i <name_of_package>
```

For example

```shell
npm --proxy http://127.0.0.1:7890 i -g yarn
```
