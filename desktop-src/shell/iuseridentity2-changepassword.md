---
description: 不支援 ChangePassword，未來可能會變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2：： ChangePassword 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092695"
---
# <a name="iuseridentity2changepassword-method"></a>IUserIdentity2：： ChangePassword 方法

\[不支援 **ChangePassword** ，未來可能會變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

為身分識別設定新的密碼。

## <a name="syntax"></a>語法


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szOldPass* \[在\]
</dt> <dd>

類型： **WCHAR \***

寬字元字串，其中包含目前與身分識別相關聯的密碼。

</dd> <dt>

*szNewPass* \[在\]
</dt> <dd>

類型： **WCHAR \***

包含要與身分識別相關聯之新密碼的寬字元字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

*SzOldPass* 的值必須符合身分識別的目前密碼，才能套用 *szNewPass* 。 *SzOldPass* 的值不正確會導致 E 的傳回值 \_ 失敗。

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



 

 




