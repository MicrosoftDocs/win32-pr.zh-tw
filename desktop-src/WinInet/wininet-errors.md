---
title: " (Wininet. h) 的錯誤訊息"
description: WinINet 函數會在適當的情況下傳回錯誤碼。 下列是 WinINet 函數特有的錯誤。
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106458"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="d424f-104"> (Wininet. h) 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="d424f-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="d424f-105">WinINet 函數會在適當的情況下傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d424f-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="d424f-106">下列是 WinINet 函數特有的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="d424f-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**錯誤 \_ FTP \_ 中斷**</span><span class="sxs-lookup"><span data-stu-id="d424f-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-108">12111</span><span class="sxs-lookup"><span data-stu-id="d424f-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="d424f-109">FTP 作業未完成，因為會話已中止。</span><span class="sxs-lookup"><span data-stu-id="d424f-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**錯誤 \_ FTP \_ 無 \_ 被動 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="d424f-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-111">12112</span><span class="sxs-lookup"><span data-stu-id="d424f-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="d424f-112">被動模式無法在伺服器上使用。</span><span class="sxs-lookup"><span data-stu-id="d424f-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**\_FTP \_ 傳輸 \_ 進行中 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-114">12110</span><span class="sxs-lookup"><span data-stu-id="d424f-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="d424f-115">無法在 FTP 會話控制碼上進行要求的作業，因為操作已在進行中。</span><span class="sxs-lookup"><span data-stu-id="d424f-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 GOPHER 屬性**</span><span class="sxs-lookup"><span data-stu-id="d424f-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-117">12137</span><span class="sxs-lookup"><span data-stu-id="d424f-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="d424f-118">找不到要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="d424f-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-119">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**錯誤 \_ GOPHER \_ 資料 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-121">12132</span><span class="sxs-lookup"><span data-stu-id="d424f-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="d424f-122">從 Gopher 伺服器接收資料時，偵測到錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-123">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**錯誤 \_ GOPHER \_ \_ 資料結尾 \_**</span><span class="sxs-lookup"><span data-stu-id="d424f-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-125">12133</span><span class="sxs-lookup"><span data-stu-id="d424f-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="d424f-126">已到達資料的結尾。</span><span class="sxs-lookup"><span data-stu-id="d424f-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-127">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**錯誤 \_ GOPHER \_ 不正確的 \_ 定位器 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d424f-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-129">12135</span><span class="sxs-lookup"><span data-stu-id="d424f-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="d424f-130">此操作的定位器類型不正確。</span><span class="sxs-lookup"><span data-stu-id="d424f-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-131">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**錯誤 \_ GOPHER \_ 無效 \_ 定位器**</span><span class="sxs-lookup"><span data-stu-id="d424f-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-133">12134</span><span class="sxs-lookup"><span data-stu-id="d424f-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="d424f-134">提供的定位器無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-135">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**錯誤 \_ GOPHER \_ 非 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="d424f-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-137">12131</span><span class="sxs-lookup"><span data-stu-id="d424f-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="d424f-138">您必須對檔案定位器提出要求。</span><span class="sxs-lookup"><span data-stu-id="d424f-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-139">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**錯誤 \_ GOPHER \_ 未 \_ GOPHER \_ 加號**</span><span class="sxs-lookup"><span data-stu-id="d424f-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-141">12136</span><span class="sxs-lookup"><span data-stu-id="d424f-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="d424f-142">要求的作業只能針對 Gopher + 伺服器，或使用指定 Gopher + 作業的定位器進行。</span><span class="sxs-lookup"><span data-stu-id="d424f-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-143">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**錯誤 \_ GOPHER \_ 通訊協定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-145">12130</span><span class="sxs-lookup"><span data-stu-id="d424f-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="d424f-146">剖析從 Gopher 伺服器傳回的資料時，偵測到錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-147">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**錯誤 \_ GOPHER \_ 未知 \_ 定位器**</span><span class="sxs-lookup"><span data-stu-id="d424f-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-149">12138</span><span class="sxs-lookup"><span data-stu-id="d424f-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="d424f-150">定位器類型未知。</span><span class="sxs-lookup"><span data-stu-id="d424f-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-151">僅限 windows XP 及 Windows Server 2003 R2 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**\_拒絕 HTTP \_ COOKIE \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-153">12162</span><span class="sxs-lookup"><span data-stu-id="d424f-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="d424f-154">伺服器拒絕了 HTTP cookie。</span><span class="sxs-lookup"><span data-stu-id="d424f-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**錯誤 \_ HTTP \_ COOKIE \_ 需要 \_ 確認**</span><span class="sxs-lookup"><span data-stu-id="d424f-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-156">12161</span><span class="sxs-lookup"><span data-stu-id="d424f-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="d424f-157">HTTP cookie 需要確認。</span><span class="sxs-lookup"><span data-stu-id="d424f-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-158">Windows Vista 和 Windows Server 2008 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**\_HTTP \_ 下層 \_ 伺服器錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-160">12151</span><span class="sxs-lookup"><span data-stu-id="d424f-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="d424f-161">伺服器未傳回任何標頭。</span><span class="sxs-lookup"><span data-stu-id="d424f-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**錯誤 \_ HTTP \_ 標頭 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="d424f-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-163">12155</span><span class="sxs-lookup"><span data-stu-id="d424f-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="d424f-164">無法新增標頭，因為它已經存在。</span><span class="sxs-lookup"><span data-stu-id="d424f-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**\_ \_ \_ 找不到 HTTP 標頭 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-166">12150</span><span class="sxs-lookup"><span data-stu-id="d424f-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="d424f-167">找不到要求的標頭。</span><span class="sxs-lookup"><span data-stu-id="d424f-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**錯誤 \_ HTTP \_ 無效 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="d424f-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-169">12153</span><span class="sxs-lookup"><span data-stu-id="d424f-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="d424f-170">提供的標頭無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**\_HTTP \_ 無效 \_ 查詢 \_ 要求錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-172">12154</span><span class="sxs-lookup"><span data-stu-id="d424f-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="d424f-173">對 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) 提出的要求無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**錯誤 \_ HTTP \_ 不正確 \_ 伺服器 \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="d424f-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-175">12152</span><span class="sxs-lookup"><span data-stu-id="d424f-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="d424f-176">無法剖析伺服器回應。</span><span class="sxs-lookup"><span data-stu-id="d424f-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**錯誤 \_ HTTP \_ 未重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="d424f-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-178">12160</span><span class="sxs-lookup"><span data-stu-id="d424f-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="d424f-179">未重新導向 HTTP 要求。</span><span class="sxs-lookup"><span data-stu-id="d424f-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**錯誤 \_ HTTP 重新 \_ 導向 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="d424f-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-181">12156</span><span class="sxs-lookup"><span data-stu-id="d424f-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="d424f-182">重新導向失敗，因為配置變更 (例如，將 HTTP 變更為 FTP) 或嘗試重新導向失敗 (預設為五次嘗試) 。</span><span class="sxs-lookup"><span data-stu-id="d424f-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**錯誤 \_ HTTP 重新 \_ 導向 \_ 需要 \_ 確認**</span><span class="sxs-lookup"><span data-stu-id="d424f-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-184">12168</span><span class="sxs-lookup"><span data-stu-id="d424f-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="d424f-185">重新導向需要使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d424f-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**錯誤 \_ 網際網路 \_ 非同步 \_ 執行緒 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="d424f-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-187">12047</span><span class="sxs-lookup"><span data-stu-id="d424f-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="d424f-188">應用程式無法啟動非同步執行緒。</span><span class="sxs-lookup"><span data-stu-id="d424f-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**錯誤 \_ 網際網路 \_ 錯誤 \_ 自動 \_ PROXY \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="d424f-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-190">12166</span><span class="sxs-lookup"><span data-stu-id="d424f-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="d424f-191">自動 proxy 設定腳本中發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**\_網際網路錯誤 \_ \_ 選項 \_ 長度錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-193">12010</span><span class="sxs-lookup"><span data-stu-id="d424f-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="d424f-194">針對指定的選項類型，提供給 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 或 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 之選項的長度不正確。</span><span class="sxs-lookup"><span data-stu-id="d424f-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**網際網路錯誤的登錄 \_ \_ \_ \_ 參數錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-196">12022</span><span class="sxs-lookup"><span data-stu-id="d424f-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="d424f-197">找不到必要的登錄值，但是不正確的類型或具有不正確值。</span><span class="sxs-lookup"><span data-stu-id="d424f-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**\_網際網路 \_ 無法 \_ 連接時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-199">12029</span><span class="sxs-lookup"><span data-stu-id="d424f-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="d424f-200">嘗試連接到伺服器失敗。</span><span class="sxs-lookup"><span data-stu-id="d424f-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**\_INTERNET \_ CHG \_ POST \_ 不 \_ \_ 安全的錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-202">12042</span><span class="sxs-lookup"><span data-stu-id="d424f-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="d424f-203">應用程式正在張貼，並且嘗試在不安全的伺服器上變更多行文字。</span><span class="sxs-lookup"><span data-stu-id="d424f-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**\_需要網際網路 \_ 客戶 \_ 端 \_ 驗證 \_ 憑證時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-205">12044</span><span class="sxs-lookup"><span data-stu-id="d424f-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="d424f-206">伺服器正在要求用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="d424f-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**\_ \_ \_ \_ 未設定網際網路用戶端驗證時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="d424f-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-208">12046</span><span class="sxs-lookup"><span data-stu-id="d424f-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="d424f-209">未在這部電腦上設定用戶端授權。</span><span class="sxs-lookup"><span data-stu-id="d424f-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**\_網際網路 \_ 連接已 \_ 中止時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-211">12030</span><span class="sxs-lookup"><span data-stu-id="d424f-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="d424f-212">與伺服器的連接已終止。</span><span class="sxs-lookup"><span data-stu-id="d424f-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**\_網際網路 \_ 連接 \_ 重設時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-214">12031</span><span class="sxs-lookup"><span data-stu-id="d424f-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="d424f-215">與伺服器的連接已重設。</span><span class="sxs-lookup"><span data-stu-id="d424f-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**錯誤 \_ 網際網路 \_ 解碼 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="d424f-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-217">12175</span><span class="sxs-lookup"><span data-stu-id="d424f-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="d424f-218">WinINet 無法對回應執行內容解碼。</span><span class="sxs-lookup"><span data-stu-id="d424f-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="d424f-219">如需詳細資訊，請參閱 [**內容編碼**](content-encoding.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="d424f-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**錯誤 \_ 網際網路 \_ 對話方塊 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="d424f-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-221">12049</span><span class="sxs-lookup"><span data-stu-id="d424f-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="d424f-222">另一個執行緒正在進行密碼對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d424f-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**\_網際網路中斷連線時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="d424f-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-224">12163</span><span class="sxs-lookup"><span data-stu-id="d424f-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="d424f-225">網際網路連線已中斷。</span><span class="sxs-lookup"><span data-stu-id="d424f-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**\_網際網路 \_ 擴充 \_ 錯誤時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-227">12003</span><span class="sxs-lookup"><span data-stu-id="d424f-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="d424f-228">從伺服器傳回了擴充錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-228">An extended error was returned from the server.</span></span> <span data-ttu-id="d424f-229">這通常是包含詳細錯誤訊息的字串或緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d424f-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="d424f-230">呼叫 [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) 以取得錯誤文字。</span><span class="sxs-lookup"><span data-stu-id="d424f-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**\_網際網路 \_ 失敗 \_ DUETOSECURITYCHECK 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-232">12171</span><span class="sxs-lookup"><span data-stu-id="d424f-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="d424f-233">因為有安全性檢查，所以函數失敗。</span><span class="sxs-lookup"><span data-stu-id="d424f-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**\_網際網路 \_ 強制 \_ 重試時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-235">12032</span><span class="sxs-lookup"><span data-stu-id="d424f-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="d424f-236">函數需要重做要求。</span><span class="sxs-lookup"><span data-stu-id="d424f-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**\_需要的網際網路 \_ FORTEZZA \_ 登 \_ 入錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-238">12054</span><span class="sxs-lookup"><span data-stu-id="d424f-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="d424f-239">要求的資源需要 Fortezza 驗證。</span><span class="sxs-lookup"><span data-stu-id="d424f-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**\_網際網路 \_ 控制碼 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-241">12036</span><span class="sxs-lookup"><span data-stu-id="d424f-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="d424f-242">要求失敗，因為控制碼已存在。</span><span class="sxs-lookup"><span data-stu-id="d424f-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**\_ \_ \_ \_ \_ REDIR 上的網際網路 HTTP 至 \_ HTTPS 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-244">12039</span><span class="sxs-lookup"><span data-stu-id="d424f-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="d424f-245">由於有重新導向，因此應用程式會從非 SSL 連線到 SSL 連線。</span><span class="sxs-lookup"><span data-stu-id="d424f-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**\_網際網路 \_ HTTPS \_ HTTP \_ 提交 \_ REDIR 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-247">12052</span><span class="sxs-lookup"><span data-stu-id="d424f-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="d424f-248">提交至 SSL 連線的資料會被重新導向至非 SSL 連線。</span><span class="sxs-lookup"><span data-stu-id="d424f-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**\_ \_ \_ \_ \_ REDIR 上的網際網路 HTTPS 與 \_ HTTP 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-250">12040</span><span class="sxs-lookup"><span data-stu-id="d424f-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="d424f-251">由於有重新導向，因此應用程式會從 SSL 移至非 SSL 連線。</span><span class="sxs-lookup"><span data-stu-id="d424f-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**\_網際網路 \_ 格式不正確 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-253">12027</span><span class="sxs-lookup"><span data-stu-id="d424f-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="d424f-254">要求的格式無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**錯誤的 \_ 網際網路錯誤 \_ \_ 處理 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d424f-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-256">12019</span><span class="sxs-lookup"><span data-stu-id="d424f-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="d424f-257">因為提供的控制碼不是正確的狀態，所以無法執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="d424f-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**\_網際網路 \_ 不正確的 \_ 控制碼 \_ 類型錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-259">12018</span><span class="sxs-lookup"><span data-stu-id="d424f-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="d424f-260">提供的控制碼類型對這項作業而言不正確。</span><span class="sxs-lookup"><span data-stu-id="d424f-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**錯誤的 \_ 網際網路錯誤 \_ \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="d424f-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-262">12014</span><span class="sxs-lookup"><span data-stu-id="d424f-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="d424f-263">無法完成連接和登入 FTP 伺服器的要求，因為提供的密碼不正確。</span><span class="sxs-lookup"><span data-stu-id="d424f-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**錯誤 \_ 網際網路 \_ 不正確的 \_ 使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="d424f-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-265">12013</span><span class="sxs-lookup"><span data-stu-id="d424f-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="d424f-266">無法完成連接和登入 FTP 伺服器的要求，因為提供的使用者名稱不正確。</span><span class="sxs-lookup"><span data-stu-id="d424f-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**\_網際網路 \_ 插入 \_ CDROM 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-268">12053</span><span class="sxs-lookup"><span data-stu-id="d424f-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="d424f-269">要求需要將 CD-ROM 插入 cd-rom 光碟機，以找出所要求的資源。</span><span class="sxs-lookup"><span data-stu-id="d424f-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-270">Windows Vista 和 Windows Server 2008 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**\_網際網路 \_ 內部 \_ 錯誤時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-272">12004</span><span class="sxs-lookup"><span data-stu-id="d424f-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="d424f-273">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**\_網際網路 \_ 不正確 \_ CA 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-275">12045</span><span class="sxs-lookup"><span data-stu-id="d424f-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="d424f-276">此函數不熟悉產生伺服器憑證的憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="d424f-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**\_網際網路 \_ 無效 \_ 操作時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-278">12016</span><span class="sxs-lookup"><span data-stu-id="d424f-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="d424f-279">要求的作業無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**\_網際網路 \_ 無效 \_ 選項時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-281">12009</span><span class="sxs-lookup"><span data-stu-id="d424f-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="d424f-282">要求 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 或 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 指定了不正確選項值。</span><span class="sxs-lookup"><span data-stu-id="d424f-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**\_網際網路 \_ 不正確 \_ PROXY \_ 要求時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-284">12033</span><span class="sxs-lookup"><span data-stu-id="d424f-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="d424f-285">對 proxy 的要求無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**\_網際網路 \_ 不正確 \_ URL 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-287">12005</span><span class="sxs-lookup"><span data-stu-id="d424f-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="d424f-288">URL 無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**\_ \_ \_ 找不到網際網路 \_ 專案錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-290">12028</span><span class="sxs-lookup"><span data-stu-id="d424f-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="d424f-291">找不到要求的專案。</span><span class="sxs-lookup"><span data-stu-id="d424f-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**\_網際網路 \_ 登入 \_ 失敗時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-293">12015</span><span class="sxs-lookup"><span data-stu-id="d424f-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="d424f-294">連接和登入 FTP 伺服器的要求失敗。</span><span class="sxs-lookup"><span data-stu-id="d424f-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**\_網際網路 \_ 登入 \_ 失敗 \_ 顯示 \_ 實體 \_ 主體時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-296">12174</span><span class="sxs-lookup"><span data-stu-id="d424f-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="d424f-297">已從網站傳回 MS-Logoff 摘要標頭。</span><span class="sxs-lookup"><span data-stu-id="d424f-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="d424f-298">此標頭會明確指示摘要套件清除相關領域的認證。</span><span class="sxs-lookup"><span data-stu-id="d424f-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="d424f-299">只有在已設定 [網際網路 \_ 錯誤 \_ 遮罩 \_ 登入 \_ 失敗 \_ 顯示 \_ 實體 \_](option-flags.md) 內容選項時，才會傳回此錯誤; 否則會傳回 **錯誤 \_ 網際網路登入 \_ \_ 失敗** 。</span><span class="sxs-lookup"><span data-stu-id="d424f-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**\_網際網路 \_ 混合 \_ 安全性錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-301">12041</span><span class="sxs-lookup"><span data-stu-id="d424f-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="d424f-302">內容並不完全安全。</span><span class="sxs-lookup"><span data-stu-id="d424f-302">The content is not entirely secure.</span></span> <span data-ttu-id="d424f-303">某些正在觀看的內容可能來自不安全的伺服器。</span><span class="sxs-lookup"><span data-stu-id="d424f-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**錯誤 \_ 網際網路 \_ 名稱 \_ 未 \_ 解決**</span><span class="sxs-lookup"><span data-stu-id="d424f-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-305">12007</span><span class="sxs-lookup"><span data-stu-id="d424f-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="d424f-306">無法解析伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d424f-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**\_網際網路 \_ 需要 \_ MSN \_ SSPI \_ PKG 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-308">12173</span><span class="sxs-lookup"><span data-stu-id="d424f-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="d424f-309">目前未實作。</span><span class="sxs-lookup"><span data-stu-id="d424f-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**\_網際網路 \_ 需要 \_ UI 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-311">12034</span><span class="sxs-lookup"><span data-stu-id="d424f-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="d424f-312">已要求使用者介面或其他封鎖作業。</span><span class="sxs-lookup"><span data-stu-id="d424f-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="d424f-313">Windows Vista 和 Windows Server 2008 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="d424f-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**錯誤 \_ 網際網路 \_ 沒有 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="d424f-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-315">12025</span><span class="sxs-lookup"><span data-stu-id="d424f-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="d424f-316">因為尚未設定回呼函式，所以無法進行非同步要求。</span><span class="sxs-lookup"><span data-stu-id="d424f-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**錯誤 \_ 網際網路 \_ 沒有 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="d424f-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-318">12024</span><span class="sxs-lookup"><span data-stu-id="d424f-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="d424f-319">因為提供了零內容值，所以無法進行非同步要求。</span><span class="sxs-lookup"><span data-stu-id="d424f-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**錯誤 \_ 網際網路 \_ 沒有 \_ 直接 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="d424f-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-321">12023</span><span class="sxs-lookup"><span data-stu-id="d424f-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="d424f-322">目前無法進行直接網路存取。</span><span class="sxs-lookup"><span data-stu-id="d424f-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**\_ \_ 未初始化網際網路 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-324">12172</span><span class="sxs-lookup"><span data-stu-id="d424f-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="d424f-325">尚未初始化 WinINet API。</span><span class="sxs-lookup"><span data-stu-id="d424f-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="d424f-326">指出尚未呼叫較高層級的函式，例如 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)。</span><span class="sxs-lookup"><span data-stu-id="d424f-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**\_網際網路 \_ 不是 \_ PROXY \_ 要求時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-328">12020</span><span class="sxs-lookup"><span data-stu-id="d424f-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="d424f-329">無法透過 proxy 提出要求。</span><span class="sxs-lookup"><span data-stu-id="d424f-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**錯誤 \_ 網際網路 \_ 操作已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="d424f-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-331">12017</span><span class="sxs-lookup"><span data-stu-id="d424f-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="d424f-332">作業已取消，通常是因為要求操作的控制碼已在作業完成之前關閉。</span><span class="sxs-lookup"><span data-stu-id="d424f-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**\_ \_ \_ 無法設定錯誤網際網路 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="d424f-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-334">12011</span><span class="sxs-lookup"><span data-stu-id="d424f-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="d424f-335">無法設定所要求的選項，只能進行查詢。</span><span class="sxs-lookup"><span data-stu-id="d424f-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**\_網際網路 \_ \_ 的 \_ 控制碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-337">12001</span><span class="sxs-lookup"><span data-stu-id="d424f-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="d424f-338">目前無法產生更多的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d424f-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**錯誤 \_ 網際網路 \_ POST \_ 為 \_ 非 \_ 安全的**</span><span class="sxs-lookup"><span data-stu-id="d424f-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-340">12043</span><span class="sxs-lookup"><span data-stu-id="d424f-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="d424f-341">應用程式正在將資料張貼至不安全的伺服器。</span><span class="sxs-lookup"><span data-stu-id="d424f-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**\_ \_ \_ 找不到網際網路通訊協定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-343">12008</span><span class="sxs-lookup"><span data-stu-id="d424f-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="d424f-344">找不到要求的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d424f-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**\_無法連線到網際網路 \_ PROXY \_ 伺服器 \_ 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-346">12165</span><span class="sxs-lookup"><span data-stu-id="d424f-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="d424f-347">無法連線到指定的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d424f-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**錯誤 \_ 網際網路重新 \_ 導向 \_ 配置 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="d424f-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-349">12048</span><span class="sxs-lookup"><span data-stu-id="d424f-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="d424f-350">函數無法處理重新導向，因為配置 (例如，將 HTTP 變更為 FTP) 。</span><span class="sxs-lookup"><span data-stu-id="d424f-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**\_ \_ \_ \_ \_ 找不到網際網路登錄值錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-352">12021</span><span class="sxs-lookup"><span data-stu-id="d424f-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="d424f-353">找不到必要的登錄值。</span><span class="sxs-lookup"><span data-stu-id="d424f-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**\_網際網路 \_ 要求 \_ 暫止時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-355">12026</span><span class="sxs-lookup"><span data-stu-id="d424f-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="d424f-356">因為有一或多個要求暫止，所以無法完成所需的作業。</span><span class="sxs-lookup"><span data-stu-id="d424f-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_網際網路 \_ 重試 \_ 對話方塊時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-358">12050</span><span class="sxs-lookup"><span data-stu-id="d424f-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="d424f-359">對話方塊應該會重試。</span><span class="sxs-lookup"><span data-stu-id="d424f-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**\_INTERNET \_ SEC \_ CERT \_ CN \_ 不正確錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-361">12038</span><span class="sxs-lookup"><span data-stu-id="d424f-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="d424f-362">SSL 憑證一般名稱 (主控制項名稱欄位) 不正確，例如，如果您輸入 www.server.com，而憑證上的一般名稱顯示為 www.different.com。</span><span class="sxs-lookup"><span data-stu-id="d424f-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**錯誤 \_ 網際網路 \_ SEC \_ 憑證 \_ 日期 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="d424f-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-364">12037</span><span class="sxs-lookup"><span data-stu-id="d424f-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="d424f-365">從伺服器收到的 SSL 憑證日期不正確。</span><span class="sxs-lookup"><span data-stu-id="d424f-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="d424f-366">憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="d424f-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_INTERNET \_ SEC \_ CERT \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-368">12055</span><span class="sxs-lookup"><span data-stu-id="d424f-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="d424f-369">SSL 憑證包含錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**錯誤 \_ 網際網路 \_ SEC \_ CERT \_ 沒有 \_ REV**</span><span class="sxs-lookup"><span data-stu-id="d424f-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-371">12056</span><span class="sxs-lookup"><span data-stu-id="d424f-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="d424f-372">SSL 憑證未撤銷。</span><span class="sxs-lookup"><span data-stu-id="d424f-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**\_INTERNET \_ SEC \_ CERT \_ REV \_ 失敗的錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-374">12057</span><span class="sxs-lookup"><span data-stu-id="d424f-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="d424f-375">撤銷 SSL 憑證失敗。</span><span class="sxs-lookup"><span data-stu-id="d424f-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**\_INTERNET \_ SEC CERT \_ 已 \_ 撤銷的錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-377">12170</span><span class="sxs-lookup"><span data-stu-id="d424f-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="d424f-378">SSL 憑證已撤銷。</span><span class="sxs-lookup"><span data-stu-id="d424f-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**錯誤 \_ 網際網路 \_ SEC \_ 無效 \_ 的憑證**</span><span class="sxs-lookup"><span data-stu-id="d424f-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-380">12169</span><span class="sxs-lookup"><span data-stu-id="d424f-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="d424f-381">SSL 憑證無效。</span><span class="sxs-lookup"><span data-stu-id="d424f-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**錯誤 \_ 網際網路 \_ 安全性 \_ 通道 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-383">12157</span><span class="sxs-lookup"><span data-stu-id="d424f-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="d424f-384">應用程式在載入 SSL 程式庫時遇到內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="d424f-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**\_網際網路 \_ 伺服器 \_ 無法連線時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-386">12164</span><span class="sxs-lookup"><span data-stu-id="d424f-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="d424f-387">指定的網站或伺服器無法連線。</span><span class="sxs-lookup"><span data-stu-id="d424f-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**\_網際網路 \_ 關機時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-389">12012</span><span class="sxs-lookup"><span data-stu-id="d424f-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="d424f-390">WinINet 支援即將關閉或卸載。</span><span class="sxs-lookup"><span data-stu-id="d424f-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**\_ \_ \_ 未安裝網際網路 TCPIP \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-392">12159</span><span class="sxs-lookup"><span data-stu-id="d424f-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="d424f-393">未載入所需的通訊協定堆疊，且應用程式無法啟動 WinSock。</span><span class="sxs-lookup"><span data-stu-id="d424f-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**錯誤 \_ 網際網路 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="d424f-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-395">12002</span><span class="sxs-lookup"><span data-stu-id="d424f-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="d424f-396">要求已逾時。</span><span class="sxs-lookup"><span data-stu-id="d424f-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**\_網際網路 \_ 無法 \_ \_ 緩存 \_ 檔時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-398">12158</span><span class="sxs-lookup"><span data-stu-id="d424f-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="d424f-399">函數無法快取該檔案。</span><span class="sxs-lookup"><span data-stu-id="d424f-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**\_網際網路 \_ 無法 \_ \_ 下載 \_ 腳本時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-401">12167</span><span class="sxs-lookup"><span data-stu-id="d424f-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="d424f-402">無法下載自動 proxy 設定腳本。</span><span class="sxs-lookup"><span data-stu-id="d424f-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="d424f-403">網際網路 \_ 旗標 \_ 必須設定快取 \_ \_ 要求旗標。</span><span class="sxs-lookup"><span data-stu-id="d424f-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**\_網際網路 \_ 無法辨識的 \_ 配置時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d424f-405">12006</span><span class="sxs-lookup"><span data-stu-id="d424f-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="d424f-406">無法辨識或不支援 URL 配置。</span><span class="sxs-lookup"><span data-stu-id="d424f-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**錯誤 \_ 不正確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="d424f-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d424f-408">傳遞至 API 的控制碼已無效或已關閉。</span><span class="sxs-lookup"><span data-stu-id="d424f-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="d424f-409">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="d424f-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**錯誤 \_ 的 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="d424f-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d424f-411">有更多可用的資料。</span><span class="sxs-lookup"><span data-stu-id="d424f-411">More data is available.</span></span>

