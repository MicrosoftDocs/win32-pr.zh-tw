---
description: 依類別顯示度量。
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Msvm_MetricService 類別的 ShowMetricsByClass 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996722"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Msvm MetricService 類別的 ShowMetricsByClass 方法 \_

依類別顯示度量。

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

當方法成功完成時，可能會包含 [**cim \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的參考，而這些實例會定義可供 *主體* 參數所識別之 [**cim \_ ManagedElement**](cim-managedelement.md)收集的計量。

</dd> <dt>

*MetricNames* \[擴展\]
</dt> <dd>

當方法成功完成時，每個陣列索引都包含 *DefinitionList* 參數的對應陣列索引所參考之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)實例的 **名稱** 屬性值。

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

這個方法會傳回下列其中一個值：

<dl> <dt>

**成功** () 
</dt> <dt>

**不支援** () 
</dt> <dt>

**失敗** 的 () 
</dt> <dt>

**方法保留** () 
</dt> <dt>

**特定廠商** () 
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

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




