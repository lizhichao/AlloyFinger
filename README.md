![preview](http://alloyteam.github.io/AlloyFinger/alloyfinger.png)

# Usage

```js
//element为需要监听手势的dom对象
new AlloyFinger(element, {
    pointStart: function () {
        //手指触摸屏幕触发
    },
    multipointStart: function () {
        //一个手指以上触摸屏幕触发
    },
    rotate: function (evt) {
        //evt.angle代表两个手指旋转的角度
        console.log(evt.angle);
    },
    pinch: function (evt) {
        //evt.scale代表两个手指缩放的比例
        console.log(evt.scale);
    },
    multipointEnd: function () {
        //当手指离开，屏幕只剩一个手指或零个手指触发
    },
    pressMove: function (evt) {
        //evt.deltaX和evt.deltaY代表在屏幕上移动的距离
        console.log(evt.deltaX);
        console.log(evt.deltaY);
    },
    tap: function (evt) {
        //点按触发
    },
    doubleTap: function (evt) {
        //双击屏幕触发
    },
    longTap: function (evt) {
        //长按屏幕750ms触发
    },
    swipe: function (evt) {
        //evt.direction代表滑动的方向
        console.log("swipe" + evt.direction);
    },
    singleTap: function (evt) {
        //单击
    }
});
```

### React Version:

```js
render() {
    return (
        <AlloyFinger
            onTap={this.onTap.bind(this)}
            onMultipointStart={this.onMultipointStart.bind(this)}
            onLongTap={this.onLongTap.bind(this)}
            onSwipe={this.onSwipe.bind(this)}
            onPinch={this.onPinch.bind(this)}
            onRotate={this.onRotate.bind(this)}
            onPressMove={this.onPressMove.bind(this)}
            onMultipointEnd={this.onMultipointEnd.bind(this)}
            onDoubleTap={this.onDoubleTap.bind(this)}>
            <div className="test">the element that you want to bind event</div>
        </AlloyFinger>
    );
}
```


# Install

You can install it via npm:

```html
npm install alloyfinger
```

# Who is using AlloyFinger?

![preview](http://sqimg.qq.com/qq_product_operations/im/qqlogo/imlogo.png)

# License
This content is released under the [MIT](http://opensource.org/licenses/MIT) License.
