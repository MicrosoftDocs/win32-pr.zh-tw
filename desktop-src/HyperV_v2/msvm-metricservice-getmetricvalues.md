---
description: 取得度量值。
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Msvm_MetricService 類別的 GetMetricValues 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c22aa9adab9fc69876329f6be0ff011765da61a714c518241c47d3b2bd882ec2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521458"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a>Msvm MetricService 類別的 GetMetricValues 方法 \_

取得度量值。

## <a name="syntax"></a>語法


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*定義* \[在\]
</dt> <dd>

識別將傳回其計量的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 。

</dd> <dt>

*範圍* \[在\]
</dt> <dd>

識別如何選取實例。 排序值實例的演算法是特定的度量定義。

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**最小** (2) 


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**最大** (3) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**廠商特定** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> <dt>

*計數* \[在\]
</dt> <dd>

識別方法所傳回的最大實例數目。

</dd> <dt>

*值* \[擴展\]
</dt> <dd>

當方法成功完成時，會包含 [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md)實例的參考，並根據輸入參數的值進行篩選。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

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

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

 




