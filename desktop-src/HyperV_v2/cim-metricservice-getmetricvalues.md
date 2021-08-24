---
description: 提供可傳回已篩選之 CIM BaseMetricValue 實例清單的能力 \_ 。
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: CIM_MetricService 類別的 GetMetricValues 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d010128bdef9bec4ce7df5fb3b1021a80a6ac99bdfbaf797958a76b27a812479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694998"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>CIM MetricService 類別的 GetMetricValues 方法 \_

提供可傳回已篩選之 [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) 實例清單的能力。

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

 

 




