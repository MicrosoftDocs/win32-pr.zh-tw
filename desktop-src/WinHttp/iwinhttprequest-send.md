---
description: Send 方法會將 HTTP 要求傳送至 HTTP 伺服器。
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: IWinHttpRequest：： Send 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Send
- WinHttpRequest.Send
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0040ed6c09814a2b2112a91173d84430b8130a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694195"
---
# <a name="iwinhttprequestsend-method"></a><span data-ttu-id="45c27-103">IWinHttpRequest：： Send 方法</span><span class="sxs-lookup"><span data-stu-id="45c27-103">IWinHttpRequest::Send method</span></span>

<span data-ttu-id="45c27-104">Send 方法會將 HTTP 要求 **傳送** 至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="45c27-104">The **Send** method sends an HTTP request to an HTTP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c27-105">語法</span><span class="sxs-lookup"><span data-stu-id="45c27-105">Syntax</span></span>


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a><span data-ttu-id="45c27-106">參數</span><span class="sxs-lookup"><span data-stu-id="45c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c27-107">*主體* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="45c27-107">*Body* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="45c27-108">要傳送至伺服器的資料。</span><span class="sxs-lookup"><span data-stu-id="45c27-108">Data to be sent to the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c27-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="45c27-109">Return value</span></span>

<span data-ttu-id="45c27-110">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="45c27-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="45c27-111">備註</span><span class="sxs-lookup"><span data-stu-id="45c27-111">Remarks</span></span>

<span data-ttu-id="45c27-112">要傳送的要求是在先前的 [**Open**](iwinhttprequest-open.md) 方法呼叫中定義。</span><span class="sxs-lookup"><span data-stu-id="45c27-112">The request to be sent was defined in a prior call to the [**Open**](iwinhttprequest-open.md) method.</span></span> <span data-ttu-id="45c27-113">呼叫應用程式可以提供資料，以透過 *主體* 參數傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="45c27-113">The calling application can provide data to be sent to the server through the *Body* parameter.</span></span> <span data-ttu-id="45c27-114">如果物件的 [*HTTP 動詞*](glossary.md)[**命令為 "**](iwinhttprequest-open.md) GET"，則這個方法會傳送沒有 *主體* 的要求，即使是由呼叫的應用程式提供也一樣。</span><span class="sxs-lookup"><span data-stu-id="45c27-114">If the [*HTTP verb*](glossary.md) of the object's [**Open**](iwinhttprequest-open.md) is "GET", this method sends the request without *Body*, even if it is provided by the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="45c27-115">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="45c27-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="45c27-116">範例</span><span class="sxs-lookup"><span data-stu-id="45c27-116">Examples</span></span>

<span data-ttu-id="45c27-117">下列範例顯示如何開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="45c27-117">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print response to console.
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



<span data-ttu-id="45c27-118">下列腳本範例示範如何開啟 HTTP 連接、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="45c27-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="45c27-119">下列腳本範例顯示如何將資料張貼至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="45c27-119">The following scripting example shows how to post data to an HTTP server.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a><span data-ttu-id="45c27-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="45c27-120">Requirements</span></span>



| <span data-ttu-id="45c27-121">需求</span><span class="sxs-lookup"><span data-stu-id="45c27-121">Requirement</span></span> | <span data-ttu-id="45c27-122">值</span><span class="sxs-lookup"><span data-stu-id="45c27-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c27-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45c27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="45c27-124">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45c27-124">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="45c27-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45c27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="45c27-126">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="45c27-126">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="45c27-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="45c27-127">Redistributable</span></span><br/>          | <span data-ttu-id="45c27-128">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="45c27-128">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="45c27-129">Idl</span><span class="sxs-lookup"><span data-stu-id="45c27-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45c27-130"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="45c27-130"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="45c27-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="45c27-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="45c27-132"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45c27-132"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="45c27-133">DLL</span><span class="sxs-lookup"><span data-stu-id="45c27-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45c27-134"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45c27-134"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="45c27-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45c27-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c27-136">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="45c27-136">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="45c27-137">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="45c27-137">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="45c27-138">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="45c27-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




