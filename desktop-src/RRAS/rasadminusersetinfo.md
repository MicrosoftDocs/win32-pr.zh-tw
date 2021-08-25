---
title: 'RasAdminUserSetInfo 函式 (Rassapi) '
description: RasAdminUserSetInfo 函式會設定指定使用者的 RAS 許可權和回撥電話號碼。
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51bc4b56b9aa606892002fbef0eda8036c45442c06ce06b8561afba57620b7a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028428"
---
# <a name="rasadminusersetinfo-function"></a>RasAdminUserSetInfo 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) 函式。\]

**RasAdminUserSetInfo** 函式會設定指定使用者的 RAS 許可權和回撥電話號碼。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
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

以 null 結束的 Unicode 字串指標，指定要設定 RAS 資訊之使用者的名稱。

</dd> <dt>

*pRasUser0* \[在\]
</dt> <dd>

[**RAS \_ 使用者 \_ 0**](ras-user-0-str.md)結構的指標，指定指定使用者的新 RAS 資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可以是下列其中一個錯誤碼。



| 值                                                                                                           | 描述                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 資料**</dt> </dl>             | *PRasUser0* 緩衝區包含不正確資料。<br/>                                        |
| <dl> <dt>**錯誤 \_ 不正確 \_ 回呼 \_ 號碼**</dt> </dl> | *PRasUser0* 緩衝區中指定的回呼號碼包含不正確字元。<br/> |
| <dl> <dt>**NERR \_BufTooSmall**</dt> </dl>               | 記憶體不足，無法執行此功能。<br/>                                        |



 

此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

設定使用者的 RAS 許可權時， [**RAS \_ 使用者 \_ 0**](ras-user-0-str.md)結構的 **bfPrivilege** 成員必須指定至少一個回撥旗標。 例如，若要將使用者的許可權設定為允許撥入許可權，但沒有回呼許可權，請將 **bfPrivilege** 設定為 RASPRIV \_ DialinPrivilege \| RASPRIV \_ NoCallback。

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

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> </dl>

 

