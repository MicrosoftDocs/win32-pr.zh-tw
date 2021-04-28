---
description: Msvm_VssComponent 類別的 RequestStateChange 方法-要求狀態變更。
ms.assetid: 27a8ab6e-afbd-4d87-afd6-8da0cc5e3fba
title: Msvm_VssComponent 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f75d0e2eed242155f27a7355182bf616d14de7e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109266"
---
# <a name="requeststatechange-method-of-the-msvm_vsscomponent-class"></a>Msvm VssComponent 類別的 RequestStateChange 方法 \_

要求狀態變更。

## <a name="syntax"></a>語法


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedState* \[在\]
</dt> <dd>

新狀態。 如果 **RequestStateChange** 方法的傳回碼為0或4096，資訊就會放在實例的 **RequestedState** 屬性中。 如需詳細資訊，請參閱元素的 **EnabledState** 和 **RequestedState** 屬性的描述。 這必須是下列值之一。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**關機** (4) 


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**離線** (6) 


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**測試** (7) 


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**延** 後 (8) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**靜止** (9) 


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**重新開機** (10) 


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**重設** (11) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> <dt>

*作業* \[擴展\]
</dt> <dd>

可能包含建立之 [**CIM \_ ConcreteJob**](cim-concretejob.md) 的參考，以追蹤方法調用所起始的狀態轉換。

</dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。 間隔格式必須用來指定 **TimeoutPeriod**。 值為0或 null 參數表示用戶端沒有轉換的時間需求。

如果這個屬性不包含0或 null，且執行不支援這個參數，則應該傳回「不支援使用 Timeout 參數」的傳回碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
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

[**Msvm \_ VssComponent**](msvm-vsscomponent.md)
</dt> </dl>

 

 




