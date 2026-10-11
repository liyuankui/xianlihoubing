# 先礼后兵 · 埋点事件字典

- PostHog EU · project = `xianlihoubing` · uid key = `xianlihoubing-uid`
- 匿名随机 8 位 uid，零 PII；localhost 跳过；sendBeacon。

| 事件 | 触发 | 属性 |
|------|------|------|
| `page_view` | 页面加载 | `page=index`，`ref`（来路域名） |
| `nav_click` | 顶部导航跳板块 | `to` ∈ {radar, rules, why, etiquette, china} |
| `share_copy` | 复制分享文案 | — |

查询一律带 `properties.project = 'xianlihoubing'` 过滤。

## Swipe Mode · 社死自测（2026-10-11）

| 事件 | 属性 | 触发 |
|------|------|------|
| `swipe_open` | `cards`（入池卡数） | 打开自测模式（FAB / #swipe 深链） |
| `swipe_card` | `card_id`, `card`（标题前 40 字）, `section`（规则/礼数/球商/本地）, `verdict`（ok / not_yet） | 每张卡滑定 |
| `swipe_done` | `ok`, `total`, `rank`（称号） | 完成整套 |
| `swipe_share` | `rank`, `ok`, `total` | 点击复制战报 |

分析口径：`swipe_card` 按 `section` 聚合可看四大维度全国「不知道率」；按 `card` 聚合即内容热度榜（哪张卡最常被左滑）。
