---
title: SystemRestore 類別的 Restore 方法
description: 起始系統還原。
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restore 方法系統還原
- Restore 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，Restore 方法
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a296c50493c5735651179febf1a55254557019aa91f8677071f4e769a35202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675885"
---
# <a name="restore-method-of-the-systemrestore-class"></a>SystemRestore 類別的 Restore 方法

起始系統還原。 呼叫端必須強制系統重新開機。 在重新開機期間進行實際的還原。

## <a name="syntax"></a>語法


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SequenceNumber* \[在\]
</dt> <dd>

還原點的序號。 若要判斷特定還原點的序號，請列舉系統上的所有還原點。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK。 否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。

## <a name="examples"></a>範例


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                         |
| 命名空間<br/>                | 根 \\ \\ 預設值<br/>                                                        |
| MOF<br/>                      | <dl> <dt>Sr-iov</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





