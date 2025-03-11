# sdk

## 使用 pnpm workspace

阻止使用 bootstrap、link 和 add 命令。相反，您应该直接使用 pnpm 命令来管理依赖项

```json
{
	"dependencies": {
		"some-package": "workspace:*"
	}
}
```

-   workspace：这是关键字，用于表明该依赖是指向工作区内的某个包，而不是外部的 npm 包。它是多包管理工具（如 pnpm、yarn workspaces 等）识别工作区依赖的标识。
-   *：这里的星号是一个通配符，表示匹配任意版本。也就是说，当使用 workspace:*时，它会匹配工作区内同名包的任意版本，工具会根据工作区的配置和实际情况，自动解析为具体的版本。
