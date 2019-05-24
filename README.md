### jest单元测试简单演示(1+1等于2)

> 简单的sum方法测试

[官网](https://jestjs.io/docs/zh-Hans/getting-started.html)

安装

```
 $ npm i jest -D
```
被测试文件sum.js
```
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```
单元测试文件sum.test.js
```
const sum = require('./sum');   //引入方法文件

test('adds 1 + 1 to equal 2 这里是测试标题', () => {
  expect(sum(1, 1)).toBe(2);    //期望sum(1,1)计算后为2,如果是2则测试通过,否则测试不通过
});
```
启动测试
```js
    用npm启动
        //package.json
        "scripts": {
        	"test": "jest"
        }
        $ npm run test
    或者直接命令行启动
        $ "./node_modules/.bin/jest" //window必须加引号,你懂得
```