---
title: 教程：使用 Power BI 连接到 GitHub 示例
description: 在本教程中，使用 Power BI 连接到 GitHub 服务中的真实数据，Power BI 即会自动创建仪表板和报表。
author: maggiesMSFT
manager: kfile
ms.reviewer: SarinaJoan
ms.service: powerbi
ms.subservice: powerbi-service
ms.custom: connect-to-services
ms.topic: tutorial
ms.date: 05/17/2018
ms.author: maggies
LocalizationGroup: Connect to services
ms.openlocfilehash: 8f44356f79b8a77ef06fe464671dbbaaaa4187e9
ms.sourcegitcommit: 5e83fa6c93a0bc6599f76cc070fb0e5c1fce0082
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/13/2019
ms.locfileid: "56215564"
---
# <a name="tutorial-connect-to-a-github-sample-with-power-bi"></a>教程：使用 Power BI 连接到 GitHub 示例
在本教程中，将介绍如何使用 Power BI 连接到 GitHub 服务中的真实数据，并自动创建仪表板和报表。 当连接到 Power BI 内容公共存储库（也称为“存储库”）后可以查看以下信息：包括有多少人参与编辑 Power BI 公共内容？ 谁的贡献最多？ 一周中哪天的贡献最大？ 以及其他一些问题。 

![Power BI 中的 GitHub 报表](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-punch-card.png)

在本教程中，将完成以下步骤：

> [!div class="checklist"]
> * 如果还没有 GitHub 帐户，请先注册一个帐户 
> * 登录 Power BI 帐户或进行注册（如果还没有）
> * 打开 Power BI 服务
> * 查找 GitHub 应用
> * 输入 Power BI 公共 GitHub 存储库的信息
> * 查看具有 GitHub 数据的仪表板和报表
> * 通过删除应用来清理资源

如果未注册 Power BI，请先[免费注册](https://app.powerbi.com/signupredirect?pbi_source=web)后再进行操作。

## <a name="prerequisites"></a>先决条件

要完成本教程，需要一个 GitHub 帐户，如果没有，请进行注册。 

- 注册 [GitHub 帐户](https://docs.microsoft.com/contribute/get-started-setup-github)


## <a name="how-to-connect"></a>如何连接
1. 登录 Power BI 服务 (http://powerbi.com) 。 
2. 在左侧导航窗格中，选择“应用”，然后选择“获取应用”。
   
   ![Power BI 获取应用](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial.png) 

3. 选择“应用”，然后在搜索框中键入 github 立即获取。
   
   ![Power BI 获取 GitHub](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-get-it-now.png) 

4. 在“安装当前Power BI应用？”中选择“安装”。
5. 在“你的新应用以及准备好”中选择“打开应用“。
6. 在“连接您的数据”中选择“连接数据”。
   ![开始使用新应用](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-connect-data.png)
7. 输入该存储库的存储库名称和存储库所有者。 此存储库的 URL 为 https://github.com/MicrosoftDocs/powerbi-docs，因此存储库所有者为 MicrosoftDocs，而存储库为 powerbi-docs。 
   
    ![Power BI GitHub 存储库名称](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-repo-name.png)

8. 输入创建的 GitHub 凭据。 如果已在浏览器中登录到 GitHub，Power BI 可能会跳过此步骤。 

9. 对于**身份验证方法**，选择**oAuth2**\>**登录**。

10. 按照 Github 验证界面执行操作。 向 Power BI 授予访问 GitHub 数据的权限。
   
   之后，Power BI 即可连接到 GitHub 并获取数据。  数据会每天刷新一次。

11. Power BI 导入数据后，将会生成一个名为 GitHub 的新工作区。 

12. 选择左侧导航栏内工作区名字旁边的箭头将其展开，能看到工作区内包含一个仪表板和一个报表。

    ![左侧导航栏上的应用](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-left-nav-expanded.png)

13. 选择仪表板名称旁的省略号（...）然后点击“重命名”，输入“GitHub仪表板”。
   ![Power BI中的GitHub仪表板 ](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-left-nav.png) 
14. 选择“全局导航”图标将左侧导航窗格最小化，以获得更多空间。

    ![“全局导航”图标](media/service-tutorial-connect-to-github/power-bi-global-navigation-icon.png)
    
15. 随即打开 GitHub 仪表板。 这是实时数据，因此看到的值可能有所不同。

    ![Power BI 中的 GitHub 仪表板](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-dashboard.png)

    

## <a name="ask-a-question"></a>提问

1. 将光标置于“询问数据相关问题”，然后选择“拉取请求”。 

    ![Power BI 提出数据相关问题](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-ask-question.png)

2. 键入“按月”。
 
    ![按月拉取请求](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-ask-question-by-month.png)

     Power BI 创建一个条形图，显示每月的拉取请求数量。

3. 选择“退出问答”。

## <a name="view-the-github-report"></a>查看 GitHub 报表 

1. 在 GitHub 仪表板中，选择“按月拉取请求”列线图，打开相关报表。

    ![“按月拉取请求”组合图](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-pull-requests-combo-chart.png)

2. 在“拉取请求总数(按用户)”图表中选择一个用户名，并查看其平均小时数是否大于 3 月份的平均总小时数（如本例所示）。

    ![Power BI GitHub 报表突出显示](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-report-highlight.png)

3. 选择“穿孔卡”选项卡来查看下一报表页面。 
 
    ![Power BI GitHub 穿孔片](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-tues-3pm.png)

    显然，用户最常在星期二下午 3 点查看提交项。

## <a name="clean-up-resources"></a>清理资源

现在，在完成本教程后，可删除 GitHub 应用。 

1. 在左侧导航栏中选择“应用”。
2. 将鼠标悬停在 GitHub 磁贴上，然后选择“删除”垃圾箱。

    ![删除 GitHub 应用](media/service-tutorial-connect-to-github/power-bi-github-app-tutorial-delete.png)

## <a name="next-steps"></a>后续步骤

在本教程中，已完成连接到 GitHub 公共存储库并获取经过Power BI 格式化后加载到仪表板和报表中的数据。 已通过浏览仪表板和报表回答了一些数据相关问题。 现在可深入了解如何连接到其他服务，例如 Salesforce、Microsoft Dynamics 和 Google Analytics。 
 
> [!div class="nextstepaction"]
> [连接到所使用的联机服务](service-connect-to-services.md)


