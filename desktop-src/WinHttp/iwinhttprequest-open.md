---
description: 開啟 HTTP 資源的 HTTP 連接。
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: IWinHttpRequest：： Open 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979802"
---
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="d6c03-103">IWinHttpRequest：： Open 方法</span><span class="sxs-lookup"><span data-stu-id="d6c03-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="d6c03-104">**Open** 方法會開啟 HTTP 資源的 HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="d6c03-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c03-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6c03-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="d6c03-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c03-107">*方法* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6c03-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c03-108">指定用於 **Open** 方法的 [*HTTP 動詞*](glossary.md)，例如 "GET" 或 "PUT"。</span><span class="sxs-lookup"><span data-stu-id="d6c03-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="d6c03-109">一律使用大寫作為某些伺服器會忽略小寫 *HTTP 動詞* 命令。</span><span class="sxs-lookup"><span data-stu-id="d6c03-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="d6c03-110">*Url* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6c03-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c03-111">指定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6c03-111">Specifies the name of the resource.</span></span> <span data-ttu-id="d6c03-112">這必須是絕對 URL。</span><span class="sxs-lookup"><span data-stu-id="d6c03-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="d6c03-113">*非同步* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d6c03-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c03-114">指出是否要在非同步模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="d6c03-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="d6c03-115">值</span><span class="sxs-lookup"><span data-stu-id="d6c03-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d6c03-116">意義</span><span class="sxs-lookup"><span data-stu-id="d6c03-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="d6c03-117"><dt>**VARIANT \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c03-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d6c03-118">以同步模式開啟 HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="d6c03-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="d6c03-119">在 [WinHTTP](about-winhttp.md)完全收到回應之前，不會傳回 [**傳送**](iwinhttprequest-send.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="d6c03-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="d6c03-120"><dt>**VARIANT \_ TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="d6c03-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="d6c03-121">以非同步模式開啟 HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="d6c03-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c03-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6c03-122">Return value</span></span>

<span data-ttu-id="d6c03-123">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="d6c03-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c03-124">備註</span><span class="sxs-lookup"><span data-stu-id="d6c03-124">Remarks</span></span>

<span data-ttu-id="d6c03-125">這個方法會使用 *方法* 中指定的 [*HTTP 指令動詞*](glossary.md)，開啟 *Url* 中所識別資源的連接。</span><span class="sxs-lookup"><span data-stu-id="d6c03-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="d6c03-126">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="d6c03-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d6c03-127">範例</span><span class="sxs-lookup"><span data-stu-id="d6c03-127">Examples</span></span>

<span data-ttu-id="d6c03-128">下列範例顯示如何開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="d6c03-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
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



<span data-ttu-id="d6c03-129">下列腳本範例示範如何開啟 HTTP 連接、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="d6c03-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d6c03-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6c03-130">Requirements</span></span>



| <span data-ttu-id="d6c03-131">需求</span><span class="sxs-lookup"><span data-stu-id="d6c03-131">Requirement</span></span> | <span data-ttu-id="d6c03-132">值</span><span class="sxs-lookup"><span data-stu-id="d6c03-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c03-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6c03-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c03-134">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6c03-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d6c03-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6c03-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c03-136">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="d6c03-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d6c03-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d6c03-137">Redistributable</span></span><br/>          | <span data-ttu-id="d6c03-138">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d6c03-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d6c03-139">Idl</span><span class="sxs-lookup"><span data-stu-id="d6c03-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6c03-140"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6c03-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="d6c03-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6c03-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6c03-142"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6c03-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="d6c03-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d6c03-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6c03-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6c03-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d6c03-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6c03-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c03-146">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d6c03-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="d6c03-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d6c03-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="d6c03-148">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="d6c03-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




