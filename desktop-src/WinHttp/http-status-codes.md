---
description: 這些常數和對應的值表示網際網路上的伺服器所傳回的 HTTP 狀態碼。
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: " (WinHTTP. h) 的 HTTP 狀態碼"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf4103cdc382bd5ab0d582fe99212083e2780ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193454"
---
# <a name="http-status-codes-winhttph"></a><span data-ttu-id="94b36-103"> (WinHTTP. h) 的 HTTP 狀態碼</span><span class="sxs-lookup"><span data-stu-id="94b36-103">HTTP Status Codes (Winhttp.h)</span></span>

<span data-ttu-id="94b36-104">這些常數和對應的值表示網際網路上的伺服器所傳回的 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="94b36-104">These constants and corresponding values indicate HTTP status codes returned by servers on the Internet.</span></span>

<dl> <dt>

<span data-ttu-id="94b36-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP \_ 狀態 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="94b36-105"><span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-106">100</span><span class="sxs-lookup"><span data-stu-id="94b36-106">100</span></span>
</dt> <dt>



<span data-ttu-id="94b36-107">要求可以繼續。</span><span class="sxs-lookup"><span data-stu-id="94b36-107">The request can be continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP \_ 狀態 \_ 切換 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="94b36-108"><span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP\_STATUS\_SWITCH\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-109">101</span><span class="sxs-lookup"><span data-stu-id="94b36-109">101</span></span>
</dt> <dt>



<span data-ttu-id="94b36-110">伺服器已切換升級標頭中的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94b36-110">The server has switched protocols in an upgrade header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP \_ 狀態 \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="94b36-111"><span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP\_STATUS\_OK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-112">200</span><span class="sxs-lookup"><span data-stu-id="94b36-112">200</span></span>
</dt> <dt>



<span data-ttu-id="94b36-113">要求已順利完成。</span><span class="sxs-lookup"><span data-stu-id="94b36-113">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**已 \_ 建立 HTTP 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="94b36-114"><span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**HTTP\_STATUS\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-115">201</span><span class="sxs-lookup"><span data-stu-id="94b36-115">201</span></span>
</dt> <dt>



<span data-ttu-id="94b36-116">要求已完成，並導致建立新的資源。</span><span class="sxs-lookup"><span data-stu-id="94b36-116">The request has been fulfilled and resulted in the creation of a new resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP \_ 狀態已 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="94b36-117"><span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP\_STATUS\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-118">202</span><span class="sxs-lookup"><span data-stu-id="94b36-118">202</span></span>
</dt> <dt>



<span data-ttu-id="94b36-119">已接受要求進行處理，但處理尚未完成。</span><span class="sxs-lookup"><span data-stu-id="94b36-119">The request has been accepted for processing, but the processing has not been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP \_ 狀態 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="94b36-120"><span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP\_STATUS\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-121">203</span><span class="sxs-lookup"><span data-stu-id="94b36-121">203</span></span>
</dt> <dt>



<span data-ttu-id="94b36-122">在實體標頭中傳回的中繼資料不是源伺服器中可用的明確集合。</span><span class="sxs-lookup"><span data-stu-id="94b36-122">The returned meta information in the entity-header is not the definitive set available from the originating server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP \_ 狀態 \_ 沒有 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="94b36-123"><span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP\_STATUS\_NO\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-124">204</span><span class="sxs-lookup"><span data-stu-id="94b36-124">204</span></span>
</dt> <dt>



<span data-ttu-id="94b36-125">伺服器已完成要求，但沒有要傳回的新資訊。</span><span class="sxs-lookup"><span data-stu-id="94b36-125">The server has fulfilled the request, but there is no new information to send back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP \_ 狀態 \_ 重設 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="94b36-126"><span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP\_STATUS\_RESET\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-127">205</span><span class="sxs-lookup"><span data-stu-id="94b36-127">205</span></span>
</dt> <dt>



