# 1 Drawing Contexts

`Drawing Contexts`是你在程序中用于绘制内容的虚拟的一块画布。在这一章节，你将了解到隐藏于iOS绘图底下的核心技术。你会用到上下文（contexts）来创建图像、文档和自定义视图，学习到使用UIKit，Core Graphics和Quartz来进行基础绘图。

## Frameworks
iOS的基础绘图程序主要来自于UIKit框架和QuartzCore框架。它们由现代风格的OC接口（来自于UIKit）和较老的基于C函数和CoreFoundation风格对象混合组成。这些内容共存于你的代码里。下面是一个用于说明一个UIKit绘图操作以及后续的Quartz绘图操作:

    // Draw a rounded rectangle in UIKit 
    UIBezierPath *bezierPath = [UIBezierPath bezierPathWithRoundedRect:inset cornerRadius:12]; [bezierPath stroke];    // Fill an ellipse in Quartz     CGContextFillEllipseInRect(context, rect);
QuartzCore框架通常被称为 Quartz 或者 Quartz 2D. 后者是苹果官方为其本地2D渲染和抗锯齿(antialiasing) API的命名。 它同样是Apple's developer library中用于提供基础绘图的参考指南 “Quartz 2D Programming Guide”的文件名。