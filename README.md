# MeiWidgetView
[![](https://jitpack.io/v/HpWens/MeiWidgetView.svg)](https://jitpack.io/#HpWens/MeiWidgetView)
[![](https://img.shields.io/scrutinizer/build/g/filp/whoops.svg)](https://blog.csdn.net/u012551350/)
[![Hex.pm](https://img.shields.io/hexpm/l/plug.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![Hex.pm](https://img.shields.io/github/stars/HpWens/MeiWidgetView.svg)](https://github.com/HpWens/MeiWidgetView)


# MeiWidgetView
一款汇总了郭霖，鸿洋，以及自己平时收集的自定义控件的集合库。主旨帮助大家学习自定义控件中的一些技巧，分析问题解决问题的一种思路。

## 引入

### Step 1. Add the JitPack repository to your build file

root gradle

````
    allprojects {
        repositories {
            ...
            maven { url "https://jitpack.io" }
        }
    }

````

### Step 2. Add the dependency

app gradle 

````
	dependencies {
	       implementation 'com.github.HpWens:MeiWidgetView:v0.0.1'
	}
````

## Preview

<img src="/gif/mei_main.gif" width="280px"/> 

文字路径

````
    <com.meis.widget.MeiTextPathView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
````

属性 

````
    <declare-styleable name="MeiTextPathView">
        <!-- 路径文字 -->
        <attr name="text" format="string"/>  
	<!-- 路径文字大小 -->
        <attr name="textSize" format="dimension"/>
	<!-- 路径文字颜色 -->
        <attr name="textColor" format="color"/>
	<!-- 路径绘制时长 -->
        <attr name="duration" format="integer"/>
	<!-- 文字的描边宽度 -->
        <attr name="strokeWidth" format="dimension"/>
	<!-- 是否循环绘制 -->
        <attr name="cycle" format="boolean"/>
	<!-- 是否自动开始播放 -->
        <attr name="autoStart" format="boolean"/>
    </declare-styleable>
````

参考文章

[文字路径动画控件TextPathView解析](https://blog.csdn.net/totond/article/details/79375200)

### 1、弹跳小球

<img src="/gif/bounce_ball.gif" width="280px"/> 

````
    <com.meis.widget.ball.BounceBallView
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
````

属性

- bounce_count :小球弹跳次数
- ball_color:小球颜色
- ball_count:小球数量
- ball_radius:小球半径
- ball_delay:小球出现时间间隔（当小球数大于1时）
- anim_duration:小球一次动画时长
- physic_mode : 开启物理效果（下落加速上升减速）
- random_color: 开启小球颜色随机
- random_radius: 开启小球大小随机（在基础大小上下浮动）
- random_path: 开启小球路径随机（在基础路径坐标上下浮动）

参考文章

[自定义View之小球自由落体弹跳加载控件](https://blog.csdn.net/totond/article/details/79375200)

### 2、扩散圆（主题切换）

<img src="/gif/mei_ripple.gif" width="280px"/> 

````
    <com.meis.widget.MeiRippleView
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />
````

方法

````
    /**
     * @param startX      被点击view相对屏幕的 view中心点x坐标
     * @param startY      被点击view相对屏幕的 view中心点y坐标
     * @param startRadius 开始扩散的半径
     */
    public void startRipple(int startX, int startY, int startRadius)
````

参考文章

[Android自定义View实现炫酷的主题切换动画(仿酷安客户端)](https://blog.csdn.net/u011387817/article/details/79604418)

### 3、酷炫的路径

<img src="/gif/mei_line_path.gif" width="280px"/> 

````
    <com.meis.widget.MeiLinePathView
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />
````

参考文章

[Android仿bilibili弹幕聊天室后面的线条动画](https://blog.csdn.net/u011387817/article/details/78817827)

### 4、滚动视差

<img src="/gif/mei_parallax.gif" width="280px"/> 

````
    <com.meis.widget.MeiScrollParallaxView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>	
````

属性

````
    <declare-styleable name="MeiScrollParallaxView">
        <!-- 滚动速率 （0~1） 值越大滚动视差越明显 -->
        <attr name="parallaxRate" format="float"/>
        <!-- 滑动是否显示视差 默认 true -->
        <attr name="enableParallax" format="boolean"/>
        <!-- 圆角宽度 默认 0  若通过修改父类来实现 则不需要设置此值-->
        <attr name="roundWidth" format="dimension"/>
        <!-- 是否显示圆形 默认 0  若通过修改父类来实现 则不需要设置此值-->
        <attr name="enableCircle" format="boolean"></attr>
        <!--圆角外的颜色 默认白色  若通过修改父类来实现 则不需要设置此值-->
        <attr name="outRoundColor" format="color"/>
    </declare-styleable>
````

### 5、直播间送爱心

<img src="/gif/mei_heart.gif" width="280px"/> 

````
    <com.meis.widget.heart.MeiHeartView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>
````

属性

````
    <declare-styleable name="MeiHeartView">
        <!--爱心动画时长-->
        <attr name="heartDuration" format="integer"/>
        <!--是否显示透明度动画-->
        <attr name="heartEnableAlpha" format="boolean"/>
        <!--是否显示缩放动画-->
        <attr name="heartEnableScale" format="boolean"/>
    </declare-styleable>
````

## Contact

QQ群：478720016

## LICENSE
````
Copyright 2018 文淑

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````

