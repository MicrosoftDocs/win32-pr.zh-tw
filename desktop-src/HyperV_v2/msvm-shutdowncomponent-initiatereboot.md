---
description: 在相關聯的子虛擬機器上起始作業系統重新開機操作。
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Msvm_ShutdownComponent 類別的 InitiateReboot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20ec6e4522f4a9060ced517b5f9944177a98dfa5455c35e15285921467ed4620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950487"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>Msvm ShutdownComponent 類別的 InitiateReboot 方法 \_

在相關聯的子虛擬機器上起始作業系統重新開機操作。

如果傳回零 (0) ，則會成功啟動重新開機。 任何其他傳回碼表示錯誤狀況。

## <a name="syntax"></a>語法


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Force* \[在\]
</dt> <dd>

若為 TRUE，則會強制關閉應用程式，儘管有尚未儲存的資料。

</dd> <dt>

*原因* \[在\]
</dt> <dd>

重新開機操作的原因。 這是使用者定義的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值：

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




