---
description: 這些常數和對應的值表示網際網路上的伺服器所傳回的 HTTP 狀態碼。
ms.assetid: 3de6a35d-41e9-4fce-ab92-e970c7c07e55
title: " (WinHTTP. h) 的 HTTP 狀態碼"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86f145a2a7b5f7e807d1b393d9c4fd9b4f71c81052f0f023a04f72e139842637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744569"
---
# <a name="http-status-codes-winhttph"></a> (WinHTTP. h) 的 HTTP 狀態碼

這些常數和對應的值表示網際網路上的伺服器所傳回的 HTTP 狀態碼。

<dl> <dt>

<span id="HTTP_STATUS_CONTINUE"></span><span id="http_status_continue"></span>**HTTP \_ 狀態 \_ 繼續**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



要求可以繼續。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SWITCH_PROTOCOLS"></span><span id="http_status_switch_protocols"></span>**HTTP \_ 狀態 \_ 切換 \_ 通訊協定**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



伺服器已切換升級標頭中的通訊協定。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_OK"></span><span id="http_status_ok"></span>**HTTP \_ 狀態 \_ 確定**
</dt> <dd> <dl> <dt>

200
</dt> <dt>



要求已順利完成。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CREATED"></span><span id="http_status_created"></span>**已 \_ 建立 HTTP 狀態 \_**
</dt> <dd> <dl> <dt>

201
</dt> <dt>



要求已完成，並導致建立新的資源。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_ACCEPTED"></span><span id="http_status_accepted"></span>**HTTP \_ 狀態已 \_ 接受**
</dt> <dd> <dl> <dt>

202
</dt> <dt>



已接受要求進行處理，但處理尚未完成。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL"></span><span id="http_status_partial"></span>**HTTP \_ 狀態 \_ 部分**
</dt> <dd> <dl> <dt>

203
</dt> <dt>



在實體標頭中傳回的中繼資料不是源伺服器中可用的明確集合。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NO_CONTENT"></span><span id="http_status_no_content"></span>**HTTP \_ 狀態 \_ 沒有 \_ 內容**
</dt> <dd> <dl> <dt>

204
</dt> <dt>



伺服器已完成要求，但沒有要傳回的新資訊。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RESET_CONTENT"></span><span id="http_status_reset_content"></span>**HTTP \_ 狀態 \_ 重設 \_ 內容**
</dt> <dd> <dl> <dt>

205
</dt> <dt>



要求已完成，而且用戶端程式應該重設造成要求傳送的檔視圖，讓使用者可以輕鬆地起始另一個輸入動作。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PARTIAL_CONTENT"></span><span id="http_status_partial_content"></span>**HTTP \_ 狀態 \_ 部分 \_ 內容**
</dt> <dd> <dl> <dt>

206
</dt> <dt>



伺服器已滿足部分資源的 GET 要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_WEBDAV_MULTI_STATUS"></span><span id="http_status_webdav_multi_status"></span>**HTTP \_ 狀態 \_ WEBDAV \_ 多重 \_ 狀態**
</dt> <dd> <dl> <dt>

207
</dt> <dt>



在 World Wide Web 分散式撰寫和版本控制 (WebDAV) 作業期間，這表示單一回應的多個狀態碼。 回應主體包含描述狀態碼可延伸標記語言 (XML)  (XML) 。 如需詳細資訊，請參閱 [分散式撰寫的 HTTP 擴充](../webdav/webdav-portal.md)功能。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_AMBIGUOUS"></span><span id="http_status_ambiguous"></span>**HTTP \_ 狀態不 \_ 明確**
</dt> <dd> <dl> <dt>

300
</dt> <dt>



要求的資源可在一或多個位置使用。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_MOVED"></span><span id="http_status_moved"></span>**已 \_ 移動 HTTP 狀態 \_**
</dt> <dd> <dl> <dt>

301
</dt> <dt>



要求的資源已指派給新的永久統一資源識別項 (URI) ，而此資源的任何未來參考都應該使用其中一個傳回的 Uri 來完成。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT"></span><span id="http_status_redirect"></span>**HTTP \_ 狀態重新 \_ 導向**
</dt> <dd> <dl> <dt>