<span data-ttu-id="94b36-128">要求已完成，而且用戶端程式應該重設造成要求傳送的檔視圖，讓使用者可以輕鬆地起始另一個輸入動作。</span><span class="sxs-lookup"><span data-stu-id="94b36-128">The request has been completed, and the client program should reset the document view that caused the request to be sent to allow the user to easily initiate another input action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP \_ 狀態 \_ 部分 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="94b36-129"><span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP\_STATUS\_PARTIAL\_CONTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-130">206</span><span class="sxs-lookup"><span data-stu-id="94b36-130">206</span></span>
</dt> <dt>



<span data-ttu-id="94b36-131">伺服器已滿足部分資源的 GET 要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-131">The server has fulfilled the partial GET request for the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP \_ 狀態 \_ WEBDAV \_ 多重 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="94b36-132"><span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP\_STATUS\_WEBDAV\_MULTI\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-133">207</span><span class="sxs-lookup"><span data-stu-id="94b36-133">207</span></span>
</dt> <dt>



<span data-ttu-id="94b36-134">在 World Wide Web 分散式撰寫和版本控制 (WebDAV) 作業期間，這表示單一回應的多個狀態碼。</span><span class="sxs-lookup"><span data-stu-id="94b36-134">During a World Wide Web Distributed Authoring and Versioning (WebDAV) operation, this indicates multiple status codes for a single response.</span></span> <span data-ttu-id="94b36-135">回應主體包含描述狀態碼可延伸標記語言 (XML)  (XML) 。</span><span class="sxs-lookup"><span data-stu-id="94b36-135">The response body contains Extensible Markup Language (XML) that describes the status codes.</span></span> <span data-ttu-id="94b36-136">如需詳細資訊，請參閱 [分散式撰寫的 HTTP 擴充](../webdav/webdav-portal.md)功能。</span><span class="sxs-lookup"><span data-stu-id="94b36-136">For more information, see [HTTP Extensions for Distributed Authoring](../webdav/webdav-portal.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP \_ 狀態不 \_ 明確**</span><span class="sxs-lookup"><span data-stu-id="94b36-137"><span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP\_STATUS\_AMBIGUOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-138">300</span><span class="sxs-lookup"><span data-stu-id="94b36-138">300</span></span>
</dt> <dt>



<span data-ttu-id="94b36-139">要求的資源可在一或多個位置使用。</span><span class="sxs-lookup"><span data-stu-id="94b36-139">The requested resource is available at one or more locations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**已 \_ 移動 HTTP 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="94b36-140"><span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**HTTP\_STATUS\_MOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-141">301</span><span class="sxs-lookup"><span data-stu-id="94b36-141">301</span></span>
</dt> <dt>



<span data-ttu-id="94b36-142">要求的資源已指派給新的永久統一資源識別項 (URI) ，而此資源的任何未來參考都應該使用其中一個傳回的 Uri 來完成。</span><span class="sxs-lookup"><span data-stu-id="94b36-142">The requested resource has been assigned to a new permanent Uniform Resource Identifier (URI), and any future references to this resource should be done using one of the returned URIs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP \_ 狀態重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="94b36-143"><span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP\_STATUS\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-144">302</span><span class="sxs-lookup"><span data-stu-id="94b36-144">302</span></span>
</dt> <dt>



<span data-ttu-id="94b36-145">要求的資源暫時位於不同的 URI 下。</span><span class="sxs-lookup"><span data-stu-id="94b36-145">The requested resource resides temporarily under a different URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP \_ 狀態重新 \_ 導向 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="94b36-146"><span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP\_STATUS\_REDIRECT\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-147">303</span><span class="sxs-lookup"><span data-stu-id="94b36-147">303</span></span>
</dt> <dt>



<span data-ttu-id="94b36-148">您可以在不同的 URI 下找到要求的回應，而且應該使用該資源上的 GET [*HTTP 指令動詞*](glossary.md) 來加以取出。</span><span class="sxs-lookup"><span data-stu-id="94b36-148">The response to the request can be found under a different URI and should be retrieved using a GET [*HTTP verb*](glossary.md) on that resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_ \_ 未修改 HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="94b36-149"><span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**HTTP\_STATUS\_NOT\_MODIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-150">304</span><span class="sxs-lookup"><span data-stu-id="94b36-150">304</span></span>
</dt> <dt>



<span data-ttu-id="94b36-151">未修改要求的資源。</span><span class="sxs-lookup"><span data-stu-id="94b36-151">The requested resource has not been modified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ 狀態 \_ 使用 \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="94b36-152"><span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP\_STATUS\_USE\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-153">305</span><span class="sxs-lookup"><span data-stu-id="94b36-153">305</span></span>
</dt> <dt>



<span data-ttu-id="94b36-154">要求的資源必須透過 [位置] 欄位提供的 proxy 存取。</span><span class="sxs-lookup"><span data-stu-id="94b36-154">The requested resource must be accessed through the proxy given by the location field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP \_ 狀態重新 \_ 導向 \_ 保留 \_ 動詞**</span><span class="sxs-lookup"><span data-stu-id="94b36-155"><span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP\_STATUS\_REDIRECT\_KEEP\_VERB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-156">307</span><span class="sxs-lookup"><span data-stu-id="94b36-156">307</span></span>
</dt> <dt>



<span data-ttu-id="94b36-157">重新導向的要求會保留相同的 [*HTTP 動詞*](glossary.md)命令。</span><span class="sxs-lookup"><span data-stu-id="94b36-157">The redirected request keeps the same [*HTTP verb*](glossary.md).</span></span> <span data-ttu-id="94b36-158">HTTP/1.1 行為。</span><span class="sxs-lookup"><span data-stu-id="94b36-158">HTTP/1.1 behavior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP \_ 狀態不 \_ 正確的 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="94b36-159"><span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP\_STATUS\_BAD\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-160">400</span><span class="sxs-lookup"><span data-stu-id="94b36-160">400</span></span>
</dt> <dt>



<span data-ttu-id="94b36-161">因為語法無效，所以伺服器無法處理此要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-161">The request could not be processed by the server due to invalid syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP \_ 狀態已 \_ 拒絕**</span><span class="sxs-lookup"><span data-stu-id="94b36-162"><span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP\_STATUS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-163">401</span><span class="sxs-lookup"><span data-stu-id="94b36-163">401</span></span>
</dt> <dt>



<span data-ttu-id="94b36-164">要求的資源需要進行使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="94b36-164">The requested resource requires user authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP \_ 狀態 \_ 付款 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="94b36-165"><span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP\_STATUS\_PAYMENT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-166">402</span><span class="sxs-lookup"><span data-stu-id="94b36-166">402</span></span>
</dt> <dt>



<span data-ttu-id="94b36-167">未在 HTTP 通訊協定中執行。</span><span class="sxs-lookup"><span data-stu-id="94b36-167">Not implemented in the HTTP protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP \_ 狀態 \_ 禁止**</span><span class="sxs-lookup"><span data-stu-id="94b36-168"><span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP\_STATUS\_FORBIDDEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-169">403</span><span class="sxs-lookup"><span data-stu-id="94b36-169">403</span></span>
</dt> <dt>



<span data-ttu-id="94b36-170">伺服器瞭解要求，但無法完成。</span><span class="sxs-lookup"><span data-stu-id="94b36-170">The server understood the request, but cannot fulfill it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_ \_ 找不到 HTTP 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="94b36-171"><span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**HTTP\_STATUS\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-172">404</span><span class="sxs-lookup"><span data-stu-id="94b36-172">404</span></span>
</dt> <dt>



<span data-ttu-id="94b36-173">伺服器找不到任何符合所要求 URI 的專案。</span><span class="sxs-lookup"><span data-stu-id="94b36-173">The server has not found anything that matches the requested URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ 狀態 \_ 不良 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="94b36-174"><span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP\_STATUS\_BAD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-175">405</span><span class="sxs-lookup"><span data-stu-id="94b36-175">405</span></span>
</dt> <dt>



<span data-ttu-id="94b36-176">不允許使用的 [*HTTP 動詞*](glossary.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="94b36-176">The [*HTTP verb*](glossary.md) used is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP \_ 狀態 \_ 無 \_ 接受**</span><span class="sxs-lookup"><span data-stu-id="94b36-177"><span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP\_STATUS\_NONE\_ACCEPTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-178">406</span><span class="sxs-lookup"><span data-stu-id="94b36-178">406</span></span>
</dt> <dt>



<span data-ttu-id="94b36-179">找不到用戶端可接受的回應。</span><span class="sxs-lookup"><span data-stu-id="94b36-179">No responses acceptable to the client were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP \_ 狀態 \_ PROXY \_ 驗證 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="94b36-180"><span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP\_STATUS\_PROXY\_AUTH\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-181">407</span><span class="sxs-lookup"><span data-stu-id="94b36-181">407</span></span>
</dt> <dt>



<span data-ttu-id="94b36-182">需要 Proxy 驗證。</span><span class="sxs-lookup"><span data-stu-id="94b36-182">Proxy authentication required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP \_ 狀態 \_ 要求 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="94b36-183"><span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP\_STATUS\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-184">408</span><span class="sxs-lookup"><span data-stu-id="94b36-184">408</span></span>
</dt> <dt>



<span data-ttu-id="94b36-185">伺服器要求等待逾時。</span><span class="sxs-lookup"><span data-stu-id="94b36-185">The server timed out waiting for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP \_ 狀態 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="94b36-186"><span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP\_STATUS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-187">409</span><span class="sxs-lookup"><span data-stu-id="94b36-187">409</span></span>
</dt> <dt>



<span data-ttu-id="94b36-188">因為與資源目前的狀態衝突，所以無法完成要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-188">The request could not be completed due to a conflict with the current state of the resource.</span></span> <span data-ttu-id="94b36-189">使用者應以詳細資訊重新提交。</span><span class="sxs-lookup"><span data-stu-id="94b36-189">The user should resubmit with more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP \_ 狀態已 \_ 消失**</span><span class="sxs-lookup"><span data-stu-id="94b36-190"><span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP\_STATUS\_GONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-191">410</span><span class="sxs-lookup"><span data-stu-id="94b36-191">410</span></span>
</dt> <dt>



<span data-ttu-id="94b36-192">伺服器無法再使用要求的資源，且沒有已知的轉送位址。</span><span class="sxs-lookup"><span data-stu-id="94b36-192">The requested resource is no longer available at the server, and no forwarding address is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_需要 HTTP 狀態 \_ 長度 \_**</span><span class="sxs-lookup"><span data-stu-id="94b36-193"><span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**HTTP\_STATUS\_LENGTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-194">411</span><span class="sxs-lookup"><span data-stu-id="94b36-194">411</span></span>
</dt> <dt>



<span data-ttu-id="94b36-195">伺服器無法在沒有定義的內容長度的情況下接受要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-195">The server cannot accept the request without a defined content length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP \_ 狀態 \_ PRECOND \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="94b36-196"><span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP\_STATUS\_PRECOND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-197">412</span><span class="sxs-lookup"><span data-stu-id="94b36-197">412</span></span>
</dt> <dt>



<span data-ttu-id="94b36-198">在一或多個要求標頭欄位中指定的前置條件，會在伺服器上進行測試時評估為 false。</span><span class="sxs-lookup"><span data-stu-id="94b36-198">The precondition given in one or more of the request header fields evaluated to false when it was tested on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP \_ 狀態 \_ 要求 \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="94b36-199"><span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP\_STATUS\_REQUEST\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-200">413</span><span class="sxs-lookup"><span data-stu-id="94b36-200">413</span></span>
</dt> <dt>



<span data-ttu-id="94b36-201">伺服器無法處理要求，因為要求實體大於伺服器能夠處理的數目。</span><span class="sxs-lookup"><span data-stu-id="94b36-201">The server cannot process the request because the request entity is larger than the server is able to process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP \_ 狀態 \_ URI \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="94b36-202"><span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP\_STATUS\_URI\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-203">414</span><span class="sxs-lookup"><span data-stu-id="94b36-203">414</span></span>
</dt> <dt>



<span data-ttu-id="94b36-204">因為要求 URI 的長度超過伺服器可解讀的長度，所以伺服器無法服務該要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-204">The server cannot service the request because the request URI is longer than the server can interpret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP \_ 狀態 \_ 不支援的 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="94b36-205"><span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP\_STATUS\_UNSUPPORTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-206">415</span><span class="sxs-lookup"><span data-stu-id="94b36-206">415</span></span>
</dt> <dt>



<span data-ttu-id="94b36-207">伺服器無法服務要求，因為要求的資源所要求的資源格式不受要求的要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-207">The server cannot service the request because the entity of the request is in a format not supported by the requested resource for the requested method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP \_ 狀態 \_ 重試 \_**</span><span class="sxs-lookup"><span data-stu-id="94b36-208"><span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP\_STATUS\_RETRY\_WITH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-209">449</span><span class="sxs-lookup"><span data-stu-id="94b36-209">449</span></span>
</dt> <dt>



<span data-ttu-id="94b36-210">執行適當的動作之後，應重試要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-210">The request should be retried after doing the appropriate action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP \_ 狀態 \_ 伺服器 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="94b36-211"><span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP\_STATUS\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-212">500</span><span class="sxs-lookup"><span data-stu-id="94b36-212">500</span></span>
</dt> <dt>



<span data-ttu-id="94b36-213">伺服器發生未預期的狀況，導致無法履行要求。</span><span class="sxs-lookup"><span data-stu-id="94b36-213">The server encountered an unexpected condition that prevented it from fulfilling the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_ \_ 不支援 HTTP \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="94b36-214"><span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**HTTP\_STATUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-215">501</span><span class="sxs-lookup"><span data-stu-id="94b36-215">501</span></span>
</dt> <dt>



<span data-ttu-id="94b36-216">伺服器不支援完成要求所需的功能。</span><span class="sxs-lookup"><span data-stu-id="94b36-216">The server does not support the functionality required to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP \_ 狀態 \_ 錯誤的 \_ 閘道**</span><span class="sxs-lookup"><span data-stu-id="94b36-217"><span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP\_STATUS\_BAD\_GATEWAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-218">502</span><span class="sxs-lookup"><span data-stu-id="94b36-218">502</span></span>
</dt> <dt>



<span data-ttu-id="94b36-219">作為閘道或 proxy 的伺服器在嘗試完成要求時所存取的上游伺服器收到不正確回應。</span><span class="sxs-lookup"><span data-stu-id="94b36-219">The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP \_ 狀態 \_ 服務 \_ UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="94b36-220"><span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP\_STATUS\_SERVICE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-221">503</span><span class="sxs-lookup"><span data-stu-id="94b36-221">503</span></span>
</dt> <dt>



<span data-ttu-id="94b36-222">服務暫時超載。</span><span class="sxs-lookup"><span data-stu-id="94b36-222">The service is temporarily overloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP \_ 狀態 \_ 閘道 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="94b36-223"><span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP\_STATUS\_GATEWAY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-224">504</span><span class="sxs-lookup"><span data-stu-id="94b36-224">504</span></span>
</dt> <dt>



<span data-ttu-id="94b36-225">要求閘道等待逾時。</span><span class="sxs-lookup"><span data-stu-id="94b36-225">The request was timed out waiting for a gateway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94b36-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP \_ 狀態 \_ 版本 \_ 不是 \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="94b36-226"><span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP\_STATUS\_VERSION\_NOT\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94b36-227">505</span><span class="sxs-lookup"><span data-stu-id="94b36-227">505</span></span>
</dt> <dt>



<span data-ttu-id="94b36-228">伺服器不支援要求訊息中所使用的 HTTP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="94b36-228">The server does not support the HTTP protocol version that was used in the request message.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94b36-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="94b36-229">Requirements</span></span>



| <span data-ttu-id="94b36-230">需求</span><span class="sxs-lookup"><span data-stu-id="94b36-230">Requirement</span></span> | <span data-ttu-id="94b36-231">值</span><span class="sxs-lookup"><span data-stu-id="94b36-231">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="94b36-232">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94b36-232">Minimum supported client</span></span><br/> | <span data-ttu-id="94b36-233">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94b36-233">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="94b36-234">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94b36-234">Minimum supported server</span></span><br/> | <span data-ttu-id="94b36-235">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="94b36-235">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>   |
| <span data-ttu-id="94b36-236">標頭</span><span class="sxs-lookup"><span data-stu-id="94b36-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="94b36-237"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="94b36-237"><dt>Winhttp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b36-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94b36-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b36-239">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="94b36-239">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

