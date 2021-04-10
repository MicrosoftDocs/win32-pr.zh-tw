---
title: 'HTTP_LOGGING_FLAG_ 常數 (Http.sys) '
description: 定義要在 HTTP 伺服器 API 上設定記錄的選項。
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686158"
---
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="951b9-103">HTTP \_ 記錄 \_ 旗標 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="951b9-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="951b9-104">**Http \_ 記錄 \_ 旗 \_** 標常數定義了在 HTTP 伺服器 API 上設定記錄的選項。</span><span class="sxs-lookup"><span data-stu-id="951b9-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="951b9-105">這些常數會在 [**HTTP \_ 記錄 \_ 資訊**](/windows/desktop/api/Http/ns-http-http_logging_info) 結構中使用。</span><span class="sxs-lookup"><span data-stu-id="951b9-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="951b9-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP \_ 記錄 \_ 旗標 \_ 本地 \_ 時間 \_ 變換**</span><span class="sxs-lookup"><span data-stu-id="951b9-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="951b9-107">記錄檔變換是以當地時間為基礎。</span><span class="sxs-lookup"><span data-stu-id="951b9-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="951b9-108">根據預設，記錄檔變換是以國際標準時間 (UTC) 為基礎。</span><span class="sxs-lookup"><span data-stu-id="951b9-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="951b9-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**HTTP \_記錄 \_ 旗標 \_ 使用 \_ UTF8 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="951b9-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="951b9-110">寫入記錄檔時，會將 unicode 欄位轉換成 UTF8 multibytes。</span><span class="sxs-lookup"><span data-stu-id="951b9-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="951b9-111">根據預設，記錄檔會以本機字碼頁轉換來撰寫。</span><span class="sxs-lookup"><span data-stu-id="951b9-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="951b9-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP \_ 記錄 \_ 旗標 \_ 記錄檔 \_ 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="951b9-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="951b9-113">記錄檔只包含錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="951b9-113">The log files include error information only.</span></span> <span data-ttu-id="951b9-114">預設會記錄錯誤和成功回應。</span><span class="sxs-lookup"><span data-stu-id="951b9-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="951b9-115">如果 **HTTP \_ 記錄旗標 \_ \_ 記錄 \_ \_** 檔或 **HTTP \_ 記錄旗標 \_ 記錄 \_ \_ \_** 檔都沒有成功，則會記錄錯誤和成功資訊。</span><span class="sxs-lookup"><span data-stu-id="951b9-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="951b9-116">如果同時設定了 **HTTP \_ 記錄 \_ 旗標記錄檔 \_ \_ 成功 \_** 旗標，則無法設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="951b9-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="951b9-117">這兩個旗標彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="951b9-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="951b9-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**HTTP \_記錄 \_ 旗 \_ \_ \_** 標記錄檔成功</span><span class="sxs-lookup"><span data-stu-id="951b9-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="951b9-119">記錄檔只包含成功資訊。</span><span class="sxs-lookup"><span data-stu-id="951b9-119">The log files include success information only.</span></span> <span data-ttu-id="951b9-120">預設會記錄錯誤和成功交易。</span><span class="sxs-lookup"><span data-stu-id="951b9-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="951b9-121">如果 **HTTP \_ 記錄旗標 \_ \_ 記錄 \_ \_** 檔或 **HTTP \_ 記錄旗標 \_ 記錄 \_ \_ \_** 檔都沒有成功，則會記錄錯誤和成功資訊。</span><span class="sxs-lookup"><span data-stu-id="951b9-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="951b9-122">如果同時設定了 **HTTP \_ 記錄 \_ 旗標記錄檔 \_ \_ 錯誤 \_** 旗標，則無法設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="951b9-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="951b9-123">這兩個旗標彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="951b9-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="951b9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="951b9-124">Requirements</span></span>



| <span data-ttu-id="951b9-125">需求</span><span class="sxs-lookup"><span data-stu-id="951b9-125">Requirement</span></span> | <span data-ttu-id="951b9-126">值</span><span class="sxs-lookup"><span data-stu-id="951b9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="951b9-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="951b9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="951b9-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="951b9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="951b9-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="951b9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="951b9-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="951b9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="951b9-131">標頭</span><span class="sxs-lookup"><span data-stu-id="951b9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="951b9-132"><dt>Http.sys</dt></span><span class="sxs-lookup"><span data-stu-id="951b9-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="951b9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="951b9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951b9-134">HTTP 伺服器 API 版本2.0 常數</span><span class="sxs-lookup"><span data-stu-id="951b9-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="951b9-135">**HTTP \_ 記錄 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="951b9-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="951b9-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="951b9-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="951b9-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="951b9-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="951b9-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="951b9-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="951b9-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="951b9-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