302
</dt> <dt>



要求的資源暫時位於不同的 URI 下。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_METHOD"></span><span id="http_status_redirect_method"></span>**HTTP \_ 狀態重新 \_ 導向 \_ 方法**
</dt> <dd> <dl> <dt>

303
</dt> <dt>



您可以在不同的 URI 下找到要求的回應，而且應該使用該資源上的 GET [*HTTP 指令動詞*](glossary.md) 來加以取出。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_MODIFIED"></span><span id="http_status_not_modified"></span>**\_ \_ 未修改 HTTP \_ 狀態**
</dt> <dd> <dl> <dt>

304
</dt> <dt>



未修改要求的資源。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_USE_PROXY"></span><span id="http_status_use_proxy"></span>**HTTP \_ 狀態 \_ 使用 \_ PROXY**
</dt> <dd> <dl> <dt>

305
</dt> <dt>



要求的資源必須透過 [位置] 欄位提供的 proxy 存取。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REDIRECT_KEEP_VERB"></span><span id="http_status_redirect_keep_verb"></span>**HTTP \_ 狀態重新 \_ 導向 \_ 保留 \_ 動詞**
</dt> <dd> <dl> <dt>

307
</dt> <dt>



重新導向的要求會保留相同的 [*HTTP 動詞*](glossary.md)命令。 HTTP/1.1 行為。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_REQUEST"></span><span id="http_status_bad_request"></span>**HTTP \_ 狀態不 \_ 正確的 \_ 要求**
</dt> <dd> <dl> <dt>

400
</dt> <dt>



因為語法無效，所以伺服器無法處理此要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_DENIED"></span><span id="http_status_denied"></span>**HTTP \_ 狀態已 \_ 拒絕**
</dt> <dd> <dl> <dt>

401
</dt> <dt>



要求的資源需要進行使用者驗證。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PAYMENT_REQ"></span><span id="http_status_payment_req"></span>**HTTP \_ 狀態 \_ 付款 \_ 需求**
</dt> <dd> <dl> <dt>

402
</dt> <dt>



未在 HTTP 通訊協定中執行。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_FORBIDDEN"></span><span id="http_status_forbidden"></span>**HTTP \_ 狀態 \_ 禁止**
</dt> <dd> <dl> <dt>

403
</dt> <dt>



伺服器瞭解要求，但無法完成。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_FOUND"></span><span id="http_status_not_found"></span>**\_ \_ 找不到 HTTP 狀態 \_**
</dt> <dd> <dl> <dt>

404
</dt> <dt>



伺服器找不到任何符合所要求 URI 的專案。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_METHOD"></span><span id="http_status_bad_method"></span>**HTTP \_ 狀態 \_ 不良 \_ 方法**
</dt> <dd> <dl> <dt>

405
</dt> <dt>



不允許使用的 [*HTTP 動詞*](glossary.md) 命令。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NONE_ACCEPTABLE"></span><span id="http_status_none_acceptable"></span>**HTTP \_ 狀態 \_ 無 \_ 接受**
</dt> <dd> <dl> <dt>

406
</dt> <dt>



找不到用戶端可接受的回應。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="http_status_proxy_auth_req"></span>**HTTP \_ 狀態 \_ PROXY \_ 驗證 \_ 需求**
</dt> <dd> <dl> <dt>

407
</dt> <dt>



需要 Proxy 驗證。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="http_status_request_timeout"></span>**HTTP \_ 狀態 \_ 要求 \_ 超時**
</dt> <dd> <dl> <dt>

408
</dt> <dt>



伺服器要求等待逾時。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_CONFLICT"></span><span id="http_status_conflict"></span>**HTTP \_ 狀態 \_ 衝突**
</dt> <dd> <dl> <dt>

409
</dt> <dt>



因為與資源目前的狀態衝突，所以無法完成要求。 使用者應以詳細資訊重新提交。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GONE"></span><span id="http_status_gone"></span>**HTTP \_ 狀態已 \_ 消失**
</dt> <dd> <dl> <dt>

