---
description: 當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 Msvm \_ 錯誤實例。
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Msvm_StorageJob 類別的 GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 383b1bdd5fdff36b1f29c7d80a5ecee245aaeeba5db190965370754310ffc14d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532398"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a>Msvm Get-storagejob 類別的 GetErrorEx 方法 \_

當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。 但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。

## <a name="syntax"></a>語法


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*錯誤* \[擴展\]
</dt> <dd>

類型：**字串 \[ \]**

如果作業的操作狀態不是「確定」，這個方法會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例的陣列。 否則，如果作業是「確定」，則會傳回 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
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
</dt> </dl>

## <a name="remarks"></a>備註

存取 [**Msvm \_ get-storagejob**](msvm-storagejob.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ get-storagejob**](msvm-storagejob.md)
</dt> </dl>

 

