# CSS 代码规范

这个规范内容包含以下内容

- [缩进](#缩进)
- 排版
- 空格
- 属性值
- 排序
- 命名

## 缩进

采用**两个空格**而非**tab**来做缩进。

> 为了确保在每个编辑器以及在网页上面看起来都是一致

## 排版

- 每条css规则之间需要空一行空白行

  ```css
  /*错误示范*/
  .a {
    text-align: center;
  }
  .b {
    text-align: center;
  }

  /*正确示范*/
  .a {
    text-align: center;
  }

  .b {
    text-align: center;
  }
  ```

- 不管样式规则下有多少个属性，均每个属性单独一行

  ```css
  /*错误示范*/
  .a { text-align: center; }

  /*正确示范*/
  .a {
    text-align: center;
  }
  ```

## 空格


- 多个选择符的`,`后面需要有一个空格

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

- 在属性名的`:`号与属性值之间需要有一个空格

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
- 最后一个属性也需要保留`;`，且`;`与属性值之间不需要有空格

  ```css
  /*错误示范*/
  .a {
    text-align: left
  }

  /*正确示范*/
  .a {
    text-align: left;
  }
  ```

## 属性值

- 属性值为0的时候，不要带单位

  ```css
  /*错误示范*/
  .a {
    padding: 0px;
  }
  /*正确示范*/
  .a {
    padding: 0;
  }
  ```

- 设置1以下的属性值时，直接用`.x`，不需要带`0`

  ```css
  /*错误示范*/
  .a {
    opacity: 0.3;
    transition: opacity 0.8s;
  }
  /*正确示范*/
  .a {
    opacity: .3;
    transition: opacity .8s;
  }
  ```

- 如果想覆盖或修改属性某个方位的值，应该用指定方位的属性名
  - 例子：某个类名为a的段落，增加顶部内边距

    ```css
    p {
      padding: 0;
    }

    /*错误示范*/
    .a {
      padding: 10px 0 0 0;
    }
    /*正确示范*/
    .a {
      padding-top: 10px;
    }
    ```

## 建议

- 应当尽可能的使用预处理器或者后处理器来对`css`进行处理，尽量避免写原生`css`，更加推荐用`scss`（PS：虽然我更加喜欢`stylus`）
	- [stylus](http://learnboost.github.io/stylus/)
	- [sass](http://sass-lang.com/)
	- [less](http://lesscss.org/)
- 针对浏览器差异性的代码，应该用[Autoprefixer](https://github.com/postcss/autoprefixer)来做
  - [Autoprefixer - github](https://github.com/postcss/autoprefixer)
  - [gulp-autoprefixer](https://github.com/sindresorhus/gulp-autoprefixer)

  ```css
  /*错误示范*/
  .a {
    width: 100px;
    -webkit-transition: width .5s;
    transition: width .5s;
  }
  /*正确示范*/
  .a {
    width: 100px;
    transition: width .5s;
  }
  ```
