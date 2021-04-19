---
description: 設定要與 HTTP 伺服器搭配使用的認證，不論它是 proxy 伺服器或源伺服器。
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: IWinHttpRequest：： SetCredentials 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987630"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="7c6b0-103">IWinHttpRequest：： SetCredentials 方法</span><span class="sxs-lookup"><span data-stu-id="7c6b0-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="7c6b0-104">**SetCredentials** 方法會設定要與 HTTP 伺服器搭配使用的認證，不論它是 proxy 伺服器或源伺服器。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c6b0-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="7c6b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c6b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6b0-107">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c6b0-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6b0-108">指定驗證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="7c6b0-109">*密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c6b0-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6b0-110">指定驗證的密碼。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-110">Specifies the password for authentication.</span></span> <span data-ttu-id="7c6b0-111">如果 *bstrUserName* 為 **Null** 或遺失，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="7c6b0-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7c6b0-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6b0-113">指定 [**IWinHttpRequest**](iwinhttprequest-interface.md) 使用認證的時間。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="7c6b0-114">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-114">Can be one of the following values.</span></span>



| <span data-ttu-id="7c6b0-115">值</span><span class="sxs-lookup"><span data-stu-id="7c6b0-115">Value</span></span>                                                                                                               | <span data-ttu-id="7c6b0-116">意義</span><span class="sxs-lookup"><span data-stu-id="7c6b0-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7c6b0-117"><dt>\_ \_ 適用于伺服器的 HTTPREQUEST SETCREDENTIALS \_</dt></span><span class="sxs-lookup"><span data-stu-id="7c6b0-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="7c6b0-118">認證會傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="7c6b0-119"><dt>\_ \_ 適用于 PROXY 的 HTTPREQUEST SETCREDENTIALS \_</dt></span><span class="sxs-lookup"><span data-stu-id="7c6b0-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="7c6b0-120">認證會傳遞至 proxy。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6b0-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c6b0-121">Return value</span></span>

<span data-ttu-id="7c6b0-122">傳回值在成功時為 **\_ [正常]** ，否則為錯誤值。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c6b0-123">備註</span><span class="sxs-lookup"><span data-stu-id="7c6b0-123">Remarks</span></span>

<span data-ttu-id="7c6b0-124">如果 [**開啟**](iwinhttprequest-open.md) 的呼叫尚未順利完成，此方法會傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="7c6b0-125">假設有一些與 proxy 伺服器或源伺服器互動的量值必須在使用者可以設定會話的認證之前進行。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="7c6b0-126">此外，在使用者知道 (s) 支援的驗證配置之前，他們無法格式化認證。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="7c6b0-127">針對 Windows XP 和 Windows 2000，請參閱 WinHTTP 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="7c6b0-128">若要同時驗證服務器和 proxy，應用程式必須呼叫 **SetCredentials** 兩次;首先，將 *flags* 參數設定為 **HTTPREQUEST \_ SETCREDENTIALS \_ for \_ SERVER**，其次，將 *flags* 參數設定為 **HTTPREQUEST \_ SETCREDENTIALS \_ for \_ PROXY**。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="7c6b0-129">範例</span><span class="sxs-lookup"><span data-stu-id="7c6b0-129">Examples</span></span>

<span data-ttu-id="7c6b0-130">下列範例示範如何開啟 HTTP 連接、設定伺服器的認證、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="7c6b0-131">這個範例必須從命令提示字元執行。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-131">This example must be run from a command prompt.</span></span>


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
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="7c6b0-132">下列腳本範例示範如何開啟 HTTP 連接、設定伺服器的認證、設定 proxy 的認證（如果使用的話）、傳送 HTTP 要求，以及讀取回應文字。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="7c6b0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c6b0-133">Requirements</span></span>



| <span data-ttu-id="7c6b0-134">需求</span><span class="sxs-lookup"><span data-stu-id="7c6b0-134">Requirement</span></span> | <span data-ttu-id="7c6b0-135">值</span><span class="sxs-lookup"><span data-stu-id="7c6b0-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6b0-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c6b0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6b0-137">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c6b0-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7c6b0-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c6b0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6b0-139">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="7c6b0-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7c6b0-140">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7c6b0-140">Redistributable</span></span><br/>          | <span data-ttu-id="7c6b0-141">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7c6b0-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7c6b0-142">Idl</span><span class="sxs-lookup"><span data-stu-id="7c6b0-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c6b0-143"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c6b0-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c6b0-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c6b0-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c6b0-145"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c6b0-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="7c6b0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7c6b0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c6b0-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c6b0-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7c6b0-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c6b0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6b0-149">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7c6b0-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="7c6b0-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7c6b0-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="7c6b0-151">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="7c6b0-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




