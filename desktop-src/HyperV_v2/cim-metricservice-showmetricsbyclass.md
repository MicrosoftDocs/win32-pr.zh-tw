---
description: 報告下列各項：可針對 CIM 類別的所有實例收集的計量、可供收集 CIM BaseMetricDefinition 實例所定義之計量的 CIM 類別， \_ 以及目前是否正在為 managed 元素收集特定的度量。
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: CIM_MetricService 類別的 ShowMetricsByClass 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c70d81f153471e841803dde195f09886137f29b390298c2c7d09ce69ad1648e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694948"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>CIM MetricService 類別的 ShowMetricsByClass 方法 \_

報告下列各項：可針對 CIM 類別的所有實例收集的計量、可供收集 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例所定義之計量的 cim 類別，以及目前是否正在為 managed 元素收集特定的度量。

## <a name="syntax"></a>語法


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

主旨 \[在\]
</dt> <dd>

識別 CIM 類別，其方法會將參考傳回給 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 的實例，以定義可針對類別的所有實例來捕捉的度量。

</dd> <dt>

*定義* \[在\]
</dt> <dd>

識別 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)的實例。 方法會傳回 [**cim \_ ManagedElement**](cim-managedelement.md) 實例的參考，以供收集 **cim \_ BaseMetricDefinition** 實例所定義的計量。

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

指出是否要針對 managed 專案類別的所有實例收集度量。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


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

 

 




