---
description: GetIdentityByCookie 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'IUserIdentityManager：： GetIdentityByCookie 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510771"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>IUserIdentityManager：： GetIdentityByCookie 方法

\[**GetIdentityByCookie** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

依據用來唯一識別它的 cookie 取得特定使用者身分識別。

## <a name="syntax"></a>語法


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uidCookie* \[在\]
</dt> <dd>

類型： **GUID \** _

_ *GUID** 值的位址，代表您要取得之身分識別的 cookie。

</dd> <dt>

*ppIdentity* \[擴展\]
</dt> <dd>

類型： **[ **IUserIdentity**](iuseridentity.md)\*\***

將接收使用者識別物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

抓取要求的結果。 如果成功，則會傳回 \_ [確定]。 否則，它會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                            | Description                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E \_ \_ 找不 \_ 到身分識別**</dt> </dl> | 找不到要求的身分識別。<br/>     |
| <dl> <dt>**E 身分識別 \_ \_ 已停用**</dt> </dl> | 系統上的身分識別管理已停用。<br/> |



 

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



 

 




