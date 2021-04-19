---
description: 抓取 HTTP 回應標頭。
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: IWinHttpRequest：： GetResponseHeader 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992502"
---
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="37c9a-103">IWinHttpRequest：： GetResponseHeader 方法</span><span class="sxs-lookup"><span data-stu-id="37c9a-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="37c9a-104">**GetResponseHeader** 方法會抓取 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="37c9a-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c9a-105">語法</span><span class="sxs-lookup"><span data-stu-id="37c9a-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="37c9a-106">參數</span><span class="sxs-lookup"><span data-stu-id="37c9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c9a-107">*標頭* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37c9a-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37c9a-108">指定不區分大小寫的標頭名稱。</span><span class="sxs-lookup"><span data-stu-id="37c9a-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="37c9a-109">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="37c9a-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="37c9a-110">接收產生的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="37c9a-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c9a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="37c9a-111">Return value</span></span>

<span data-ttu-id="37c9a-112">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="37c9a-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c9a-113">備註</span><span class="sxs-lookup"><span data-stu-id="37c9a-113">Remarks</span></span>

<span data-ttu-id="37c9a-114">這個方法會傳回 *標頭* 中所命名的回應標頭值。</span><span class="sxs-lookup"><span data-stu-id="37c9a-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="37c9a-115">請注意，automation 用戶端（例如 script）會將標頭資料取得為函式呼叫的傳回值，而不是透過函式參數。</span><span class="sxs-lookup"><span data-stu-id="37c9a-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="37c9a-116">只有在呼叫 [**Send**](iwinhttprequest-send.md) 方法之後，才叫用此方法。</span><span class="sxs-lookup"><span data-stu-id="37c9a-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="37c9a-117">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="37c9a-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="37c9a-118">範例</span><span class="sxs-lookup"><span data-stu-id="37c9a-118">Examples</span></span>

<span data-ttu-id="37c9a-119">下列範例示範如何開啟 HTTP 連線、傳送 HTTP 要求，以及取得回應中的日期標頭。</span><span class="sxs-lookup"><span data-stu-id="37c9a-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="37c9a-120">這個範例必須從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="37c9a-120">This example must be run from a command prompt.</span></span>


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

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                         &clsid);

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
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
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



<span data-ttu-id="37c9a-121">下列腳本範例示範如何開啟 HTTP 連線、傳送 HTTP 要求，以及取得回應中的日期標頭。</span><span class="sxs-lookup"><span data-stu-id="37c9a-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
```



## <a name="requirements"></a><span data-ttu-id="37c9a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="37c9a-122">Requirements</span></span>



| <span data-ttu-id="37c9a-123">需求</span><span class="sxs-lookup"><span data-stu-id="37c9a-123">Requirement</span></span> | <span data-ttu-id="37c9a-124">值</span><span class="sxs-lookup"><span data-stu-id="37c9a-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c9a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37c9a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37c9a-126">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37c9a-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="37c9a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37c9a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37c9a-128">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="37c9a-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="37c9a-129">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="37c9a-129">Redistributable</span></span><br/>          | <span data-ttu-id="37c9a-130">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="37c9a-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="37c9a-131">Idl</span><span class="sxs-lookup"><span data-stu-id="37c9a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37c9a-132"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="37c9a-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="37c9a-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="37c9a-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="37c9a-134"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="37c9a-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="37c9a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="37c9a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37c9a-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37c9a-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="37c9a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37c9a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c9a-138">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="37c9a-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="37c9a-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="37c9a-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="37c9a-140">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="37c9a-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="37c9a-141">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="37c9a-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




