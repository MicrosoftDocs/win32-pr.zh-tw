---
description: 抓取所有 HTTP 回應標頭。
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: IWinHttpRequest：： GetAllResponseHeaders 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991912"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="ed93a-103">IWinHttpRequest：： GetAllResponseHeaders 方法</span><span class="sxs-lookup"><span data-stu-id="ed93a-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="ed93a-104">**GetAllResponseHeaders** 方法會抓取所有 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="ed93a-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed93a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed93a-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="ed93a-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed93a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed93a-107">*標頭* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ed93a-108">接收產生的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="ed93a-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed93a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed93a-109">Return value</span></span>

<span data-ttu-id="ed93a-110">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="ed93a-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed93a-111">備註</span><span class="sxs-lookup"><span data-stu-id="ed93a-111">Remarks</span></span>

<span data-ttu-id="ed93a-112">這個方法會傳回最近的伺服器回應中包含的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="ed93a-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="ed93a-113">個別的標頭會以換行字元和換行字元組合 (ASCII 13 和 10) 分隔。</span><span class="sxs-lookup"><span data-stu-id="ed93a-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="ed93a-114">最後一個專案後面會加上兩個分隔符號 (13、10、13、10) 。</span><span class="sxs-lookup"><span data-stu-id="ed93a-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="ed93a-115">只有在呼叫 [**Send**](iwinhttprequest-send.md) 方法之後，才叫用此方法。</span><span class="sxs-lookup"><span data-stu-id="ed93a-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="ed93a-116">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="ed93a-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ed93a-117">範例</span><span class="sxs-lookup"><span data-stu-id="ed93a-117">Examples</span></span>

<span data-ttu-id="ed93a-118">下列範例示範如何開啟 HTTP 連線、傳送 HTTP 要求，以及取得回應中的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="ed93a-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="ed93a-119">此範例應從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="ed93a-119">This example should be run from a command prompt.</span></span>


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

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



<span data-ttu-id="ed93a-120">下列腳本範例示範如何開啟 HTTP 連線、傳送 HTTP 要求，以及取得回應中的所有標頭。</span><span class="sxs-lookup"><span data-stu-id="ed93a-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="ed93a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed93a-121">Requirements</span></span>



| <span data-ttu-id="ed93a-122">需求</span><span class="sxs-lookup"><span data-stu-id="ed93a-122">Requirement</span></span> | <span data-ttu-id="ed93a-123">值</span><span class="sxs-lookup"><span data-stu-id="ed93a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed93a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed93a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ed93a-125">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="ed93a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed93a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ed93a-127">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="ed93a-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="ed93a-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ed93a-128">Redistributable</span></span><br/>          | <span data-ttu-id="ed93a-129">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ed93a-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="ed93a-130">Idl</span><span class="sxs-lookup"><span data-stu-id="ed93a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed93a-131"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed93a-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="ed93a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed93a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed93a-133"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed93a-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ed93a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ed93a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed93a-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed93a-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ed93a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed93a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed93a-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ed93a-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="ed93a-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="ed93a-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="ed93a-139">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="ed93a-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="ed93a-140">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="ed93a-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




