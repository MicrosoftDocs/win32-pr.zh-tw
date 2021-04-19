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
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985320"
---
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="edc82-103">IWinHttpRequest：： WaitForResponse 方法</span><span class="sxs-lookup"><span data-stu-id="edc82-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="edc82-104">**WaitForResponse** 方法會等候非同步 [**傳送**](iwinhttprequest-send.md)方法完成，並以秒為單位的選擇性超時值。</span><span class="sxs-lookup"><span data-stu-id="edc82-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc82-105">語法</span><span class="sxs-lookup"><span data-stu-id="edc82-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="edc82-106">參數</span><span class="sxs-lookup"><span data-stu-id="edc82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc82-107">*Timeout* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="edc82-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="edc82-108">超時值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="edc82-108">Time-out value, in seconds.</span></span> <span data-ttu-id="edc82-109">預設的超時時間是無限的。</span><span class="sxs-lookup"><span data-stu-id="edc82-109">Default time-out is infinite.</span></span> <span data-ttu-id="edc82-110">若要明確地將超時時間設定為無限，請使用值-1。</span><span class="sxs-lookup"><span data-stu-id="edc82-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="edc82-111">*成功* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="edc82-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="edc82-112">接收下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="edc82-112">Receives one of the following values.</span></span>



| <span data-ttu-id="edc82-113">值</span><span class="sxs-lookup"><span data-stu-id="edc82-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="edc82-114">意義</span><span class="sxs-lookup"><span data-stu-id="edc82-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="edc82-115"><dt>**VARIANT \_ TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="edc82-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="edc82-116">已收到回應。</span><span class="sxs-lookup"><span data-stu-id="edc82-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="edc82-117"><dt>**VARIANT \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="edc82-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="edc82-118">已超過指定的超時時間。</span><span class="sxs-lookup"><span data-stu-id="edc82-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc82-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="edc82-119">Return value</span></span>

<span data-ttu-id="edc82-120">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="edc82-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="edc82-121">備註</span><span class="sxs-lookup"><span data-stu-id="edc82-121">Remarks</span></span>

<span data-ttu-id="edc82-122">這個方法會在等候非同步要求的回應時暫停執行。</span><span class="sxs-lookup"><span data-stu-id="edc82-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="edc82-123">[**傳送**](iwinhttprequest-send.md)之後，應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="edc82-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="edc82-124">呼叫應用程式可以指定選擇性的 *超時* 值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="edc82-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="edc82-125">如果這個方法超時，要求就不會中止。</span><span class="sxs-lookup"><span data-stu-id="edc82-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="edc82-126">如此一來，呼叫的應用程式就可以在後續呼叫這個方法時，繼續等待要求（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="edc82-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="edc82-127">在同步 [**傳送**](iwinhttprequest-send.md) 方法立即傳回之後呼叫這個屬性，而且沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="edc82-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="edc82-128">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="edc82-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="edc82-129">範例</span><span class="sxs-lookup"><span data-stu-id="edc82-129">Examples</span></span>

<span data-ttu-id="edc82-130">下列範例顯示如何開啟非同步 HTTP 連線、傳送 HTTP 要求、等候回應，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="edc82-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


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



<span data-ttu-id="edc82-131">下列腳本範例示範如何開啟非同步 HTTP 連接、傳送 HTTP 要求、等候回應，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="edc82-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="edc82-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="edc82-132">Requirements</span></span>



| <span data-ttu-id="edc82-133">需求</span><span class="sxs-lookup"><span data-stu-id="edc82-133">Requirement</span></span> | <span data-ttu-id="edc82-134">值</span><span class="sxs-lookup"><span data-stu-id="edc82-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc82-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edc82-135">Minimum supported client</span></span><br/> | <span data-ttu-id="edc82-136">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edc82-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="edc82-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edc82-137">Minimum supported server</span></span><br/> | <span data-ttu-id="edc82-138">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="edc82-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="edc82-139">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="edc82-139">Redistributable</span></span><br/>          | <span data-ttu-id="edc82-140">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="edc82-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="edc82-141">Idl</span><span class="sxs-lookup"><span data-stu-id="edc82-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edc82-142"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="edc82-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="edc82-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="edc82-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="edc82-144"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="edc82-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="edc82-145">DLL</span><span class="sxs-lookup"><span data-stu-id="edc82-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edc82-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edc82-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="edc82-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edc82-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc82-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="edc82-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="edc82-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="edc82-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="edc82-150">**打開**</span><span class="sxs-lookup"><span data-stu-id="edc82-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="edc82-151">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="edc82-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




