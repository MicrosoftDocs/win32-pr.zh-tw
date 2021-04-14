---
title: 'HTTP 狀態碼 (Wininet. h) '
description: 下表包含網際網路上伺服器所傳回的 HTTP 狀態碼的常數和對應的值。
ms.assetid: 28a5e889-c8f3-4996-a1ca-c48866fa59d7
topic_type:
- apiref
api_name:
- HTTP_STATUS_CONTINUE
- HTTP_STATUS_SWITCH_PROTOCOLS
- HTTP_STATUS_OK
- HTTP_STATUS_CREATED
- HTTP_STATUS_ACCEPTED
- HTTP_STATUS_PARTIAL
- HTTP_STATUS_NO_CONTENT
- HTTP_STATUS_RESET_CONTENT
- HTTP_STATUS_PARTIAL_CONTENT
- HTTP_STATUS_AMBIGUOUS
- HTTP_STATUS_MOVED
- HTTP_STATUS_REDIRECT
- HTTP_STATUS_REDIRECT_METHOD
- HTTP_STATUS_NOT_MODIFIED
- HTTP_STATUS_USE_PROXY
- HTTP_STATUS_REDIRECT_KEEP_VERB
- HTTP_STATUS_BAD_REQUEST
- HTTP_STATUS_DENIED
- HTTP_STATUS_PAYMENT_REQ
- HTTP_STATUS_FORBIDDEN
- HTTP_STATUS_NOT_FOUND
- HTTP_STATUS_BAD_METHOD
- HTTP_STATUS_NONE_ACCEPTABLE
- HTTP_STATUS_PROXY_AUTH_REQ
- HTTP_STATUS_REQUEST_TIMEOUT
- HTTP_STATUS_CONFLICT
- HTTP_STATUS_GONE
- HTTP_STATUS_LENGTH_REQUIRED
- HTTP_STATUS_PRECOND_FAILED
- HTTP_STATUS_REQUEST_TOO_LARGE
- HTTP_STATUS_URI_TOO_LONG
- HTTP_STATUS_UNSUPPORTED_MEDIA
- HTTP_STATUS_RETRY_WITH
- HTTP_STATUS_SERVER_ERROR
- HTTP_STATUS_NOT_SUPPORTED
- HTTP_STATUS_BAD_GATEWAY
- HTTP_STATUS_SERVICE_UNAVAIL
- HTTP_STATUS_GATEWAY_TIMEOUT
- HTTP_STATUS_VERSION_NOT_SUP
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6933617b0488e059c029dd783af238a3ddbb3ecb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385225"
---
# <a name="http-status-codes-winineth"></a><span data-ttu-id="c4a14-103">HTTP 狀態碼 (Wininet. h) </span><span class="sxs-lookup"><span data-stu-id="c4a14-103">HTTP Status Codes (Wininet.h)</span></span>

