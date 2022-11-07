# How to configure proxy for

The goal of this repo is to free yourself from endless search on Google how to configure proxy for dev tools foo, bar and baz.

PRs and issues are welcomed.

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