410
</dt> <dt>



伺服器無法再使用要求的資源，且沒有已知的轉送位址。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_LENGTH_REQUIRED"></span><span id="http_status_length_required"></span>**\_需要 HTTP 狀態 \_ 長度 \_**
</dt> <dd> <dl> <dt>

411
</dt> <dt>



伺服器無法在沒有定義的內容長度的情況下接受要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_PRECOND_FAILED"></span><span id="http_status_precond_failed"></span>**HTTP \_ 狀態 \_ PRECOND \_ 失敗**
</dt> <dd> <dl> <dt>

412
</dt> <dt>



在一或多個要求標頭欄位中指定的前置條件，會在伺服器上進行測試時評估為 false。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_REQUEST_TOO_LARGE"></span><span id="http_status_request_too_large"></span>**HTTP \_ 狀態 \_ 要求 \_ 太 \_ 大**
</dt> <dd> <dl> <dt>

413
</dt> <dt>



伺服器無法處理要求，因為要求實體大於伺服器能夠處理的數目。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_URI_TOO_LONG"></span><span id="http_status_uri_too_long"></span>**HTTP \_ 狀態 \_ URI \_ 太 \_ 長**
</dt> <dd> <dl> <dt>

414
</dt> <dt>



因為要求 URI 的長度超過伺服器可解讀的長度，所以伺服器無法服務該要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_UNSUPPORTED_MEDIA"></span><span id="http_status_unsupported_media"></span>**HTTP \_ 狀態 \_ 不支援的 \_ 媒體**
</dt> <dd> <dl> <dt>

415
</dt> <dt>



伺服器無法服務要求，因為要求的資源所要求的資源格式不受要求的要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_RETRY_WITH"></span><span id="http_status_retry_with"></span>**HTTP \_ 狀態 \_ 重試 \_**
</dt> <dd> <dl> <dt>

449
</dt> <dt>



執行適當的動作之後，應重試要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVER_ERROR"></span><span id="http_status_server_error"></span>**HTTP \_ 狀態 \_ 伺服器 \_ 錯誤**
</dt> <dd> <dl> <dt>

500
</dt> <dt>



伺服器發生未預期的狀況，導致無法履行要求。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_NOT_SUPPORTED"></span><span id="http_status_not_supported"></span>**\_ \_ 不支援 HTTP \_ 狀態**
</dt> <dd> <dl> <dt>

501
</dt> <dt>



伺服器不支援完成要求所需的功能。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_BAD_GATEWAY"></span><span id="http_status_bad_gateway"></span>**HTTP \_ 狀態 \_ 錯誤的 \_ 閘道**
</dt> <dd> <dl> <dt>

502
</dt> <dt>



作為閘道或 proxy 的伺服器在嘗試完成要求時所存取的上游伺服器收到不正確回應。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="http_status_service_unavail"></span>**HTTP \_ 狀態 \_ 服務 \_ UNAVAIL**
</dt> <dd> <dl> <dt>

503
</dt> <dt>



服務暫時超載。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="http_status_gateway_timeout"></span>**HTTP \_ 狀態 \_ 閘道 \_ 超時**
</dt> <dd> <dl> <dt>

504
</dt> <dt>



要求閘道等待逾時。


</dt> </dl> </dd> <dt>

<span id="HTTP_STATUS_VERSION_NOT_SUP"></span><span id="http_status_version_not_sup"></span>**HTTP \_ 狀態 \_ 版本 \_ 不是 \_ SUP**
</dt> <dd> <dl> <dt>

505
</dt> <dt>



伺服器不支援要求訊息中所使用的 HTTP 通訊協定版本。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsXP、Windows 2000 Professional 搭配 SP3 \[ desktop 應用程式\]<br/>      |
| 最低支援的伺服器<br/> | Windows伺服器2003、Windows 2000 伺服器（僅含 SP3 \[ desktop 應用程式）\]<br/>   |
| 標頭<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinHTTP 版本](winhttp-versions.md)
</dt> </dl>

 

