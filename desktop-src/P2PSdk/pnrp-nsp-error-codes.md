---
description: PNRP NSP 錯誤碼
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: PNRP NSP 錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acee7465a86d56af9b2e07a1ae6948dd1b1a1e9145cee2165b7dd4e90f2a5f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061346"
---
# <a name="pnrp-nsp-error-codes"></a>PNRP NSP 錯誤碼

如果命名空間提供者 (NSP) 函數傳回 **通訊端 \_ 錯誤**，則必須使用 [WSAGetLastError](winsock-nsp-reference-links.md) 來取得更多錯誤資訊。 PNRP NSP 會傳回下列錯誤碼：



| 詞彙                                                                                                                                                                     | 描述                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E 已 \_ 取消<br/>                                                                         | 作業已取消。<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ 否 \_ 其他<br/>                                                                         | 已解決要求的結果尚未就緒。 這可能不是錯誤。<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span> WSA \_ IO \_ 暫止 <br/>                                                                      | 作業未完成。<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>WSA \_ 沒有 \_ 足夠的 \_ 記憶體<br/>                                                      | 沒有足夠的記憶體可完成指定的動作。<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>已 \_ 中止 WSA 作業 \_<br/>                                                       | 作業已取消。<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>WSA \_ PNRP \_ 雲端 \_ 已停用<br/>                                                | 已停用指定的雲端名稱。<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>\_ \_ \_ \_ 找不到 WSA PNRP 雲端<br/>                                            | 無法使用指定的雲端名稱。<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ 雲端 \_ \_ \_ 僅限搜尋<br/>                            | 已嘗試在已設定為僅解析的雲端中註冊名稱。<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>WSA \_ PNRP \_ 用戶端不正確區間 \_ \_ \_ 識別碼<br/> | 在預設值以外的區間使用 PNRP。 PNRP 只會在預設區間中運作。<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>WSA \_ PNRP \_ 不正確身分 \_ 識別<br/>                                          | 無法存取指定的身分識別。<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>WSA \_ PNRP \_ 太 \_ 多 \_ 載入<br/>                                                  | 因為電腦沒有處理要求的資源，所以無法建立對等名稱。 <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | 目前的狀態不允許作業。<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | 指定了不正確參數或參數組合。<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | 網路的連線已遺失。<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | PNRP 未執行指定的功能。<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | PNRP 不支援指定的功能。<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | 作業未完成。<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span>\_找不 \_ 到 WSASERVICE<br/>                                                     | 不支援指定的提供者、命名空間或服務識別碼。<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | 服務尚未啟動。<br/>                                                                             |



 

 

 




