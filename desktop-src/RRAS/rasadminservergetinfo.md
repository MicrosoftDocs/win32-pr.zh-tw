---
title: 'RasAdminServerGetInfo 函式 (Rassapi) '
description: RasAdminServerGetInfo 函數會取得 RAS 伺服器的伺服器設定。
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993577"
---
# <a name="rasadminservergetinfo-function"></a>RasAdminServerGetInfo 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) 函式。\]

**RasAdminServerGetInfo** 函數會取得 RAS 伺服器的伺服器設定。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

以 **null** 結束的 Unicode 字串指標，指定 Windows NT/WINDOWS 2000 RAS 伺服器的名稱。 如果此參數為 **Null**，則函式會傳回本機電腦的相關資訊。 \\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。

</dd> <dt>

*pRasServer0* \[擴展\]
</dt> <dd>

[**RAS \_ 伺服器 \_ 0**](ras-server-0-str.md)結構的指標，此結構會接收伺服器上設定的埠數目、目前使用中的埠數目，以及伺服器版本號碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值是錯誤碼。 可能的錯誤代碼包括由 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 針對 [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) 函式傳回的錯誤碼。 此函數沒有任何延伸的錯誤資訊;請勿呼叫 **GetLastError**。

## <a name="remarks"></a>備註

若要列舉網域中的所有 RAS 伺服器，請呼叫 [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) 函式， \_ 並 \_ 為 *servertype* 參數指定 SV 類型撥入。

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

[**NetServerEnum**](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[**RAS \_ 伺服器 \_ 0**](ras-server-0-str.md)
</dt> </dl>

 

