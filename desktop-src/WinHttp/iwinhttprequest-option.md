---
description: 設定或抓取 Microsoft Windows HTTP 服務 (WinHTTP) 選項值。
ms.assetid: 913573e6-fad3-42a5-bb5d-25a3d2ac9616
title: IWinHttpRequest：： Option 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Option
- IWinHttpRequest.get_Option
- IWinHttpRequest.put_Option
- WinHttpRequest.Option
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: c76df3f09871984da9f4bc093e9ac96d7484558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001753"
---
# <a name="iwinhttprequestoption-property"></a><span data-ttu-id="52f48-103">IWinHttpRequest：： Option 屬性</span><span class="sxs-lookup"><span data-stu-id="52f48-103">IWinHttpRequest::Option property</span></span>

<span data-ttu-id="52f48-104">**選項** 屬性會設定或抓取 MICROSOFT Windows HTTP Services (WinHTTP) 選項值。</span><span class="sxs-lookup"><span data-stu-id="52f48-104">The **Option** property sets or retrieves a Microsoft Windows HTTP Services (WinHTTP) option value.</span></span>

<span data-ttu-id="52f48-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="52f48-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52f48-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="52f48-106">Syntax</span></span>


```C++
HRESULT put_Option(
  [in]          WinHttpRequestOption Option,
  [in]          VARIANT              Value
);

HRESULT get_Option(
  [in]          WinHttpRequestOption Option,
  [out, retval] VARIANT              *Value
);
```


```JScript

vtOption = WinHttpRequest.Option
WinHttpRequest.Option = vtOption
```





## <a name="property-value"></a><span data-ttu-id="52f48-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="52f48-107">Property value</span></span>

<span data-ttu-id="52f48-108">包含選項值的 **變數** 值。</span><span class="sxs-lookup"><span data-stu-id="52f48-108">A **Variant** value that contains the option value.</span></span>

<span data-ttu-id="52f48-109">*Option* 參數指定要設定或取出的 [**WinHttpRequestOption**](winhttprequestoption.md) 。</span><span class="sxs-lookup"><span data-stu-id="52f48-109">The *Option* parameter specifies the [**WinHttpRequestOption**](winhttprequestoption.md) to set or retrieve.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52f48-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="52f48-110">Error codes</span></span>

<span data-ttu-id="52f48-111">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="52f48-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f48-112">備註</span><span class="sxs-lookup"><span data-stu-id="52f48-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52f48-113">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="52f48-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="52f48-114">範例</span><span class="sxs-lookup"><span data-stu-id="52f48-114">Examples</span></span>

<span data-ttu-id="52f48-115">下列範例將示範如何設定和查看 [*使用者代理*](glossary.md) 字串選項，以及查看其他各種選項。</span><span class="sxs-lookup"><span data-stu-id="52f48-115">The following example shows how to set and view the [*user agent*](glossary.md) string option and view various other options.</span></span>


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
    VARIANT         varUserAgent;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    varUserAgent.vt = VT_BSTR;
    varUserAgent.bstrVal = NULL;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Specify the user agent.
        varUserAgent.vt = VT_BSTR;
        varUserAgent.bstrVal =
                   SysAllocString(
                           L"A WinHttpRequest Example Program");

        //varUserAgent is L"A WinHttpRequest Example Program");
        hr = pIWinHttpRequest->put_Option(
                                 WinHttpRequestOption_UserAgentString,
                                 varUserAgent);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get user agent string.
        hr = pIWinHttpRequest->get_Option(
                                 WinHttpRequestOption_UserAgentString,
                                 &varUserAgent);
        // Print response to console.
        wprintf(L"%s\n\n", varUserAgent.bstrVal);

        // Get URL.
        hr = pIWinHttpRequest->get_Option(WinHttpRequestOption_URL,
                                          &varUserAgent);
        // Print response to console.
        wprintf(L"%s\n\n", varUserAgent.bstrVal);

        // Get URL Code Page.
        hr = pIWinHttpRequest->get_Option(
                                     WinHttpRequestOption_URLCodePage,
                                     &varUserAgent);
        // Print response to console.
        wprintf(L"%u\n\n", varUserAgent.lVal);

        // Convert percent symbols to escape sequences.
        hr = pIWinHttpRequest->get_Option(
                              WinHttpRequestOption_EscapePercentInURL,
                              &varUserAgent);
        // Print response to console.
        wprintf(L"%s\n", varUserAgent.boolVal?L"True":L"False");
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);
    if (varUserAgent.bstrVal)
        SysFreeString(varUserAgent.bstrVal);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="52f48-116">下列腳本範例顯示如何設定和查看選項。</span><span class="sxs-lookup"><span data-stu-id="52f48-116">The following scripting example shows how to set and view options.</span></span>


```JScript
// Define the constants used by the option property.
WinHttpRequestOption_UserAgentString = 0;    // Name of the user agent
WinHttpRequestOption_URL = 1;                // Current URL
WinHttpRequestOption_URLCodePage = 2;        // Code page
WinHttpRequestOption_EscapePercentInURL = 3; // Convert percents 
                                             // in the URL

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the WinHTTP option values.
WScript.Echo( 'User agent:      '+
             WinHttpReq.Option(WinHttpRequestOption_UserAgentString));
WScript.Echo( 'URL:             '+
             WinHttpReq.Option(WinHttpRequestOption_URL));
WScript.Echo( 'Code page:       '+
             WinHttpReq.Option(WinHttpRequestOption_URLCodePage));
WScript.Echo( 'Escape percents: '+
          WinHttpReq.Option(WinHttpRequestOption_EscapePercentInURL));
```



## <a name="requirements"></a><span data-ttu-id="52f48-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="52f48-117">Requirements</span></span>



| <span data-ttu-id="52f48-118">需求</span><span class="sxs-lookup"><span data-stu-id="52f48-118">Requirement</span></span> | <span data-ttu-id="52f48-119">值</span><span class="sxs-lookup"><span data-stu-id="52f48-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f48-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52f48-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52f48-121">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52f48-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="52f48-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52f48-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52f48-123">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="52f48-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="52f48-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="52f48-124">Redistributable</span></span><br/>          | <span data-ttu-id="52f48-125">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="52f48-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="52f48-126">Idl</span><span class="sxs-lookup"><span data-stu-id="52f48-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52f48-127"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="52f48-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="52f48-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="52f48-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="52f48-129"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52f48-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="52f48-130">DLL</span><span class="sxs-lookup"><span data-stu-id="52f48-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52f48-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52f48-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="52f48-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52f48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f48-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="52f48-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="52f48-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="52f48-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="52f48-135">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="52f48-135">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> <dt>

[<span data-ttu-id="52f48-136">**WinHttpRequestOption**</span><span class="sxs-lookup"><span data-stu-id="52f48-136">**WinHttpRequestOption**</span></span>](winhttprequestoption.md)
</dt> </dl>

 

 




