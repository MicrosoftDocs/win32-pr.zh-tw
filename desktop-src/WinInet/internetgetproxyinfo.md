---
title: InternetGetProxyInfo 函式
description: 抓取用來存取指定資源的 proxy 資料。
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- InternetGetProxyInfo 函數 WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76965f63afb751e810daa6feffe76774f03daaaf7278996b4c6800f0efa42dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113682"
---
# <a name="internetgetproxyinfo-function"></a>InternetGetProxyInfo 函式

> [!NOTE]
> 這個函數已被取代。 針對自動代理程式支援，請改用 (WinHTTP) 5.1 版的 HTTP 服務。 如需詳細資訊，請參閱 [WinHTTP 自動代理程式支援](../winhttp/winhttp-autoproxy-support.md)。

抓取用來存取指定資源的 proxy 資料。 只有動態連結至 "JSProxy.dll"，才能呼叫此函式。

## <a name="syntax"></a>語法

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*lpszUrl* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定目標 HTTP 資源的 URL。

</dd> <dt>

*dwUrlLength* \[在\]
</dt> <dd>

*LpszUrl* 所指向的 URL 大小（以位元組為單位）。

</dd> <dt>

*lpszUrlHostName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定目標 URL 的主機名稱。

</dd> <dt>

*dwUrlHostNameLength* \[在\]
</dt> <dd>

*LpszUrlHostName* 所指向之主機名稱的大小（以位元組為單位）。

</dd> <dt>

*lplpszProxyHostName* \[擴展\]
</dt> <dd>

緩衝區位址的指標，此緩衝區會接收要在指定資源的 HTTP 要求中使用之 proxy 的 URL。 應用程式會負責釋放這個字串。

</dd> <dt>

*lpdwProxyHostNameLength* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 *lplpszProxyHostName* 緩衝區中傳回之字串的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。 若要取得擴充的錯誤資料，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

若要呼叫 **InternetGetProxyInfo**，您必須使用定義的函式指標類型 **pfnInternetGetProxyInfo**，以動態方式連結至該函式。 下列程式碼片段顯示如何宣告此函式指標類型的實例，然後初始化並呼叫它。

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

如同 WinINet API 的所有其他層面，無法從 DllMain 或全域物件的函式和析構函式中，安全地呼叫這個函式。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>另請參閱

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
