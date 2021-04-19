---
title: 'HTTP_LOG_FIELD_ 常數 (Http.sys) '
description: 定義 W3C 記錄檔和錯誤記錄檔中的欄位。
ms.assetid: 44307d5a-f413-4ee9-9f9c-586c824d5493
topic_type:
- apiref
api_name:
- HTTP_LOG_FIELD_DATE
- HTTP_LOG_FIELD_TIME
- HTTP_LOG_FIELD_CLIENT_IP
- HTTP_LOG_FIELD_USER_NAME
- HTTP_LOG_FIELD_SITE_NAME
- HTTP_LOG_FIELD_COMPUTER_NAME
- HTTP_LOG_FIELD_SERVER_IP
- HTTP_LOG_FIELD_METHOD
- HTTP_LOG_FIELD_URI_STEM
- HTTP_LOG_FIELD_URI_QUERY
- HTTP_LOG_FIELD_STATUS
- HTTP_LOG_FIELD_WIN32_STATUS
- HTTP_LOG_FIELD_BYTES_SENT
- HTTP_LOG_FIELD_BYTES_RECV
- HTTP_LOG_FIELD_TIME_TAKEN
- HTTP_LOG_FIELD_SERVER_PORT
- HTTP_LOG_FIELD_USER_AGENT
- HTTP_LOG_FIELD_COOKIE
- HTTP_LOG_FIELD_REFERER
- HTTP_LOG_FIELD_VERSION
- HTTP_LOG_FIELD_HOST
- HTTP_LOG_FIELD_SUB_STATUS
- HTTP_LOG_FIELD_CLIENT_PORT
- HTTP_LOG_FIELD_URI
- HTTP_LOG_FIELD_SITE_ID
- HTTP_LOG_FIELD_REASON
- HTTP_LOG_FIELD_QUEUE_NAME
- HTTP_LOG_FIELD_STREAMID
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ab05a9126cb5ffb81b65a460e6a9d671c268bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966100"
---
# <a name="http_log_field_-constants"></a><span data-ttu-id="f3e9a-103">HTTP \_ 記錄 \_ 欄位 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f3e9a-103">HTTP\_LOG\_FIELD\_ Constants</span></span>

<span data-ttu-id="f3e9a-104">**HTTP \_ 記錄 \_ 欄位 \_** 常數會定義 W3C 記錄檔和錯誤記錄檔中的欄位。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-104">The **HTTP\_LOG\_FIELD\_** constants define the fields in the W3C log and the error logs.</span></span>

