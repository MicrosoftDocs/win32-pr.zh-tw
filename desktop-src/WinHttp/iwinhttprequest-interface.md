---
description: IWinHttpRequest 介面提供 Microsoft Windows HTTP Services (WinHTTP) 的所有 nonevent 方法。
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: IWinHttpRequest 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193072"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="86e8e-103">IWinHttpRequest 介面</span><span class="sxs-lookup"><span data-stu-id="86e8e-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="86e8e-104">**IWinHttpRequest** 介面提供 [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)的所有 nonevent 方法。</span><span class="sxs-lookup"><span data-stu-id="86e8e-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="86e8e-105">成員</span><span class="sxs-lookup"><span data-stu-id="86e8e-105">Members</span></span>

<span data-ttu-id="86e8e-106">**IWinHttpRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="86e8e-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86e8e-107">**IWinHttpRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86e8e-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="86e8e-108">方法</span><span class="sxs-lookup"><span data-stu-id="86e8e-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="86e8e-109">屬性</span><span class="sxs-lookup"><span data-stu-id="86e8e-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="86e8e-110">方法</span><span class="sxs-lookup"><span data-stu-id="86e8e-110">Methods</span></span>

<span data-ttu-id="86e8e-111">**IWinHttpRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="86e8e-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="86e8e-112">方法</span><span class="sxs-lookup"><span data-stu-id="86e8e-112">Method</span></span>                                                                 | <span data-ttu-id="86e8e-113">描述</span><span class="sxs-lookup"><span data-stu-id="86e8e-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86e8e-114">**中止**</span><span class="sxs-lookup"><span data-stu-id="86e8e-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="86e8e-115">中止 [WinHTTP](about-winhttp.md) [**傳送**](iwinhttprequest-send.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="86e8e-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="86e8e-116">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="86e8e-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="86e8e-117">抓取所有 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="86e8e-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="86e8e-118">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="86e8e-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="86e8e-119">抓取 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="86e8e-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="86e8e-120">**打開**</span><span class="sxs-lookup"><span data-stu-id="86e8e-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="86e8e-121">開啟 HTTP 資源的 HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="86e8e-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="86e8e-122">**傳送**</span><span class="sxs-lookup"><span data-stu-id="86e8e-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="86e8e-123">將 HTTP 要求傳送至 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="86e8e-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="86e8e-124">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="86e8e-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="86e8e-125">設定目前的 [自動登入原則](authentication-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="86e8e-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="86e8e-126">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="86e8e-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="86e8e-127">選取要傳送至安全超文字傳輸通訊協定 (HTTPS) 伺服器的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="86e8e-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="86e8e-128">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="86e8e-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="86e8e-129">設定要用於 HTTP 伺服器的認證，也就是 proxy 伺服器或源伺服器。</span><span class="sxs-lookup"><span data-stu-id="86e8e-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="86e8e-130">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="86e8e-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="86e8e-131">設定 proxy 伺服器資訊。</span><span class="sxs-lookup"><span data-stu-id="86e8e-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="86e8e-132">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="86e8e-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="86e8e-133">新增、變更或刪除 HTTP 要求標頭。</span><span class="sxs-lookup"><span data-stu-id="86e8e-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="86e8e-134">**SetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="86e8e-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="86e8e-135">指定傳送/接收作業的個別超時元件（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="86e8e-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="86e8e-136">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="86e8e-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="86e8e-137">使用選擇性的超時值（以秒為單位），等候非同步 [**傳送**](iwinhttprequest-send.md) 方法完成。</span><span class="sxs-lookup"><span data-stu-id="86e8e-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86e8e-138">屬性</span><span class="sxs-lookup"><span data-stu-id="86e8e-138">Properties</span></span>

<span data-ttu-id="86e8e-139">**IWinHttpRequest** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="86e8e-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="86e8e-140">屬性</span><span class="sxs-lookup"><span data-stu-id="86e8e-140">Property</span></span>                                                            | <span data-ttu-id="86e8e-141">存取類型</span><span class="sxs-lookup"><span data-stu-id="86e8e-141">Access type</span></span>           | <span data-ttu-id="86e8e-142">Description</span><span class="sxs-lookup"><span data-stu-id="86e8e-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="86e8e-143">**選項**</span><span class="sxs-lookup"><span data-stu-id="86e8e-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="86e8e-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86e8e-144">Read/write</span></span><br/> | <span data-ttu-id="86e8e-145">WinHTTP 選項值。</span><span class="sxs-lookup"><span data-stu-id="86e8e-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="86e8e-146">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="86e8e-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="86e8e-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="86e8e-147">Read-only</span></span><br/>  | <span data-ttu-id="86e8e-148">以不帶正負號的位元組陣列形式的回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="86e8e-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="86e8e-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="86e8e-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="86e8e-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="86e8e-150">Read-only</span></span><br/>  | <span data-ttu-id="86e8e-151">作為 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)的回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="86e8e-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="86e8e-152">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="86e8e-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="86e8e-153">唯讀</span><span class="sxs-lookup"><span data-stu-id="86e8e-153">Read-only</span></span><br/>  | <span data-ttu-id="86e8e-154">回應實體主體。</span><span class="sxs-lookup"><span data-stu-id="86e8e-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="86e8e-155">**狀態**</span><span class="sxs-lookup"><span data-stu-id="86e8e-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="86e8e-156">唯讀</span><span class="sxs-lookup"><span data-stu-id="86e8e-156">Read-only</span></span><br/>  | <span data-ttu-id="86e8e-157">上次回應中的 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="86e8e-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="86e8e-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="86e8e-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="86e8e-159">唯讀</span><span class="sxs-lookup"><span data-stu-id="86e8e-159">Read-only</span></span><br/>  | <span data-ttu-id="86e8e-160">HTTP 狀態文字。</span><span class="sxs-lookup"><span data-stu-id="86e8e-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="86e8e-161">備註</span><span class="sxs-lookup"><span data-stu-id="86e8e-161">Remarks</span></span>

<span data-ttu-id="86e8e-162">Httprequest 中定義的 **IWinHttpRequest** 介面是由具有 **CLSID \_ WinHttpRequest** 識別碼的類別所執行。</span><span class="sxs-lookup"><span data-stu-id="86e8e-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="86e8e-163">應用程式會使用 **CLSID \_ WinHttpRequest** 類別識別碼和 **IID \_ IWinHttpRequest** 的介面識別碼呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="86e8e-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="86e8e-164">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="86e8e-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86e8e-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="86e8e-165">Requirements</span></span>



| <span data-ttu-id="86e8e-166">需求</span><span class="sxs-lookup"><span data-stu-id="86e8e-166">Requirement</span></span> | <span data-ttu-id="86e8e-167">值</span><span class="sxs-lookup"><span data-stu-id="86e8e-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e8e-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86e8e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="86e8e-169">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86e8e-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="86e8e-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86e8e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="86e8e-171">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="86e8e-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="86e8e-172">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="86e8e-172">Redistributable</span></span><br/>          | <span data-ttu-id="86e8e-173">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="86e8e-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="86e8e-174">Idl</span><span class="sxs-lookup"><span data-stu-id="86e8e-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86e8e-175"><dt>HttpRequest .idl</dt></span><span class="sxs-lookup"><span data-stu-id="86e8e-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="86e8e-176">程式庫</span><span class="sxs-lookup"><span data-stu-id="86e8e-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="86e8e-177"><dt>WinHTTP .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86e8e-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="86e8e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="86e8e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e8e-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e8e-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="86e8e-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86e8e-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e8e-181">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="86e8e-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="86e8e-182">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="86e8e-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

