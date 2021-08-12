---
description: 設定 proxy 伺服器資訊。
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: IWinHttpRequest：： SetProxy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: bb85466da6b7492d04bd2e69f4cd51c0c390e9595df13af8d7e6768596771822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562591"
---
# <a name="iwinhttprequestsetproxy-method"></a>IWinHttpRequest：： SetProxy 方法

**SetProxy** 方法會設定 proxy 伺服器資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProxySetting* \[在\]
</dt> <dd>

控制此方法的旗標。 可以是下列其中一個值。



| 值                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ 預設值</dt> </dl>   | 預設 proxy 設定。 相當於 **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG**。<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG</dt> </dl> | 指出應該從登錄取得 proxy 設定。 這會假設 [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) 已執行。 如果未執行 Proxycfg.exe 且指定了 **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG** ，則行為相當於 **HTTPREQUEST \_ PROXYSETTING \_ DIRECT**。<br/> |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ DIRECT</dt> </dl>    | 表示應該直接存取所有 HTTP 和 HTTPS 伺服器。 如果沒有任何 proxy 伺服器，則使用此命令。<br/>                                                                                                                                                                                                                       |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ PROXY</dt> </dl>     | 指定 **HTTPREQUEST \_ PROXYSETTING \_ PROXY** 時， *varProxyServer* 應該設定為 proxy 伺服器字串，而 *varBypassList* 應設定為網域略過清單字串。 此 proxy 設定只適用于目前的 [**WinHttpRequest**](winhttprequest.md) 物件實例。<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[在中，選擇性\]
</dt> <dd>

當 *ProxySetting* 等於 **HTTPREQUEST \_ ProxySetting \_ proxy** 時，設定為 proxy 伺服器字串。

</dd> <dt>

*BypassList* \[在中，選擇性\]
</dt> <dd>

當 *ProxySetting* 等於 **HTTPREQUEST \_ ProxySetting \_ PROXY** 時，設定為網域略過清單字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

可讓呼叫的應用程式指定使用 proxy 設定工具 (設定的預設 proxy 資訊，) 或覆寫 [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md)。 呼叫 [**Send**](iwinhttprequest-send.md) 方法之前，必須先呼叫這個方法。 如果在 [**傳送**](iwinhttprequest-send.md) 方法之後呼叫此方法，則不會有任何作用。

[**IWinHttpRequest**](iwinhttprequest-interface.md)會將這些參數傳遞給 Microsoft Windows (WinHTTP) 的 HTTP 服務。

> [!Note]  
> 如 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的[執行時間需求](winhttp-start-page.md)一節。

 

## <a name="examples"></a>範例

下列範例顯示如何設定特定 proxy 伺服器的 proxy 設定、開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。 這個範例必須從命令提示字元執行。 只有當您的 proxy 伺服器名為「proxy \_ 伺服器」（使用埠80），且當主機名稱的結尾是 ". microsoft.com" 時，您的電腦可以略過 proxy 伺服器，這些 proxy 設定才適用。


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
        }
    if (SUCCEEDED(hr))
    {   // Open WinHttpRequest.
            BSTR bstrMethod  = SysAllocString(L"GET");
                BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
                SysFreeString(bstrMethod);
                SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
                hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



下列腳本範例顯示如何設定特定 proxy 伺服器的 proxy 設定、開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。 只有當您的 proxy 伺服器名為「proxy \_ 伺服器」（使用埠80），且當主機名稱的結尾是 ". microsoft.com" 時，您的電腦可以略過 proxy 伺服器，這些 proxy 設定才適用。


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WinHTTP .lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




