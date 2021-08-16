---
description: IUserIdentity：： GetName 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'IUserIdentity：： GetName 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 035f7c61290fb60e70821f0a43676c41dca0fc92cebc8ecfb963bb757ab47a5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661188"
---
# <a name="iuseridentitygetname-method"></a>IUserIdentity：： GetName 方法

\[**IUserIdentity：： GetName** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

取得與此使用者識別相關聯的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszName* \[在\]
</dt> <dd>

類型： **WCHAR \***

寬字元字串的指標，此字串會接收此使用者識別的名稱。

</dd> <dt>

*ulBuffSize* \[在\]
</dt> <dd>

類型： **ULONG**

值，指定 *pszName* 的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**SetName**](iuseridentity2-setname.md)
</dt> </dl>

 

 




