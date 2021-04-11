---
description: 當其中一個 Microsoft Windows HTTP 服務 (WinHTTP) 函式失敗時，此主題中所識別的錯誤值會由 GetLastError 傳回。
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: " (WinHTTP. h) 的錯誤訊息"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850116"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="541e7-103"> (WinHTTP. h) 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="541e7-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="541e7-104">當其中一個 Microsoft Windows HTTP 服務 (WinHTTP) 函式失敗時， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回下列錯誤值，且在 [**HRESULT**](../com/structure-of-com-error-codes.md) 錯誤的較低16位中也會傳回 [**WinHttpRequest**](winhttprequest.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="541e7-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="541e7-105">名稱開頭為 "ERROR \_ WINHTTP \_ " 的錯誤值是 WINHTTP 函式特有的。</span><span class="sxs-lookup"><span data-stu-id="541e7-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="541e7-106">在適當的情況下，WinHTTP 函數也會傳回 Windows 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="541e7-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="541e7-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**錯誤 \_ WINHTTP \_ 自動 \_ PROXY \_ 服務 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-108">12178</span><span class="sxs-lookup"><span data-stu-id="541e7-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="541e7-109">當找不到指定 URL 的 proxy 時， [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) 會傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**錯誤 \_ WINHTTP 自動偵測 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="541e7-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-111">12180</span><span class="sxs-lookup"><span data-stu-id="541e7-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="541e7-112">如果 WinHTTP 無法探索 Proxy 自動設定 (PAC) 檔的 URL，則會傳回 [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**錯誤 \_ WINHTTP 錯誤的 \_ \_ 自動 \_ PROXY \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="541e7-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-114">12166</span><span class="sxs-lookup"><span data-stu-id="541e7-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="541e7-115">在 Proxy 自動設定 (PAC) 檔中執行腳本時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**\_ \_ \_ \_ 在開啟之後，WINHTTP 無法呼叫錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-117">12103</span><span class="sxs-lookup"><span data-stu-id="541e7-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="541e7-118">如果在呼叫 [**Open**](iwinhttprequest-open.md)方法之後無法要求指定的選項， [**HttpRequest**](winhttprequest.md)物件會傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 在傳送後呼叫 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-120">12102</span><span class="sxs-lookup"><span data-stu-id="541e7-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="541e7-121">如果在呼叫 [**Send**](iwinhttprequest-send.md)方法之後無法執行要求的作業， [**HttpRequest**](winhttprequest.md)物件會傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 在開啟之前呼叫 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-123">12100</span><span class="sxs-lookup"><span data-stu-id="541e7-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="541e7-124">如果在呼叫 [**Open**](iwinhttprequest-open.md)方法之前無法執行要求的作業， [**HttpRequest**](winhttprequest.md)物件會傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 在傳送前呼叫 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-126">12101</span><span class="sxs-lookup"><span data-stu-id="541e7-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="541e7-127">如果在呼叫 [**傳送**](iwinhttprequest-send.md)方法之前無法執行要求的作業，則由 [**HttpRequest**](winhttprequest.md)物件傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**錯誤 \_ WINHTTP \_ 無法 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="541e7-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-129">12029</span><span class="sxs-lookup"><span data-stu-id="541e7-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="541e7-130">如果與伺服器的連接失敗，則傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**\_需要 WINHTTP \_ 客戶 \_ 端 \_ 驗證 \_ 憑證錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-132">伺服器需要 SSL 用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="541e7-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="541e7-133">應用程式會使用 **WINHTTP \_ 選項 [ \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單**] 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ，以抓取憑證簽發者的清單。</span><span class="sxs-lookup"><span data-stu-id="541e7-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="541e7-134">如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。</span><span class="sxs-lookup"><span data-stu-id="541e7-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="541e7-135">如果伺服器要求用戶端憑證，但不需要它，應用程式可以使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容** 選項來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="541e7-136">在此情況下，應用程式會 \_ \_ \_ \_ 在 **WinHttpSetOption** 的 *lpBuffer* 參數中指定 WINHTTP NO CLIENT CERT CONTEXT 宏。</span><span class="sxs-lookup"><span data-stu-id="541e7-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="541e7-137">如需詳細資訊，請參閱 **WINHTTP \_ option \_ CLIENT \_ CERT \_ CONTEXT** 選項。</span><span class="sxs-lookup"><span data-stu-id="541e7-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="541e7-138">**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**錯誤 \_ WINHTTP \_ 用戶端憑證 \_ \_ 無 \_ 存取 \_ 私密金鑰 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-140">應用程式沒有存取與用戶端憑證相關聯之私密金鑰的必要許可權。</span><span class="sxs-lookup"><span data-stu-id="541e7-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="541e7-141">**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**錯誤 \_ WINHTTP \_ 用戶端憑證 \_ \_ 沒有 \_ 私密金鑰 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-143">SSL 用戶端憑證的內容沒有相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="541e7-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="541e7-144">用戶端憑證可能已匯入沒有私密金鑰的電腦。</span><span class="sxs-lookup"><span data-stu-id="541e7-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="541e7-145">**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**錯誤 \_ WINHTTP \_ 區塊 \_ 編碼 \_ 標頭 \_ 大小 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="541e7-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-147">12183</span><span class="sxs-lookup"><span data-stu-id="541e7-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="541e7-148">當剖析區塊編碼過程中發生溢位狀況時，由 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**\_需要 WINHTTP \_ 客戶 \_ 端 \_ 驗證 \_ 憑證錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-150">12044</span><span class="sxs-lookup"><span data-stu-id="541e7-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="541e7-151">當伺服器要求用戶端驗證時， [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 會傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="541e7-152">**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 不支援此錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**發生錯誤 \_ WINHTTP \_ 連接 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-154">12030</span><span class="sxs-lookup"><span data-stu-id="541e7-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="541e7-155">與伺服器的連接已重設或終止，或遇到不相容的 SSL 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="541e7-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="541e7-156">例如，除非用戶端明確啟用，否則 WinHTTP 5.1 版不支援 SSL2。</span><span class="sxs-lookup"><span data-stu-id="541e7-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**錯誤 \_ WINHTTP \_ 標頭 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="541e7-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-158">12155</span><span class="sxs-lookup"><span data-stu-id="541e7-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="541e7-159">目前不再使用。</span><span class="sxs-lookup"><span data-stu-id="541e7-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**超過錯誤的 \_ WINHTTP \_ 標頭 \_ 計數 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-161">12181</span><span class="sxs-lookup"><span data-stu-id="541e7-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="541e7-162">當回應中出現的標頭數目超過 WinHTTP 可能接收的標頭數目時， [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 會傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**\_ \_ \_ \_ 找不到錯誤的 WINHTTP 標頭**</span><span class="sxs-lookup"><span data-stu-id="541e7-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-164">12150</span><span class="sxs-lookup"><span data-stu-id="541e7-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="541e7-165">找不到要求的標頭。</span><span class="sxs-lookup"><span data-stu-id="541e7-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**錯誤 \_ WINHTTP \_ 標頭 \_ 大小 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="541e7-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-167">12182</span><span class="sxs-lookup"><span data-stu-id="541e7-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="541e7-168">當收到的標頭大小超過要求控制碼的限制時，由 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**錯誤 \_ WINHTTP 錯誤的 \_ \_ 處理 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="541e7-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-170">12019</span><span class="sxs-lookup"><span data-stu-id="541e7-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="541e7-171">因為提供的控制碼不是正確的狀態，所以無法執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="541e7-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**錯誤 \_ WINHTTP 錯誤的 \_ \_ 控制碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="541e7-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-173">12018</span><span class="sxs-lookup"><span data-stu-id="541e7-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="541e7-174">提供的控制碼類型對這項作業而言不正確。</span><span class="sxs-lookup"><span data-stu-id="541e7-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**錯誤 \_ WINHTTP \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-176">12004</span><span class="sxs-lookup"><span data-stu-id="541e7-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="541e7-177">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**錯誤 \_ WINHTTP \_ 無效 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="541e7-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-179">12009</span><span class="sxs-lookup"><span data-stu-id="541e7-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="541e7-180">要求 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 指定了不正確選項值。</span><span class="sxs-lookup"><span data-stu-id="541e7-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**錯誤 \_ WINHTTP \_ 不正確 \_ 查詢 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="541e7-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-182">12154</span><span class="sxs-lookup"><span data-stu-id="541e7-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="541e7-183">目前不再使用。</span><span class="sxs-lookup"><span data-stu-id="541e7-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**錯誤 \_ WINHTTP \_ 不正確 \_ 伺服器 \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="541e7-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-185">12152</span><span class="sxs-lookup"><span data-stu-id="541e7-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="541e7-186">無法剖析伺服器回應。</span><span class="sxs-lookup"><span data-stu-id="541e7-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**錯誤 \_ WINHTTP \_ 不正確 \_ URL**</span><span class="sxs-lookup"><span data-stu-id="541e7-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-188">12005</span><span class="sxs-lookup"><span data-stu-id="541e7-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="541e7-189">URL 無效。</span><span class="sxs-lookup"><span data-stu-id="541e7-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**錯誤 \_ WINHTTP \_ 登入 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="541e7-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-191">12015</span><span class="sxs-lookup"><span data-stu-id="541e7-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="541e7-192">登入嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="541e7-192">The login attempt failed.</span></span> <span data-ttu-id="541e7-193">當遇到此錯誤時，應使用 [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)來關閉要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="541e7-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="541e7-194">必須先建立新的要求控制碼，才能重試原本產生此錯誤的函式。</span><span class="sxs-lookup"><span data-stu-id="541e7-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**錯誤 \_ WINHTTP \_ 名稱 \_ 未 \_ 解決**</span><span class="sxs-lookup"><span data-stu-id="541e7-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-196">12007</span><span class="sxs-lookup"><span data-stu-id="541e7-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="541e7-197">無法解析伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="541e7-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**錯誤 \_ WINHTTP \_ 未 \_ 初始化**</span><span class="sxs-lookup"><span data-stu-id="541e7-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-199">12172</span><span class="sxs-lookup"><span data-stu-id="541e7-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="541e7-200">目前不再使用。</span><span class="sxs-lookup"><span data-stu-id="541e7-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**\_WINHTTP \_ 操作已 \_ 取消時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-202">12017</span><span class="sxs-lookup"><span data-stu-id="541e7-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="541e7-203">作業已取消，通常是因為要求操作的控制碼已在作業完成之前關閉。</span><span class="sxs-lookup"><span data-stu-id="541e7-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**\_ \_ \_ 無法設定錯誤 WINHTTP \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="541e7-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-205">12011</span><span class="sxs-lookup"><span data-stu-id="541e7-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="541e7-206">無法設定所要求的選項，只能進行查詢。</span><span class="sxs-lookup"><span data-stu-id="541e7-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**\_WINHTTP \_ 超出 \_ \_ 控制碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-208">12001</span><span class="sxs-lookup"><span data-stu-id="541e7-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="541e7-209">目前不再使用。</span><span class="sxs-lookup"><span data-stu-id="541e7-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**錯誤 \_ WINHTTP 重新 \_ 導向 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="541e7-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-211">12156</span><span class="sxs-lookup"><span data-stu-id="541e7-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="541e7-212">重新導向失敗，因為配置變更或嘗試重新導向失敗 (預設為五次嘗試) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**\_WINHTTP \_ 重新傳送 \_ 要求時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-214">12032</span><span class="sxs-lookup"><span data-stu-id="541e7-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="541e7-215">WinHTTP 函數失敗。</span><span class="sxs-lookup"><span data-stu-id="541e7-215">The WinHTTP function failed.</span></span> <span data-ttu-id="541e7-216">您可以在相同的要求控制碼上重試所需的函數。</span><span class="sxs-lookup"><span data-stu-id="541e7-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**錯誤 \_ WINHTTP \_ 回應 \_ 清空 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="541e7-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-218">12184</span><span class="sxs-lookup"><span data-stu-id="541e7-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="541e7-219">當傳入回應超過內部 WinHTTP 大小限制時傳回。</span><span class="sxs-lookup"><span data-stu-id="541e7-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**錯誤 \_ WINHTTP \_ 腳本 \_ 執行 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-221">12177</span><span class="sxs-lookup"><span data-stu-id="541e7-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="541e7-222">執行腳本時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**錯誤 \_ WINHTTP \_ 安全 \_ CERT \_ CN \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="541e7-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-224">12038</span><span class="sxs-lookup"><span data-stu-id="541e7-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="541e7-225">當憑證 CN 名稱不符合傳遞的值時傳回 (相當於 **CERT \_ E \_ CN \_ NO \_ match** error) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 憑證 \_ 日期 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="541e7-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-227">12037</span><span class="sxs-lookup"><span data-stu-id="541e7-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="541e7-228">指出當確認憑證中的目前系統時鐘或時間戳記時，所需的憑證不在有效期間內，或是憑證鏈的有效期間未正確地 (等於 **cert \_ e 已 \_ 過期** 或 **cert \_ e \_ VALIDITYPERIODNESTING** 錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**錯誤 \_ WINHTTP \_ 安全 \_ CERT \_ REV \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="541e7-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-230">12057</span><span class="sxs-lookup"><span data-stu-id="541e7-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="541e7-231">表示無法檢查撤銷，因為撤銷伺服器已離線 (相當於 **\_ \_ \_ 離線 CRYPT E 撤銷**) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**錯誤 \_ WINHTTP \_ 安全憑證已 \_ \_ 撤銷**</span><span class="sxs-lookup"><span data-stu-id="541e7-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-233">12170</span><span class="sxs-lookup"><span data-stu-id="541e7-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="541e7-234">表示已撤銷憑證 (相當於 **CRYPT \_ E \_ 撤銷** 的) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 憑證 \_ 錯誤的 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="541e7-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-236">12179</span><span class="sxs-lookup"><span data-stu-id="541e7-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="541e7-237">指出憑證對要求的使用方式無效 (等同于 **CERT \_ E \_ 錯誤的 \_ 使用** 方式) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 通道 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-239">12157</span><span class="sxs-lookup"><span data-stu-id="541e7-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="541e7-240">指出與安全通道有關的錯誤 (與以 "SEC \_ E \_ " 和 "sec I" 開頭的錯誤碼相同 \_ \_) 的 "winerror.h .h" 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="541e7-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="541e7-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-242">12175</span><span class="sxs-lookup"><span data-stu-id="541e7-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="541e7-243">伺服器傳送的安全通訊端層 (SSL) 憑證中找到一或多個錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="541e7-244">若要判斷所遇到的錯誤類型，請檢查狀態回呼函式中的 [**WINHTTP \_ 回呼 \_ 狀態 \_ 安全 \_ 失敗**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 通知。</span><span class="sxs-lookup"><span data-stu-id="541e7-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="541e7-245">如需詳細資訊，請參閱 [**WINHTTP \_ 狀態 \_ 回呼**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)。</span><span class="sxs-lookup"><span data-stu-id="541e7-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 不正確 \_ CA**</span><span class="sxs-lookup"><span data-stu-id="541e7-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-247">12045</span><span class="sxs-lookup"><span data-stu-id="541e7-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="541e7-248">指出已處理憑證鏈，但在信任提供者不信任的根憑證中終止 (等同于 **CERT \_ E \_ UNTRUSTEDROOT**) 。</span><span class="sxs-lookup"><span data-stu-id="541e7-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**錯誤 \_ WINHTTP \_ 安全 \_ 無效 \_ 的憑證**</span><span class="sxs-lookup"><span data-stu-id="541e7-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-250">12169</span><span class="sxs-lookup"><span data-stu-id="541e7-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="541e7-251">指出憑證無效 (等同于 **cert \_ e \_ 角色**、 **cert \_ e \_ PATHLENCONST**、 **cert \_ e \_ CRITICAL**、 **Cert \_ e \_ 用途**、 **cert \_ e \_ ISSUERCHAINING**、 **cert \_ e \_ 格式錯誤** 和 **cert \_ e \_ 鏈**) 等錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**\_WINHTTP \_ 關機錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-253">12012</span><span class="sxs-lookup"><span data-stu-id="541e7-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="541e7-254">正在關閉或卸載 WinHTTP 函數支援。</span><span class="sxs-lookup"><span data-stu-id="541e7-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**錯誤 \_ WINHTTP \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="541e7-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-256">12002</span><span class="sxs-lookup"><span data-stu-id="541e7-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="541e7-257">要求已逾時。</span><span class="sxs-lookup"><span data-stu-id="541e7-257">The request has timed out.</span></span>

<span data-ttu-id="541e7-258">無論在 Windows HTTP 服務中設定的超時值為何，都可能會因為 TCP/IP 超時行為而傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="541e7-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**錯誤 \_ WINHTTP \_ 無法 \_ \_ 下載 \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="541e7-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-260">12167</span><span class="sxs-lookup"><span data-stu-id="541e7-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="541e7-261">無法下載 PAC 檔案。</span><span class="sxs-lookup"><span data-stu-id="541e7-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="541e7-262">例如，PAC URL 所參考的伺服器可能無法連線，或伺服器傳回404找不到的回應。</span><span class="sxs-lookup"><span data-stu-id="541e7-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**錯誤 \_ WINHTTP \_ 未處理的 \_ 腳本 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="541e7-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-264">12176</span><span class="sxs-lookup"><span data-stu-id="541e7-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="541e7-265">不支援腳本類型。</span><span class="sxs-lookup"><span data-stu-id="541e7-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**錯誤 \_ WINHTTP \_ 無法辨識的 \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="541e7-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="541e7-267">12006</span><span class="sxs-lookup"><span data-stu-id="541e7-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="541e7-268">URL 指定了 "HTTP：" 或 "HTTPs：" 以外的配置。</span><span class="sxs-lookup"><span data-stu-id="541e7-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="541e7-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-270">可用的記憶體不足，無法完成要求的操作。</span><span class="sxs-lookup"><span data-stu-id="541e7-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="541e7-271">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="541e7-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**\_緩衝區不足的錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-273">提供給函數的緩衝區大小（以位元組為單位）不足以包含傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="541e7-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="541e7-274">如需詳細資訊，請參閱特定功能。</span><span class="sxs-lookup"><span data-stu-id="541e7-274">For more information, see the specific function.</span></span>

<span data-ttu-id="541e7-275">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="541e7-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**錯誤 \_ 不正確 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="541e7-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-277">傳遞至應用程式設計介面 (API) 的控制碼已失效或已關閉。</span><span class="sxs-lookup"><span data-stu-id="541e7-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="541e7-278">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="541e7-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**錯誤 \_ 的 \_ 檔案 \_**</span><span class="sxs-lookup"><span data-stu-id="541e7-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-280">找不到其他檔案。</span><span class="sxs-lookup"><span data-stu-id="541e7-280">No more files have been found.</span></span>

<span data-ttu-id="541e7-281">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="541e7-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_沒有 \_ 其他 \_ 專案的錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-283">找不到更多專案。</span><span class="sxs-lookup"><span data-stu-id="541e7-283">No more items have been found.</span></span>

<span data-ttu-id="541e7-284">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="541e7-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="541e7-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**\_不 \_ 支援的錯誤**</span><span class="sxs-lookup"><span data-stu-id="541e7-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="541e7-286">未載入所需的通訊協定堆疊，且應用程式無法啟動 WinSock。</span><span class="sxs-lookup"><span data-stu-id="541e7-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="541e7-287">**標頭：** 在 Winerror.h 中宣告</span><span class="sxs-lookup"><span data-stu-id="541e7-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="541e7-288">備註</span><span class="sxs-lookup"><span data-stu-id="541e7-288">Remarks</span></span>

<span data-ttu-id="541e7-289">針對 Windows XP 和 Windows 2000，請參閱 WinHttp 起始頁的 [執行時間需求](winhttp-start-page.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="541e7-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="541e7-290">規格需求</span><span class="sxs-lookup"><span data-stu-id="541e7-290">Requirements</span></span>



| <span data-ttu-id="541e7-291">需求</span><span class="sxs-lookup"><span data-stu-id="541e7-291">Requirement</span></span> | <span data-ttu-id="541e7-292">值</span><span class="sxs-lookup"><span data-stu-id="541e7-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="541e7-293">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="541e7-293">Minimum supported client</span></span><br/> | <span data-ttu-id="541e7-294">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="541e7-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="541e7-295">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="541e7-295">Minimum supported server</span></span><br/> | <span data-ttu-id="541e7-296">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="541e7-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="541e7-297">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="541e7-297">Redistributable</span></span><br/>          | <span data-ttu-id="541e7-298">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="541e7-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="541e7-299">標頭</span><span class="sxs-lookup"><span data-stu-id="541e7-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="541e7-300"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="541e7-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="541e7-301">另請參閱</span><span class="sxs-lookup"><span data-stu-id="541e7-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541e7-302">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="541e7-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

