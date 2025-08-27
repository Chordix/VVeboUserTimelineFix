# VVeboUserTimelineFix

> 修复 `VVebo` 用户时间线（QuantumultX）

## 使用

设置界面划到最底部，点击`编辑`并添加如下内容

```conf
[mitm]
hostname = api.weibo.cn

[rewrite_local]
^https:\/\/api\.weibo\.cn\/2\/users\/show\? url script-request-header https://cdn.jsdelivr.net/gh/Chordix/VVeboUserTimelineFix@main/QuantumultX/vvebo.js
^https:\/\/api\.weibo\.cn\/2\/statuses\/user_timeline\? url script-request-header https://cdn.jsdelivr.net/gh/Chordix/VVeboUserTimelineFix@main/QuantumultX/vvebo.js
^https:\/\/api\.weibo\.cn\/2\/profile\/statuses\/tab\? url script-response-body https://cdn.jsdelivr.net/gh/Chordix/VVeboUserTimelineFix@main/QuantumultX/vvebo.js
```

打开`重写`和 `MITM` 功能即可

## 来源

- [利用 HTTP 重写，找回 VVebo 的用户时间线](https://sspai.com/post/83704)
- [bin64/Scripts/blob/main/QuantumultX/vvebo.js](https://github.com/bin64/Scripts/blob/main/QuantumultX/vvebo.js)
- [suiyuran/stash](https://github.com/suiyuran/stash)
