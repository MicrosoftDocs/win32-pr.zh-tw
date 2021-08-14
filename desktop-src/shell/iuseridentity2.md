---
description: IUserIdentity2 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: 'IUserIdentity2 介面 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a1a23ea6e0d5832ee6d78453f3a246b9db749c0d7b24b90a2199a7e8cfd225b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720584"
---
# <a name="iuseridentity2-interface"></a>IUserIdentity2 介面

\[**IUserIdentity2** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

公開方法，以提供特定使用者身分識別的命名、密碼和序數控制項。

## <a name="members"></a>成員

**IUserIdentity2** 介面繼承自 [**IUserIdentity**](iuseridentity.md)。 **IUserIdentity2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IUserIdentity2** 介面具有這些方法。



| 方法                                                  | 描述                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | 已取代。 為身分識別設定新的密碼。<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | 已取代。 取得此身分識別的序號。<br/> |
| [**SetName**](iuseridentity2-setname.md)               | 已取代。 設定身分識別的顯示名稱。<br/>     |



 

## <a name="remarks"></a>備註

這個介面也會提供它所繼承之 [**IUserIdentity**](iuseridentity.md) 介面的方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> </dl>

 

 




