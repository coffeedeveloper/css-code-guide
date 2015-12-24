# CSS 代码规范

## 缩进

采用**两个空格**而非**tab**来做缩进。

> 为了确保在每个编辑器上面看起来都是一致

## 换行

每条css规则之间需要空一行空白行

```css
/*错误示范*/
.a {

}
.b {

}

/*正确示范*/
.a {

}

.b {

}
```

## 代码风格

不管样式规则下有多少个属性，均每个属性单独一行

```css
/*错误示范*/
.a { text-align: center; }

/*正确示范*/
.a {
  text-align: center;
}
```

## 空格

- 在选择符与左大括号之间需要有一个空格

  ```css
  /*错误示范*/
  .a{
    text-align: center;
  }
  /*正确示范*/
  .a {
    text-align: center;
  }
  ```
  
- 在属性名的`:`号和属性值之间需要有一个空格

  ```css
  /*错误示范*/
  .a {
    text-align:center;
  }
  /*正确示范*/
  .a {
    text-align: center;
  }
  ```

- 两个选择符之间需要有一个空格

  ```css
  /*错误示范*/
  .a,.b {
    text-align: center;
  }
  /*正确示范*/
  .a, .b {
    text-align: center;
  }
  ```