<span data-ttu-id="f3e9a-105">這些常數會在 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info) 結構中使用。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="f3e9a-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP \_ 記錄 \_ 欄位 \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-106"><span id="HTTP_LOG_FIELD_DATE"></span><span id="http_log_field_date"></span>**HTTP\_LOG\_FIELD\_DATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-107">活動發生的日期。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-107">The date on which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP \_ 記錄 \_ 欄位 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-108"><span id="HTTP_LOG_FIELD_TIME"></span><span id="http_log_field_time"></span>**HTTP\_LOG\_FIELD\_TIME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-109">發生活動的時間，以國際標準時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-109">The time, in coordinated universal time (UTC), at which the activity occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP \_ 記錄 \_ 欄位 \_ 用戶端 \_ IP**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-110"><span id="HTTP_LOG_FIELD_CLIENT_IP"></span><span id="http_log_field_client_ip"></span>**HTTP\_LOG\_FIELD\_CLIENT\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-111">發出要求之用戶端的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-111">The IP address of the client that made the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP \_ 記錄 \_ 欄位 \_ 使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-112"><span id="HTTP_LOG_FIELD_USER_NAME"></span><span id="http_log_field_user_name"></span>**HTTP\_LOG\_FIELD\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-113">存取您的伺服器之已驗證使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-113">The name of the authenticated user who accessed your server.</span></span> <span data-ttu-id="f3e9a-114">匿名使用者會以連字號表示。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-114">Anonymous users are indicated by a hyphen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP \_ 記錄 \_ 欄位 \_ 網站 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-115"><span id="HTTP_LOG_FIELD_SITE_NAME"></span><span id="http_log_field_site_name"></span>**HTTP\_LOG\_FIELD\_SITE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-116">產生記錄檔專案所在的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-116">The name of the site on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span>**HTTP \_記錄 \_ 欄位 \_ 電腦 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-117"><span id="_HTTP_LOG_FIELD_COMPUTER_NAME"></span><span id="_http_log_field_computer_name"></span> **HTTP\_LOG\_FIELD\_COMPUTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-118">產生記錄檔專案所在的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-118">The name of the computer on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP \_ 記錄 \_ 欄位 \_ 伺服器 \_ IP**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-119"><span id="HTTP_LOG_FIELD_SERVER_IP"></span><span id="http_log_field_server_ip"></span>**HTTP\_LOG\_FIELD\_SERVER\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-120">產生記錄檔專案之伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-120">The IP address of the server on which the log file entry was generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP \_ 記錄 \_ 欄位 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-121"><span id="HTTP_LOG_FIELD_METHOD"></span><span id="http_log_field_method"></span>**HTTP\_LOG\_FIELD\_METHOD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-122">要求的動作，例如 get 方法。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-122">The requested action, for example, a get method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span>**HTTP \_記錄 \_ 欄位 \_ URI \_ 詞幹**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-123"><span id="_HTTP_LOG_FIELD_URI_STEM"></span><span id="_http_log_field_uri_stem"></span> **HTTP\_LOG\_FIELD\_URI\_STEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-124">動作的目標，例如 Default.htm。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-124">The target of the action, for example, Default.htm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP \_ 記錄 \_ 欄位 \_ URI \_ 查詢**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-125"><span id="HTTP_LOG_FIELD_URI_QUERY"></span><span id="http_log_field_uri_query"></span>**HTTP\_LOG\_FIELD\_URI\_QUERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-126">用戶端嘗試執行的查詢（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-126">The query, if any, that the client was trying to perform.</span></span> <span data-ttu-id="f3e9a-127">只有針對動態頁面才需要執行通用資源識別元 (URI) 查詢。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-127">A Universal Resource Identifier (URI) query is necessary only for dynamic pages.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP \_ 記錄 \_ 欄位 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-128"><span id="HTTP_LOG_FIELD_STATUS"></span><span id="http_log_field_status"></span>**HTTP\_LOG\_FIELD\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-129">HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-129">The HTTP status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP \_ 記錄 \_ 欄位 \_ WIN32 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-130"><span id="HTTP_LOG_FIELD_WIN32_STATUS"></span><span id="http_log_field_win32_status"></span>**HTTP\_LOG\_FIELD\_WIN32\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-131">Windows 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-131">The Windows status code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP \_ 記錄 \_ 欄位 \_ 傳送位元組數 \_**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-132"><span id="HTTP_LOG_FIELD_BYTES_SENT"></span><span id="http_log_field_bytes_sent"></span>**HTTP\_LOG\_FIELD\_BYTES\_SENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-133">伺服器所傳送的位元組數目（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-133">The number, in bytes, sent by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP \_ 記錄 \_ 欄位 \_ 位元組 \_ 接收**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-134"><span id="HTTP_LOG_FIELD_BYTES_RECV"></span><span id="http_log_field_bytes_recv"></span>**HTTP\_LOG\_FIELD\_BYTES\_RECV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-135">伺服器收到的數位（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-135">The number, in bytes, received by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**花費的 HTTP \_ 記錄 \_ 欄位 \_ 時間 \_**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-136"><span id="HTTP_LOG_FIELD_TIME_TAKEN"></span><span id="http_log_field_time_taken"></span>**HTTP\_LOG\_FIELD\_TIME\_TAKEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-137">動作的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-137">The time, in milliseconds, of the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP \_ 記錄 \_ 欄位 \_ 伺服器 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-138"><span id="HTTP_LOG_FIELD_SERVER_PORT"></span><span id="http_log_field_server_port"></span>**HTTP\_LOG\_FIELD\_SERVER\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-139">針對服務設定的伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-139">The server port number that is configured for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span>**HTTP \_記錄 \_ 欄位 \_ 使用者 \_ 代理程式**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-140"><span id="_HTTP_LOG_FIELD_USER_AGENT"></span><span id="_http_log_field_user_agent"></span> **HTTP\_LOG\_FIELD\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-141">用戶端使用的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-141">The application that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP \_ 記錄 \_ 欄位 \_ COOKIE**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-142"><span id="HTTP_LOG_FIELD_COOKIE"></span><span id="http_log_field_cookie"></span>**HTTP\_LOG\_FIELD\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-143">傳送或接收的 cookie 內容（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-143">The content of the cookie sent or received, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP \_ 記錄 \_ 欄位 \_ 推薦者**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-144"><span id="HTTP_LOG_FIELD_REFERER"></span><span id="http_log_field_referer"></span>**HTTP\_LOG\_FIELD\_REFERER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-145">使用者上次造訪的網站。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-145">The site that the user last visited.</span></span> <span data-ttu-id="f3e9a-146">這個網站提供目前網站的連結。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-146">This site provided a link to the current site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP \_ 記錄 \_ 欄位 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-147"><span id="HTTP_LOG_FIELD_VERSION"></span><span id="http_log_field_version"></span>**HTTP\_LOG\_FIELD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-148">用戶端使用的 HTTP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-148">The HTTP protocol version that the client used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP \_ 記錄 \_ 欄位 \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-149"><span id="HTTP_LOG_FIELD_HOST"></span><span id="http_log_field_host"></span>**HTTP\_LOG\_FIELD\_HOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-150">主機標頭名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-150">The host header name, if any.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP \_ 記錄 \_ 欄位 \_ 子 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-151"><span id="HTTP_LOG_FIELD_SUB_STATUS"></span><span id="http_log_field_sub_status"></span>**HTTP\_LOG\_FIELD\_SUB\_STATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-152">子狀態錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-152">The substatus error code.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="f3e9a-153">下列常數用於 HTTP 錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-153">The following constants are used for HTTP error logging.</span></span>

