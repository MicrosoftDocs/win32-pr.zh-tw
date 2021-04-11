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
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="b9537-103">IWinHttpRequest：： SetTimeouts 方法</span><span class="sxs-lookup"><span data-stu-id="b9537-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="b9537-104">**SetTimeouts** 方法會指定傳送/接收作業的個別超時元件（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9537-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9537-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9537-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="b9537-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9537-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9537-107">*ResolveTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9537-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9537-108">在解析主機名稱時套用的超時值 (例如 `www.microsoft.com`) 至 IP 位址 (例如 192.168.131.199) （以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9537-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="b9537-109">預設值為零，表示沒有超時 (無限) 。</span><span class="sxs-lookup"><span data-stu-id="b9537-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="b9537-110">如果使用名稱解析 timeout 來指定 DNS timeout \_ \_ ，則每個要求會有一個執行緒的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="b9537-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="b9537-111">*ConnectTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9537-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9537-112">與目標伺服器建立通訊通訊端時所套用的超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9537-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="b9537-113">預設值為 60000 (60 秒) 。</span><span class="sxs-lookup"><span data-stu-id="b9537-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="b9537-114">*SendTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9537-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9537-115">將通訊通訊端上要求資料的個別封包傳送至目標伺服器時，套用的超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9537-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="b9537-116">傳送至 HTTP 伺服器的大型要求通常會分成多個封包;傳送超時適用于個別傳送每個封包。</span><span class="sxs-lookup"><span data-stu-id="b9537-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="b9537-117">預設值為 30000 (30 秒) 。</span><span class="sxs-lookup"><span data-stu-id="b9537-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="b9537-118">*ReceiveTimeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9537-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9537-119">從目標伺服器接收回應資料的封包時，套用的超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9537-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="b9537-120">大型回應會分成多個封包;接收時間輸出適用于從通訊端提取每個資料封包。</span><span class="sxs-lookup"><span data-stu-id="b9537-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="b9537-121">預設值為 30000 (30 秒) 。</span><span class="sxs-lookup"><span data-stu-id="b9537-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9537-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9537-122">Return value</span></span>

<span data-ttu-id="b9537-123">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="b9537-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9537-124">備註</span><span class="sxs-lookup"><span data-stu-id="b9537-124">Remarks</span></span>

<span data-ttu-id="b9537-125">全部都是必要參數。</span><span class="sxs-lookup"><span data-stu-id="b9537-125">All parameters are required.</span></span> <span data-ttu-id="b9537-126">值為0或-1 時，會設定一段時間來無限期等候。</span><span class="sxs-lookup"><span data-stu-id="b9537-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="b9537-127">大於0的值會設定超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9537-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="b9537-128">例如，30000會將時間設定為30秒。</span><span class="sxs-lookup"><span data-stu-id="b9537-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="b9537-129">-1 以外的所有負值都會導致此方法失敗。</span><span class="sxs-lookup"><span data-stu-id="b9537-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="b9537-130">超時值適用于 Winsock 層。</span><span class="sxs-lookup"><span data-stu-id="b9537-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="b9537-131">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="b9537-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b9537-132">範例</span><span class="sxs-lookup"><span data-stu-id="b9537-132">Examples</span></span>

<span data-ttu-id="b9537-133">下列範例顯示如何將所有的 WinHTTP 超時設定為30秒、開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="b9537-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="b9537-134">下列腳本範例示範如何將所有的 WinHTTP 超時設定為30秒、開啟 HTTP 連接，以及傳送 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="b9537-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b9537-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9537-135">Requirements</span></span>



| <span data-ttu-id="b9537-136">需求</span><span class="sxs-lookup"><span data-stu-id="b9537-136">Requirement</span></span> | <span data-ttu-id="b9537-137">值</span><span class="sxs-lookup"><span data-stu-id="b9537-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9537-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9537-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b9537-139">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9537-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b9537-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9537-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b9537-141">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="b9537-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b9537-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b9537-142">Redistributable</span></span><br/>          | <span data-ttu-id="b9537-143">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b9537-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b9537-144">Idl</span><span class="sxs-lookup"><span data-stu-id="b9537-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9537-145"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9537-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9537-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9537-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9537-147"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9537-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="b9537-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b9537-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9537-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9537-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b9537-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9537-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9537-151">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b9537-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="b9537-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b9537-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="b9537-153">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="b9537-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




