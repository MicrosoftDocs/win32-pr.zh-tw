---
description: Status 屬性會從上一個回應中抓取 HTTP 狀態碼。
ms.assetid: 80b05e69-7f00-455d-94c3-a06eaa997cae
title: IWinHttpRequest：： Status 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Status
- IWinHttpRequest.get_Status
- WinHttpRequest.Status
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ea7569867336547bba4639e36cf65f7b5a08ae6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852880"
---
# <a name="iwinhttprequeststatus-property"></a><span data-ttu-id="4ccaa-103">IWinHttpRequest：： Status 屬性</span><span class="sxs-lookup"><span data-stu-id="4ccaa-103">IWinHttpRequest::Status property</span></span>

<span data-ttu-id="4ccaa-104">**Status** 屬性會從上一個回應中抓取 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-104">The **Status** property retrieves the HTTP status code from the last response.</span></span>

<span data-ttu-id="4ccaa-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccaa-106">語法</span><span class="sxs-lookup"><span data-stu-id="4ccaa-106">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] long *Status
);
```


```JScript

Status = WinHttpRequest.Status
```





## <a name="property-value"></a><span data-ttu-id="4ccaa-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4ccaa-107">Property value</span></span>

<span data-ttu-id="4ccaa-108">**Long** 類型的值，可接收傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-108">A value of type **long** that receives the returned status code.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ccaa-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4ccaa-109">Error codes</span></span>

<span data-ttu-id="4ccaa-110">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ccaa-111">備註</span><span class="sxs-lookup"><span data-stu-id="4ccaa-111">Remarks</span></span>

<span data-ttu-id="4ccaa-112">只有在 [**傳送**](iwinhttprequest-send.md) 方法成功完成之後，這個屬性的結果才有效。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-112">The results of this property are valid only after the [**Send**](iwinhttprequest-send.md) method has successfully completed.</span></span> <span data-ttu-id="4ccaa-113">如需狀態碼的清單，請參閱 [**HTTP 狀態碼**](http-status-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-113">For a list of status codes see [**HTTP Status Codes**](http-status-codes.md).</span></span>

> [!Note]  
> <span data-ttu-id="4ccaa-114">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4ccaa-115">範例</span><span class="sxs-lookup"><span data-stu-id="4ccaa-115">Examples</span></span>

<span data-ttu-id="4ccaa-116">下列範例顯示如何開啟 HTTP 連線、傳送 HTTP 要求、顯示 **狀態** 和 [**StatusText**](iwinhttprequest-statustext.md)，以及讀取回應標頭。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-116">The following example shows how to open an HTTP connection, send an HTTP request, display the **Status** and [**StatusText**](iwinhttprequest-statustext.md), and read the response headers.</span></span> <span data-ttu-id="4ccaa-117">這個範例必須從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-117">This example must be run from a command prompt.</span></span>


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
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="4ccaa-118">下列腳本範例示範如何開啟 HTTP 連接、傳送 HTTP 要求、顯示 **狀態** 和 [**StatusText**](iwinhttprequest-statustext.md)，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, display the **Status** and [**StatusText**](iwinhttprequest-statustext.md), and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="4ccaa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ccaa-119">Requirements</span></span>



| <span data-ttu-id="4ccaa-120">需求</span><span class="sxs-lookup"><span data-stu-id="4ccaa-120">Requirement</span></span> | <span data-ttu-id="4ccaa-121">值</span><span class="sxs-lookup"><span data-stu-id="4ccaa-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccaa-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ccaa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccaa-123">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ccaa-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4ccaa-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ccaa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccaa-125">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="4ccaa-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4ccaa-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4ccaa-126">Redistributable</span></span><br/>          | <span data-ttu-id="4ccaa-127">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4ccaa-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4ccaa-128">Idl</span><span class="sxs-lookup"><span data-stu-id="4ccaa-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ccaa-129"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4ccaa-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ccaa-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4ccaa-131"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4ccaa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4ccaa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccaa-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ccaa-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4ccaa-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ccaa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccaa-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4ccaa-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4ccaa-137">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="4ccaa-137">**StatusText**</span></span>](iwinhttprequest-statustext.md)
</dt> <dt>

[<span data-ttu-id="4ccaa-138">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="4ccaa-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




