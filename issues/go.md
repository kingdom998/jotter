
* go mod tidy 报错
  ```
  gitlab.pixocial.com/themeu-ai/themeu-api/api/middleware imports
        go.opentelemetry.io/otel/attribute tested by
        go.opentelemetry.io/otel/attribute.test imports
        github.com/google/go-cmp/cmp: gitlab.pixocial.com/manhattan/pkg@v0.0.2: reading gitlab.pixocial.com/manhattan/pkg/go.mod at revision v0.0.2: git ls-remote -q origin in /Users/pixocial.001/go/pkg/mod/cache/vcs/6ce7c5a3a4e424c377ad50f05d932e4a2d7a17634106b8cb4c611371dfb711c9: exit status 128:
        fatal: could not read Username for 'https://gitlab.pixocial.com': terminal prompts disabled
    Confirm the import path was entered correctly.
    If this is a private repository, see https://golang.org/doc/faq#git_https for additional information.
    ```
  
    * 解决方法：
  [参考链接](https://go.dev/doc/faq#git_https)
  <br>
  修改 git 配置，将go get 获取包的方式由 https 改为ssh
    ```
    [url "ssh://git@github.com/"]
	insteadOf = https://github.com/

    ```