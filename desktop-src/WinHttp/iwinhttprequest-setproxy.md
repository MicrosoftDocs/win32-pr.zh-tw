---
description: 設定 proxy 伺服器資訊。
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: IWinHttpRequest：： SetProxy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000195"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="211fd-103">IWinHttpRequest：： SetProxy 方法</span><span class="sxs-lookup"><span data-stu-id="211fd-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="211fd-104">**SetProxy** 方法會設定 proxy 伺服器資訊。</span><span class="sxs-lookup"><span data-stu-id="211fd-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="211fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="211fd-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="211fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="211fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211fd-107">*ProxySetting* \[在\]</span><span class="sxs-lookup"><span data-stu-id="211fd-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="211fd-108">控制此方法的旗標。</span><span class="sxs-lookup"><span data-stu-id="211fd-108">The flags that control this method.</span></span> <span data-ttu-id="211fd-109">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="211fd-109">Can be one of the following values.</span></span>



| <span data-ttu-id="211fd-110">值</span><span class="sxs-lookup"><span data-stu-id="211fd-110">Value</span></span>                                                                                                           | <span data-ttu-id="211fd-111">意義</span><span class="sxs-lookup"><span data-stu-id="211fd-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="211fd-112"><dt>HTTPREQUEST \_ PROXYSETTING \_ 預設值</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="211fd-113">預設 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="211fd-113">Default proxy setting.</span></span> <span data-ttu-id="211fd-114">相當於 **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG**。</span><span class="sxs-lookup"><span data-stu-id="211fd-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="211fd-115"><dt>HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="211fd-116">指出應該從登錄取得 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="211fd-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="211fd-117">這會假設 [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) 已執行。</span><span class="sxs-lookup"><span data-stu-id="211fd-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="211fd-118">如果未執行 Proxycfg.exe 且指定了 **HTTPREQUEST \_ PROXYSETTING \_ PRECONFIG** ，則行為相當於 **HTTPREQUEST \_ PROXYSETTING \_ DIRECT**。</span><span class="sxs-lookup"><span data-stu-id="211fd-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="211fd-119"><dt>HTTPREQUEST \_ PROXYSETTING \_ DIRECT</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="211fd-120">表示應該直接存取所有 HTTP 和 HTTPS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="211fd-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="211fd-121">如果沒有任何 proxy 伺服器，則使用此命令。</span><span class="sxs-lookup"><span data-stu-id="211fd-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="211fd-122"><dt>HTTPREQUEST \_ PROXYSETTING \_ PROXY</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="211fd-123">指定 **HTTPREQUEST \_ PROXYSETTING \_ PROXY** 時， *varProxyServer* 應該設定為 proxy 伺服器字串，而 *varBypassList* 應設定為網域略過清單字串。</span><span class="sxs-lookup"><span data-stu-id="211fd-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="211fd-124">此 proxy 設定只適用于目前的 [**WinHttpRequest**](winhttprequest.md) 物件實例。</span><span class="sxs-lookup"><span data-stu-id="211fd-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="211fd-125">*ProxyServer* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="211fd-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="211fd-126">當 *ProxySetting* 等於 **HTTPREQUEST \_ ProxySetting \_ proxy** 時，設定為 proxy 伺服器字串。</span><span class="sxs-lookup"><span data-stu-id="211fd-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="211fd-127">*BypassList* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="211fd-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="211fd-128">當 *ProxySetting* 等於 **HTTPREQUEST \_ ProxySetting \_ PROXY** 時，設定為網域略過清單字串。</span><span class="sxs-lookup"><span data-stu-id="211fd-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211fd-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="211fd-129">Return value</span></span>

<span data-ttu-id="211fd-130">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="211fd-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="211fd-131">備註</span><span class="sxs-lookup"><span data-stu-id="211fd-131">Remarks</span></span>

<span data-ttu-id="211fd-132">可讓呼叫的應用程式指定使用 proxy 設定工具 (設定的預設 proxy 資訊，) 或覆寫 [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="211fd-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="211fd-133">呼叫 [**Send**](iwinhttprequest-send.md) 方法之前，必須先呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="211fd-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="211fd-134">如果在 [**傳送**](iwinhttprequest-send.md) 方法之後呼叫此方法，則不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="211fd-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="211fd-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) 會將這些參數傳遞給 MICROSOFT Windows HTTP Services (WinHTTP) 。</span><span class="sxs-lookup"><span data-stu-id="211fd-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="211fd-136">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="211fd-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="211fd-137">範例</span><span class="sxs-lookup"><span data-stu-id="211fd-137">Examples</span></span>

<span data-ttu-id="211fd-138">下列範例顯示如何設定特定 proxy 伺服器的 proxy 設定、開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="211fd-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="211fd-139">這個範例必須從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="211fd-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="211fd-140">只有當您的 proxy 伺服器名為「proxy \_ 伺服器」（使用埠80），且當主機名稱的結尾是 ". microsoft.com" 時，您的電腦可以略過 proxy 伺服器，這些 proxy 設定才適用。</span><span class="sxs-lookup"><span data-stu-id="211fd-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


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
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
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
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="211fd-141">下列腳本範例顯示如何設定特定 proxy 伺服器的 proxy 設定、開啟 HTTP 連線、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="211fd-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="211fd-142">只有當您的 proxy 伺服器名為「proxy \_ 伺服器」（使用埠80），且當主機名稱的結尾是 ". microsoft.com" 時，您的電腦可以略過 proxy 伺服器，這些 proxy 設定才適用。</span><span class="sxs-lookup"><span data-stu-id="211fd-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="211fd-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="211fd-143">Requirements</span></span>



| <span data-ttu-id="211fd-144">需求</span><span class="sxs-lookup"><span data-stu-id="211fd-144">Requirement</span></span> | <span data-ttu-id="211fd-145">值</span><span class="sxs-lookup"><span data-stu-id="211fd-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="211fd-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="211fd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="211fd-147">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="211fd-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="211fd-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="211fd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="211fd-149">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="211fd-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="211fd-150">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="211fd-150">Redistributable</span></span><br/>          | <span data-ttu-id="211fd-151">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="211fd-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="211fd-152">Idl</span><span class="sxs-lookup"><span data-stu-id="211fd-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="211fd-153"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="211fd-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="211fd-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="211fd-155"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="211fd-156">DLL</span><span class="sxs-lookup"><span data-stu-id="211fd-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211fd-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="211fd-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="211fd-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="211fd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211fd-159">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="211fd-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="211fd-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="211fd-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="211fd-161">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="211fd-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




