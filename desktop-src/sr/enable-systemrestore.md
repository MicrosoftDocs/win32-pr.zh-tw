---
title: Enable SystemRestore 類別的方法
description: 在特定磁片磁碟機上啟用監視。
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- 啟用方法系統還原
- Enable 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，Enable 方法
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91989b3c75b4a825dd3cfdc752a8b659e4e4a0cf26107e8d9cdfad5b9bfb824b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047568"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Enable SystemRestore 類別的方法

在特定磁片磁碟機上啟用監視。

## <a name="syntax"></a>語法


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*磁片磁碟機* \[在\]
</dt> <dd>

要啟用的磁片磁碟機。 磁片磁碟機字串的格式應為 "C： \\ "。 如果此參數為系統磁片磁碟機，或 ( "" ) 的空字串，則會監視所有磁片磁碟機。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK。 否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。

## <a name="remarks"></a>備註

**Enable** 方法在傳回之前，不會等待監視完全啟用，因為這可能需要一些時間。 相反地，它會在啟動系統還原服務和篩選器驅動程式之後立即返回。

若要在非系統磁片磁碟機上啟用系統還原，您必須先在系統磁片磁碟機上啟用系統還原。

在安全模式中，這個方法會失敗。

## <a name="examples"></a>範例


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                         |
| 命名空間<br/>                | 根 \\ 預設值<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr-iov</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





