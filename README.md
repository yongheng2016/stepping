# Stepping - write a dsl, run on any framework.

Stepping a tools for code design, event storming, domain model generate. 

Usage
---

1.Install

```
yarn global add stepping
```

or 

```
npm install -g stepping
```

2.Run

```
stepping -i FILE_NAME
```

example ``stepping`` file: ``ddd.ing``

```
domain: 库存子域
  aggregate: 库存
    event: 库存已增加
    event: 库存已恢复
    event: 库存已扣减
    event: 库存已锁定
    command: 编辑库存

  aggregate: 商品
    event: 商品已创建
    command: 添加商品

domain: 订单子域
  aggregate: 订单
    event: 订单已创建
    event: 订单已支付
    event: 订单已撤销
    event: 订单已投拆
    command: 提交订单
    command: 提交投诉
```

Result:

![DDD Example](./graphics/example.png)

create demo app with Django & Angular 2 

```
...

detail: 商品
  model: product
   - id: int (long, md5)
   - name: string (64)
   - number: string (64)
   - manufacturers: string (128)
```

Thanks
---


DSL Design

![Event Storming Example](./graphics/event-storming.png)

DSL to aggregate event

![Architecture](./graphics/domain-event.png)

TypeScript DDD Base: [https://github.com/yaakaito/typescript-dddbase](https://github.com/yaakaito/typescript-dddbase)

Springy: [https://github.com/dhotson/springy](https://github.com/dhotson/springy)

Jison: [https://github.com/zaach/jison](https://github.com/zaach/jison)

js-sequence-diagrams: [https://bramp.github.io/js-sequence-diagrams/](https://bramp.github.io/js-sequence-diagrams/)

[Handbook of Graph Drawing and Visualization](https://cs.brown.edu/~rt/gdhandbook/)

License
---

[![Phodal's Idea](http://brand.phodal.com/shields/idea-small.svg)](http://ideas.phodal.com/)

© 2017 A [Phodal Huang](https://www.phodal.com)'s [Idea](http://github.com/phodal/ideas).  This code is distributed under the MIT license. See `LICENSE` in this directory.

[待我代码编成，娶你为妻可好](http://www.xuntayizhan.com/blog/ji-ke-ai-qing-zhi-er-shi-dai-wo-dai-ma-bian-cheng-qu-ni-wei-qi-ke-hao-wan/)
