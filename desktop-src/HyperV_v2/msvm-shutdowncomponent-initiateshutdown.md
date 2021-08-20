---
description: 在相關聯的子虛擬機器上起始作業系統關閉操作。 如果傳回零 (0) ，則會成功啟動關機。 任何其他傳回碼表示錯誤狀況。
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: 'Msvm_ShutdownComponent 類別的 InitiateShutdown 方法 (Winreg. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f128eb2babfed0c70aca063832e579ad254ca1b02d6beaefb451c64598faa8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950397"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Msvm ShutdownComponent 類別的 InitiateShutdown 方法 \_

在相關聯的子虛擬機器上起始作業系統關閉操作。 如果傳回零 (0) ，則會成功啟動關機。 任何其他傳回碼表示錯誤狀況。

## <a name="syntax"></a>語法


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Force* \[在\]
</dt> <dd>

類型： **布林值**

若 **為 True，則** 會強制關閉應用程式，儘管有尚未儲存的資料。

</dd> <dt>

*原因* \[在\]
</dt> <dd>

類型： **字串**

關機操作的原因。 這是使用者定義的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**System 使用** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> <dt>

**找不到** 檔案 (32779) 
</dt> <dt>

**系統未就緒** (32780) 
</dt> <dt>

**電腦已鎖定，無法在沒有強制選項的情況下關閉** (32781) 
</dt> <dt>

**系統關機正在進行中** (32782) 
</dt> </dl>

## <a name="remarks"></a>備註

存取 [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| 標頭<br/>                   | <dl> <dt>Winreg. h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

