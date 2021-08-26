---
title: 'RasAdminGetUserAccountServer 函式 (Rassapi) '
description: RasAdminGetUserAccountServer 函式會抓取具有使用者帳戶資料庫的伺服器名稱。 在 RasAdminUserGetInfo 和 RasAdminUserSetInfo 函數中使用傳回的伺服器名稱，以取得或設定指定使用者的相關資訊。
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2ac4052ad4638c3e0e2483adb68857f4c2b670322434107d93100b6a177855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028538"
---
# <a name="rasadmingetuseraccountserver-function"></a>RasAdminGetUserAccountServer 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) 函式。\]

**RasAdminGetUserAccountServer** 函式會抓取具有使用者帳戶資料庫的伺服器名稱。 在 [**RasAdminUserGetInfo**](rasadminusergetinfo.md) 和 [**RasAdminUserSetInfo**](rasadminusersetinfo.md) 函數中使用傳回的伺服器名稱，以取得或設定指定使用者的相關資訊。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszDomain* \[在\]
</dt> <dd>

以 **null** 結束的 Unicode 字串指標，指定 RAS 伺服器所屬之網域的名稱。 對於在非網域成員的工作站或伺服器上執行的 RAS 管理應用程式而言，這個參數是 **Null** 。 如果此參數為 **null**，則 *lpszServer* 參數必須為非 **null**。

</dd> <dt>

*lpszServer* \[在\]
</dt> <dd>

以 **null** 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。 \\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。 如果 *lpszDomain* 參數不是 **null**，這個參數可以是 **null** 。

</dd> <dt>

*lpszUserAccountServer* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收以 **null** 終止的 Unicode 字串，這個字串會指定擁有使用者帳戶資料庫之網域控制站的名稱。 緩衝區必須夠大，才能保存伺服器名稱 (UNCLEN + 1) 。 函數會在傳回的伺服器名稱前面加 \\ \\ 上 "" 字元，格式為： \\ \\ *servername*。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列錯誤碼。



| 值                                                                                                    | 意義                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl> | *LpszDomain* 和 *LpszServer* 都是 **Null**。<br/> |



 

此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**RasAdminGetUserAccountServer** 函數會取得具有使用者帳戶資料庫的伺服器名稱。 此函數需要 RAS 伺服器的名稱，或 RAS 伺服器所在網域的名稱。

*LpszDomain* 參數應指定有效的功能變數名稱。 對於在非網域成員的伺服器上執行的 RAS 系統管理應用程式而言，這個參數是 **Null** (例如，伺服器位於自己的工作組) 中。 在此情況下， *lpszServer* 參數必須指定伺服器名稱。 若要取得伺服器名稱，請呼叫 [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) 函數。 請務必在伺服器名稱前面加上 " \\ \\ " 字元。

如果 *lpszServer* 所指定的伺服器名稱是獨立伺服器 (也就是伺服器或工作站不是網域) 的成員，則伺服器名稱本身會在 *lpszUserAccountServer* 緩衝區中傳回。

然後，在 [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) 函式的呼叫中使用使用者帳戶伺服器的名稱，以列舉使用者帳戶資料庫中的使用者。

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

[**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

