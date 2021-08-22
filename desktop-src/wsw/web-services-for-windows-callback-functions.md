---
title: WindowsWeb 服務回呼函數
description: 回呼可讓應用程式呼叫在另一層或層級定義的函數。
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a78bce5c4023d889748af103148088462cb4b267192b1c0b3845fc735fd1bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926868"
---
# <a name="windows-web-services-callback-functions"></a>WindowsWeb 服務回呼函數

回呼可讓應用程式呼叫在另一層或層級定義的函數。 應用程式會將函式引數註冊為處理常式，稍後視需要以非同步方式呼叫。 如果函式以非同步方式完成，表示函式成功或錯誤，則會叫用回呼。 如果作業同步完成，則不會呼叫回呼。

Windows Web 服務 API 包含下列回呼函數：

-   [**WS \_ 放棄 \_ 訊息 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**WS \_ 中止 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**WS \_ 中止接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ 接受 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**WS \_ ASYNC \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**WS \_ ASYNC \_ 函數**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**WS \_ CERT \_ 簽發者 \_ 清單 \_ 通知 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**WS \_ 憑證 \_ 驗證 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**WS \_ 關閉 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**WS \_ 關閉接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ 建立 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**接聽 \_ \_ \_ 程式回呼的 \_ WS CREATE 通道 \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ 建立 \_ 解碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**WS \_ 建立 \_ 編碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**WS \_ 建立接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**WS \_ 解碼 \_ 解碼 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**WS \_ 解碼器 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**WS \_ 解碼 \_ 取得 \_ 內容 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**WS \_ 解碼 \_ 開始 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**WS \_ 持續時間 \_ 比較 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**WS \_ 動態 \_ 字串 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**WS \_ 編碼器 \_ 編碼 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**WS \_ 編碼器 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**WS \_ 編碼器 \_ 取得 \_ 內容 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**WS \_ 編碼器 \_ 啟動 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**WS \_ FREE \_ CHANNEL \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**WS \_ FREE \_ 解碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**WS \_ 免費 \_ 編碼器 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**WS \_ 免費接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ CERT \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**WS \_ GET \_ 通道 \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**WS \_ GET 接聽程式 \_ \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS \_ HTTP 重新 \_ 導向 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ 是 \_ 預設 \_ 值 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**WS \_ 訊息 \_ 完成 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**WS \_ 開啟 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**WS \_ 開啟接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS \_ 操作 \_ 取消 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**WS \_ 作業 \_ 可用 \_ 狀態 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**WS \_ PROXY \_ 訊息 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**WS \_ 提取 \_ 位元組 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS \_ PUSH \_ BYTES \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ 讀取 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**WS \_ 讀取 \_ 訊息 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**WS \_ 讀取 \_ 訊息 \_ 開始 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**WS \_ 讀取 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS \_ 重設 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**WS \_ 重設接聽程式 \_ \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS \_ 服務 \_ 接受 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**WS \_ 服務 \_ 關閉 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**WS \_ 服務 \_ 訊息 \_ 接收 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**WS \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**WS \_ 服務 \_ 存根 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**WS \_ 設定 \_ 通道 \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**WS \_ SET 接聽程式 \_ \_ 屬性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**WS \_ 關機 \_ 會話 \_ 通道 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**WS \_ 驗證 \_ 密碼 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**WS \_ 驗證 \_ SAML \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**WS \_ 寫入 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**WS \_ 寫入 \_ 訊息 \_ 結束 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**WS \_ 寫入 \_ 訊息 \_ 開始 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**WS \_ 寫入 \_ 類型 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




