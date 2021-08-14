---
title: Disable SystemRestore 類別的方法
description: 停用特定磁片磁碟機上的監視。
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- 停用方法系統還原
- Disable 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，Disable 方法
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a05d53ee13e2f06c2f4765d2947f49a417ed798965406185619dfce207cf76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452919"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Disable SystemRestore 類別的方法

停用特定磁片磁碟機上的監視。

## <a name="syntax"></a>語法


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*磁片磁碟機* \[在\]
</dt> <dd>

要停用的磁片磁碟機。 磁片磁碟機字串的格式應為 "C： \\ "。 如果此參數為系統磁片磁碟機或空字串 ( "" ) ，則不會監視任何磁片磁碟機。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK。 否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。

## <a name="examples"></a>範例


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
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

 

 





