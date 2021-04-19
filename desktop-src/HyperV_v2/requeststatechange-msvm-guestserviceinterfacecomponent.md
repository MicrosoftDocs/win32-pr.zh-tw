---
description: 要求 guest 服務介面元件的狀態變更為指定的值。
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: Msvm_GuestServiceInterfaceComponent：： RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976881"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a>Msvm \_ GuestServiceInterfaceComponent：： RequestStateChange 方法

要求 guest 服務介面元件的狀態變更為指定的值。

## <a name="syntax"></a>語法


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedState* \[在\]
</dt> <dd>

類型： **uint16**

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

類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。 如果有，則會使用傳回的參考來監視進度，並取得方法的結果。

</dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

類型： **datetime**

指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。 間隔格式必須用來指定時間長度。 值為0或 **Null** 表示用戶端沒有轉換的時間需求。 如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                                                       | Description         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>                           | 成功。<br/> |
| <dl> <dt>**不支援**</dt> <dt>1</dt> </dl>                                     |                     |
| <dl> <dt>**未知/未指定的錯誤**</dt> <dt>2</dt> </dl>                         |                     |
| <dl> <dt>**無法在 Timeout 期限3內完成**</dt> <dt></dt> </dl>            |                     |
| <dl> <dt>**失敗**</dt> <dt>4</dt> </dl>                                            |                     |
| <dl> <dt>**不正確參數**</dt> <dt>5</dt> </dl>                                 |                     |
| <dl> <dt>**使用中**</dt> <dt>6</dt> </dl>                                            |                     |
| <dl> 已 <dt>**保留 DMTF**</dt> <dt></dt> </dl>                                    |                     |
| <dl> <dt>**方法參數檢查-轉換已啟動**</dt> <dt>4096</dt> </dl> |                     |
| <dl> <dt>**不正確狀態轉換**</dt> <dt>4097</dt> </dl>                       |                     |
| <dl> <dt>**不支援使用 Timeout 參數**</dt> <dt>4098</dt> </dl>         |                     |
| <dl> <dt>**忙碌**</dt> <dt>4099</dt> </dl>                                           |                     |
| <dl> <dt>**方法保留**</dt><dt>的 4100. 32767</dt> </dl>                         |                     |
| <dl> <dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt> </dl>                        |                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