<dl> <dt>

<span data-ttu-id="f3e9a-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP \_ 記錄 \_ 欄位 \_ 用戶端 \_ 埠**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-154"><span id="HTTP_LOG_FIELD_CLIENT_PORT"></span><span id="http_log_field_client_port"></span>**HTTP\_LOG\_FIELD\_CLIENT\_PORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-155">接收要求的用戶端埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-155">The client port number from which the request is received.</span></span> <span data-ttu-id="f3e9a-156">此記錄欄位只會用於錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-156">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP \_ 記錄 \_ 欄位 \_ URI**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-157"><span id="HTTP_LOG_FIELD_URI"></span><span id="http_log_field_uri"></span>**HTTP\_LOG\_FIELD\_URI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-158">要求中收到的 URI，包括查詢部分。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-158">The URI received in the request including the query portion.</span></span> <span data-ttu-id="f3e9a-159">此記錄欄位只會用於錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-159">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP \_ 記錄 \_ 欄位 \_ 網站 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-160"><span id="HTTP_LOG_FIELD_SITE_ID"></span><span id="http_log_field_site_id"></span>**HTTP\_LOG\_FIELD\_SITE\_ID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-161">路由要求的 URL 群組之應用程式特定的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-161">The application-specific numeric ID of the URL Group on which the request is routed.</span></span> <span data-ttu-id="f3e9a-162">此記錄欄位只會用於錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-162">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP \_ 記錄 \_ 欄位 \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-163"><span id="HTTP_LOG_FIELD_REASON"></span><span id="http_log_field_reason"></span>**HTTP\_LOG\_FIELD\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-164">錯誤原因片語。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-164">The error reason phrase.</span></span> <span data-ttu-id="f3e9a-165">此記錄欄位只會用於錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-165">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP \_ 記錄 \_ 欄位 \_ 佇列 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-166"><span id="HTTP_LOG_FIELD_QUEUE_NAME"></span><span id="http_log_field_queue_name"></span>**HTTP\_LOG\_FIELD\_QUEUE\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-167">分派要求的要求佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-167">The name of the request queue to which the request is dispatched.</span></span> <span data-ttu-id="f3e9a-168">此記錄欄位只會用於錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-168">This log field is only used for error logging.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3e9a-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP \_ 記錄 \_ 欄位 \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-169"><span id="HTTP_LOG_FIELD_STREAMID"></span><span id="http_log_field_streamid"></span>**HTTP\_LOG\_FIELD\_STREAMID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3e9a-170">資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3e9a-170">The stream id.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3e9a-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3e9a-171">Requirements</span></span>



| <span data-ttu-id="f3e9a-172">需求</span><span class="sxs-lookup"><span data-stu-id="f3e9a-172">Requirement</span></span> | <span data-ttu-id="f3e9a-173">值</span><span class="sxs-lookup"><span data-stu-id="f3e9a-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f3e9a-174">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3e9a-174">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e9a-175">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3e9a-175">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3e9a-176">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3e9a-176">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e9a-177">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3e9a-177">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f3e9a-178">標頭</span><span class="sxs-lookup"><span data-stu-id="f3e9a-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e9a-179"><dt>Http.sys</dt></span><span class="sxs-lookup"><span data-stu-id="f3e9a-179"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e9a-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3e9a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e9a-181">HTTP 伺服器 API 版本2.0 常數</span><span class="sxs-lookup"><span data-stu-id="f3e9a-181">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="f3e9a-182">**HTTP \_ 記錄 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-182">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="f3e9a-183">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-183">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="f3e9a-184">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-184">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="f3e9a-185">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-185">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="f3e9a-186">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="f3e9a-186">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





