---
description: GetIdentityFolder 不受支援，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'IUserIdentity：： GetIdentityFolder 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 20357dde27214177a454eb585dcd51182228c247da5aeae5ef887089b73ed85d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720604"
---
# <a name="iuseridentitygetidentityfolder-method"></a>IUserIdentity：： GetIdentityFolder 方法

\[**GetIdentityFolder** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

取得與此身分識別相關聯的檔案資料夾。

## <a name="syntax"></a>語法


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

類型： **DWORD**

必要。 值，這個值會指定與此身分識別相關聯的資料夾是否為漫遊。 必須是下列其中一個值。

<dt>



  (GIF \_ 漫遊 \_ 資料夾) 


</dt> <dd>

此資料夾為漫遊。

</dd> <dt>



  (GIF \_ 非 \_ 漫遊 \_ 資料夾) 


</dt> <dd>

資料夾是本機資料夾。

</dd> </dl> </dd> <dt>

*pszPath* \[在\]
</dt> <dd>

類型： **WCHAR \***

接收資料夾路徑的寬字元字串指標。

</dd> <dt>

*ulBuffSize* \[在\]
</dt> <dd>

類型： **ULONG**

值，指定 *pszPath* 的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




