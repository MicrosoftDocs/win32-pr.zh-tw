---
description: 深入瞭解： WUA 網路錯誤代碼
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: 'WUA 網路錯誤代碼 (Wuerror .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995001"
---
# <a name="wua-networking-error-codes"></a>WUA 網路錯誤代碼

Windows Update 代理程式 (WUA) API 在執行網路作業（例如搜尋更新）時，可能會傳回下列錯誤代碼：



| 常數/值                                                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**WU \_E \_ WINHTTP \_ 不正確 \_ FILE**</dt> <dt>0x80240038</dt> </dl>                                  | 下載的檔案包含非預期的內容類型。<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 不良 \_ 要求**</dt> <dt>0x80244016</dt> </dl>              | 與 HTTP 狀態400相同–伺服器無法處理要求，因為語法無效。<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 拒絕**</dt> <dt>0x80244017</dt> </dl>                              | 與 HTTP 狀態401相同–要求的資源需要使用者驗證。<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 禁止**</dt> <dt>0x80244018</dt> </dl>                     | 與 HTTP 狀態403相同–伺服器瞭解要求，但拒絕完成要求。<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ \_ 找不到**</dt> <dt>0x80244019</dt> </dl>                    | 與 HTTP 狀態404相同–伺服器找不到要求的 URI (統一資源識別項) 。<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態不 \_ 正確的 \_ 方法**</dt> <dt>0x8024401A</dt> </dl>                 | 與 HTTP 狀態405相同-不允許 HTTP 方法。<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ PROXY \_ 驗證 \_ 需求**</dt> <dt>0x8024401B</dt> </dl>    | 與 HTTP 狀態407相同–需要 Proxy 驗證。<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 要求 \_ 超時**</dt> <dt>0x8024401C</dt> </dl>  | 與 HTTP 狀態408相同–伺服器等待要求時發生超時。<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 衝突**</dt> <dt>0x8024401D</dt> </dl>                        | 與 HTTP 狀態409相同–因為與資源目前的狀態衝突，所以未完成要求。<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態已 \_ 消失**</dt> <dt>0x8024401E</dt> </dl>                                    | 與 HTTP 狀態410相同–要求的資源已無法在伺服器上使用。<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 伺服器 \_ 錯誤**</dt> <dt>0x8024401F</dt> </dl>           | 與 HTTP 狀態500相同–伺服器內部發生錯誤，導致無法完成要求。<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**WU \_E \_ PT \_ \_ \_ 不 \_ 支援的 HTTP 狀態**</dt> <dt>0x80244020</dt> </dl>        | 與 HTTP 狀態501相同-伺服器不支援完成要求所需的功能。 <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態不 \_ 正確的 \_ 閘道**</dt> <dt>0x80244021</dt> </dl>              | 與 HTTP 狀態502相同–做為閘道或 proxy 的伺服器在嘗試完成要求時所存取的上游伺服器收到不正確回應。<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 服務 \_ UNAVAIL**</dt> <dt>0x80244022</dt> </dl>  | 與 HTTP 狀態503相同–服務暫時超載。<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 閘道 \_ 超時**</dt> <dt>0x80244023</dt> </dl>  | 與 HTTP 狀態504相同–要求已等待閘道等候。<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 版本 \_ 不是 \_ SUP**</dt> <dt>0x80244024</dt> </dl> | 與 HTTP 狀態505相同-伺服器不支援用於要求的 HTTP 通訊協定版本。<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**WU \_E \_ PT \_ HTTP \_ 狀態 \_ 未 \_ 對應**</dt> <dt>0x8024402B</dt> </dl>                 | 無法完成要求，且原因未對應至任何 WU \_ E \_ PT \_ HTTP \_ \* 錯誤碼。<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**WU \_E \_ PT \_ WINHTTP \_ 名稱 \_ 無法 \_ 解析**</dt> <dt>0x8024402C</dt> </dl>        | 與錯誤 \_ WINHTTP \_ 名稱 \_ 無法解析相同 \_ -無法解析 proxy 伺服器或目標伺服器名稱。<br/>                                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wuerror。h</dt> </dl> |



 

 




