#jQuery fullPage.js

----------

> 
> fullPage.js 是一个基于 jQuery 的插件，它能够很方便、很轻松的制作出全屏网站，主要功能有：
> 
> - 支持鼠标滚动
> - 支持前进后退和键盘控制
> - 多个回调函数
> - 支持手机、平板触摸事件
> - 支持 CSS3 动画
> - 支持窗口缩放
> - 窗口缩放时自动调整
> - 可设置滚动宽度、背景颜色、滚动速度、循环选项、回调、文本对齐方式等等


##兼容性

jQuery 兼容

兼容 jQuery 1.7+。

浏览器兼容

![](http://img.hb.aicdn.com/3049b17d6c0ac98d9c86a40bc33661b4b343842e5614-16FfaO)


##使用方法

###1、引入文件

	在sass文件中引用样式
	@import "components/jquery-fullPage/jquery.fullPage.scss";

	require('jquery-fullPage');

	$('#dowebok').fullpage();

###2、HTML

	<div id="dowebok">
	    <div class="section">
	        <h3>第一屏</h3>
	    </div>
	    <div class="section">
	        <h3>第二屏</h3>
	    </div>
	    <div class="section">
	        <h3>第三屏</h3>
	    </div>
	    <div class="section">
	        <h3>第四屏</h3>
	    </div>
	</div>

每个 section 代表一屏，默认显示“第一屏”，如果要指定加载页面时显示的“屏幕”，可以在对应的 section 加上 class=”active”，如：

	<div class="section active">第三屏</div>

同时，可以在 section 内加入 slide，如：

	<div id="dowebok">
	    <div class="section">第一屏</div>
	    <div class="section">第二屏</div>
	    <div class="section">
	        <div class="slide">第三屏的第一屏</div>
	        <div class="slide">第三屏的第二屏</div>
	        <div class="slide">第三屏的第三屏</div>
	        <div class="slide">第三屏的第四屏</div>
	    </div>
	    <div class="section">第四屏</div>
	</div>


##配置

##1、选项

<table>
	<thead>
		<tr>
		<th>选项</th>
		<th width="50px">类型</th>
		<th>默认值</th>
		<th>说明</th>
		</tr>
	</thead>
	<tbody>

		<tr>
			<td>menu</td>
			<td>布尔值</td>
			<td>false</td>
			<td>绑定菜单，设定的相关属性与 anchors 的值对应后，菜单可以控制滚动#myMenu</td>
		</tr>
		<tr>
			<td>lockAnchors</td>
			<td>布尔值</td>
			<td>false</td>
			<td></td>
		</tr>
		<tr>
			<td>anchors</td>
			<td>数组</td>
			<td>无</td>
			<td>定义锚链接['firstPage', 'secondPage']</td>
		</tr>
		<tr>
			<td>navigation</td>
			<td>布尔值</td>
			<td>false</td>
			<td>是否显示项目导航</td>
		</tr>
		<tr>
			<td>navigationPosition</td>
			<td>字符串</td>
			<td>right</td>
			<td>项目导航的位置，可选 left 或 right</td>
		</tr>
		<tr>
			<td>navigationTooltips</td>
			<td>数组</td>
			<td>空</td>
			<td>项目导航的 tip</td>
		</tr>
		<tr>
			<td>slidesNavigation</td>
			<td>布尔值</td>
			<td>false</td>
			<td>是否显示左右滑块的项目导航</td>
		</tr>
		<tr>
			<td>slidesNavPosition</td>
			<td>字符串</td>
			<td>bottom</td>
			<td>左右滑块的项目导航的位置，可选 top 或 bottom</td>
		</tr>


		<tr>
			<td>css3</td>
			<td>布尔值</td>
			<td>true</td>
			<td>是否使用 CSS3 transforms 滚动</td>
		</tr>
		<tr>
			<td>scrollingSpeed</td>
			<td>整数</td>
			<td>700</td>
			<td>滚动速度，单位为毫秒</td>
		</tr>
		<tr>
			<td>autoScrolling</td>
			<td>布尔值</td>
			<td>true</td>
			<td></td>
		</tr>
		<tr>
			<td>fitToSection</td>
			<td>布尔值</td>
			<td>true</td>
			<td></td>
		</tr>
		<tr>
			<td>scrollBar</td>
			<td>布尔值</td>
			<td>true</td>
			<td></td>
		</tr>
		<tr>
			<td>easing</td>
			<td>字符串</td>
			<td>easeInOutCubic</td>
			<td>需要jquery.easings.min.js的支持</td>
		</tr>
		<tr>
			<td>easingcss3</td>
			<td>字符串</td>
			<td>ease</td>
			<td>css3:true,css3的过度效果</td>
		</tr>
		<tr>
			<td>loopBottom</td>
			<td>布尔值</td>
			<td>false</td>
			<td>滚动到最底部后是否滚回顶部</td>
		</tr>
		<tr>
			<td>loopTop</td>
			<td>布尔值</td>
			<td>false</td>
			<td>滚动到最顶部后是否滚底部</td>
		</tr>
		<tr>
			<td>loopHorizontal</td>
			<td>布尔值</td>
			<td>true</td>
			<td>左右滑块是否循环滑动</td>
		</tr>
		<tr>
			<td>continuousVertical</td>
			<td>布尔值</td>
			<td>false</td>
			<td>是否循环滚动，与 loopTop 及 loopBottom 不兼容</td>
		</tr>
		<tr>
			<td>normalScrollElements</td>
			<td></td>
			<td>无</td>
			<td>'#element1, .element2'</td>
		</tr>
		<tr>
			<td>scrollOverflow</td>
			<td>布尔值</td>
			<td>false</td>
			<td>内容超过满屏后是否显示滚动条,需要jquery.slimscroll.min支持</td>
		</tr>
		<tr>
			<td>touchSensitivity</td>
			<td>整数</td>
			<td>5</td>
			<td></td>
		</tr>
		<tr>
			<td>normalScrollElementTouchThreshold</td>
			<td>整数</td>
			<td>5</td>
			<td></td>
		</tr>


		<tr>
			<td>keyboardScrolling</td>
			<td>布尔值</td>
			<td>true</td>
			<td>是否使用键盘方向键导航</td>
		</tr>
		<tr>
			<td>animateAnchor</td>
			<td>布尔值</td>
			<td>true</td>
			<td></td>
		</tr>
		<tr>
			<td>recordHistory</td>
			<td>布尔值</td>
			<td>true</td>
			<td>历史记录</td>
		</tr>


		<tr>
			<td>controlArrows</td>
			<td>布尔值</td>
			<td>true</td>
			<td>使用控制箭头幻灯片左或右</td>
		</tr>
		<tr>
			<td>verticalCentered</td>
			<td>字符串</td>
			<td>true</td>
			<td>内容是否垂直居中</td>
		</tr>
		<tr>
			<td>resize</td>
			<td>布尔值</td>
			<td>false</td>
			<td>字体是否随着窗口缩放而缩放</td>
		</tr>
		<tr>
			<td>sectionsColor</td>
			<td>数组</td>
			<td>none</td>
			<td>设置背景颜色['#f2f2f2', '#4BBFC3', '#7BAABE', 'whitesmoke', '#000']</td>
		</tr>
		<tr>
			<td>paddingTop</td>
			<td>字符串</td>
			<td>0</td>
			<td>与顶部的距离</td>
			</tr>
		<tr>
			<td>paddingBottom</td>
			<td>字符串</td>
			<td>0</td>
			<td>与底部距离</td>
		</tr>
		<tr>
			<td>fixedElements</td>
			<td>字符串</td>
			<td>无</td>
			<td>#header, .footer</td>
		</tr>
		<tr>
			<td>responsiveWidth</td>
			<td>整数</td>
			<td>0</td>
			<td></td>
		</tr>
		<tr>
			<td>responsiveHeight</td>
			<td>整数</td>
			<td>0</td>
			<td></td>
		</tr>

		<tr>
			<td>sectionSelector</td>
			<td>字符串</td>
			<td>.section</td>
			<td></td>
		</tr>
		<tr>
			<td>slideSelector</td>
			<td>字符串</td>
			<td>.slide</td>
			<td></td>
		</tr>
	</tbody>
</table>


##方法

<table>
	<thead>
	<tr>
		<th>名称</th>
		<th>说明</th>
	</tr>
	</thead>
	<tbody>
		<tr>
			<td>moveSectionUp()</td>
			<td>向上滚动</td>
		</tr>
		<tr>
			<td>moveSectionDown()</td>
			<td>向下滚动</td>
		</tr>
		<tr>
			<td>moveTo(section, slide)</td>
			<td>滚动到</td>
		</tr>
		<tr>
			<td>moveSlideRight()</td>
			<td>slide 向右滚动</td>
		</tr>
		<tr>
			<td>moveSlideLeft()</td>
			<td>slide 向左滚动</td>
		</tr>
		<tr>
			<td>setAutoScrolling()</td>
			<td>设置页面滚动方式，设置为 true 时自动滚动</td>
		</tr>
		<tr>
			<td>setAllowScrolling()</td>
			<td>添加或删除鼠标滚轮/触控板控制</td>
		</tr>
		<tr>
			<td>setKeyboardScrolling()</td>
			<td>添加或删除键盘方向键控制</td>
		</tr>
		<tr>
			<td>setScrollingSpeed()</td>
			<td>定义以毫秒为单位的滚动速度</td>
		</tr>
	</tbody>
</table>

##回调函数

<table>
	<thead>
		<tr>
			<th>名称</th>
			<th>说明</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>afterLoad</td>
			<td>滚动到某一屏后的回调函数，接收 anchorLink 和 index 两个参数，anchorLink 是锚链接的名称，index 是序号，从1开始计算</td>
		</tr>
		<tr>
			<td>onLeave</td>
			<td>
				<p>滚动前的回调函数，接收 index、nextIndex 和 direction 3个参数：index 是离开的“页面”的序号，从1开始计算；</p>
				<p>nextIndex 是滚动到的“页面”的序号，从1开始计算；</p>
				<p>direction 判断往上滚动还是往下滚动，值是 up 或 down。</p>
			</td>
		</tr>
		<tr>
			<td>afterRender</td>
			<td>页面结构生成后的回调函数，或者说页面初始化完成后的回调函数</td>
		</tr>
		<tr>
			<td>afterSlideLoad</td>
			<td>滚动到某一水平滑块后的回调函数，与 afterLoad 类似，接收 anchorLink、index、slideIndex、direction 4个参数</td>
		</tr>
		<tr>
			<td>onSlideLeave</td>
			<td>某一水平滑块滚动前的回调函数，与 onLeave 类似，接收 anchorLink、index、slideIndex、direction 4个参数</td>
		</tr>
		<tr>
			<td>afterResize</td>
			<td>浏览器窗口变化</td>
		</tr>
	</tbody>
</table>