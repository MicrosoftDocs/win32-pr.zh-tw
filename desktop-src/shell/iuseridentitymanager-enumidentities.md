---
description: IUserIdentityManager：： EnumIdentities 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'IUserIdentityManager：： EnumIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111717"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>IUserIdentityManager：： EnumIdentities 方法

\[**IUserIdentityManager：： EnumIdentities** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

取得 [**IEnumUserIdentity**](ienumuseridentity.md) 物件，可用來列舉系統上存在的使用者身分識別。

## <a name="syntax"></a>語法


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnumUser* \[擴展\]
</dt> <dd>

類型： **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

新身分識別列舉物件之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

抓取作業的結果。 如果成功，則會傳回 \_ [確定]。 如果無法建立列舉物件，它會傳回 E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個方法適用于反覆運算系統上的身分識別清單。 若要在不存取清單的情況下，透過 cookie 取得單一身分識別，請呼叫 [**IUserIdentityManager：： GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)。

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

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




