---
title: SystemRestore 類別的 GetLastRestoreStatus 方法
description: 捕獲上次系統還原的狀態。
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- GetLastRestoreStatus 方法系統還原
- GetLastRestoreStatus 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，GetLastRestoreStatus 方法
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965468"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>SystemRestore 類別的 GetLastRestoreStatus 方法

捕獲上次系統還原的狀態。

## <a name="syntax"></a>語法


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個狀態值。



| 傳回值                                                                 | 描述                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | 上次還原失敗。<br/>          |
| <dl> <dt>1</dt> </dl> | 上次還原成功。<br/>  |
| <dl> <dt>2</dt> </dl> | 上次還原已中斷。<br/> |



 

## <a name="examples"></a>範例


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                         |
| 命名空間<br/>                | 根 \\ 預設值<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr-iov</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





