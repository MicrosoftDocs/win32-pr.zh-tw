---
Description: 本主題提供有關搭配使用 WinHTTP WinHttpRequest COM 物件與指令碼語言的資訊。
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: WinHttpRequest 物件
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995305"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="304fd-103">WinHttpRequest 物件</span><span class="sxs-lookup"><span data-stu-id="304fd-103">WinHttpRequest object</span></span>

<span data-ttu-id="304fd-104">本主題提供有關搭配使用 WinHTTP **WinHttpRequest** COM 物件與指令碼語言的資訊。</span><span class="sxs-lookup"><span data-stu-id="304fd-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="304fd-105">如需詳細資訊，包括 c + + API (WinHTTP) 請參閱 [關於 winHTTP](about-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="304fd-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="304fd-106">如需這些介面的比較，請參閱 [選擇 WinHTTP 介面](choosing-a-winhttp-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="304fd-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="304fd-107">範例</span><span class="sxs-lookup"><span data-stu-id="304fd-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="304fd-108">取自 [IWinHttpRequest：： Status 屬性](iwinhttprequest-status.md)的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="304fd-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="304fd-109">成員</span><span class="sxs-lookup"><span data-stu-id="304fd-109">Members</span></span>

<span data-ttu-id="304fd-110">**WinHttpRequest** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="304fd-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="304fd-111">事件</span><span class="sxs-lookup"><span data-stu-id="304fd-111">Events</span></span>](#events)
-   [<span data-ttu-id="304fd-112">方法</span><span class="sxs-lookup"><span data-stu-id="304fd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="304fd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="304fd-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="304fd-114">事件</span><span class="sxs-lookup"><span data-stu-id="304fd-114">Events</span></span>

<span data-ttu-id="304fd-115">**WinHttpRequest** 物件具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="304fd-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="304fd-116">事件</span><span class="sxs-lookup"><span data-stu-id="304fd-116">Event</span></span>                                                                            | <span data-ttu-id="304fd-117">描述</span><span class="sxs-lookup"><span data-stu-id="304fd-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="304fd-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="304fd-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="304fd-119">當應用程式中發生執行階段錯誤時發生。</span><span class="sxs-lookup"><span data-stu-id="304fd-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="304fd-120">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="304fd-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="304fd-121">當資料可從回應中取得時，就會發生。</span><span class="sxs-lookup"><span data-stu-id="304fd-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="304fd-122">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="304fd-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="304fd-123">當回應資料完成時發生。</span><span class="sxs-lookup"><span data-stu-id="304fd-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="304fd-124">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="304fd-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="304fd-125">在開始接收回應資料時發生。</span><span class="sxs-lookup"><span data-stu-id="304fd-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="304fd-126">方法</span><span class="sxs-lookup"><span data-stu-id="304fd-126">Methods</span></span>

<span data-ttu-id="304fd-127">**WinHttpRequest** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="304fd-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="304fd-128">方法</span><span class="sxs-lookup"><span data-stu-id="304fd-128">Method</span></span>                                                                 | <span data-ttu-id="304fd-129">描述</span><span class="sxs-lookup"><span data-stu-id="304fd-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="304fd-130">**中止**</span><span class="sxs-lookup"><span data-stu-id="304fd-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="304fd-131">中止 [WinHTTP](about-winhttp.md) [**傳送**](iwinhttprequest-send.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="304fd-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="304fd-132">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="304fd-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="304fd-133">抓取所有 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="304fd-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="304fd-134">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="304fd-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="304fd-135">抓取 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="304fd-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="304fd-136">**打開**</span><span class="sxs-lookup"><span data-stu-id="304fd-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="304fd-137">開啟 HTTP 資源的 HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="304fd-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="304fd-138">**傳送**</span><span class="sxs-lookup"><span data-stu-id="304fd-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="304fd-139">將 HTTP 要求傳送至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="304fd-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="304fd-140">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="304fd-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="304fd-141">設定目前的 [自動登入原則](authentication-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="304fd-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="304fd-142">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="304fd-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="304fd-143">選取要傳送至安全超文字傳輸通訊協定 (HTTPS) 伺服器的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="304fd-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="304fd-144">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="304fd-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="304fd-145">設定要與 HTTP 伺服器（來源或 proxy 伺服器）搭配使用的認證。</span><span class="sxs-lookup"><span data-stu-id="304fd-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="304fd-146">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="304fd-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="304fd-147">設定 proxy 伺服器資訊。</span><span class="sxs-lookup"><span data-stu-id="304fd-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="304fd-148">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="304fd-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="304fd-149">新增、變更或刪除 HTTP 要求標頭。</span><span class="sxs-lookup"><span data-stu-id="304fd-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="304fd-150">**SetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="304fd-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="304fd-151">指定傳送/接收作業的個別超時元件（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="304fd-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="304fd-152">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="304fd-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="304fd-153">以秒為單位，指定非同步 [**傳送**](iwinhttprequest-send.md) 方法完成的等候時間（以秒為單位），並提供選擇性的超時值。</span><span class="sxs-lookup"><span data-stu-id="304fd-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="304fd-154">屬性</span><span class="sxs-lookup"><span data-stu-id="304fd-154">Properties</span></span>

<span data-ttu-id="304fd-155">**WinHttpRequest** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="304fd-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="304fd-156">屬性</span><span class="sxs-lookup"><span data-stu-id="304fd-156">Property</span></span>                                                            | <span data-ttu-id="304fd-157">存取類型</span><span class="sxs-lookup"><span data-stu-id="304fd-157">Access type</span></span>           | <span data-ttu-id="304fd-158">Description</span><span class="sxs-lookup"><span data-stu-id="304fd-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="304fd-159">**選項**</span><span class="sxs-lookup"><span data-stu-id="304fd-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="304fd-160">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="304fd-160">Read/write</span></span><br/> | <span data-ttu-id="304fd-161">設定或抓取 WinHTTP 選項值。</span><span class="sxs-lookup"><span data-stu-id="304fd-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="304fd-162">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="304fd-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="304fd-163">唯讀</span><span class="sxs-lookup"><span data-stu-id="304fd-163">Read-only</span></span><br/>  | <span data-ttu-id="304fd-164">以不帶正負號的位元組陣列形式捕獲回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="304fd-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="304fd-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="304fd-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="304fd-166">唯讀</span><span class="sxs-lookup"><span data-stu-id="304fd-166">Read-only</span></span><br/>  | <span data-ttu-id="304fd-167">以 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)形式抓取回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="304fd-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="304fd-168">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="304fd-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="304fd-169">唯讀</span><span class="sxs-lookup"><span data-stu-id="304fd-169">Read-only</span></span><br/>  | <span data-ttu-id="304fd-170">以文字形式抓取回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="304fd-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="304fd-171">**狀態**</span><span class="sxs-lookup"><span data-stu-id="304fd-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="304fd-172">唯讀</span><span class="sxs-lookup"><span data-stu-id="304fd-172">Read-only</span></span><br/>  | <span data-ttu-id="304fd-173">從上一個回應中抓取 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="304fd-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="304fd-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="304fd-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="304fd-175">唯讀</span><span class="sxs-lookup"><span data-stu-id="304fd-175">Read-only</span></span><br/>  | <span data-ttu-id="304fd-176">抓取 HTTP 狀態文字。</span><span class="sxs-lookup"><span data-stu-id="304fd-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="304fd-177">備註</span><span class="sxs-lookup"><span data-stu-id="304fd-177">Remarks</span></span>

<span data-ttu-id="304fd-178">**WinHttpRequest** 物件會使用 [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo)介面來提供錯誤資料。</span><span class="sxs-lookup"><span data-stu-id="304fd-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="304fd-179">您可以使用 Microsoft Visual Basic Scripting Edition (VBScript) 中的 [Err](/previous-versions//sbf5ze0e(v=vs.85)) 物件和 microsoft JScript 中的 [error](https://msdn.microsoft.com/library/dww52sbt.aspx) 物件，取得描述和數值錯誤值。</span><span class="sxs-lookup"><span data-stu-id="304fd-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="304fd-180">錯誤號碼的較低16位會對應到在 [**錯誤訊息**](error-messages.md)中找到的值。</span><span class="sxs-lookup"><span data-stu-id="304fd-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="304fd-181">針對 Windows XP 和 Windows 2000，請參閱 [執行時間需求](winhttp-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="304fd-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="304fd-182">規格需求</span><span class="sxs-lookup"><span data-stu-id="304fd-182">Requirements</span></span>



| <span data-ttu-id="304fd-183">需求</span><span class="sxs-lookup"><span data-stu-id="304fd-183">Requirement</span></span> | <span data-ttu-id="304fd-184">值</span><span class="sxs-lookup"><span data-stu-id="304fd-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="304fd-185">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="304fd-185">Minimum supported client</span></span><br/> | <span data-ttu-id="304fd-186">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="304fd-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="304fd-187">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="304fd-187">Minimum supported server</span></span><br/> | <span data-ttu-id="304fd-188">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="304fd-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="304fd-189">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="304fd-189">Redistributable</span></span><br/>          | <span data-ttu-id="304fd-190">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="304fd-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="304fd-191">Idl</span><span class="sxs-lookup"><span data-stu-id="304fd-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="304fd-192"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="304fd-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="304fd-193">程式庫</span><span class="sxs-lookup"><span data-stu-id="304fd-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="304fd-194"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="304fd-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="304fd-195">DLL</span><span class="sxs-lookup"><span data-stu-id="304fd-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="304fd-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="304fd-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="304fd-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="304fd-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304fd-198">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="304fd-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

