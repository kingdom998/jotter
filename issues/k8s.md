## 问题总结

## [命令行格式错乱](https://stackoverflow.com/questions/43144822/disabling-network-logs-on-kubernetes-when-running-kubectl-exec)
```text
) Data frame handling
                     I0331 17:46:15.486652    3807 logs.go:41] (0xc4201158c0) Data frame received for 5
                                                                                                       I0331 17:46:15.486671    3807 logs.go:41] (0xc42094a000) (5) Data frame handling
                                                                                                                                                                                       I0331 17:46:15.486682    3807 logs.go:41] (0xc42094a000) (5) Data frame sent
                                                                                                                                                                                                                                                                   root@hello-node-2399519400-6q6s3:/# I0331 17:46:16.667823    3807 logs.go:41] (0xc420687680) (3) Writing data frame
                                                  I0331 17:46:16.669223    3807 logs.go:41] (0xc4201158c0) Data frame received for 5
                                                                                                                                    I0331 17:46:16.669244    3807 logs.go:41] (0xc42094a000) (5) Data frame handling
                                                                                                                                                                                                                    I0331 17:46:16.669254    3807 logs.go:41] (0xc42094a000) (5) Data frame sent

root@hello-node-2399519400-6q6s3:/# I0331 17:46:17.331753    3807 logs.go:41] (0xc420687680) (3) Writing data frame
                                                                                                                   I0331 17:46:17.333338    3807 logs.go:41] (0xc4201158c0) Data frame received for 5
                                                                                                                                                                                                     I0331 17:46:17.333358    3807 logs.go:41] (0xc42094a000) (5) Data frame handling
                                                                                                                                                                                                                                                                                     I0331 17:46:17.333369    3807 logs.go:41] (0xc42094a000) (5) Data frame sent

I0331 17:46:17.333922    3807 logs.go:41] (0xc4201158c0) Data frame received for 5
                                                                                  I0331 17:46:17.333943    3807 logs.go:41] (0xc42094a000) (5) Data frame handling
                                                                                                                                                                  I0331 17:46:17.333956    3807 logs.go:41] (0xc42094a000) (5) Data frame sent
                                                                                                                                                                                                                                              root@hello-node-2399519400-6q6s3:/# I0331 17:46:17.738444    3807 logs.go:41] (0xc420687680) (3) Writing data frame
                             I0331 17:46:17.740563    3807 logs.go:41] (0xc4201158c0) Data frame received for 5
                                                                                                               I0331 17:46:17.740591    3807 logs.go:41] (0xc42094a000) (5) Data frame handling
                                                                                                                                                                                               I0331 17:46:17.740606    3807 logs.go:41] (0xc42094a000) (5) Data frame sent
```
## 解决办法：
```shell
unset DEBUG
```