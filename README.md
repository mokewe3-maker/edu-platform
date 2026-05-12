# 专业辅助教师教学平台

一个基于纯前端技术的教育管理平台，为教师提供全面的教学辅助功能。

## 功能模块

### 教师端 (teacher.html)
- 📊 **个人中心** - 教师信息管理、快捷操作入口
- 📢 **通知公告** - 查看学校/班级通知公告
- 📝 **教学日志** - 记录每日教学工作，支持导出
- ✅ **班级考勤** - 学生考勤管理，支持批量操作
- 📚 **教学资源** - 上传、下载、管理教学资源
- 📋 **教学周报** - 自动汇总本周教学数据，支持导出

### 管理端 (admin.html)
- 用户权限管理
- 班级与学生管理
- 数据统计与分析

## 技术栈

- HTML5 + CSS3 + JavaScript
- LocalStorage 数据持久化
- 无需后端，纯前端部署

## 快速开始

### 本地运行
```bash
# 直接在浏览器打开 index.html
# 或使用任意静态服务器
npx serve .
# 或
python -m http.server 8080
```

### 默认账号

**管理员**
- 用户名: `admin`
- 密码: `admin123`

**教师**
- 用户名: `teacher1`
- 密码: `teacher123`

> ⚠️ 首次登录后请及时修改默认密码

## 安全特性

- 密码哈希存储（不可逆向还原）
- 防暴力破解（登录失败锁定）
- 单设备登录检测
- 开发者模式检测

## 部署到 GitHub Pages

1. Fork 或克隆此仓库
2. 进入仓库 `Settings` -> `Pages`
3. Source 选择 `Deploy from a branch`
4. Branch 选择 `main`，文件夹选择 `/ (root)`
5. 保存后等待部署完成
6. 访问 `https://你的用户名.github.io/仓库名/`

## 项目结构

```
edu-platform/
├── index.html      # 登录页面
├── teacher.html    # 教师端工作台
├── admin.html      # 管理端工作台
├── .gitignore      # Git忽略配置
└── README.md       # 项目文档
```

## 数据说明

所有数据存储在浏览器 LocalStorage 中：
- `edu_admin` - 管理员信息
- `edu_teachers` - 教师列表
- `edu_lessons` - 备课记录
- `edu_students` - 学生信息
- `edu_homework` - 作业记录
- `edu_attendance` - 考勤记录
- `edu_teaching_logs` - 教学日志
- `edu_weekly_reports` - 教学周报
- `edu_resources` - 教学资源
- `edu_announcements` - 通知公告

> 💡 数据仅存储在本地浏览器，切换设备不会同步

## License

MIT
