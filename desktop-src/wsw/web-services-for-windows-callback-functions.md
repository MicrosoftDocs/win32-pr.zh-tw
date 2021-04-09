---
title: Windows Web 服務回呼函數
description: 回呼可讓應用程式呼叫在另一層或層級定義的函數。
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a385ca21d00e8845f89bda0d9b04221a922ba421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092223"
---
# <a name="windows-web-services-callback-functions"></a><span data-ttu-id="26e6b-105">Windows Web 服務回呼函數</span><span class="sxs-lookup"><span data-stu-id="26e6b-105">Windows Web Services Callback Functions</span></span>

<span data-ttu-id="26e6b-106">回呼可讓應用程式呼叫在另一層或層級定義的函數。</span><span class="sxs-lookup"><span data-stu-id="26e6b-106">Callbacks enable an application to call a function defined at another layer or level.</span></span> <span data-ttu-id="26e6b-107">應用程式會將函式引數註冊為處理常式，稍後視需要以非同步方式呼叫。</span><span class="sxs-lookup"><span data-stu-id="26e6b-107">The application registers the function argument as a handler that is to be called asynchronously at a later time as required.</span></span> <span data-ttu-id="26e6b-108">如果函式以非同步方式完成，表示函式成功或錯誤，則會叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="26e6b-108">The callback is invoked if the function completes asynchronously indicating function success or error.</span></span> <span data-ttu-id="26e6b-109">如果作業同步完成，則不會呼叫回呼。</span><span class="sxs-lookup"><span data-stu-id="26e6b-109">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="26e6b-110">Windows Web 服務 API 包含下列回呼函數：</span><span class="sxs-lookup"><span data-stu-id="26e6b-110">The Windows Web Services API includes the following callback functions:</span></span>

