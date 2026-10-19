# YFX · AI个人档案 部署包

> 东北哥 · 深圳市量化供应链有限公司 · 海南偏爱投资有限公司 · 品牌「易复兴YFX」
> 用途：将本档案与AI资产上传 GitHub 存档，并用 Cloudflare 连接部署为可访问页面。

---

## 一、包内文件

| 文件 | 用途 |
|------|------|
| `东北哥_AI个人档案.html` | 四板块个人档案（①两家公司 ②喜好 ③习惯 ④AI资产） |
| `易复兴YFX_Skill库内测发布.html` | Master+Skill 可视化内测门户 |
| `样本_Skill_2026-10-19_前100个.json` | 结构化Skill样本100个 |
| `腾讯WorkBuddy_Master总控系统.md` | Master总控提示词+接入配置 |
| `腾讯WorkBuddy_10大子Agent提示词大全.md` | 10个专家专属提示词 |
| `腾讯WorkBuddy_CreateAgent导入模板.json` | WorkBuddy批量创建Agent的JSON |
| `index.html` | 站点入口页（列表+跳转） |

---

## 二、部署方式：GitHub 仓库 + Cloudflare Pages 连接

### 第1步：在 GitHub 建仓库并上传
1. 登录 github.com → New repository → 命名（如 `yfx-ai-profile`）→ 选 Public 或 Private → Create。
2. 把本部署包全部文件上传进仓库（网页 Upload files 或 git push 均可）。

### 第2步：用 Cloudflare 连接该仓库（Cloudflare Pages）
1. 登录 dash.cloudflare.com → Workers 与 Pages → Create → **Pages** → **Connect to Git**。
2. 授权 Cloudflare 访问你的 GitHub（首次需 Connect to GitHub 授权）。
3. 选刚建好的仓库 `yfx-ai-profile`。
4. 构建设置：
   - 框架预设：**None**
   - 构建命令：留空
   - 输出目录：`/`（或留空）
5. 点 **Save and Deploy** → 等待构建完成。
6. 部署完成后生成 `https://<项目名>.pages.dev` 在线链接。

### 第3步：绑定自定义域名（可选）
- 在 Pages → Custom domains 添加你的域名（如 `yfx.example.com`），Cloudflare 会自动配 DNS。

---

## 三、说明
- 本档案为**自包含静态HTML**，无需后端，Cloudflare Pages 可直接托管。
- 上传存档与部署需 GitHub 与 Cloudflare 账号授权（登录态/Token）。
- 若遇构建失败，多为输出目录设置问题，改输出目录为 `/` 即可。

*生成时间：2026-10-20 · 待授权上传*
