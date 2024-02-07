<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./documentation_images/CustomTkinter_logo_dark.png">
    <img src="./documentation_images/CustomTkinter_logo_light.png">
  </picture>
</p>

<div align="center">

![PyPI](https://img.shields.io/pypi/v/customtkinter)
![PyPI - Downloads](https://img.shields.io/pypi/dm/customtkinter?color=green&label=downloads)
![Downloads last 6 month](https://static.pepy.tech/personalized-badge/customtkinter?period=total&units=international_system&left_color=grey&right_color=green&left_text=downloads%20last%206%20month)
![PyPI - License](https://img.shields.io/badge/license-MIT-blue)
![LOC](https://tokei.rs/b1/github/tomschimansky/customtkinter?category=lines)

</div>

---

<div align="center">
<a href="https://www.paypal.com/donate/?hosted_button_id=LK5QAZYRN2R2A"><img src="documentation_images/paypal_donate_button.png" width=170 alt="Paypal donation button"></a>
<h3>
Official website: https://customtkinter.tomschimansky.com
</h3>
</div>

CustomTkinter 是一个基于 Tkinter 的 Python UI 库，它提供了新的、现代的和
完全可定制的小部件。 它们的创建和使用就像普通的 Tkinter 小部件一样
也可以与普通 Tkinter 元素结合使用。 小部件
窗口颜色要么适应系统外观，要么适应手动设置的模式
（'light'、'dark'），所有 CustomTkinter 小部件和窗口都支持 HighDPI 缩放
（Windows、macOS）。 使用 CustomTkinter，您将获得一致且现代的外观
桌面平台（Windows、macOS、Linux）。

![](documentation_images/complex_example_dark_Windows.png)
| _`complex_example.py` 在 Windows 11 的 深色主题 and 'blue' 主题_

![](documentation_images/complex_example_light_macOS.png)
| _`complex_example.py` 在 macOS 浅色 and 标准 'blue' 主题_
###


## 安装
用pip安装模块:
```
pip3 install customtkinter
```
**更新现有安装:** ```pip3 install customtkinter --upgrade```\
(尽可能频繁地更新，因为该库正在积极开发中)

## 文档

**官方** 文档在这:

**➡️ https://customtkinter.tomschimansky.com/documentation**.

## 示例程序
要测试 customtkinter，您可以尝试这个仅使用一个按钮的简单示例：
```python
import customtkinter

customtkinter.set_appearance_mode("System")  # Modes: system (default), light, dark
customtkinter.set_default_color_theme("blue")  # Themes: blue (default), dark-blue, green

app = customtkinter.CTk()  # create CTk window like you do with the Tk window
app.geometry("400x240")

def button_function():
    print("button pressed")

# Use CTkButton instead of tkinter Button
button = customtkinter.CTkButton(master=app, text="CTkButton", command=button_function)
button.place(relx=0.5, rely=0.5, anchor=customtkinter.CENTER)

app.mainloop()
```
这会在 macOS 上出现以下窗口：

<img src="documentation_images/single_button_macOS.png" width="400"/>

在 [examples folder](https://github.com/TomSchimansky/CustomTkinter/tree/master/examples), 你
可以找到更多示例程序并在 [文档](https://github.com/TomSchimansky/CustomTkinter/wiki)
您可以找到有关外观模式、缩放、主题和所有小部件的更多信息。

## 更多示例和展示

### 外观模式变更和缩放比例变更

CustomTkinter可以适配Windows 10/11浅色或深色模式：

https://user-images.githubusercontent.com/66446067/204672968-6584f360-4c52-434f-9c16-25761341368b.mp4

| _`complex_example.py` 在 Windows 11 上，系统外观模式更改和标准'蓝色'主题_

在 macOS 上，您需要 python3.10 或更高版本，或者需要 anaconda python
获取暗窗口标题的版本（Tcl/Tk >= 8.6.9）：

https://user-images.githubusercontent.com/66446067/204673854-b6cbcfda-d9a1-4425-92a3-5b57d7f2fd6b.mp4

| _`complex_example.py` 在 macOS 上，系统外观模式更改、用户缩放更改和标准'蓝色'主题_
###

### 带图像的按钮
可以将图像放在 CTkButton 上。 你只需要
使用 ``image`` 参数将 PhotoImage 对象传递给 CTkButton。
如果你根本不需要文本，你必须设置 ``text=""``或者你指定
如何使用 ``compound`` 选项同时定位文本和图像：

![](documentation_images/image_example_dark_Windows.png)
| _`image_example.py` 在 Windows 11上_
###

### 可滚动框架
可滚动框架可以垂直或水平方向，并且可以组合
与任何其他小部件。
![](documentation_images/scrollable_frame_example_Windows.png)
| _`scrollable_frame_example.py` 在 Windows 11上_

### 集成 TkinterMapView 小部件
在下面的示例中，我使用了 TkinterMapView，它集成了
以及 CustomTkinter 程序。 这是一个基于图块的地图小部件，显示
OpenStreetMap 或其他基于图块的地图：

https://user-images.githubusercontent.com/66446067/204675835-1584a8da-5acc-4993-b4a9-e70f06fa14b0.mp4

| _`examples/map_with_customtkinter.py` 来自 Windows 11 上的 TkinterMapView 存储库_

可以在此处找到 TkinterMapView 库和示例程序：
https://github.com/TomSchimansky/TkinterMapView
