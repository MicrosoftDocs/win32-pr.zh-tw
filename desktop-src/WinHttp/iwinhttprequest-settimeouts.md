---
description: SetTimeouts 方法會指定傳送/接收作業的個別超時元件（以毫秒為單位）。
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: IWinHttpRequest：： SetTimeouts 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104196159"
---
# <a name="iwinhttprequestsettimeouts-method"></a>IWinHttpRequest：： SetTimeouts 方法

**SetTimeouts** 方法會指定傳送/接收作業的個別超時元件（以毫秒為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ResolveTimeout* \[在\]
</dt> <dd>

在解析主機名稱時套用的超時值 (例如 `www.microsoft.com`) 至 IP 位址 (例如 192.168.131.199) （以毫秒為單位）。 預設值為零，表示沒有超時 (無限) 。 如果使用名稱解析 timeout 來指定 DNS timeout \_ \_ ，則每個要求會有一個執行緒的額外負荷。

</dd> <dt>

*ConnectTimeout* \[在\]
</dt> <dd>

與目標伺服器建立通訊通訊端時所套用的超時值（以毫秒為單位）。 預設值為 60000 (60 秒) 。

</dd> <dt>

*SendTimeout* \[在\]
</dt> <dd>

將通訊通訊端上要求資料的個別封包傳送至目標伺服器時，套用的超時值（以毫秒為單位）。 傳送至 HTTP 伺服器的大型要求通常會分成多個封包;傳送超時適用于個別傳送每個封包。 預設值為 30000 (30 秒) 。

</dd> <dt>

*ReceiveTimeout* \[在\]
</dt> <dd>

從目標伺服器接收回應資料的封包時，套用的超時值（以毫秒為單位）。 大型回應會分成多個封包;接收時間輸出適用于從通訊端提取每個資料封包。 預設值為 30000 (30 秒) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。

## <a name="remarks"></a>備註

全部都是必要參數。 值為0或-1 時，會設定一段時間來無限期等候。 大於0的值會設定超時時間值（以毫秒為單位）。 例如，30000會將時間設定為30秒。 -1 以外的所有負值都會導致此方法失敗。

超時值適用于 Winsock 層。

> [!Note]  
> 針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。

 

## <a name="examples"></a>範例

下列範例顯示如何將所有的 WinHTTP 超時設定為30秒、開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
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



下列腳本範例示範如何將所有的 WinHTTP 超時設定為30秒、開啟 HTTP 連接，以及傳送 HTTP 要求。


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>            |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>         |
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

 

 




