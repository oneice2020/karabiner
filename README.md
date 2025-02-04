# 设置输入法切换快捷键为 ⌃ + Shift + F12
<details>
  <summary>为避免和 IntelliJ IDEA Ultimate 的 ⌃ + Space 快捷键冲突，修改输入法切换快捷键为 ⌃ + Shift + F12：</summary>
  <img width="751" alt="image" src="https://github.com/oneice2020/karabiner/assets/46884636/4beb7593-728b-44a5-997e-5a4fdea3d018">
</details>

# Karabiner 单键切换输入法配置

通过 短按 ( `⌘` | `⌥` ) 切换 `中`、`英` 输入法

1. 短按 左 Command `⌘` 轮换 `ZH`
2. 短按 左 Command `⌘` 切换 `ZH` **（与前一项冲突，请二选一）**
3. 短按 右 Command `⌘` 切换 `EN`
4. 短按 左 Option `⌥` 切换 `EN`

5. 短按 左 Shift `⇧` 轮换
6. 短按 左 Shift `⇧` 切换 `EN` **（与前一项冲突，请二选一）**

7. 短按 `Caps Lock` 切换 `EN`，并替换 `Caps Lock` 为组合键：⌃ + ⌘ + ⌥ + ⇧
8. 短按 `Caps Lock` 轮换，并替换 `Caps Lock` 为组合键：⌃ + ⌘ + ⌥ + ⇧ **（与前一项冲突，请二选一）**

9. ~~长按 `Caps Lock` 锁定 `大小写`~~

## 安装

### 第一种：远程导入

复制到浏览器打开

```
karabiner://karabiner/assets/complex_modifications/import?url=https://raw.githubusercontent.com/oneice2020/karabiner/main/karabiner.json
```

### 第二种：本地安装

把 `karabiner.json` 复制到: `~/.config/karabiner/assets/complex_modifications` 下

## 然后

1. 只保留 `ABC` 和 `中文` 两种输入法
2. 关掉中文输入法的 `中英` 切换快捷键

## 为什么？

由于，我们码字的时候经常不知道当前是处于哪个输入法，中文输入法还有 `中` \ `英` 两种状态

另外， `macOS` 切换 `中` \ `英` 状态时还有可能会失败 (延时原因)

所以，我希望：

1. 短按 `⌘` 的时候切到 `中文` 输入法
2. 短按 `⌥` 的时候切到 `英文` 文输入法

这样我就不用盲猜当前输入法是什么状态了

## 其他说明

### 关于：1. 短按 左 Command `⌘` 轮换 `ZH`，为什么要叫 `轮换` ?

因为指定切换与中文输入法会不稳定出 BUG (显示切到中文了，但实际打出来的还是英文)

所以切换中文实现的方式是： 模拟一次 `⌃` + `space`

这样做的好处是切换不会出 BUG

坏处是系统只能保留 `ABC` 和 `中文` 两种输入法

### 关于：6. 替换 `Caps Lock` 为组合键: `⌃` + `⌘` + `⌥` + `⇧`

因为我有些快捷键是：

`⌃` + `⌘` + `⌥` + `⇧` + `D`：选词翻译

`⌃` + `⌘` + `⌥` + `⇧` + `S`：识图翻译

`⌃` + `⌘` + `⌥` + `⇧` + `C`：使用 Code 打开当前目录

`⌃` + `⌘` + `⌥` + `⇧` + `T`：使用 终端 打开当前目录

这样我只需要 `Caps Lock` + `D` 就可以选词翻译了

> 如果不需要，可以 `Remove` 这个映射
