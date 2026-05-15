# Daily Standup Template

## Format
```markdown
# 每日站会 - {DATE}

## 昨日完成
- [Task 1 description]
- [Task 2 description]

## 今日计划
- [Task 1 description]
- [Task 2 description]

## 阻碍/风险
- [Blocker description] (if any)

## 需要帮助
- [Help request] (if any)
```

## Standup Rules
1. 每天北京时间 10:00 前提交
2. 每项不超过1行
3. 阻碍项需要标记优先级 (P0/P1/P2)
4. 超过2天的阻碍需要升级

## Automated Collection
```yaml
# .github/ISSUE_TEMPLATE/daily-standup.yml
name: Daily Standup
description: Submit daily standup
labels: ['standup', 'daily']
body:
  - type: textarea
    id: yesterday
    attributes:
      label: 昨日完成
    validations:
      required: true
  - type: textarea
    id: today
    attributes:
      label: 今日计划
    validations:
      required: true
  - type: textarea
    id: blockers
    attributes:
      label: 阻碍/风险
```
