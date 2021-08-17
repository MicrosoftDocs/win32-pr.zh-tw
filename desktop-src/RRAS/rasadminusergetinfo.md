---
title: 'RasAdminUserGetInfo 函式 (Rassapi) '
description: RasAdminUserGetInfo 函式會取得指定使用者的 RAS 許可權和回呼電話號碼資訊。
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RasAdminUserGetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4cda41447af832bd4ae04a14c6f8038fee4b61a17ac98c919c0b085261b242d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788684"
---
# <a name="rasadminusergetinfo-function"></a>RasAdminUserGetInfo 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) 函式。\]

**RasAdminUserGetInfo** 函式會取得指定使用者的 RAS 許可權和回呼電話號碼資訊。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszUserAccountServer* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，指定具有使用者帳戶資料庫之主要或備份網域控制站的名稱。 使用 [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) 函數來取得此伺服器名稱。

</dd> <dt>

*lpszUser* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，指定要取得其 RAS 資訊的使用者名稱。

</dd> <dt>

*pRasUser0* 
</dt> <dd>

[**Ras \_ 使用者 \_ 0**](ras-user-0-str.md)結構的指標，此結構會接收指定使用者的 ras 資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列錯誤碼。



| 值                                                                                            | 意義                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NERR \_ BufTooSmall**</dt> </dl> | 記憶體不足，無法執行此功能。<br/> |



 

此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/> | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                | <dl> <dt>Rassapi。h</dt> </dl>   |
| 程式庫<br/>               | <dl> <dt>Rassapi .lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理功能](ras-server-administration-functions.md)
</dt> <dt>

[**RAS \_ 使用者 \_ 0**](ras-user-0-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

