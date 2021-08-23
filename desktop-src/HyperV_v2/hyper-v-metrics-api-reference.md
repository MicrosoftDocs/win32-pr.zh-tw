---
description: Hyper-v 計量 API 會定義下列程式設計項目。
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Hyper-v 計量 API 參考
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b833d96d26a3c48183c341ab0f1ff2bc9f5b178ca4439e1c035d82551ec3e094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532248"
---
# <a name="hyper-v-metrics-api-reference"></a>Hyper-v 計量 API 參考

Hyper-v 計量 API 會定義下列程式設計項目。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                    | 描述                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | 代表衍生自另一個計量值之度量的定義方面。<br/>                                                                                                                                                                                                                             |
| [**Msvm \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | 表示 [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) 類別的實例所定義之度量的實例值。<br/>                                                                                                                                                         |
| [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)<br/>               | 表示度量的定義方面。<br/>                                                                                                                                                                                                                                                                       |
| [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | 表示 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 類別的實例所定義的度量值。<br/>                                                                                                                                                                                       |
| [**Msvm \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | 表示兩個計量定義或兩個度量值之間的關聯。<br/>                                                                                                                                                                                                                                      |
| [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | 定義 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 與 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 之間的關聯，以定義後者的度量。 計量定義是由 ManagedElement 提供的內容，這就是定義相依于元素的原因。<br/> |
| [**Msvm \_ MetricForME**](msvm-metricforme.md)<br/>                                 | 此關聯會將 managed 元素連結至為其維護的度量值。<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | 表示計量值物件與其度量定義之間的關聯。<br/>                                                                                                                                                                                                                                    |
| [**Msvm \_ MetricService**](msvm-metricservice.md)<br/>                             | 提供管理計量的能力。<br/>                                                                                                                                                                                                                                                                              |
| [**Msvm \_ MetricServiceCapabilities**](msvm-metricservicecapabilities.md)<br/>     | 描述相關聯 [**Msvm \_ MetricService**](msvm-metricservice.md) 實例的功能。<br/>                                                                                                                                                                                                             |
| [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | 表示度量服務的設定。 無法直接修改這個類別的屬性。 用戶端必須呼叫 [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) 方法來修改任何這些屬性。<br/>                                                              |



 

 

