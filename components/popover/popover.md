# Popper 气泡层



## 基本用法
最基本的用法。

```jsx
import { Button, Popover, Select } from 'zarm-web';

class Demo extends React.Component {
  state = {
    visible: false,
    direction: 'top',
    trigger: 'click',
  }

  render() {
    const { visible, direction, trigger, animationType } = this.state;

    return (
      <>
      
        <Popover
          content="我是气泡层的内容"
          visible={visible}
          destroy={false}
          trigger={trigger}
          direction={direction}
          className="custom-content"
        >
        <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
            点击{visible ? '隐藏' : '显示'}
        </Button>
        </Popover>
      </>
    );
  }
}

ReactDOM.render(<Demo />, mountNode);
```

## 自定义箭头
自定义箭头位置

```jsx
import { Button, Popover, Select } from 'zarm-web';

class Demo extends React.Component {
  state = {
    visible: false,
    direction: 'top',
    trigger: 'click',
  }

  render() {
    const { visible, direction, trigger, animationType } = this.state;

    return (
      <>
                <div>
                  <div style={{ marginLeft: 110 }}>
                     <Popover
                        content="我是气泡层的内容"
                        destroy={false}
                        visible={visible}
                        trigger={trigger}
                        direction="topLeft"
                        className="custom-content"
                      >
                        <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                          上方（左）
                        </Button>
                      </Popover>
                     <Popover
                        content="我是气泡层的内容"
                        destroy={false}
                        visible={visible}
                        trigger={trigger}
                        direction="top"
                        className="custom-content"
                      >
                        <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                          上方（中）
                        </Button>
                      </Popover>
                     <Popover
                        content="我是气泡层的内容"
                        destroy={false}
                        visible={visible}
                        trigger={trigger}
                        direction="topRight"
                        className="custom-content"
                      >
                        <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                          上方（右）
                        </Button>
                      </Popover>
                  </div>
      
                  <div style={{ width: 60, float: 'left', clear: 'both' }}>
                   <Popover
                     content="我是气泡层的内容"
                     destroy={false}
                     visible={visible}
                     trigger={trigger}
                     direction="leftTop"
                     className="custom-content"
                   >
                     <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                       左边（上）
                     </Button>
                   </Popover>
                  <Popover
                     content="我是气泡层的内容"
                     destroy={false}
                     visible={visible}
                     trigger={trigger}
                     direction="left"
                     className="custom-content"
                   >
                     <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                       左边（中）
                     </Button>
                   </Popover>
                  <Popover
                     content="我是气泡层的内容"
                     destroy={false}
                     visible={visible}
                     trigger={trigger}
                     direction="leftBottom"
                     className="custom-content"
                   >
                     <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                       左边（下）
                     </Button>
                   </Popover>
                  </div>
      
                  <div style={{ width: 100, marginLeft: 100 * 4 + 20 }}>
                    <Popover
                       content="我是气泡层的内容"
                       destroy={false}
                       visible={visible}
                       trigger={trigger}
                       direction="rightTop"
                       className="custom-content"
                     >
                       <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                         右边（上）
                       </Button>
                     </Popover>
                    <Popover
                       content="我是气泡层的内容"
                       destroy={false}
                       visible={visible}
                       trigger={trigger}
                       direction="right"
                       className="custom-content"
                     >
                       <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                         右边（中）
                       </Button>
                     </Popover>
                    <Popover
                       content="我是气泡层的内容"
                       destroy={false}
                       visible={visible}
                       trigger={trigger}
                       direction="rightBottom"
                       className="custom-content"
                     >
                       <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                         右边（下）
                       </Button>
                     </Popover>
                  </div>
      
                  <div style={{ marginLeft: 110, clear: 'both' }}>
                    <Popover
                       content="我是气泡层的内容"
                       destroy={false}
                       visible={visible}
                       trigger={trigger}
                       direction="bottomLeft"
                       className="custom-content"
                     >
                       <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                         下方（左）
                       </Button>
                     </Popover>
                    <Popover
                       content="我是气泡层的内容"
                       destroy={false}
                       visible={visible}
                       trigger={trigger}
                       direction="bottom"
                       className="custom-content"
                     >
                       <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                         下方（中）
                       </Button>
                     </Popover>
                    <Popover
                       content="我是气泡层的内容"
                       destroy={false}
                       visible={visible}
                       trigger={trigger}
                       direction="bottomRight"
                       className="custom-content"
                     >
                       <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
                         下方（右）
                       </Button>
                     </Popover>
                  </div>
                </div>
        
      </>
    );
  }
}

ReactDOM.render(<Demo />, mountNode);
```

## 自定义气泡内容
content传入HTML标签以自定义气泡内容。

```jsx
import { Button, Popover, Select } from 'zarm-web';

class Demo extends React.Component {
  state = {
    visible: false,
    direction: 'top',
    trigger: 'click',
  }

  render() {
    const { visible, direction, trigger, animationType } = this.state;

    return (
      <>
      
        <Popover
          content={<div><h1>这是标题</h1><p>这里是内容</p></div>}
          destroy={false}
          visible={visible}
          trigger={trigger}
          direction={direction}
          className="custom-content"
        >
          <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
            点击{visible ? '隐藏' : '显示'}
          </Button>
        </Popover>
      </>
    );
  }
}

ReactDOM.render(<Demo />, mountNode);
```

## 蒙层及蒙层事件
设置蒙层、添加蒙层事件

```jsx
import { Button, Popover, Select } from 'zarm-web';

class Demo extends React.Component {
  state = {
    direction: 'top',
    trigger: 'click',
  }

  render() {
    const { visible, direction, trigger, animationType } = this.state;

    return (
      <>
      
        <Popover
          content={<div><h1>这是标题</h1><p>这里是内容</p></div>}
          destroy={false}
          visible={visible}
          trigger={trigger}
          direction={direction}
          mask={true}
          onMaskClick={() => { this.setState({ visible: false }) }}
          className="custom-content"
        >
          <Button theme="primary" size="xs" onClick={() => trigger === 'manual' && this.setState({ visible: !visible })}>
            点击{visible ? '隐藏' : '显示'}
          </Button>
        </Popover>
      </>
    );
  }
}

ReactDOM.render(<Demo />, mountNode);
```



## API

| 属性 | 类型 | 默认值 | 说明 |
| :--- | :--- | :--- | :--- |
| className | string | - | 气泡层类名追加 |
| content | ReactNode | - | 显示内容 |
| direction | string | 'top' | 显示方向，可选值 `topLeft`、`top`、`topRight`、`rightTop`、`right`、`rightBottom`、`bottomLeft`、`bottom`、`bottomRight`、`leftTop`、`left`、`leftBottom` |
| trigger | string | 移动端为'click' <br /> 桌面端为'hover' | 触发方式，可选值为：`click` 点击触发状态、`hover` 鼠标经过触发、`focus` 聚焦状态触发、`manual` 受控触发、`contextMenu` 右键触发 |
| mask | boolean | false | 是否有蒙层 |
| onMaskClick | (e) => void | - | 点击蒙层时候触发的事件 |
