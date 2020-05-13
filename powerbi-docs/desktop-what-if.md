---
title: 使用 what-if 参数可视化变量
description: 创建自己的模拟变量，想象并可视化 Power BI 报表中的变量
author: davidiseminger
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 01/21/2020
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 8a72bc43bcceae6e676728934ceec81c8cb27d04
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2020
ms.locfileid: "76539350"
---
# <a name="create-and-use-what-if-parameters-to-visualize-variables-in-power-bi-desktop"></a>创建和使用 What-if 参数可视化 Power BI Desktop 中的变量

从 Power BI Desktop 2018 年 8 月版开始，你可为报表创建 what-if 变量、以切片器的形式与变量交互，并对报表中的不同键值进行可视化和量化。

![新参数选项](media/desktop-what-if/what-if_01.png)

在 Power BI Desktop 中的“建模”选项卡上创建一个 what-if 参数。选择该参数后，你可看到一个对话框，可在其中配置该参数。

## <a name="creating-a-what-if-parameter"></a>创建模拟参数

要创建 what-if 参数，可在 Power BI Desktop 中的“建模”选项卡上选择“新建参数”。在下图中，我们创建了一个名为“折扣率”的参数，并将其数据类型设置为十进制数。最小值为 0。最大值为 0.50 (50%)。我们还将增量设置为 0.05，即 5%。这就是在报表中进行交互时参数的调整量。

![模拟参数值](media/desktop-what-if/what-if_02.png)

> [!NOTE]
> 对于十进制数，请务必在数值前加上一个 0（如 0.50 而不是 .50）。否则，该数值无法通过验证并且“确定”按钮不可选择。 
> 
> 

为方便起见，“将切片器添加到此页”  复选框会将切片器和模拟参数自动放置在当前报表页上。

![当前报表页上的新切片器](media/desktop-what-if/what-if_03.png)

除了创建参数之外，创建模拟参数还会创建一个度量值，可以用于直观显示模拟参数的当前值。

![为模拟参数创建的度量值](media/desktop-what-if/what-if_04.png)

注意，创建了一个 what-if 参数后，该参数和度量值便会成为模型的一部分，这一点很重要，也很实用。因此，它们可在整个报表上使用，也可用于其他报表页。由于它们是模型的一部分，你可从报表页中删除切片器。若要恢复该切片器，只需从“字段”列表中选择该 what-if 参数并将它拖动到画布上，然后将视觉对象更改为切片器即可。

## <a name="using-a-what-if-parameter"></a>使用模拟参数

让我们创建一个使用 what-if 参数的简单示例。我们在上一节中创建了一个 what-if 参数。现在，我们创建一个值随滑块一起调整的新度量值，以使用该参数。

![添加要用于参数的新度量值](media/desktop-what-if/what-if_05.png)

新的度量值只是简单地在总销售额上设置了折扣率。可创建复杂而有趣的度量值，使报表的使用者可对 what-if 参数的变量进行可视化。例如，你可创建一个报表，让销售人员可查看他们在完成特定销售目标或销售百分比时的薪酬，或者查看销售额增加对更优厚折扣力度的影响。

在公式栏中键入度量值公式，并将公式命名为“折后销售额”  。

![“折后销售额”定义](media/desktop-what-if/what-if_06.png)

然后，我们创建一个以“订单日期”为轴的柱形视觉对象，并将“销售额”和刚创建的度量值“折后销售额”作为值。

![SalesAmount 的可视化效果](media/desktop-what-if/what-if_07.png)

然后，当我们移动滑块时，可看到“折后销售额”柱反映了折扣后的销售额。

![滑块与可视化效果交互](media/desktop-what-if/what-if_08.png)

以上就是所有的内容。你可在各种情况下使用 what-if 参数。这些参数使报表的使用者能够与你在报表中创建的不同场景进行交互。
