---
title: 'DsSetAuthIdentity 函式 (Ntdsbcli) '
description: 設定用來呼叫目錄備份 Api 的安全性內容。
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- DsSetAuthIdentity 函式 Active Directory
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695503"
---
# <a name="dssetauthidentity-function"></a>DsSetAuthIdentity 函式

\[此函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 從 Windows Vista 開始，請改用[磁碟區陰影複製服務 (VSS) ](../vss/volume-shadow-copy-service-overview.md) 。\]

**DsSetAuthIdentity** 函式會設定用來呼叫目錄備份 api 的安全性內容。

## <a name="syntax"></a>語法


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szUserName* \[在\]
</dt> <dd>

指定使用者名稱的以 null 結束的字串。

</dd> <dt>

*szDomainName* \[在\]
</dt> <dd>

以 null 終止的字串，指定使用者所屬之網域的名稱。

</dd> <dt>

*szPassword* \[在\]
</dt> <dd>

以 null 終止的字串，指定指定網域中使用者的密碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回標準的 **HRESULT** 成功碼;否則，會傳回失敗碼。

## <a name="remarks"></a>備註

如果未呼叫 **DsSetAuthIdentity** ，則會假設為目前進程的安全性內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Ntdsbcli .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DsSetAuthIdentityW** (Unicode) 和 **DsSetAuthIdentityA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[備份與還原 Active Directory 伺服器](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[目錄備份功能](directory-backup-functions.md)
</dt> </dl>

 

