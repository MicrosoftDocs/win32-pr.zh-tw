---
description: 管理受控元素的度量。
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: CIM_MetricService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978992"
---
# <a name="cim_metricservice-class"></a>CIM \_ MetricService 類別

管理受控元素的度量。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>成員

**CIM \_ MetricService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**CIM \_ MetricService** 類別具有這些方法。



| 方法                                                                   | 描述                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ControlMetrics**](cim-metricservice-controlmetrics.md)               | 啟用及停用計量收集。<br/>                                                                                                                          |
| [**ControlMetricsByClass**](cim-metricservice-controlmetricsbyclass.md) | 啟用及停用類別的計量集合。<br/>                                                                                                              |
| [**ControlSampleTimes**](cim-metricservice-controlsampletimes.md)       | 指定收集計量的時機。<br/>                                                                                                                                     |
| [**GetMetricValues**](cim-metricservice-getmetricvalues.md)             | 抓取度量值的篩選清單。<br/>                                                                                                                              |
| [**ShowMetrics**](cim-metricservice-showmetrics.md)                     | 指出是否已針對指定的 managed 專案啟用計量收集，並指出可針對每個 managed 元素收集的計量。<br/> |
| [**ShowMetricsByClass**](cim-metricservice-showmetricsbyclass.md)       | 指出可針對 CIM 類別的所有實例收集哪些計量。<br/>                                                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 服務**](cim-service.md)
</dt> </dl>

 

 




