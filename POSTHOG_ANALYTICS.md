# 先礼后兵 · 埋点事件字典

- PostHog EU · project = `xianlihoubing` · uid key = `xianlihoubing-uid`
- 匿名随机 8 位 uid，零 PII；localhost 跳过；sendBeacon。

| 事件 | 触发 | 属性 |
|------|------|------|
| `page_view` | 页面加载 | `page=index`，`ref`（来路域名） |
| `nav_click` | 顶部导航跳板块 | `to` ∈ {radar, rules, etiquette, china} |
| `share_copy` | 复制分享文案 | — |

查询一律带 `properties.project = 'xianlihoubing'` 过滤。
