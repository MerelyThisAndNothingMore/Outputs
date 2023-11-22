---
tags: 
alias:
---
```dataviewjs
// Render Title 
dv.span("**Daily Work**")

// Define Data
const calendarData = {
    year: 2023,
    colors: {
        oldGithubGreen11:[
            "hsl(65, 83%, 88%)",
            "hsl(70, 77%, 78%)",
            "hsl(80, 62%, 72%)",
            "hsl(95, 52%, 66%)",
            "hsl(112, 45%, 61%)",
            "hsl(125, 43%, 56%)",
            "hsl(132, 41%, 49%)",
            "hsl(132, 45%, 43%)",
            "hsl(132, 49%, 36%)",
            "hsl(132, 54%, 29%)", 
            "hsl(132, 59%, 24%)",
        ]
    },
    entries: [],
    showCurrentDayBorder: true,
    intensityScaleEnd: 50
}

// Get files data
for (let group of dv.pages().where(p=>p.file.cday).groupBy(p=>p.file.cday)) {
 calendarData.entries.push({
  date: group.key.toFormat("yyyy-MM-dd"),
  intensity: group.rows.length
 })
}

renderHeatmapCalendar(this.container, calendarData)


```

# Plan

关键节点

- 财报分析
- 讲故事
- 德州
- 书籍

魔兽世界背景下重写亮亮丽君故事
《真实的艾泽拉斯》


历史中的权力斗争

人生的路，怎么越走越窄

南街村
巴统
小岗村
