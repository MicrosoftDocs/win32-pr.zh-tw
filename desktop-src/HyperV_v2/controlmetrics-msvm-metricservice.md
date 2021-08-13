---
description: 用來控制 managed 元素或元素的計量集合。
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Msvm_MetricService 類別的 ControlMetrics 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 051a08f261432c817bc0e56cab323c56cd11935c1541c40357b6b151a14f4074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645844"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Msvm MetricService 類別的 ControlMetrics 方法 \_

用來控制 managed 元素或元素的計量集合。

## <a name="syntax"></a>語法


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

主旨 \[在\]
</dt> <dd>

[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)實例，識別將收集計量的 managed 元素。 如果此參數為 **Null**，則會收集與 *定義* 參數相關聯之所有 managed 元素的度量。

</dd> <dt>

*定義* \[在\]
</dt> <dd>

指定將收集哪些計量的 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 實例。 如果此參數為 **Null**，則會收集與 *Subject* 參數所識別之 managed 元素相關聯之所有定義的計量。

</dd> <dt>

*MetricCollectionEnabled* \[在\]
</dt> <dd>

指定要在計量集合上執行的作業。 這必須是下列值之一。

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**啟用** (2) 


</dt> <dd>

啟用計量收集。

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (3) 


</dt> <dd>

停用計量收集。

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (4) 


</dt> <dd>

重設度量值。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

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

## <a name="remarks"></a>備註

在下列實例中，這個方法將會失敗：

-   *主體* 和 *定義* 參數都是 **Null**。
-   主旨 *和**定義* 參數都不是 **Null** ，而且沒有關聯兩個實例的 [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)實例。
-   *定義* 參數是 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)實例的參考，該實例與 [**Msvm \_ MetricService**](msvm-metricservice.md)之間的關聯性不會透過 [**Msvm \_ ServiceAffectsElement**](msvm-serviceaffectselement.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

