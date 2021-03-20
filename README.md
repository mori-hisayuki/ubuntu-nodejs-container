# Ubuntu Nodejs Remote Container

実際に使っているときのディレクトリ構造

```
|--.devcontainer
|  |--devcontainer.env
|  |--devcontainer.json
|  |--docker-compose.yml
|  |--ubuntu
|  |  |--Dockerfile
|  |--ssh
|  |  |--config
|  |  |--github
|  |  |--github.pub
|  |  |--known_hosts
|--.gitignore
|--README.md
```



## Githubへの接続
- Host側の`.ssh`と同じ設定


## 環境変数
- `.devecontainer`の直下に`devcontainer.env`ファイルを配置すると読み込まれる
- `docker-compose.yml`で読み込む設定になっているため空ファイルで作成してください
    - もし作成したくない場合は`docker-compose.yml`から設定を外してください(13行目: `env_file: devcontainer.env`)
    - `devcontainer.env`はGithub上にあげないほうがよいこともあるので、デフォルトでは`.gitignore`の対象にしています

## default Extension(上から順)
- Vim
- Git Graph
- vscode-icons
- gitflow
- GitLens
- Indent-Rainbow
- Path Autocomplete
- Prettier
- REST Client
- TabNine Autocomplete
- GitHub Pull Requests and Issues
- Code Spell Checker
- Live Server
- Svelte for VS Code
- Tailwind CSS IntelliSense


必要に応じて、追加削除をしてください。
`devcontainer.json`の`extension`を編集