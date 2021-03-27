---
description: 已取代。 抓取登錄中對應此使用者識別的索引鍵。
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'IUserIdentity：： OpenIdentityRegKey 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972320"
---
# <a name="iuseridentityopenidentityregkey-method"></a>IUserIdentity：： OpenIdentityRegKey 方法

\[**IUserIdentity：： OpenIdentityRegKey** 方法可用於 Windows 2000。 在 Windows XP 中，這項功能已由 [使用者帳戶取代為快速使用者切換和遠端桌面](fastuserswitching.md)，而且可能會在後續版本中變更或無法使用。\]

已取代。 抓取登錄中對應此使用者識別的索引鍵。

## <a name="syntax"></a>語法


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwDesiredAccess* \[在\]
</dt> <dd>

類型： **DWORD**

值，描述登錄機碼要求的存取層級。

</dd> <dt>

*phKey* \[擴展\]
</dt> <dd>

類型： **HKEY \** _

接收登錄機碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

登錄要求的結果。 如果成功，則會 **傳回 \_ [確定]**。 否則，它會傳回下列其中一個錯誤碼。



| 傳回碼                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**E \_ \_ 找不 \_ 到身分識別**</dt> </dl> | 此身分識別沒有相關聯的登錄機碼。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                 | 無法存取登錄機碼。<br/>             |



 

## <a name="remarks"></a>備註

*DwDesiredAccess* 參數是標準的登錄存取安全描述項，描述您想要對登錄機碼取得的存取權。 如需登錄安全性的詳細資訊，包括此參數可接受的值清單，請參閱登錄機 [碼安全性和存取權限](../sysinfo/registry-key-security-and-access-rights.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
