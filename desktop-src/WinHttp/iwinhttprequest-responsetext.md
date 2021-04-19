---
description: 以文字形式抓取回應實體主體。
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: IWinHttpRequest：： ResponseText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975213"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="919e2-103">IWinHttpRequest：： ResponseText 屬性</span><span class="sxs-lookup"><span data-stu-id="919e2-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="919e2-104">**ResponseText** 屬性會以文字形式抓取回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="919e2-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="919e2-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="919e2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="919e2-106">語法</span><span class="sxs-lookup"><span data-stu-id="919e2-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="919e2-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="919e2-107">Property value</span></span>

<span data-ttu-id="919e2-108">以文字形式接收回應之實體主體的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="919e2-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="919e2-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="919e2-109">Error codes</span></span>

<span data-ttu-id="919e2-110">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="919e2-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="919e2-111">備註</span><span class="sxs-lookup"><span data-stu-id="919e2-111">Remarks</span></span>

<span data-ttu-id="919e2-112">這個屬性只能在呼叫 [**Send**](iwinhttprequest-send.md) 方法之後叫用。</span><span class="sxs-lookup"><span data-stu-id="919e2-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="919e2-113">在同步模式中使用此屬性時，它所傳回的字元數目限制大約為2169895。</span><span class="sxs-lookup"><span data-stu-id="919e2-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="919e2-114">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="919e2-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="919e2-115">範例</span><span class="sxs-lookup"><span data-stu-id="919e2-115">Examples</span></span>

<span data-ttu-id="919e2-116">下列範例顯示如何開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="919e2-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="919e2-117">這個範例必須從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="919e2-117">This example must be run from a command prompt.</span></span>


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

    // Print the response to a console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="919e2-118">下列腳本範例示範如何開啟 HTTP 連接、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="919e2-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="919e2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="919e2-119">Requirements</span></span>



| <span data-ttu-id="919e2-120">需求</span><span class="sxs-lookup"><span data-stu-id="919e2-120">Requirement</span></span> | <span data-ttu-id="919e2-121">值</span><span class="sxs-lookup"><span data-stu-id="919e2-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="919e2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="919e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="919e2-123">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="919e2-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="919e2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="919e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="919e2-125">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="919e2-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="919e2-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="919e2-126">Redistributable</span></span><br/>          | <span data-ttu-id="919e2-127">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="919e2-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="919e2-128">Idl</span><span class="sxs-lookup"><span data-stu-id="919e2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="919e2-129"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="919e2-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="919e2-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="919e2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="919e2-131"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="919e2-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="919e2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="919e2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="919e2-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919e2-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="919e2-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="919e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919e2-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="919e2-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="919e2-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="919e2-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="919e2-137">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="919e2-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="919e2-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="919e2-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="919e2-139">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="919e2-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




