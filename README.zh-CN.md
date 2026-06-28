# Frontend Harness Slides

**[English](README.md)**

`frontend-harness-slides` 把幻灯片当成一个真正的工程项目来做：Playwright **harness** 守护每一帧、**registry** 把顺序与文件名解耦、绝对 16:9 **stage** 保证任何屏幕上版式一致。相比单体 HTML slides 高一档——稳健、可维护，随着 deck 增长和多次编辑也不易改坏。

## 安装

```bash
npx skills add patrick-fu/frontend-harness-slides
```

后续更新：

```bash
npx skills update
```

## 它能做什么

- **用 registry 而非文件名**：中心数组掌管顺序，插入一页不必重命名文件、不会打断快照（告别“重构序号地狱”）。
- **绝对 16:9 舞台**：内容锁在虚拟 1920×1080 画布上整体缩放，不做按设备 reflow。
- **真正的测试 harness**：Playwright 把动画冻结成稳定帧、逐 scene/beat 做像素回归、审计布局（16px 字号下限、元素不得逸出舞台）。harness 全绿才算改完。
- **为长期迭代而建**：query 路由状态（`?scene=&beat=`）、肉眼挑主题、PDF 导出、query-safe 的 Vercel 部署，全部为长期维护接好线。

## 何时用它

当你要的是一套**随增长仍然稳固**、可长期创建/扩展/重构的演示，而不是一次性的单文件 deck 时，用它。

## 更多 Skills

更多可复用的 agent skills，见
[Awesome Skills](https://github.com/patrick-fu/awesome-skills)。