<span data-ttu-id="d424f-412">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="d424f-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**錯誤 \_ 的 \_ 檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="d424f-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d424f-414">找不到其他檔案。</span><span class="sxs-lookup"><span data-stu-id="d424f-414">No more files have been found.</span></span>

<span data-ttu-id="d424f-415">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="d424f-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d424f-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_沒有 \_ 其他 \_ 專案的錯誤**</span><span class="sxs-lookup"><span data-stu-id="d424f-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d424f-417">找不到更多專案。</span><span class="sxs-lookup"><span data-stu-id="d424f-417">No more items have been found.</span></span>

<span data-ttu-id="d424f-418">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="d424f-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d424f-419">備註</span><span class="sxs-lookup"><span data-stu-id="d424f-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d424f-420">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="d424f-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="d424f-421">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="d424f-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="d424f-422">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="d424f-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d424f-423">規格需求</span><span class="sxs-lookup"><span data-stu-id="d424f-423">Requirements</span></span>



| <span data-ttu-id="d424f-424">需求</span><span class="sxs-lookup"><span data-stu-id="d424f-424">Requirement</span></span> | <span data-ttu-id="d424f-425">值</span><span class="sxs-lookup"><span data-stu-id="d424f-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d424f-426">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d424f-426">Minimum supported client</span></span><br/> | <span data-ttu-id="d424f-427">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d424f-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d424f-428">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d424f-428">Minimum supported server</span></span><br/> | <span data-ttu-id="d424f-429">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d424f-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d424f-430">標頭</span><span class="sxs-lookup"><span data-stu-id="d424f-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="d424f-431"><dt>Wininet</dt></span><span class="sxs-lookup"><span data-stu-id="d424f-431"><dt>Wininet.h</dt></span></span> </dl> |



 

