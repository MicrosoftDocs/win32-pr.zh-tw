---
description: 報告下列各項：可針對 managed 元素收集的計量、可供收集 CIM BaseMetricDefinition 實例所定義之計量的受控元素， \_ 以及目前是否正在收集 managed 專案的特定度量。
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: CIM_MetricService 類別的 ShowMetrics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115632"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a>CIM MetricService 類別的 ShowMetrics 方法 \_

報告下列各項：可針對 managed 元素收集的計量、可供收集 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例所定義之計量的受控元素，以及目前是否正在收集 managed 專案的特定度量。

## <a name="syntax"></a>語法


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

主旨 \[在\]
</dt> <dd>

識別 [**cim \_ managedelement**](cim-managedelement.md) 的實例，該實例會傳回 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例的參考，而該實例會定義針對 **cim \_ ManagedElement** 所捕捉的度量。

</dd> <dt>

*定義* \[在\]
</dt> <dd>

識別 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的實例。 方法會傳回 [**cim \_ ManagedElement**](cim-managedelement.md) 實例的參考，以供收集 **cim \_ BaseMetricDefinition** 實例所定義的計量。

</dd> <dt>

*ManagedElements* \[擴展\]
</dt> <dd>

成功時，可能會包含 [**CIM \_ ManagedElement**](cim-managedelement.md) 物件的參考，而這些物件是由 *定義* 參數所識別的計量可供收集。

</dd> <dt>

*DefinitionList* \[擴展\]
</dt> <dd>

成功時，可能會包含 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)物件之實例的參考，這些物件定義了針對 *Subject* 參數所識別之 [**cim \_ ManagedElement**](cim-managedelement.md)可收集的計量。

</dd> <dt>

*MetricNames* \[擴展\]
</dt> <dd>

成功時，每個陣列索引都應該包含 *DefinitionList* 參數的對應陣列索引所參考之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的 **名稱** 屬性值。

</dd> <dt>

*MetricCollectionEnabled* \[擴展\]
</dt> <dd>

指出是否針對 managed 元素收集度量。

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**停** 用 (3) 


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**保留** (4) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**方法保留** ( .。。) 
</dt> <dt>

**廠商特定** (32768. 65535) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ MetricService**](cim-metricservice.md)
</dt> </dl>

 

 




