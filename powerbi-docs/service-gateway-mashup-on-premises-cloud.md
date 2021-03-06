---
title: 合并或追加本地和云数据源
description: 使用本地数据网关合并或追加同一查询中的本地和云数据源。
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-gateways
ms.topic: conceptual
ms.date: 06/06/2018
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 2547be7f7bdadb7f991db54230d4fd791941838d
ms.sourcegitcommit: 127df71c357127cca1b3caf5684489b19ff61493
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2018
ms.locfileid: "37600054"
---
# <a name="merge-or-append-on-premises-and-cloud-data-sources"></a>合并或追加本地和云数据源

借助本地数据网关，可合并或追加同一查询中的本地和云数据源。 这非常有用，因为无需使用单独的查询即可糅合来自多个源的数据。

## <a name="prerequisites"></a>先决条件

- 安装在本地计算机上的[网关](service-gateway-install.md)。
- 包含合并了本地和云数据源的查询的 Power BI Desktop 文件。

1. 在 Power BI 服务的右上角，选择齿轮图标![“设置”齿轮图标](media/service-gateway-mashup-on-premises-cloud/icon-gear.png) > “管理网关”。

    ![管理网关](media/service-gateway-mashup-on-premises-cloud/manage-gateways.png)

2. 选择要配置的网关。

3. 在“网关群集设置”下，选择“允许用户的云数据源通过此网关群集刷新” > “应用”。

    ![通过此网关群集刷新](media/service-gateway-mashup-on-premises-cloud/refresh-gateway-cluster.png)

4. 在此网关群集下，添加查询中使用的任何[本地数据源](service-gateway-enterprise-manage-scheduled-refresh.md#add-a-data-source)。 无需在此处添加云数据源。

5. 将包含合并了本地和云数据源的查询的 Power BI Desktop 文件上传到 Power BI 服务。

6. 在新数据集的“数据集设置”页上：

   - 对于本地源，选择与此数据源关联的网关。

   - 在“数据源凭据”下，根据需要编辑云数据源凭据。

     ![数据集设置](media/service-gateway-mashup-on-premises-cloud/dataset-settings.png)

7. 设置云凭据后，可使用“立即刷新”选项刷新数据集，或计划为定期刷新。


## <a name="next-steps"></a>后续步骤

若要详细了解网关的数据刷新，请参阅[将数据源用于定期刷新](service-gateway-enterprise-manage-scheduled-refresh.md#using-the-data-source-for-scheduled-refresh)。