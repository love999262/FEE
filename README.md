## 公共类

- 自我介绍  
- 你所经历过的最难的事情是什么?如何解决?(性能优化)
- 列举自己的优缺点
- 三年规划 五年规划 为了达到 需要怎么做
- 为什么离职/为什么想来
- 你有什么想问我的吗

## 技术类

### 公共
- 为什么要用TS,有什么好处
- 前端工程化组件化的理解
- [从输入URL到页面被渲染完成中间发生了什么事情](https://zhuanlan.zhihu.com/p/34453198)
- 前端性能优化: 降低首屏渲染时间/渲染优化/Canvas性能优化
- [XSS与CSRF](http://www.cnblogs.com/coco1s/p/5777260.html)
- [重绘与回流](https://juejin.im/post/5a9923e9518825558251c96a)
- 跨域
- 写一个快排,快排的时间复杂度O(n*logn) 最坏(n^2) 最坏(logn),二分查找,冒泡排序.
```js
        const quickSort = function (arr) {
            if (arr.length <= 1) {
                return arr;
            }
            const basic = arr[0];
            const left = [];
            const right = [];
            for (let i = 1; i < arr.length; i++) {
                if (arr[0] >= arr[i]) {
                    left.push(arr[i]);
                } else {
                    right.push(arr[i]);
                }
            }
            return quickSort(left).concat(basic, quickSort(right));
        }
        const bubbleSort = function (arr) {
            for (let i = 0; i < arr.length - 1; i++) {
                for (let j = 0; j < arr.length - i - 1; j++) {
                    if (arr[j] >= arr[j + 1]) {
                        [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
                    }
                }
            }
            return arr;
        }
        const binarySearch = function (l, h, k, arr) {
            if (l > h) {
                return false;
            }
            let mid = Math.ceil((l + h) / 2);
            if (arr[mid] > k) {
                binarySearch(l, mid - 1, k, arr);
                if (arr[mid] < k) {
                    binarySearch(mid + 1, h, k, arr);
                }
            }
            return mid;
        }
        const _binarySearch = function (arr, k) {
            let mid = Math.floor(arr.length / 2);
            let low = 0;
            let high = arr.length;
            while (arr[low] < arr[high]) {
                if (arr[mid] > k) {
                    high = mid - 1;
                } else if (arr[mid] < k) {
                    low = mid + 1;
                }
            }
            return mid;
        }
```
- 如何监控前端性能
- HTTP协议
- 对缓存的了解?
- 进程与线程的区别
- TS有什么好处

### JS
- promise
- Generator/async/await
- Proxy
- iterable
- 模拟apply/call/bind
- 如何实现深拷贝?(Json.parse(JSON.stringift(obj))方法的弊端,可以使用递归extend的方式)
- [如何实现类式继承](https://juejin.im/post/58f94c9bb123db411953691b)
- new操作发生了什么
- 实现一个EventBus
- 数据双向绑定的原理
- this
- 装饰器
- 泛型
- 迭代器
- [canvas性能优化](https://juejin.im/post/5a48d0496fb9a0451b04e54f)

### CSS

- 垂直居中的手段?能写几种?
- 标准盒模型/IE盒模型