-   [<span data-ttu-id="26e6b-111">**WS \_ 放棄 \_ 訊息 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-111">**WS\_ABANDON\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [<span data-ttu-id="26e6b-112">**WS \_ 中止 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-112">**WS\_ABORT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [<span data-ttu-id="26e6b-113">**WS \_ 中止接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-113">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="26e6b-114">**WS \_ 接受 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-114">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="26e6b-115">**WS \_ ASYNC \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-115">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [<span data-ttu-id="26e6b-116">**WS \_ ASYNC \_ 函數**</span><span class="sxs-lookup"><span data-stu-id="26e6b-116">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [<span data-ttu-id="26e6b-117">**WS \_ CERT \_ 簽發者 \_ 清單 \_ 通知 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-117">**WS\_CERT\_ISSUER\_LIST\_NOTIFICATION\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [<span data-ttu-id="26e6b-118">**WS \_ 憑證 \_ 驗證 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-118">**WS\_CERTIFICATE\_VALIDATION\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [<span data-ttu-id="26e6b-119">**WS \_ 關閉 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-119">**WS\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [<span data-ttu-id="26e6b-120">**WS \_ 關閉接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-120">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="26e6b-121">**WS \_ 建立 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-121">**WS\_CREATE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [<span data-ttu-id="26e6b-122">**接聽 \_ \_ \_ 程式回呼的 \_ WS CREATE 通道 \_**</span><span class="sxs-lookup"><span data-stu-id="26e6b-122">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="26e6b-123">**WS \_ 建立 \_ 解碼器 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-123">**WS\_CREATE\_DECODER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [<span data-ttu-id="26e6b-124">**WS \_ 建立 \_ 編碼器 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-124">**WS\_CREATE\_ENCODER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [<span data-ttu-id="26e6b-125">**WS \_ 建立接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-125">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="26e6b-126">**WS \_ 解碼 \_ 解碼 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-126">**WS\_DECODER\_DECODE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [<span data-ttu-id="26e6b-127">**WS \_ 解碼器 \_ 結束 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-127">**WS\_DECODER\_END\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [<span data-ttu-id="26e6b-128">**WS \_ 解碼 \_ 取得 \_ 內容 \_ 類型 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-128">**WS\_DECODER\_GET\_CONTENT\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [<span data-ttu-id="26e6b-129">**WS \_ 解碼 \_ 開始 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-129">**WS\_DECODER\_START\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [<span data-ttu-id="26e6b-130">**WS \_ 持續時間 \_ 比較 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-130">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="26e6b-131">**WS \_ 動態 \_ 字串 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-131">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="26e6b-132">**WS \_ 編碼器 \_ 編碼 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-132">**WS\_ENCODER\_ENCODE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [<span data-ttu-id="26e6b-133">**WS \_ 編碼器 \_ 結束 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-133">**WS\_ENCODER\_END\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [<span data-ttu-id="26e6b-134">**WS \_ 編碼器 \_ 取得 \_ 內容 \_ 類型 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-134">**WS\_ENCODER\_GET\_CONTENT\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [<span data-ttu-id="26e6b-135">**WS \_ 編碼器 \_ 啟動 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-135">**WS\_ENCODER\_START\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [<span data-ttu-id="26e6b-136">**WS \_ FREE \_ CHANNEL \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-136">**WS\_FREE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [<span data-ttu-id="26e6b-137">**WS \_ FREE \_ 解碼器 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-137">**WS\_FREE\_DECODER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [<span data-ttu-id="26e6b-138">**WS \_ 免費 \_ 編碼器 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-138">**WS\_FREE\_ENCODER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [<span data-ttu-id="26e6b-139">**WS \_ 免費接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-139">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="26e6b-140">**WS \_ GET \_ CERT \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-140">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [<span data-ttu-id="26e6b-141">**WS \_ GET \_ 通道 \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-141">**WS\_GET\_CHANNEL\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [<span data-ttu-id="26e6b-142">**WS \_ GET 接聽程式 \_ \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-142">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="26e6b-143">**WS \_ HTTP 重新 \_ 導向 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-143">**WS\_HTTP\_REDIRECT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [<span data-ttu-id="26e6b-144">**WS \_ 是 \_ 預設 \_ 值 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-144">**WS\_IS\_DEFAULT\_VALUE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [<span data-ttu-id="26e6b-145">**WS \_ 訊息 \_ 完成 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-145">**WS\_MESSAGE\_DONE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [<span data-ttu-id="26e6b-146">**WS \_ 開啟 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-146">**WS\_OPEN\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [<span data-ttu-id="26e6b-147">**WS \_ 開啟接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-147">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="26e6b-148">**WS \_ 操作 \_ 取消 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-148">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [<span data-ttu-id="26e6b-149">**WS \_ 作業 \_ 可用 \_ 狀態 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-149">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [<span data-ttu-id="26e6b-150">**WS \_ PROXY \_ 訊息 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-150">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [<span data-ttu-id="26e6b-151">**WS \_ 提取 \_ 位元組 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-151">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="26e6b-152">**WS \_ PUSH \_ BYTES \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-152">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="26e6b-153">**WS \_ 讀取 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-153">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [<span data-ttu-id="26e6b-154">**WS \_ 讀取 \_ 訊息 \_ 結束 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-154">**WS\_READ\_MESSAGE\_END\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [<span data-ttu-id="26e6b-155">**WS \_ 讀取 \_ 訊息 \_ 開始 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-155">**WS\_READ\_MESSAGE\_START\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [<span data-ttu-id="26e6b-156">**WS \_ 讀取 \_ 類型 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-156">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="26e6b-157">**WS \_ 重設 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-157">**WS\_RESET\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [<span data-ttu-id="26e6b-158">**WS \_ 重設接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-158">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="26e6b-159">**WS \_ 服務 \_ 接受 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-159">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [<span data-ttu-id="26e6b-160">**WS \_ 服務 \_ 關閉 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [<span data-ttu-id="26e6b-161">**WS \_ 服務 \_ 訊息 \_ 接收 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-161">**WS\_SERVICE\_MESSAGE\_RECEIVE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [<span data-ttu-id="26e6b-162">**WS \_ 服務 \_ 安全性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-162">**WS\_SERVICE\_SECURITY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [<span data-ttu-id="26e6b-163">**WS \_ 服務 \_ 存根 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-163">**WS\_SERVICE\_STUB\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [<span data-ttu-id="26e6b-164">**WS \_ 設定 \_ 通道 \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-164">**WS\_SET\_CHANNEL\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [<span data-ttu-id="26e6b-165">**WS \_ SET 接聽程式 \_ \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-165">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [<span data-ttu-id="26e6b-166">**WS \_ 關機 \_ 會話 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-166">**WS\_SHUTDOWN\_SESSION\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [<span data-ttu-id="26e6b-167">**WS \_ 驗證 \_ 密碼 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-167">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [<span data-ttu-id="26e6b-168">**WS \_ 驗證 \_ SAML \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-168">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [<span data-ttu-id="26e6b-169">**WS \_ 寫入 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-169">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [<span data-ttu-id="26e6b-170">**WS \_ 寫入 \_ 訊息 \_ 結束 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-170">**WS\_WRITE\_MESSAGE\_END\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [<span data-ttu-id="26e6b-171">**WS \_ 寫入 \_ 訊息 \_ 開始 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-171">**WS\_WRITE\_MESSAGE\_START\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [<span data-ttu-id="26e6b-172">**WS \_ 寫入 \_ 類型 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="26e6b-172">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




