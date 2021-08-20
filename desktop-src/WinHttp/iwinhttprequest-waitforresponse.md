---
description: WaitForResponse 方法會等候非同步傳送方法完成，並以秒為單位的選擇性超時值。
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: IWinHttpRequest：： WaitForResponse 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: e4f72edf2a3532c6d0f2641d979885e6d294c2ad923a28f19b71b348ea3a6377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051996"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>IWinHttpRequest：： WaitForResponse 方法

**WaitForResponse** 方法會等候非同步 [**傳送**](iwinhttprequest-send.md)方法完成，並以秒為單位的選擇性超時值。

## <a name="syntax"></a>語法


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Timeout* \[在中，選擇性\]
</dt> <dd>

超時值（以秒為單位）。 預設的超時時間是無限的。 若要明確地將超時時間設定為無限，請使用值-1。

</dd> <dt>

*成功* \[退出，retval\]
</dt> <dd>

接收下列其中一個值。



| 值                                                                                                                                                         | 意義                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**VARIANT \_ TRUE**</dt> </dl>    | 已收到回應。<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**VARIANT \_ FALSE**</dt> </dl> | 已超過指定的超時時間。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

這個方法會在等候非同步要求的回應時暫停執行。 [**傳送**](iwinhttprequest-send.md)之後，應該呼叫這個方法。 呼叫應用程式可以指定選擇性的 *超時* 值（以秒為單位）。 如果這個方法超時，要求就不會中止。 如此一來，呼叫的應用程式就可以在後續呼叫這個方法時，繼續等待要求（如有需要）。

在同步 [**傳送**](iwinhttprequest-send.md) 方法立即傳回之後呼叫這個屬性，而且沒有任何作用。

> [!Note]  
> 如 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的[執行時間需求](winhttp-start-page.md)一節。

 

## <a name="examples"></a>範例

下列範例顯示如何開啟非同步 HTTP 連線、傳送 HTTP 要求、等候回應，以及讀取回應文字。


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

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



下列腳本範例示範如何開啟非同步 HTTP 連接、傳送 HTTP 要求、等候回應，以及讀取回應文字。


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>         |
| 可轉散發套件<br/>          | Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WinHTTP .lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**打開**](iwinhttprequest-open.md)
</dt> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

 




