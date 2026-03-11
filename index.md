---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

## MNIST Dataset

```python
training_data = datasets.MNIST( root=”data”,#文件下载位置的根目录 train=True, download=True,#确认是否已经从网络上爬取到了数据集，如果已经下载到了就不必再下载了。 transform=ToTensor(),#少了一个逗号 #张量，图片不能直接导入神经网络，需要转换成张量 )

test_data = datasets.MNIST( root=”data”, train=False, download=True, transform=ToTensor(),#少了一个逗号 )
```



## Neural Network

```python
class NeuralNetwork(nn.Module): #设置三层 def init(self): # def int(self):输入错误 super().init() self.flatten = nn.Flatten() self.hidden1 = nn.Linear(28*28,128)#图像是灰度的，28x28像素的 #中间隐藏层，起初可以少一层 self.hidden2 = nn.Linear(128,256) self.hidden3 = nn.Linear(256,512) self.out = nn.Linear(512,10)#为什么是10层输出层？0-9一共10个数 #优化网络，优化这里！40-43行，47行到52行 #设置数据流方向 def forward(self,x): x = self.flatten(x)

    x = self.hidden1(x)
    x = torch.relu(x)
    x = self.hidden2(x)
    x = torch.relu(x)
    x = self.hidden3(x)
    x = torch.relu(x)

    x = self.out(x)
    return x #优化到正确率为99.97%
```



### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
