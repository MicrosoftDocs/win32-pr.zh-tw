---
title: 'Delete 方法 (WSManDisp) '
description: 刪除資源 URI 中指定的資源。
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Delete 方法 Windows 遠端管理
- Delete 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理、Delete 方法
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 769ef3f462fa542e9afc6859b564e1a32ed87578894df4008fb6a19ad8aadad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858668"
---
# <a name="sessiondelete-method"></a>Session. Delete 方法

刪除資源 URI 中指定的資源。

## <a name="syntax"></a>語法


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*resourceUri* \[在\]
</dt> <dd>

要刪除之資源的 URI。 您也可以使用 [**ResourceLocator**](resourcelocator.md) 物件來指定資源。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

保留供未來使用。 必須設定為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

下列語法用來呼叫這個方法。


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>範例

下列 VBScript 程式碼範例會刪除針對 HTTP 傳輸設定的接聽程式。


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**會話**](session.md)
</dt> </dl>

 

 





