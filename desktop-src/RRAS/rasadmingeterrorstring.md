---
title: 'RasAdminGetErrorString 函式 (Rassapi) '
description: RasAdminGetErrorString 函式會抓取訊息字串，該字串會對應至其中一個 RAS 伺服器管理 (RasAdmin) 函式所傳回的 RAS 錯誤碼。
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001568"
---
# <a name="rasadmingeterrorstring-function"></a>RasAdminGetErrorString 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) 函式。\]

**RasAdminGetErrorString** 函式會抓取訊息字串，該字串會對應至其中一個 ras 伺服器管理 (RasAdmin) 函式所傳回的 ras 錯誤碼。 系統會從安裝為 RAS 一部分的 Rasmsg.dll 取出這些訊息字串。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ResourceId* \[在\]
</dt> <dd>

指定其中一個 RasAdmin 函數所傳回的錯誤碼。 此值必須在從 RASBASE 到 RASBASEEND 的錯誤碼範圍內。 這些是在 Raserror 中定義。

</dd> <dt>

*lpszString* \[擴展\]
</dt> <dd>

接收對應到指定錯誤碼之錯誤訊息的緩衝區指標。

</dd> <dt>

*InBufSize* \[在\]
</dt> <dd>

指定 *lpszString* 緩衝區的大小（以字元為單位）。 錯誤訊息通常是80個字元或更少：緩衝區大小為512個字元，一律為足夠的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值是錯誤碼。 這個值可以是 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)、 [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)或 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa) 函數所設定的最後一個錯誤值;或者，它可以是下列其中一個錯誤碼。



| 值                                                                                                      | 意義                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>   | *ResourceId* 或 *lpszString* 參數無效。<br/>      |
| <dl> <dt>**\_緩衝區不足的錯誤 \_**</dt> </dl> | *InBufSize* 參數所指定的大小太小。<br/> |



 

此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

RasAdmin 函數可以傳回不在 **RasAdminGetErrorString** 函數所支援範圍內的錯誤碼。 例如，RasAdmin 函式可能會傳回 Lmerr 中定義的錯誤碼，以及 Winerror.h. h。 在呼叫 **RasAdminGetErrorString** 之前，請確認錯誤碼位於 RASBASE 到 RASBASEEND 的範圍中，如 Raserror 中所定義。

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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[**Loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

