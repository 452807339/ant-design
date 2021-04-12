---
order: 10
title:
  zh-CN: 自定义字段名
  en-US: Custom Field Names
---

## zh-CN

自定义字段名。

## en-US

Custom field names.

```jsx
import { Cascader } from 'antd';

const options = [
  {
    code: '市场监测',
    name: '市场监测',
    items: [
      {
        code: '外汇全市场',
        name: '外汇全市场',
        items: [
          {
            code: '成交价',
            name: '成交价',
          },
        ],
      },
    ],
  },
  {
    code: 'jiangsu',
    name: 'Jiangsu',
    items: [
      {
        code: 'nanjing',
        name: 'Nanjing',
        items: [
          {
            code: 'zhonghuamen',
            name: 'Zhong Hua Men',
          },
        ],
      },
    ],
  },
];

function onChange(value) {
  console.log(value);
}

ReactDOM.render(
  <Cascader
    fieldNames={{ label: 'name', value: 'code', children: 'items' }}
    options={options}
    onChange={onChange}
    placeholder="Please select"
  />,
  mountNode,
);
```
