---
title: 'ConnectionOptions，Password 屬性 (WSManDisp. h) '
description: 設定遠端電腦上的本機或網域帳戶的密碼。 這個屬性會決定驗證的密碼。
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Password 屬性 Windows 遠端管理
- Password 屬性 Windows 遠端管理，ConnectionOptions 物件
- ConnectionOptions 物件 Windows 遠端管理，Password 屬性
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104586"
---
# <a name="connectionoptionspassword-property"></a>ConnectionOptions，Password 屬性

設定遠端電腦上的本機或網域帳戶的密碼。 這個屬性會決定驗證的密碼。 如需詳細資訊，請參閱 [遠端連線的驗證](authentication-for-remote-connections.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a>屬性值

字串，其中包含遠端電腦上的本機或網域帳戶的密碼。

如果未提供任何值，且未設定 **WSManFlagCredUsernamePassword** 旗標，則會使用執行腳本之帳戶的密碼。

如果未提供任何值，且已設定 **WSManFlagCredUsernamePassword** 旗標，則腳本會提示使用者輸入密碼 (和使用者名稱（如果未提供) ）。 如果未輸入有效的使用者名稱和密碼，則會傳回拒絕存取錯誤。

## <a name="remarks"></a>備註

請注意，您無法取得密碼。 密碼只能使用這個屬性來設定。

如果您建立 [**ConnectionOptions**](connectionoptions.md)物件，並使用使用者名稱和密碼連接到 Windows 遠端管理，則應該在對 [**WSMan. CreateSession**](wsman-createsession.md)的呼叫上設定 **WSManFlagCredUserNamePassword** 旗標。

如需設定密碼的詳細資訊，請參閱 [**ConnectionOptions**](connectionoptions.md)中的「備註」一節。

## <a name="examples"></a>範例

下列程式碼範例會建立 [**ConnectionOptions**](connectionoptions.md) 物件並設定 **密碼**。


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





