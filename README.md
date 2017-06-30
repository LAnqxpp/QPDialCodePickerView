![logo](logo.png)

[![Pod Version](http://img.shields.io/cocoapods/v/QPDialCodePickerView.svg?style=flat)](http://cocoadocs.org/docsets/QPDialCodePickerView/)
[![Pod Platform](http://img.shields.io/cocoapods/p/QPDialCodePickerView.svg?style=flat)](http://cocoadocs.org/docsets/QPDialCodePickerView/)
[![Pod License](http://img.shields.io/cocoapods/l/QPDialCodePickerView.svg?style=flat)](https://www.apache.org/licenses/LICENSE-2.0.html)

# QPDialCodePickerView 

### International Dial Code Picker View for Country or Area 国家或地区国际区号选择器
   
## 特性 / Features

1.自定义确定按钮背景颜色。

2.自定义确定按钮标题。

3.支持多种地区名称显示格式:根据当前地区本地化所有地区名称／根据地区自身本地化地区名称/根据美国(US)地区本地化所有地区名称。

4.可配置是否显示灰色背景蒙版。

5.可配置是否显示圆角。

6.默认按钮“确定”已经国际化，请确保主工程项目支持该语言国际化选项，在项目PROJECT-Localizations中添加。

## 演示 / Demo 

<p align="center" >
  <img src="demo.gif" title="demo">
</p>

<p align="center" >
  <img src="demo2.gif" title="demo">
</p>

## 安装 / Installation

方法一：直接下载, 打开工作区 `QPDialCodePickerView.xcworkspace`, 选择 Target `QPDialCodePickerView-Universal`进行编译，在根目录下的 `product` 目录下会生成 `QPDialCodePickerView.framework` 和 `QPDialCodePickerView.bundle`, 将这两个文件添加到您的项目中即可。

方法二：`QPDialCodePickerView` is available through CocoaPods. To install it, simply add the following line to your Podfile:

```
pod "QPDialCodePickerView"
```

## 使用 / Usage

```
 __weak typeof (UIButton*) weakBtn = self.btnDialCode;
 QPDialCodePickerView *pickerView = [[QPDialCodePickerView alloc] initWithAreaFormat:QPDialCodeAreaNameFormatCurrentLocale complete:^(QPDialCodeObject *item) {
     [weakBtn setTitle:[NSString stringWithFormat:@"+%@", item.dial_code] forState:UIControlStateNormal];
 }];
 pickerView.roundCorner = YES;
 [pickerView show];
```

## 关注我们 / Follow us

[![Twitter URL](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=https://github.com/pcjbird/QPDialCodePickerView)
[![Twitter Follow](https://img.shields.io/twitter/follow/pcjbird.svg?style=social)](https://twitter.com/pcjbird)
