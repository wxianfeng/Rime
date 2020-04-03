wxianfeng Rime 输入法配置
====

## 优点
* 简约
* 隐私性好
* 强大的自定义能力

## 安装
https://rime.im/download/

Mac 版本下载 鼠鬚管，我安装的是 0.14.0 版本

## 选择输入法
`ctrl` + `~` 键切换
简体中文选择: 朙月拼音・简化字

## 安装 rime-install
`curl -fsSL https://git.io/rime-install | bash`

## 安装 Emoji 插件
`bash plum/rime-install emoji`

给输入法添加 emoji 插件
`bash plum/rime-install emoji:customize:schema=luna_pinyin_simp`

重新 deploy 后可以使用表情

## 设置候选词个数
`vi default.yaml`
```
menu:
  page_size: 8
```

## 词频统计
自带词频统计，输入频率高的会显示在最前面

## 设置颜色
`touch squirrel.custom.yaml`

内容如下:
[squirrel.custom.yaml](./squirrel.custom.yaml)

## 使用符号
`vi luna_pinyin_simp.custom.yaml`
```
patch:
  punctuator/import_preset: symbols
  recognizer/patterns/punct: '^/([0-9]0?|[A-Za-z]+)$’
```

## 自定义符号
`vi symbols.yaml`
```
'/hm': [✓, 🗹, ✗, ☒]
```

输入法状态下输入 `/hm` 就会出现符号候选

## 设置模糊音
`vi luna_pinyin_simp.custom.yaml`
添加如下内容:
https://gist.github.com/lotem/2320943

需要模糊的去掉前面 # 注释

## 阿里土话
输入 `/ali` 后出现候选

## 提示
### 终端无法输入中文
    需要按下 shift 键，默认在 terminal 中是英文输入状态