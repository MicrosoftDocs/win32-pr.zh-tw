---
description: 新增、變更或刪除 HTTP 要求標頭。
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: IWinHttpRequest：： SetRequestHeader 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978192"
---
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="e3938-103">IWinHttpRequest：： SetRequestHeader 方法</span><span class="sxs-lookup"><span data-stu-id="e3938-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="e3938-104">**SetRequestHeader** 方法會新增、變更或刪除 HTTP 要求標頭。</span><span class="sxs-lookup"><span data-stu-id="e3938-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3938-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3938-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="e3938-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3938-107">*標頭* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3938-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3938-108">指定要設定之標頭的名稱，例如「深度」。</span><span class="sxs-lookup"><span data-stu-id="e3938-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="e3938-109">此參數不能包含冒號，而且必須是 HTTP 標頭的實際文字。</span><span class="sxs-lookup"><span data-stu-id="e3938-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="e3938-110">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3938-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3938-111">指定標頭的值，例如「無限大」。</span><span class="sxs-lookup"><span data-stu-id="e3938-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3938-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3938-112">Return value</span></span>

<span data-ttu-id="e3938-113">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="e3938-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3938-114">備註</span><span class="sxs-lookup"><span data-stu-id="e3938-114">Remarks</span></span>

<span data-ttu-id="e3938-115">標頭會在重新導向之間傳輸。</span><span class="sxs-lookup"><span data-stu-id="e3938-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="e3938-116">這可能會造成安全性弱點。</span><span class="sxs-lookup"><span data-stu-id="e3938-116">This can create a security vulnerability.</span></span> <span data-ttu-id="e3938-117">若要避免在發生重新導向時傳送標頭，請使用 [*WINHTTP \_ 狀態 \_ 回呼*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 回呼，在發生重新導向時更正特定標頭。</span><span class="sxs-lookup"><span data-stu-id="e3938-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="e3938-118">**SetRequestHeader** 方法可讓呼叫的應用程式在傳送要求之前，先新增或刪除 HTTP 要求標頭。</span><span class="sxs-lookup"><span data-stu-id="e3938-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="e3938-119">標頭名稱是在 *標頭* 中提供，而且標頭 token 或值會以 *值* 指定。</span><span class="sxs-lookup"><span data-stu-id="e3938-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="e3938-120">若要加入標頭，請提供標頭名稱和值。</span><span class="sxs-lookup"><span data-stu-id="e3938-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="e3938-121">如果另一個標頭已經有此名稱，則會被取代。</span><span class="sxs-lookup"><span data-stu-id="e3938-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="e3938-122">若要刪除標頭，請將 *標頭* 設定為要刪除的標頭名稱，並將 *值* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e3938-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="e3938-123">系統會驗證使用此方法加入的要求標頭名稱和值。</span><span class="sxs-lookup"><span data-stu-id="e3938-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="e3938-124">標頭的格式必須正確。</span><span class="sxs-lookup"><span data-stu-id="e3938-124">Headers must be well formed.</span></span> <span data-ttu-id="e3938-125">如需有效 HTTP 標頭的詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)。</span><span class="sxs-lookup"><span data-stu-id="e3938-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="e3938-126">如果使用不正確標頭，則會發生錯誤，而且不會新增標頭。</span><span class="sxs-lookup"><span data-stu-id="e3938-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="e3938-127">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="e3938-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e3938-128">範例</span><span class="sxs-lookup"><span data-stu-id="e3938-128">Examples</span></span>

<span data-ttu-id="e3938-129">下列範例示範如何開啟 HTTP 連接、設定要求標頭、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="e3938-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="e3938-130">這個範例必須從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="e3938-130">This example must be run from a command prompt.</span></span>


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
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



<span data-ttu-id="e3938-131">下列腳本範例示範如何開啟 HTTP 連接、設定要求標頭，以及傳送 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="e3938-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="e3938-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3938-132">Requirements</span></span>



| <span data-ttu-id="e3938-133">需求</span><span class="sxs-lookup"><span data-stu-id="e3938-133">Requirement</span></span> | <span data-ttu-id="e3938-134">值</span><span class="sxs-lookup"><span data-stu-id="e3938-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3938-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3938-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e3938-136">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3938-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e3938-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3938-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e3938-138">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="e3938-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="e3938-139">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e3938-139">Redistributable</span></span><br/>          | <span data-ttu-id="e3938-140">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e3938-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="e3938-141">Idl</span><span class="sxs-lookup"><span data-stu-id="e3938-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3938-142"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3938-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="e3938-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3938-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3938-144"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3938-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="e3938-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e3938-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3938-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3938-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e3938-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3938-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3938-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e3938-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="e3938-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e3938-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="e3938-150">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="e3938-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

