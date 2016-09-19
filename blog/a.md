## 我是a页面

```js
render () {
  marked.setOptions({
    highlight: function (code) {
      return hljs.highlightAuto(code).value;
    }
  });
  let content = this.state.wait ? '请稍等' : marked(this.state.data);
  return(
    <div>
      <div dangerouslySetInnerHTML={{__html: content}} />
    </div>
  )
}
```