<span data-ttu-id="c4a14-104">下表包含網際網路上伺服器所傳回的 HTTP 狀態碼的常數和對應的值。</span><span class="sxs-lookup"><span data-stu-id="c4a14-104">The following table contains the constants and corresponding values for the HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="c4a14-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP \_ 狀態 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="c4a14-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-106">100</span><span class="sxs-lookup"><span data-stu-id="c4a14-106">100</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-107">要求可以繼續。</span><span class="sxs-lookup"><span data-stu-id="c4a14-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP \_ 狀態 \_ 切換 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="c4a14-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-109">101</span><span class="sxs-lookup"><span data-stu-id="c4a14-109">101</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-110">伺服器已切換升級標頭中的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c4a14-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP \_ 狀態 \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="c4a14-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-112">200</span><span class="sxs-lookup"><span data-stu-id="c4a14-112">200</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-113">要求已順利完成。</span><span class="sxs-lookup"><span data-stu-id="c4a14-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**已 \_ 建立 HTTP 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="c4a14-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-115">201</span><span class="sxs-lookup"><span data-stu-id="c4a14-115">201</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-116">要求已完成，並導致建立新的資源。</span><span class="sxs-lookup"><span data-stu-id="c4a14-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP \_ 狀態已 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="c4a14-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-118">202</span><span class="sxs-lookup"><span data-stu-id="c4a14-118">202</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-119">已接受要求進行處理，但處理尚未完成。</span><span class="sxs-lookup"><span data-stu-id="c4a14-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP \_ 狀態 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="c4a14-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-121">203</span><span class="sxs-lookup"><span data-stu-id="c4a14-121">203</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-122">在實體標頭中傳回的中繼資料不是源伺服器中可用的明確集合。</span><span class="sxs-lookup"><span data-stu-id="c4a14-122">The returned meta information in the entity-header is not the definitive set available from the origin server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP \_ 狀態 \_ 沒有 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="c4a14-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-124">204</span><span class="sxs-lookup"><span data-stu-id="c4a14-124">204</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-125">伺服器已完成要求，但沒有要傳回的新資訊。</span><span class="sxs-lookup"><span data-stu-id="c4a14-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP \_ 狀態 \_ 重設 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="c4a14-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-127">205</span><span class="sxs-lookup"><span data-stu-id="c4a14-127">205</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-128">要求已完成，而且用戶端程式應該重設造成要求傳送的檔視圖，讓使用者可以輕鬆地起始另一個輸入動作。</span><span class="sxs-lookup"><span data-stu-id="c4a14-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP \_ 狀態 \_ 部分 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="c4a14-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-130">206</span><span class="sxs-lookup"><span data-stu-id="c4a14-130">206</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-131">伺服器已滿足部分資源的 GET 要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP \_ 狀態不 \_ 明確**</span><span class="sxs-lookup"><span data-stu-id="c4a14-132"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-133">300</span><span class="sxs-lookup"><span data-stu-id="c4a14-133">300</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-134">伺服器無法決定要傳回的內容。</span><span class="sxs-lookup"><span data-stu-id="c4a14-134">The server couldn't decide what to return.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**已 \_ 移動 HTTP 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="c4a14-135"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-136">301</span><span class="sxs-lookup"><span data-stu-id="c4a14-136">301</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-137">要求的資源已指派給新的永久 URI， (統一資源識別項) ，而此資源的任何未來參考都應該使用其中一個傳回的 Uri 來完成。</span><span class="sxs-lookup"><span data-stu-id="c4a14-137">The requested resource has been assigned to a new permanent URI (Uniform Resource Identifier), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP \_ 狀態重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="c4a14-138"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-139">302</span><span class="sxs-lookup"><span data-stu-id="c4a14-139">302</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-140">要求的資源會暫時位於不同的 URI 下， (統一資源識別項) 。</span><span class="sxs-lookup"><span data-stu-id="c4a14-140">The requested resource resides temporarily under a different URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP \_ 狀態重新 \_ 導向 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="c4a14-141"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-142">303</span><span class="sxs-lookup"><span data-stu-id="c4a14-142">303</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-143">您可以在不同的 URI (統一資源識別項) 找到要求的回應，而且應該使用該資源上的 GET HTTP 指令動詞來加以取出。</span><span class="sxs-lookup"><span data-stu-id="c4a14-143">The response to the request can be found under a different URI (Uniform Resource Identifier) and should be retrieved using a GET HTTP verb on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_ \_ 未修改 HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="c4a14-144"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-145">304</span><span class="sxs-lookup"><span data-stu-id="c4a14-145">304</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-146">未修改要求的資源。</span><span class="sxs-lookup"><span data-stu-id="c4a14-146">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ 狀態 \_ 使用 \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="c4a14-147"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-148">305</span><span class="sxs-lookup"><span data-stu-id="c4a14-148">305</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-149">要求的資源必須透過 [位置] 欄位提供的 proxy 存取。</span><span class="sxs-lookup"><span data-stu-id="c4a14-149">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP \_ 狀態重新 \_ 導向 \_ 保留 \_ 動詞**</span><span class="sxs-lookup"><span data-stu-id="c4a14-150"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-151">307</span><span class="sxs-lookup"><span data-stu-id="c4a14-151">307</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-152">重新導向的要求會保留相同的 HTTP 動詞命令。</span><span class="sxs-lookup"><span data-stu-id="c4a14-152">The redirected request keeps the same HTTP verb.</span></span> <span data-ttu-id="c4a14-153">HTTP/1.1 行為。</span><span class="sxs-lookup"><span data-stu-id="c4a14-153">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP \_ 狀態不 \_ 正確的 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="c4a14-154"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-155">400</span><span class="sxs-lookup"><span data-stu-id="c4a14-155">400</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-156">因為語法無效，所以伺服器無法處理此要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-156">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP \_ 狀態已 \_ 拒絕**</span><span class="sxs-lookup"><span data-stu-id="c4a14-157"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-158">401</span><span class="sxs-lookup"><span data-stu-id="c4a14-158">401</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-159">要求的資源需要進行使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="c4a14-159">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP \_ 狀態 \_ 付款 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="c4a14-160"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-161">402</span><span class="sxs-lookup"><span data-stu-id="c4a14-161">402</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-162">目前未在 HTTP 通訊協定中執行。</span><span class="sxs-lookup"><span data-stu-id="c4a14-162">Not currently implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP \_ 狀態 \_ 禁止**</span><span class="sxs-lookup"><span data-stu-id="c4a14-163"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-164">403</span><span class="sxs-lookup"><span data-stu-id="c4a14-164">403</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-165">伺服器瞭解要求，但拒絕完成此要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-165">The server understood the request, but is refusing to fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_ \_ 找不到 HTTP 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="c4a14-166"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-167">404</span><span class="sxs-lookup"><span data-stu-id="c4a14-167">404</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-168">伺服器找不到任何符合要求的 URI (統一資源識別項) 。</span><span class="sxs-lookup"><span data-stu-id="c4a14-168">The server has not found anything matching the requested URI (Uniform Resource Identifier).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ 狀態 \_ 不良 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="c4a14-169"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-170">405</span><span class="sxs-lookup"><span data-stu-id="c4a14-170">405</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-171">不允許使用的 HTTP 動詞命令。</span><span class="sxs-lookup"><span data-stu-id="c4a14-171">The HTTP verb used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP \_ 狀態 \_ 無 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="c4a14-172"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-173">406</span><span class="sxs-lookup"><span data-stu-id="c4a14-173">406</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-174">找不到用戶端可接受的回應。</span><span class="sxs-lookup"><span data-stu-id="c4a14-174">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP \_ 狀態 \_ PROXY \_ 驗證 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="c4a14-175"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-176">407</span><span class="sxs-lookup"><span data-stu-id="c4a14-176">407</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-177">需要 Proxy 驗證。</span><span class="sxs-lookup"><span data-stu-id="c4a14-177">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP \_ 狀態 \_ 要求 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="c4a14-178"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-179">408</span><span class="sxs-lookup"><span data-stu-id="c4a14-179">408</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-180">伺服器要求等待逾時。</span><span class="sxs-lookup"><span data-stu-id="c4a14-180">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP \_ 狀態 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="c4a14-181"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-182">409</span><span class="sxs-lookup"><span data-stu-id="c4a14-182">409</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-183">因為與資源目前的狀態衝突，所以無法完成要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-183">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="c4a14-184">使用者應以詳細資訊重新提交。</span><span class="sxs-lookup"><span data-stu-id="c4a14-184">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP \_ 狀態已 \_ 消失**</span><span class="sxs-lookup"><span data-stu-id="c4a14-185"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-186">410</span><span class="sxs-lookup"><span data-stu-id="c4a14-186">410</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-187">伺服器無法再使用要求的資源，且沒有已知的轉送位址。</span><span class="sxs-lookup"><span data-stu-id="c4a14-187">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_需要 HTTP 狀態 \_ 長度 \_**</span><span class="sxs-lookup"><span data-stu-id="c4a14-188"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-189">411</span><span class="sxs-lookup"><span data-stu-id="c4a14-189">411</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-190">伺服器拒絕接受未定義內容長度的要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-190">The server refuses to accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP \_ 狀態 \_ PRECOND \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="c4a14-191"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-192">412</span><span class="sxs-lookup"><span data-stu-id="c4a14-192">412</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-193">在一或多個要求標頭欄位中指定的前置條件，會在伺服器上進行測試時評估為 false。</span><span class="sxs-lookup"><span data-stu-id="c4a14-193">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP \_ 狀態 \_ 要求 \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="c4a14-194"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-195">413</span><span class="sxs-lookup"><span data-stu-id="c4a14-195">413</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-196">伺服器拒絕處理要求，因為要求實體大於伺服器願意或能夠處理的要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-196">The server is refusing to process a request because the request entity is larger than the server is willing or able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP \_ 狀態 \_ URI \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="c4a14-197"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-198">414</span><span class="sxs-lookup"><span data-stu-id="c4a14-198">414</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-199">伺服器拒絕服務此要求，因為 (統一資源識別項) 的要求 URI 長度超過伺服器願意解讀的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c4a14-199">The server is refusing to service the request because the request URI (Uniform Resource Identifier) is longer than the server is willing to interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP \_ 狀態 \_ 不支援的 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="c4a14-200"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-201">415</span><span class="sxs-lookup"><span data-stu-id="c4a14-201">415</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-202">伺服器拒絕服務要求，因為要求的資源要求的資源格式不受要求的方法所要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-202">The server is refusing to service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP \_ 狀態 \_ 重試 \_**</span><span class="sxs-lookup"><span data-stu-id="c4a14-203"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-204">449</span><span class="sxs-lookup"><span data-stu-id="c4a14-204">449</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-205">執行適當的動作之後，應重試要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-205">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP \_ 狀態 \_ 伺服器 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="c4a14-206"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-207">500</span><span class="sxs-lookup"><span data-stu-id="c4a14-207">500</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-208">伺服器發生未預期的狀況，導致無法履行要求。</span><span class="sxs-lookup"><span data-stu-id="c4a14-208">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_ \_ 不支援 HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="c4a14-209"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-210">501</span><span class="sxs-lookup"><span data-stu-id="c4a14-210">501</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-211">伺服器不支援完成要求所需的功能。</span><span class="sxs-lookup"><span data-stu-id="c4a14-211">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP \_ 狀態 \_ 錯誤的 \_ 閘道**</span><span class="sxs-lookup"><span data-stu-id="c4a14-212"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-213">502</span><span class="sxs-lookup"><span data-stu-id="c4a14-213">502</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-214">作為閘道或 proxy 的伺服器在嘗試完成要求時所存取的上游伺服器收到不正確回應。</span><span class="sxs-lookup"><span data-stu-id="c4a14-214">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP \_ 狀態 \_ 服務 \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="c4a14-215"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-216">503</span><span class="sxs-lookup"><span data-stu-id="c4a14-216">503</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-217">服務暫時超載。</span><span class="sxs-lookup"><span data-stu-id="c4a14-217">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP \_ 狀態 \_ 閘道 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="c4a14-218"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-219">504</span><span class="sxs-lookup"><span data-stu-id="c4a14-219">504</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-220">要求閘道等待逾時。</span><span class="sxs-lookup"><span data-stu-id="c4a14-220">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4a14-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP \_ 狀態 \_ 版本 \_ 不是 \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="c4a14-221"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4a14-222">505</span><span class="sxs-lookup"><span data-stu-id="c4a14-222">505</span></span>
</dt> <dt>



<span data-ttu-id="c4a14-223">伺服器不支援或拒絕支援要求訊息中所使用的 HTTP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="c4a14-223">The server does not support, or refuses to support, the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4a14-224">備註</span><span class="sxs-lookup"><span data-stu-id="c4a14-224">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c4a14-225">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="c4a14-225">WinINet does not support server implementations.</span></span> <span data-ttu-id="c4a14-226">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="c4a14-226">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c4a14-227">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="c4a14-227">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4a14-228">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4a14-228">Requirements</span></span>



| <span data-ttu-id="c4a14-229">需求</span><span class="sxs-lookup"><span data-stu-id="c4a14-229">Requirement</span></span> | <span data-ttu-id="c4a14-230">值</span><span class="sxs-lookup"><span data-stu-id="c4a14-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a14-231">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4a14-231">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a14-232">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4a14-232">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c4a14-233">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4a14-233">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a14-234">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4a14-234">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c4a14-235">標頭</span><span class="sxs-lookup"><span data-stu-id="c4a14-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a14-236"><dt>Wininet</dt></span><span class="sxs-lookup"><span data-stu-id="c4a14-236"><dt>Wininet.h</dt></span></span> </dl> |



 

