---
title: 加密功能
date: 2019-04-09
---

## 项目加密

如果项目具有私密性，不希望被公开，只有填入密钥登录后（关闭标签后登录失效），才能进入内容页面。以数组的格式设置 `keys`，可以设置多个密码，数组的值必须是字符串。

```javascript
// .vuepress/config.js

module.exports = {
  theme: 'reco',
  themeConfig: {
    // 密钥
    keyPage: {
      keys: ['123456'],
      color: '#42b983', // 登录页动画球的颜色
      lineColor: '#42b983' // 登录页动画线的颜色
    }
  }  
}  
```

## 文章加密

如果项目是公开的，而某些文章可能需要加密，需要在 `frontmatter` 以数组的格式设置 `keys`，可以设置多个密码，数组的值必须是字符串。

```yaml
---
title: vuepress-theme-reco
date: 2019-04-09
author: reco_luan
keys:
 - '123456'
---
```

> 加密页的遗留问题：  
> 从某篇单独加密的文章直接进入另一篇文章时（比如通过导航栏）加密无法隐藏  
> 使用文章加密功能时需要注意该问题