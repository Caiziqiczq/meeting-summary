# FA 会议纪要助手

> 投资人沟通记录 · 结构化整理 · 一键复制

浏览器直接使用，无需安装，手机电脑均可访问。

**线上地址：** https://caiziqiczq.github.io/meeting-summary/

---

## 功能介绍

将与投资人通话后的转写文字粘贴进来，自动调用 DeepSeek AI 整理为结构化会议纪要，生成后可直接点击编辑，一键复制粘贴到微信、飞书或公司系统。

### 输出的 9 个固定大类（顺序固定）

| # | 分类 | 说明 |
|---|------|------|
| 1 | 个人情况 | 职业经历、过往任职、专业背景 |
| 2 | 机构情况 | 成立背景、性质定位、业务范围 |
| 3 | 团队情况 | 团队规模、核心人员、内部分工 |
| 4 | 投资偏好 | 偏好行业/阶段/金额、地域、研究方向 |
| 5 | 基金情况 | 基金名称、规模、LP 构成、已投项目 |
| 6 | 落地返投情况 | 返投要求、比例、落地城市 |
| 7 | 投资动态 | 近期案例、年度 KPI、出手频率 |
| 8 | 决策情况 | 决策流程、关键决策人、决策周期 |
| 9 | 其他 | 不属于以上分类的重要信息 |

每个大类的子项由 AI 根据实际内容动态生成，没有提及的内容直接跳过。

---

## 使用方法

1. 打开 https://caiziqiczq.github.io/meeting-summary/
2. 首次使用填入 DeepSeek API Key（自动保存到本地，下次无需重填）
3. 填写会议日期、投资人姓名、机构名称
4. 粘贴通话转写文字
5. 点击「生成纪要」，等待 AI 输出
6. 点击任意内容可直接编辑修改
7. 点击「复制全文」，粘贴到目标系统

---

## 技术说明

- **部署方式：** GitHub Pages，单文件，无后端
- **AI 模型：** DeepSeek `deepseek-chat`，max_tokens 6000
- **API Key 存储：** 浏览器 `localStorage`，不上传服务器
- **UI：** Tailwind CSS CDN + Noto Sans SC，响应式布局

---

## 本地开发

```bash
git clone https://github.com/Caiziqiczq/meeting-summary.git
cd meeting-summary
# 直接用浏览器打开 index.html 即可
open index.html
```

修改 `index.html` 后推送到 `main` 分支，GitHub Pages 自动更新（约 1 分钟生效）。
