---
description: 要求作業狀態變更為指定的狀態。
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Msvm_ConcreteJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984584"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Msvm ConcreteJob 類別的 RequestStateChange 方法 \_

要求作業狀態變更為指定的狀態。 多次叫用 **RequestStateChange** 方法可能會導致較早的要求被覆寫或遺失。 如果傳回0，表示工作已順利完成。 任何其他傳回碼表示錯誤狀況。

## <a name="syntax"></a>語法


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedState* \[在\]
</dt> <dd>

類型： **uint16**

作業的新狀態。

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) 


</dt> <dd>

將狀態變更為「正在執行」。

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) 


</dt> <dd>

暫時停止作業。 其目的是要使用 "Start" 重新開機作業。 您可能可以在暫停時輸入「服務」狀態。  (這是特定作業。 ) 

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) 


</dt> <dd>

以有條理的方式，完全停止工作、儲存資料、保留狀態，以及關閉所有基礎進程。

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) 


</dt> <dd>

立即終止工作，不需要儲存資料或保留狀態。

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) 


</dt> <dd>

將工作放入廠商特定的服務狀態。 您可以重新開機作業。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**已保留 DMTF**


</dt> <dd>

保留的。

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**保留的廠商**


</dt> <dd>

保留的。

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

類型： **datetime**

指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。 間隔格式必須用來指定時間長度。 值為0或 **Null** 表示用戶端沒有轉換的時間需求。 如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (不支援使用 Timeout 參數) 必須傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**未知/未指定的錯誤** (2) 
</dt> <dt>

**無法在 Timeout 期間內完成** (3) 
</dt> <dt>

**失敗** (4) 
</dt> <dt>

**不正確參數** (5) 
</dt> <dt>

**使用** (6) 
</dt> <dt>

**DMTF 保留** 的 (7 4095) 
</dt> <dt>

**方法參數已檢查-轉換已啟動** (4096) 
</dt> <dt>

**不正確狀態轉換** (4097) 
</dt> <dt>

 (4098) **不支援使用 Timeout 參數**
</dt> <dt>

**忙碌** (4099) 
</dt> <dt>

**方法保留** (4100 32767) 
</dt> <dt>

**廠商專用** (32768 65535) 
</dt> </dl>

## <a name="remarks"></a>備註

存取 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

