# 工作记忆

## 项目概述
- 项目：edu-platform（惠教资源平台）- 教师工作台
- 技术栈：纯HTML/CSS/JavaScript，localStorage持久化

## 核心功能（已实现）

### 1. 今日教学安排（持续响铃提醒）
- 新增提醒弹窗（`reminder-alert-overlay`），到点时弹出并持续响铃
- `startContinuousBeep()`：每1.5秒循环播放提示音
- `dismissReminder()`：点击"我知道了"按钮关闭弹窗并停止响铃
- `stopReminderSound()`：停止所有音频

### 2. 教学资源搜索（嵌入全屏）
- `toggleFullscreen()`：切换全屏/退出全屏模式
- 添加"⛶ 全屏"按钮到嵌入区域
- 全屏时覆盖整个视口，退出后恢复520px高度

### 3. 作业管理（删除+标记完成）
- `deleteHW(id)`：删除作业（带确认提示）
- `markHWComplete(id)`：标记作业为已完成
- 作业列表增加"✅ 完成"和"🗑️ 删除"按钮

### 4. 备课工具增强
- 6种备课模板（新授课、复习课、习题课、实验课、试卷讲评、自由备课）
- `openLessonModalWithTemplate()`：根据模板预填内容
- `generateHWFromLesson(id)`：从备课一键生成作业
- `printLesson(id)`：打印备课内容（打开新窗口）
- 模板内容预设了标准的教学目标、教学内容、教学方法等字段

## localStorage Key Pattern
- `edu_schedule_{teacherId}`：教师日程安排
- `edu_homework`：作业数据
- `edu_students`：学生数据（含`unsubmittedCount`）
- `edu_lessons`：备课数据
- `edu_resources`：本地资源

## 用户偏好
- 用户使用中文
- 平台名称：惠教资源平台
