---
title: '選項旗標 (Wininet. h) '
description: 下列選項旗標會搭配 InternetQueryOption 和 InternetSetOption 函數使用。 所有有效的選項旗標都具有大於或等於 INTERNET \_ FIRST \_ 選項，且小於或等於 internet \_ LAST \_ 選項的值。
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106973307"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="e24b8-104">選項旗標 (Wininet. h) </span><span class="sxs-lookup"><span data-stu-id="e24b8-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="e24b8-105">下列選項旗標會搭配 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 函數使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="e24b8-106">所有有效的選項旗標都具有大於或等於 **internet \_ FIRST \_ 選項** ，且小於或等於 **internet \_ LAST \_ 選項** 的值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**網際網路 \_ 選項 \_ 改變身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="e24b8-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-108">80</span><span class="sxs-lookup"><span data-stu-id="e24b8-108">80</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-109">未實作</span><span class="sxs-lookup"><span data-stu-id="e24b8-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**網際網路 \_ 選項 \_ ASYNC**</span><span class="sxs-lookup"><span data-stu-id="e24b8-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-111">30</span><span class="sxs-lookup"><span data-stu-id="e24b8-111">30</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-112">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**網際網路 \_ 選項 \_ 非同步 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-114">15</span><span class="sxs-lookup"><span data-stu-id="e24b8-114">15</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-115">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**網際網路 \_ 選項 \_ 非同步 \_ 優先權**</span><span class="sxs-lookup"><span data-stu-id="e24b8-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-117">16</span><span class="sxs-lookup"><span data-stu-id="e24b8-117">16</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**網際網路 \_ 選項 \_ 略過 \_ 編輯 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="e24b8-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-120">64</span><span class="sxs-lookup"><span data-stu-id="e24b8-120">64</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-121">設定或取得布林值，這個值會決定系統是否應該檢查網路是否有較新的內容，並在找到較新的版本時覆寫編輯的快取專案。</span><span class="sxs-lookup"><span data-stu-id="e24b8-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="e24b8-122">如果設定為 **True**，系統會檢查網路是否有較新的內容，並以較新的版本覆寫已編輯的快取專案。</span><span class="sxs-lookup"><span data-stu-id="e24b8-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="e24b8-123">預設值為 **False**，表示應該在不檢查網路的情況下使用已編輯的快取專案。</span><span class="sxs-lookup"><span data-stu-id="e24b8-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="e24b8-124">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-125">只有在 Microsoft Internet Explorer 5 和更新版本中才有效。</span><span class="sxs-lookup"><span data-stu-id="e24b8-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**網際網路 \_ 選項快取 \_ \_ 資料流程 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-127">27</span><span class="sxs-lookup"><span data-stu-id="e24b8-127">27</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-128">不再支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**網際網路 \_ 選項快取 \_ \_ 時間戳記**</span><span class="sxs-lookup"><span data-stu-id="e24b8-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-130">69</span><span class="sxs-lookup"><span data-stu-id="e24b8-130">69</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-131">從網際網路快取中儲存的資源抓取包含 LastModified 時間和到期時間的網際網路快取 [**\_ \_ 時間戳記**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) 結構。</span><span class="sxs-lookup"><span data-stu-id="e24b8-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="e24b8-132">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**網際網路 \_ 選項 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-134">1</span><span class="sxs-lookup"><span data-stu-id="e24b8-134">1</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-135">設定或抓取為這個控制碼定義之回呼函式的位址。</span><span class="sxs-lookup"><span data-stu-id="e24b8-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="e24b8-136">此選項可用於所有 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="e24b8-137">由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**網際網路 \_ 選項 \_ 回呼 \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="e24b8-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-139">54</span><span class="sxs-lookup"><span data-stu-id="e24b8-139">54</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-140">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**網際網路 \_ 選項 \_ 用戶端憑證 \_ \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e24b8-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-142">84</span><span class="sxs-lookup"><span data-stu-id="e24b8-142">84</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-143">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="e24b8-144">*LpBuffer* 參數必須是憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)結構的指標，而不是憑證 **\_ 內容** 指標的指標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="e24b8-145">如果應用程式收到 **\_ \_ \_ \_ \_ 所需的網際網路用戶端驗證憑證錯誤**，則必須先呼叫 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) 或使用 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 來提供憑證，再重試要求。</span><span class="sxs-lookup"><span data-stu-id="e24b8-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="e24b8-146">接著會呼叫 [**CertDuplicateCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) ，讓應用程式可以獨立發行傳遞的憑證內容。</span><span class="sxs-lookup"><span data-stu-id="e24b8-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**網際網路 \_ 選項 \_ 字碼頁**</span><span class="sxs-lookup"><span data-stu-id="e24b8-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-148">68</span><span class="sxs-lookup"><span data-stu-id="e24b8-148">68</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-149">根據預設，Unicode URL 的主機或授權單位部分會根據 IDN 規格進行編碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="e24b8-150">在要求或連接控制碼上設定此選項時，若已停用 IDN，則會指定 URL 之主機部分的字碼頁編碼配置。</span><span class="sxs-lookup"><span data-stu-id="e24b8-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="e24b8-151">呼叫 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)的 *lpBuffer* 參數包含所需的 DBCS 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e24b8-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="e24b8-152">如果未在 *lpBuffer* 中指定字碼頁，WinINet 會使用預設的系統字碼頁 (CP \_ ACP) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="e24b8-153">注意：如果未停用 IDN，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="e24b8-154">如需有關如何停用 IDN 的詳細資訊，請參閱 **網際網路 \_ 選項 \_ IDN** 選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="e24b8-155">**WINDOWS XP （含 SP2）和 Windows Server 2003 （含 SP1）：** 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="e24b8-156">**版本：** 需要 Internet Explorer 7.0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**網際網路 \_ 選項 \_ 字碼頁 \_ 路徑**</span><span class="sxs-lookup"><span data-stu-id="e24b8-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-158">100</span><span class="sxs-lookup"><span data-stu-id="e24b8-158">100</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-159">根據預設，URL 的路徑部分為 UTF8 編碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="e24b8-160">WinINet API 會在高位字元上 (% ) 編碼執行 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="e24b8-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="e24b8-161">在要求或連接控制碼上設定這個選項會停用 UTF8 編碼，並設定特定的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e24b8-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="e24b8-162">呼叫 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)的 *lpBuffer* 參數包含路徑所需的 DBCS 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e24b8-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="e24b8-163">如果未在 *lpBuffer* 中指定字碼頁，WinINet 會使用預設的 CP \_ UTF8。</span><span class="sxs-lookup"><span data-stu-id="e24b8-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="e24b8-164">**WINDOWS XP （含 SP2）和 Windows Server 2003 （含 SP1）：** 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="e24b8-165">**版本：** 需要 Internet Explorer 7.0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**網際網路 \_ 選項 \_ 字碼頁 \_ 額外**</span><span class="sxs-lookup"><span data-stu-id="e24b8-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-167">101</span><span class="sxs-lookup"><span data-stu-id="e24b8-167">101</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-168">根據預設，URL 的路徑部分是預設的系統字碼頁 (CP \_ ACP) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="e24b8-169">在額外部分上，不會執行 escape 字元 (% ) 轉換。</span><span class="sxs-lookup"><span data-stu-id="e24b8-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="e24b8-170">在要求上設定此選項，或連接控制碼會停用 CP \_ ACP 編碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="e24b8-171">在 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)的呼叫中， *lpBuffer* 參數包含所需的 DBCS 字碼頁，供 URL 的額外部分之用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="e24b8-172">如果未在 *lpBuffer* 中指定字碼頁，WinINet 會使用預設的系統字碼頁 (CP \_ ACP) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="e24b8-173">**WINDOWS XP （含 SP2）和 Windows Server 2003 （含 SP1）：** 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="e24b8-174">**版本：** 需要 Internet Explorer 7.0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**網際網路 \_ 選項 \_ 壓縮 \_ 內容 \_ 長度**</span><span class="sxs-lookup"><span data-stu-id="e24b8-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-176">147</span><span class="sxs-lookup"><span data-stu-id="e24b8-176">147</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-177">針對 WinInet 將伺服器提供的內容編碼方式解壓縮的要求，會以 ULONGLONG 的形式抓取回應主體的伺服器報告內容長度。</span><span class="sxs-lookup"><span data-stu-id="e24b8-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="e24b8-178">在 Windows 10 1507 版和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**網際網路 \_ 選項 \_ 連接 \_ 輪詢**</span><span class="sxs-lookup"><span data-stu-id="e24b8-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-180">4</span><span class="sxs-lookup"><span data-stu-id="e24b8-180">4</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-181">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**網際網路 \_ 選項 \_ 連接 \_ 重試**</span><span class="sxs-lookup"><span data-stu-id="e24b8-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-183">3</span><span class="sxs-lookup"><span data-stu-id="e24b8-183">3</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-184">設定或抓取不帶正負號的長整數值，其中包含 WinINet 嘗試解析並連接至主機的次數。</span><span class="sxs-lookup"><span data-stu-id="e24b8-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="e24b8-185">每個 IP 位址只會嘗試一次。</span><span class="sxs-lookup"><span data-stu-id="e24b8-185">It only attempts once per IP address.</span></span> <span data-ttu-id="e24b8-186">例如，如果您嘗試連線到有10個 IP 位址的多路連接主機，而 [網際網路 \_ 選項 \_ 連接 \_ 重試] 設定為7，WinINet 只會嘗試解析並連接到前七個 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="e24b8-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="e24b8-187">相反地，如果有一組相同的十個 IP 位址，則當 \_ [網際網路選項 \_ 連接 \_ 重試] 設定為20時，WinINet 只會嘗試每10次。</span><span class="sxs-lookup"><span data-stu-id="e24b8-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="e24b8-188">如果主機只有一個 IP 位址，而第一次連線嘗試失敗，則沒有進一步的嘗試。</span><span class="sxs-lookup"><span data-stu-id="e24b8-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="e24b8-189">如果連接嘗試在指定的嘗試次數之後仍失敗，則會取消要求。</span><span class="sxs-lookup"><span data-stu-id="e24b8-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="e24b8-190">網際網路 \_ 選項 \_ 連接重試的預設值 \_ 為五次嘗試。</span><span class="sxs-lookup"><span data-stu-id="e24b8-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="e24b8-191">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，包括 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="e24b8-192">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**網際網路 \_ 選項 \_ 連接 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="e24b8-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-194">55</span><span class="sxs-lookup"><span data-stu-id="e24b8-194">55</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-195">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**網際網路 \_ 選項 \_ 連接 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-197">2</span><span class="sxs-lookup"><span data-stu-id="e24b8-197">2</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-198">設定或抓取不帶正負號的長整數值，其中包含用於網際網路連接要求的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e24b8-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="e24b8-199">將此選項設定為無限 (0xFFFFFFFF) 將會停用此計時器。</span><span class="sxs-lookup"><span data-stu-id="e24b8-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="e24b8-200">如果連接要求所花費的時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="e24b8-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="e24b8-201">當您嘗試連線到單一主機 (的多個 IP 位址時，) 多路連接主機，則所有 IP 位址的超時限制是累計的。</span><span class="sxs-lookup"><span data-stu-id="e24b8-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="e24b8-202">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，包括 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="e24b8-203">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**網際網路 \_ 選項 \_ 連接 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e24b8-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-205">50</span><span class="sxs-lookup"><span data-stu-id="e24b8-205">50</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-206">設定或抓取包含已連接狀態的不帶正負號長整數值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="e24b8-207">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**網際網路 \_ 選項 \_ 內容 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="e24b8-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-209">45</span><span class="sxs-lookup"><span data-stu-id="e24b8-209">45</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-210">設定或抓取 DWORD \_ 指標，其中包含與這個 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼相關聯的內容值位址。</span><span class="sxs-lookup"><span data-stu-id="e24b8-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="e24b8-211">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="e24b8-212">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-213">先前，這會將內容值設定為儲存在 **lpBuffer** 指標中的位址。</span><span class="sxs-lookup"><span data-stu-id="e24b8-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="e24b8-214">這已更正，因此會使用儲存在緩衝區中的值，且會為 [網際網路 \_ 選項 \_ 內容 \_ 值](/windows) 旗標指派新值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="e24b8-215">舊的值10是保留的，因此仍支援針對舊行為所撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e24b8-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**網際網路 \_ 選項 \_ 控制 \_ 接收 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-217">6</span><span class="sxs-lookup"><span data-stu-id="e24b8-217">6</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-218">與 [網際網路 \_ 選項 \_ 接收 \_ 超時](/windows)相同。</span><span class="sxs-lookup"><span data-stu-id="e24b8-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="e24b8-219">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**網際網路 \_ 選項 \_ 控制 \_ 傳送 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-221">5</span><span class="sxs-lookup"><span data-stu-id="e24b8-221">5</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-222">與 [網際網路 \_ 選項 \_ 傳送 \_ 超時](/windows)相同。</span><span class="sxs-lookup"><span data-stu-id="e24b8-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="e24b8-223">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**網際網路 \_ 選項 \_ 資料 \_ 接收 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-225">8</span><span class="sxs-lookup"><span data-stu-id="e24b8-225">8</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-226">設定或抓取不帶正負號的長整數值，其中包含超時時間值（以毫秒為單位），可接收對 FTP 交易之資料通道的要求回應。</span><span class="sxs-lookup"><span data-stu-id="e24b8-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="e24b8-227">如果回應時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="e24b8-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="e24b8-228">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，包括 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="e24b8-229">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="e24b8-230">此旗標不會影響 HTTP 功能。</span><span class="sxs-lookup"><span data-stu-id="e24b8-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**網際網路 \_ 選項 \_ 資料 \_ 傳送 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-232">7</span><span class="sxs-lookup"><span data-stu-id="e24b8-232">7</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-233">設定或抓取不帶正負號的長整數值（以毫秒為單位），其中包含傳送 FTP 交易之資料通道要求的超時值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="e24b8-234">如果傳送花費的時間超過這個超時值，就會取消傳送。</span><span class="sxs-lookup"><span data-stu-id="e24b8-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="e24b8-235">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，包括 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="e24b8-236">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="e24b8-237">此旗標不會影響 HTTP 功能。</span><span class="sxs-lookup"><span data-stu-id="e24b8-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**網際網路 \_ 選項 \_ 資料檔案 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="e24b8-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-239">33</span><span class="sxs-lookup"><span data-stu-id="e24b8-239">33</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-240">抓取字串值，其中包含支援下載之實體的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e24b8-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="e24b8-241">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)完成後，此旗標會是有效的。</span><span class="sxs-lookup"><span data-stu-id="e24b8-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="e24b8-242">此選項只能由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)進行查詢。</span><span class="sxs-lookup"><span data-stu-id="e24b8-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**網際網路 \_ 選項 \_ 資料檔案 \_ EXT**</span><span class="sxs-lookup"><span data-stu-id="e24b8-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-244">96</span><span class="sxs-lookup"><span data-stu-id="e24b8-244">96</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-245">設定字串值，這個值包含支援下載的實體之檔案的副檔名。</span><span class="sxs-lookup"><span data-stu-id="e24b8-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="e24b8-246">呼叫 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)之前，應該先設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="e24b8-247">此選項只能由 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)設定。</span><span class="sxs-lookup"><span data-stu-id="e24b8-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**網際網路 \_ 選項 \_ 診斷 \_ 通訊端 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="e24b8-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-249">67</span><span class="sxs-lookup"><span data-stu-id="e24b8-249">67</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-250">抓取 [**網際網路 \_ 診斷 \_ 通訊端 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) 結構，其中包含指定之 HTTP 要求的相關資料。</span><span class="sxs-lookup"><span data-stu-id="e24b8-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="e24b8-251">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="e24b8-252">**Windows 7：** 不再支援這個選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**網際網路 \_ 選項 \_ 摘要 \_ 驗證 \_ 卸載**</span><span class="sxs-lookup"><span data-stu-id="e24b8-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-254">76</span><span class="sxs-lookup"><span data-stu-id="e24b8-254">76</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-255">導致系統登出摘要式驗證 SSPI 封裝，清除為該進程建立的所有認證。</span><span class="sxs-lookup"><span data-stu-id="e24b8-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="e24b8-256">此選項不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e24b8-256">No buffer is required for this option.</span></span> <span data-ttu-id="e24b8-257">它是由 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**網際網路 \_ 選項 \_ 停用 \_ 自動撥號**</span><span class="sxs-lookup"><span data-stu-id="e24b8-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-259">70</span><span class="sxs-lookup"><span data-stu-id="e24b8-259">70</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-260">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**網際網路 \_ 選項 \_ 中斷連線 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-262">49</span><span class="sxs-lookup"><span data-stu-id="e24b8-262">49</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-263">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**網際網路 \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="e24b8-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-265">148</span><span class="sxs-lookup"><span data-stu-id="e24b8-265">148</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-266">設定可接受之 advanced HTTP 版本的 DWORD 位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="e24b8-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="e24b8-267">可以在任何控制碼類型上設定。</span><span class="sxs-lookup"><span data-stu-id="e24b8-267">May be set on any handle type.</span></span> <span data-ttu-id="e24b8-268">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="e24b8-268">Possible values are:</span></span>

-   <span data-ttu-id="e24b8-269">HTTP \_ 通訊協定 \_ 旗標 \_ HTTP2 (0x2) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="e24b8-270">在 Windows 10 1507 版和更新版本上支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="e24b8-271">舊版的 HTTP (1.1 和先前的) 無法使用這個選項停用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="e24b8-272">預設值為0x0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-272">The default is 0x0.</span></span> <span data-ttu-id="e24b8-273">在 Windows 10 1507 版和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**網際網路 \_ 選項 \_ 啟用重新導向快取 \_ \_ \_ 讀取**</span><span class="sxs-lookup"><span data-stu-id="e24b8-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-275">122</span><span class="sxs-lookup"><span data-stu-id="e24b8-275">122</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-276">在要求控制碼上，設定布林值，以控制是否會從指定要求的 WinInet 快取傳回重新導向。</span><span class="sxs-lookup"><span data-stu-id="e24b8-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="e24b8-277">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e24b8-277">The default is FALSE.</span></span> <span data-ttu-id="e24b8-278">在 Windows 8 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**\_ \_ 額外編碼的網際網路選項 \_**</span><span class="sxs-lookup"><span data-stu-id="e24b8-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-280">155</span><span class="sxs-lookup"><span data-stu-id="e24b8-280">155</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-281">取得/設定布林值，這個布林值表示查詢字串中的非 ASCII 字元是否應以百分比編碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="e24b8-282">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e24b8-282">The default is FALSE.</span></span> <span data-ttu-id="e24b8-283">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**網際網路 \_ 選項 \_ 結束 \_ 瀏覽器 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="e24b8-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-285">42</span><span class="sxs-lookup"><span data-stu-id="e24b8-285">42</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-286">從硬碟上的密碼快取中清除未使用的專案。</span><span class="sxs-lookup"><span data-stu-id="e24b8-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="e24b8-287">也會重設同步處理模式為每個會話一次時所使用的快取時間。</span><span class="sxs-lookup"><span data-stu-id="e24b8-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="e24b8-288">此選項不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e24b8-288">No buffer is required for this option.</span></span> <span data-ttu-id="e24b8-289">這是由 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**網際網路 \_ 選項 \_ 錯誤 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="e24b8-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-291">62</span><span class="sxs-lookup"><span data-stu-id="e24b8-291">62</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-292">設定不帶正負號的長整數值，其中包含可由用戶端應用程式處理的錯誤遮罩。</span><span class="sxs-lookup"><span data-stu-id="e24b8-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="e24b8-293">這可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="e24b8-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>\_ \_ \_ 合併 \_ SEC \_ CERT 的網際網路錯誤遮罩</span><span class="sxs-lookup"><span data-stu-id="e24b8-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-295">0x2</span><span class="sxs-lookup"><span data-stu-id="e24b8-295">0x2</span></span>

<span data-ttu-id="e24b8-296">表示要使用相同的錯誤傳回來報告所有憑證錯誤，也就是 **「 \_ 網際網路 \_ SEC \_ \_** 憑證錯誤」。</span><span class="sxs-lookup"><span data-stu-id="e24b8-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="e24b8-297">如果設定此旗標，請在收到「 **\_ 網際網路 SEC 憑證 \_ \_ \_ 錯誤**」錯誤時呼叫 **InternetErrorDlg** ，讓使用者可以回應描述問題的熟悉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e24b8-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="e24b8-298">無法通知使用者發生此錯誤，會讓使用者暴露于潛在的詐騙攻擊。</span><span class="sxs-lookup"><span data-stu-id="e24b8-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="e24b8-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>網際網路 \_ 錯誤 \_ 遮罩 \_ 插入 \_ CDROM</span><span class="sxs-lookup"><span data-stu-id="e24b8-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-300">0x1</span><span class="sxs-lookup"><span data-stu-id="e24b8-300">0x1</span></span>

<span data-ttu-id="e24b8-301">指出用戶端應用程式可以處理 **錯誤的 \_ 網際網路 \_ 插入 \_ CDROM** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>網際網路 \_ 錯誤 \_ 遮罩 \_ 登入 \_ 失敗 \_ 顯示 \_ 實體 \_ 主體</span><span class="sxs-lookup"><span data-stu-id="e24b8-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-303">0x8</span><span class="sxs-lookup"><span data-stu-id="e24b8-303">0x8</span></span>

<span data-ttu-id="e24b8-304">指出用戶端應用程式可以處理 **錯誤的 \_ 網際網路 \_ 登入 \_ 失敗 \_ 顯示 \_ 實體 \_ 主體** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>網際網路 \_ 錯誤 \_ 遮罩 \_ 需要 \_ MSN \_ SSPI \_ PKG</span><span class="sxs-lookup"><span data-stu-id="e24b8-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-306">0x4</span><span class="sxs-lookup"><span data-stu-id="e24b8-306">0x4</span></span>

<span data-ttu-id="e24b8-307">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="e24b8-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**網際網路 \_ 選項 \_ 企業 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e24b8-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-309">159</span><span class="sxs-lookup"><span data-stu-id="e24b8-309">159</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-310">設定包含企業識別碼 (查看適用于要求的 PWSTR https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="e24b8-311">在 Windows 10 1507 版和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**網際網路 \_ 選項 \_ 延伸 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e24b8-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-313">24</span><span class="sxs-lookup"><span data-stu-id="e24b8-313">24</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-314">抓取不帶正負號的長整數值，其中包含對應至此執行緒內容中最後傳回的 **錯誤 \_ 網際網路 \_** 錯誤訊息的 Winsock 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="e24b8-315">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)會在 **Null**[**HINTERNET**](appendix-a-hinternet-handles.md)控制碼上使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**快 \_ 取 \_ \_ 超時的網際網路選項 \_**</span><span class="sxs-lookup"><span data-stu-id="e24b8-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-317">63</span><span class="sxs-lookup"><span data-stu-id="e24b8-317">63</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-318">設定或抓取 a1n 不帶正負號的長整數值，其中包含系統在檢查快取以取得資源複本之前，應該等待回應網路要求的時間量。</span><span class="sxs-lookup"><span data-stu-id="e24b8-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="e24b8-319">如果網路要求所花費的時間超過指定的時間，而且快取中有要求的資源，則會從快取中取出資源。</span><span class="sxs-lookup"><span data-stu-id="e24b8-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="e24b8-320">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**網際網路 \_ 選項 \_ 控制碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e24b8-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-322">9</span><span class="sxs-lookup"><span data-stu-id="e24b8-322">9</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-323">抓取不帶正負號的長整數值，其中包含傳入的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="e24b8-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="e24b8-324">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 在任何 [HINTERNET](appendix-a-hinternet-handles.md) 控制碼上使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="e24b8-325">可能的傳回值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>網際網路 \_ 控制碼 \_ 類型 \_ CONNECT \_ FTP</span><span class="sxs-lookup"><span data-stu-id="e24b8-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-327">2</span><span class="sxs-lookup"><span data-stu-id="e24b8-327">2</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>網際網路 \_ 控制碼 \_ 類型 \_ 連接 \_ GOPHER</span><span class="sxs-lookup"><span data-stu-id="e24b8-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-329">3</span><span class="sxs-lookup"><span data-stu-id="e24b8-329">3</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>網際網路 \_ 控制碼 \_ 類型 \_ CONNECT \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="e24b8-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-331">4</span><span class="sxs-lookup"><span data-stu-id="e24b8-331">4</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>網際網路 \_ 控制碼 \_ 類型 \_ 檔 \_ 要求</span><span class="sxs-lookup"><span data-stu-id="e24b8-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-333">14</span><span class="sxs-lookup"><span data-stu-id="e24b8-333">14</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>網際網路 \_ 控制碼 \_ 類型 \_ FTP \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="e24b8-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-335">7</span><span class="sxs-lookup"><span data-stu-id="e24b8-335">7</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>網際網路 \_ 控制碼 \_ 類型 \_ FTP 檔案 \_ \_ HTML</span><span class="sxs-lookup"><span data-stu-id="e24b8-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-337">8</span><span class="sxs-lookup"><span data-stu-id="e24b8-337">8</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>網際網路 \_ 控制碼 \_ 類型 \_ FTP \_ 尋找</span><span class="sxs-lookup"><span data-stu-id="e24b8-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-339">5</span><span class="sxs-lookup"><span data-stu-id="e24b8-339">5</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>網際網路 \_ 控制碼 \_ 類型 \_ FTP \_ 尋找 \_ HTML</span><span class="sxs-lookup"><span data-stu-id="e24b8-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-341">6</span><span class="sxs-lookup"><span data-stu-id="e24b8-341">6</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>網際網路 \_ 控制碼 \_ 類型 \_ GOPHER \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="e24b8-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-343">11</span><span class="sxs-lookup"><span data-stu-id="e24b8-343">11</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>網際網路 \_ 控制碼 \_ 類型 \_ GOPHER 檔案 \_ \_ HTML</span><span class="sxs-lookup"><span data-stu-id="e24b8-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-345">12</span><span class="sxs-lookup"><span data-stu-id="e24b8-345">12</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>網際網路 \_ 控制碼 \_ 類型 \_ GOPHER \_ FIND</span><span class="sxs-lookup"><span data-stu-id="e24b8-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-347">9</span><span class="sxs-lookup"><span data-stu-id="e24b8-347">9</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>網際網路 \_ 控制碼 \_ 類型 \_ GOPHER \_ 尋找 \_ HTML</span><span class="sxs-lookup"><span data-stu-id="e24b8-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-349">10</span><span class="sxs-lookup"><span data-stu-id="e24b8-349">10</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>網際網路 \_ 控制碼 \_ 類型 \_ HTTP \_ 要求</span><span class="sxs-lookup"><span data-stu-id="e24b8-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-351">13</span><span class="sxs-lookup"><span data-stu-id="e24b8-351">13</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>網際網路 \_ 控制碼 \_ 類型 \_ 網際網路</span><span class="sxs-lookup"><span data-stu-id="e24b8-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-353">1</span><span class="sxs-lookup"><span data-stu-id="e24b8-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="e24b8-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**網際網路 \_ 選項 \_ HSTS**</span><span class="sxs-lookup"><span data-stu-id="e24b8-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-355">157</span><span class="sxs-lookup"><span data-stu-id="e24b8-355">157</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-356">取得/設定布林值，指出 WinInet 是否應遵循 HTTP Strict Transport Security (從伺服器 HSTS) 指示詞。</span><span class="sxs-lookup"><span data-stu-id="e24b8-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="e24b8-357">啟用時，HTTPs://schemed 對網域的要求會被重新導向至符合 HTTPs://Url 的 HSTS 原則。</span><span class="sxs-lookup"><span data-stu-id="e24b8-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="e24b8-358">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e24b8-358">The default is FALSE.</span></span> <span data-ttu-id="e24b8-359">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**網際網路 \_ 選項 \_ HTTP \_ 解碼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-361">65</span><span class="sxs-lookup"><span data-stu-id="e24b8-361">65</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-362">啟用 WinINet 以針對 gzip 和 deflate 編碼配置進行解碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="e24b8-363">如需詳細資訊，請參閱 [**內容編碼**](content-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="e24b8-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**使用的網際網路 \_ 選項 \_ HTTP \_ 通訊協定 \_**</span><span class="sxs-lookup"><span data-stu-id="e24b8-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-365">149</span><span class="sxs-lookup"><span data-stu-id="e24b8-365">149</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-366">取得 DWORD，指出指定的要求上使用的是哪個先進的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="e24b8-367">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="e24b8-367">Possible values are:</span></span>

-   <span data-ttu-id="e24b8-368">HTTP \_ 通訊協定 \_ 旗標 \_ HTTP2 (0x2) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="e24b8-369">在 Windows 10 1507 版和更新版本上支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="e24b8-370">0x0 表示 HTTP/1.1 或更早版本;\_ \_ \_ 如果需要更精確的使用舊版，請參閱網際網路選項 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="e24b8-371">在 Windows 10 1507 版和更新版本上支援。</span><span class="sxs-lookup"><span data-stu-id="e24b8-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**網際網路 \_ 選項 \_ HTTP \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="e24b8-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-373">59</span><span class="sxs-lookup"><span data-stu-id="e24b8-373">59</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-374">設定或抓取 [**HTTP \_ 版本 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) 結構，其中包含支援的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="e24b8-375">這必須用於 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="e24b8-376">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="e24b8-377">在 Windows 7、Windows Server 2008 R2 和更新版本上，Internet Explorer 設定會覆寫 [**HTTP \_ 版本 \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-http_version_info)結構中 **dwMinorVersion** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="e24b8-378">**EnableHttp1 \_ 1** 是在系統的 Internet Explorer 中設定的 **HKLM \\ Software \\ Microsoft \\ microsoft-windows-ie-internetexplorer \\ AdvacnedOptions \\ HTTP \\ GENABLE** 底下的登錄值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="e24b8-379">**EnableHttp1 \_ 1** 值預設為1。</span><span class="sxs-lookup"><span data-stu-id="e24b8-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="e24b8-380">如果 **EnableHttp1 \_ 1** 設定為1，則會忽略小於1.1 之任何 Http 版本的 **HTTP \_ 版本 \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="e24b8-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**網際網路 \_ 選項身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="e24b8-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-382">78</span><span class="sxs-lookup"><span data-stu-id="e24b8-382">78</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-383">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**網際網路 \_ 選項 \_ 閒置 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="e24b8-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-385">51</span><span class="sxs-lookup"><span data-stu-id="e24b8-385">51</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-386">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**網際網路 \_ 選項 \_ IDN**</span><span class="sxs-lookup"><span data-stu-id="e24b8-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-388">102</span><span class="sxs-lookup"><span data-stu-id="e24b8-388">102</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-389">根據預設，URL 的主機或授權單位部分會根據適用于直接和 proxy 連接的 IDN 規格進行編碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="e24b8-390">此選項可用於要求或連接控制碼，以啟用或停用 IDN。</span><span class="sxs-lookup"><span data-stu-id="e24b8-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="e24b8-391">當 IDN 停用時，WinINet 會使用系統字碼頁來編碼 URL 的主機或授權單位部分。</span><span class="sxs-lookup"><span data-stu-id="e24b8-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="e24b8-392">若要停用 IDN 主機轉換，請將 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)呼叫中的 *lpBuffer* 參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="e24b8-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="e24b8-393">若只要啟用直接連接的 IDN 轉換，請在 **InternetSetOption** 的呼叫中，于 *lpBuffer* 參數中指定 [**網際網路旗標的 \_ \_ idn \_ direct** ]。</span><span class="sxs-lookup"><span data-stu-id="e24b8-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="e24b8-394">若只要在 proxy 連接上啟用 IDN 轉換，請在呼叫 **InternetSetOption** 的 *lpBuffer* 參數中指定 **網際網路 \_ 旗標 \_ IDN \_ proxy** 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="e24b8-395">**WINDOWS XP （含 SP2）和 Windows Server 2003 （含 SP1）：** 不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="e24b8-396">**版本：** 需要 Internet Explorer 7.0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**網際網路 \_ 選項 \_ 略過 \_ 離線**</span><span class="sxs-lookup"><span data-stu-id="e24b8-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-398">77</span><span class="sxs-lookup"><span data-stu-id="e24b8-398">77</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-399">設定或抓取指定的要求控制碼是否應忽略全域離線旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="e24b8-400">此選項不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e24b8-400">No buffer is required for this option.</span></span> <span data-ttu-id="e24b8-401">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)會搭配要求控制碼來使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="e24b8-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="e24b8-402">此選項只有在 Internet Explorer 5 和更新版本中才有效。</span><span class="sxs-lookup"><span data-stu-id="e24b8-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**網際網路 \_ 選項 \_ 保留 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="e24b8-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-404">22</span><span class="sxs-lookup"><span data-stu-id="e24b8-404">22</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-405">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**網際網路 \_ 選項 \_ 接聽 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-407">11</span><span class="sxs-lookup"><span data-stu-id="e24b8-407">11</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-408">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**\_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的網際網路選項最大 CONNS**</span><span class="sxs-lookup"><span data-stu-id="e24b8-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-410">74</span><span class="sxs-lookup"><span data-stu-id="e24b8-410">74</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-411">設定或抓取不帶正負號的長整數值，其中包含每個 HTTP/1.0 伺服器允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="e24b8-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="e24b8-412">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-413">此選項只有在 Internet Explorer 5 和更新版本中才有效。</span><span class="sxs-lookup"><span data-stu-id="e24b8-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_ \_ \_ \_ 每個 \_ PROXY 的網際網路選項最大 CONNS**</span><span class="sxs-lookup"><span data-stu-id="e24b8-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-415">103</span><span class="sxs-lookup"><span data-stu-id="e24b8-415">103</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-416">設定或抓取不帶正負號的長整數值，其中包含每個 CERN proxy 允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="e24b8-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="e24b8-417">當設定或抓取這個選項時， *hInternet* 參數必須設定為 **null** 控制碼值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="e24b8-418">**Null** 控制碼值表示應該設定或查詢目前進程的選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="e24b8-419">使用這個選項呼叫 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) 時，所有現有的 proxy 物件都會收到新的值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="e24b8-420">此值的範圍限制為2到128（含）。</span><span class="sxs-lookup"><span data-stu-id="e24b8-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="e24b8-421">**版本：** 需要 Internet Explorer 8.0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**每一伺服器的網際網路 \_ 選項 \_ 最大 \_ CONNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e24b8-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-423">73</span><span class="sxs-lookup"><span data-stu-id="e24b8-423">73</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-424">設定或抓取不帶正負號的長整數值，其中包含每個伺服器允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="e24b8-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="e24b8-425">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-426">此選項只有在 Internet Explorer 5 和更新版本中才有效。</span><span class="sxs-lookup"><span data-stu-id="e24b8-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**網際網路 \_ 選項 \_ 離線 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="e24b8-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-428">26</span><span class="sxs-lookup"><span data-stu-id="e24b8-428">26</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-429">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**網際網路 \_ 選項 \_ 離線 \_ 語義**</span><span class="sxs-lookup"><span data-stu-id="e24b8-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-431">52</span><span class="sxs-lookup"><span data-stu-id="e24b8-431">52</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-432">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_ \_ 加入宣告 \_ \_ 弱 \_ 式簽章的網際網路選項**</span><span class="sxs-lookup"><span data-stu-id="e24b8-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-434">176</span><span class="sxs-lookup"><span data-stu-id="e24b8-434">176</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-435">加入弱式簽章 (例如 SHA-1) ，視為不安全。</span><span class="sxs-lookup"><span data-stu-id="e24b8-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="e24b8-436">這會指示 WinInet 使用 **CERT \_ CHAIN \_ OPT \_ \_ \_** 參數來呼叫 [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**網際網路 \_ 選項 \_ 父 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-438">21</span><span class="sxs-lookup"><span data-stu-id="e24b8-438">21</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-439">捕獲此控制碼的父控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="e24b8-440">此選項可用於 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)的任何 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**網際網路 \_ 選項 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-442">29</span><span class="sxs-lookup"><span data-stu-id="e24b8-442">29</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-443">設定或抓取字串值，此值包含與 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回之控制碼相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="e24b8-444">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**\_ \_ 每個連線 \_ \_ 選項的網際網路選項**</span><span class="sxs-lookup"><span data-stu-id="e24b8-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-446">75</span><span class="sxs-lookup"><span data-stu-id="e24b8-446">75</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-447">設定或抓取 [**\_ 每個連接 \_ \_ 選項 \_ 清單**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) 結構的網際網路，以指定特定連接的選項清單。</span><span class="sxs-lookup"><span data-stu-id="e24b8-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="e24b8-448">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-449">此選項只有在 Internet Explorer 5 和更新版本中才有效。</span><span class="sxs-lookup"><span data-stu-id="e24b8-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="e24b8-450">**網際網路 \_[ \_ 每 \_ 個 \_ 連接的選項] 選項** 會讓設定在 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)的呼叫中使用 **Null** 控制碼時，以系統範圍為基礎變更。</span><span class="sxs-lookup"><span data-stu-id="e24b8-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-451">若要重新整理全域 proxy 設定，您必須使用 **INTERNET \_ option \_ refresh** 選項旗標來呼叫 **InternetSetOption** 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="e24b8-452">若要變更整個進程的 proxy 資訊，而不影響 Internet Explorer 5 和更新版本中的全域設定，請在從 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)傳回的控制碼上使用此選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="e24b8-453">下列程式碼範例會變更整個進程的 proxy，即使 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼已關閉，且未由任何要求使用也是一樣。</span><span class="sxs-lookup"><span data-stu-id="e24b8-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="e24b8-454">如需詳細資訊和程式碼範例，請參閱 [知識庫文章 226473](https://support.microsoft.com/kb/226473)。</span><span class="sxs-lookup"><span data-stu-id="e24b8-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**網際網路 \_ 選項 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="e24b8-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-456">48</span><span class="sxs-lookup"><span data-stu-id="e24b8-456">48</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-457">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**網際網路 \_ 選項 \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="e24b8-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-459">38</span><span class="sxs-lookup"><span data-stu-id="e24b8-459">38</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-460">設定或抓取 [**網際網路 \_ PROXY \_ 資訊**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info)結構，此結構包含當 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼不是 **Null** 時，現有 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)控制碼的 PROXY 資料。</span><span class="sxs-lookup"><span data-stu-id="e24b8-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="e24b8-461">如果 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼為 **Null**，則函式會設定或查詢全域 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="e24b8-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="e24b8-462">此選項可用於 **InternetOpen** 所傳回的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="e24b8-463">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="e24b8-464">建議您 \_ 使用 [每個連接的網際網路選項] \_ 選項， \_ \_ 而不要使用 [網際網路 \_ 選項 PROXY] \_ 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="e24b8-465">如需詳細資訊，請參閱 [知識庫文章 226473](https://support.microsoft.com/kb/226473)。</span><span class="sxs-lookup"><span data-stu-id="e24b8-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**網際網路 \_ 選項 \_ PROXY \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="e24b8-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-467">44</span><span class="sxs-lookup"><span data-stu-id="e24b8-467">44</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-468">設定或抓取包含用來存取 proxy 之密碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="e24b8-469">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-470">您可以在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)傳回的控制碼上設定這個選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**網際網路 \_ 選項 \_ PROXY \_ 設定 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="e24b8-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-472">95</span><span class="sxs-lookup"><span data-stu-id="e24b8-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="e24b8-473">警示目前的 WinInet 實例，指出 proxy 設定已變更，且必須以新的設定進行更新。</span><span class="sxs-lookup"><span data-stu-id="e24b8-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="e24b8-474">若要為所有可用的 WinInet 實例發出警示，請將 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)的 *緩衝區* 參數設定為 **Null** ，並在傳遞此選項時將 *BufferLength* 設為0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="e24b8-475">您可以在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)傳回的控制碼上設定這個選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**網際網路 \_ 選項 \_ PROXY 使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="e24b8-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-477">43</span><span class="sxs-lookup"><span data-stu-id="e24b8-477">43</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-478">設定或抓取包含用來存取 proxy 之使用者名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="e24b8-479">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-480">您可以在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)傳回的控制碼上設定這個選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**網際網路 \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="e24b8-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-482">12</span><span class="sxs-lookup"><span data-stu-id="e24b8-482">12</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-483">設定或抓取不帶正負號的長整數值，其中包含讀取緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="e24b8-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="e24b8-484">此選項只能用於 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)和 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP 會話所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="e24b8-485">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)會使用此選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**網際網路 \_ 選項 \_ 接收 \_ 輸送量**</span><span class="sxs-lookup"><span data-stu-id="e24b8-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-487">57</span><span class="sxs-lookup"><span data-stu-id="e24b8-487">57</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-488">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**網際網路 \_ 選項 \_ 接收 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-490">6</span><span class="sxs-lookup"><span data-stu-id="e24b8-490">6</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-491">設定或抓取不帶正負號的長整數值，其中包含接收要求回應的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e24b8-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="e24b8-492">如果回應時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="e24b8-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="e24b8-493">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，包括 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="e24b8-494">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="e24b8-495">此選項不適合用來呈現細部、立即的超時時間。</span><span class="sxs-lookup"><span data-stu-id="e24b8-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="e24b8-496">您可以預期在設定的超時值之後，最多會在六秒內發生超時。</span><span class="sxs-lookup"><span data-stu-id="e24b8-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="e24b8-497">使用於參考 FTP 交易時，這個選項會參考控制通道。</span><span class="sxs-lookup"><span data-stu-id="e24b8-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**網際網路 \_ 選項重新整理 \_**</span><span class="sxs-lookup"><span data-stu-id="e24b8-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-499">37</span><span class="sxs-lookup"><span data-stu-id="e24b8-499">37</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-500">使 proxy 資料從登錄中重新讀取控制碼的。</span><span class="sxs-lookup"><span data-stu-id="e24b8-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="e24b8-501">不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e24b8-501">No buffer is required.</span></span> <span data-ttu-id="e24b8-502">此選項可用於 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="e24b8-503">它是由 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**網際網路 \_ 選項 \_ 移除身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="e24b8-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-505">79</span><span class="sxs-lookup"><span data-stu-id="e24b8-505">79</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-506">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**網際網路 \_ 選項 \_ 要求 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="e24b8-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-508">23</span><span class="sxs-lookup"><span data-stu-id="e24b8-508">23</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-509">抓取不帶正負號的長整數值，其中包含特殊狀態旗標，指出正在進行下載的狀態。</span><span class="sxs-lookup"><span data-stu-id="e24b8-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="e24b8-510">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="e24b8-511">[ [網際網路 \_ 選項 \_ 要求 \_ 旗標](/windows) ] 選項可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="e24b8-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ ASYNC</span><span class="sxs-lookup"><span data-stu-id="e24b8-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e24b8-513">0x00000002</span></span>

<span data-ttu-id="e24b8-514">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_ \_ \_ 已停用 INTERNET REQFLAG CACHE 寫入 \_</span><span class="sxs-lookup"><span data-stu-id="e24b8-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e24b8-516">0x00000040</span></span>

<span data-ttu-id="e24b8-517">無法 (HTTPS 要求快取網際網路要求，例如) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>來自快取 \_ 的網際網路 REQFLAG \_ \_</span><span class="sxs-lookup"><span data-stu-id="e24b8-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e24b8-519">0x00000001</span></span>

<span data-ttu-id="e24b8-520">回應來自快取。</span><span class="sxs-lookup"><span data-stu-id="e24b8-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET \_ REQFLAG \_ NET \_ TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e24b8-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e24b8-522">0x00000080</span></span>

<span data-ttu-id="e24b8-523">網際網路要求超時。</span><span class="sxs-lookup"><span data-stu-id="e24b8-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>網際網路 \_ REQFLAG \_ 沒有 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="e24b8-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e24b8-525">0x00000008</span></span>

<span data-ttu-id="e24b8-526">原始回應未包含任何標頭。</span><span class="sxs-lookup"><span data-stu-id="e24b8-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>網際網路 \_ REQFLAG \_ 被動</span><span class="sxs-lookup"><span data-stu-id="e24b8-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e24b8-528">0x00000010</span></span>

<span data-ttu-id="e24b8-529">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>\_ \_ 經由 \_ PROXY 的網際網路 REQFLAG</span><span class="sxs-lookup"><span data-stu-id="e24b8-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e24b8-531">0x00000004</span></span>

<span data-ttu-id="e24b8-532">已透過 proxy 提出要求。</span><span class="sxs-lookup"><span data-stu-id="e24b8-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="e24b8-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**網際網路 \_ 選項 \_ 要求 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="e24b8-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-534">58</span><span class="sxs-lookup"><span data-stu-id="e24b8-534">58</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-535">設定或抓取不帶正負號的長整數值，其中包含在 HTTP 控制碼上競爭連接的要求優先權。</span><span class="sxs-lookup"><span data-stu-id="e24b8-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="e24b8-536">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**網際網路 \_ 選項 \_ 重設 \_ URLCACHE \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="e24b8-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-538">60</span><span class="sxs-lookup"><span data-stu-id="e24b8-538">60</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-539">啟動進程的新快取會話。</span><span class="sxs-lookup"><span data-stu-id="e24b8-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="e24b8-540">不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e24b8-540">No buffer is required.</span></span> <span data-ttu-id="e24b8-541">這是由 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-542">此選項只會保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**網際網路 \_ 選項 \_ 次要快取 \_ \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="e24b8-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-544">53</span><span class="sxs-lookup"><span data-stu-id="e24b8-544">53</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-545">設定或抓取包含次要快取索引鍵的字串值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="e24b8-546">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="e24b8-547">此選項只會保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**網際網路 \_ 選項 \_ 安全性 \_ 憑證**</span><span class="sxs-lookup"><span data-stu-id="e24b8-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-549">35</span><span class="sxs-lookup"><span data-stu-id="e24b8-549">35</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-550">抓取 SSL/PCT 的憑證 (安全通訊端層/私用通訊技術) 伺服器轉換成格式化的字串。</span><span class="sxs-lookup"><span data-stu-id="e24b8-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="e24b8-551">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**網際網路 \_ 選項 \_ 安全性 \_ 憑證 \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="e24b8-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-553">32</span><span class="sxs-lookup"><span data-stu-id="e24b8-553">32</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-554">將 SSL/PCT 伺服器的憑證抓取到網際網路 \_ 憑證 \_ 資訊結構中。</span><span class="sxs-lookup"><span data-stu-id="e24b8-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="e24b8-555">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**網際網路 \_ 選項 \_ 安全性 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="e24b8-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-557">31</span><span class="sxs-lookup"><span data-stu-id="e24b8-557">31</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-558">抓取不帶正負號的長整數值，其中包含控制碼的安全性旗標。</span><span class="sxs-lookup"><span data-stu-id="e24b8-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="e24b8-559">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)會使用此選項。</span><span class="sxs-lookup"><span data-stu-id="e24b8-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="e24b8-560">它可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="e24b8-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>安全性 \_ 旗標 \_ 128 位</span><span class="sxs-lookup"><span data-stu-id="e24b8-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-562">0x20000000</span></span>

<span data-ttu-id="e24b8-563">與慣用值 [安全性旗標 \_ \_ 強度 \_ 強](/windows)的相同。</span><span class="sxs-lookup"><span data-stu-id="e24b8-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="e24b8-564">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>安全性 \_ 旗標 \_ 40BIT</span><span class="sxs-lookup"><span data-stu-id="e24b8-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-566">0x10000000</span></span>

<span data-ttu-id="e24b8-567">與慣用值 [安全性旗標 \_ \_ 強度 \_ 弱](/windows)的相同。</span><span class="sxs-lookup"><span data-stu-id="e24b8-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="e24b8-568">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>安全性 \_ 旗標 \_ 56BIT</span><span class="sxs-lookup"><span data-stu-id="e24b8-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-570">0x40000000</span></span>

<span data-ttu-id="e24b8-571">與慣用值 [安全性旗標 \_ \_ 強度 \_ 中](/windows)相同。</span><span class="sxs-lookup"><span data-stu-id="e24b8-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="e24b8-572">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>安全性 \_ 旗標 \_ FORTEZZA</span><span class="sxs-lookup"><span data-stu-id="e24b8-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-574">0x08000000</span></span>

<span data-ttu-id="e24b8-575">表示已使用 Fortezza 來提供指定連接的密碼、驗證和（或）完整性。</span><span class="sxs-lookup"><span data-stu-id="e24b8-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>安全性 \_ 旗標 \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="e24b8-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e24b8-577">0x00000020</span></span>

<span data-ttu-id="e24b8-578">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>安全性 \_ 旗標 \_ 忽略 \_ CERT \_ CN \_ 無效</span><span class="sxs-lookup"><span data-stu-id="e24b8-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="e24b8-580">0x00001000</span></span>

<span data-ttu-id="e24b8-581">忽略 [錯誤 \_ 網際網路 \_ SEC \_ CERT \_ CN \_ 無效](wininet-errors.md) 的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e24b8-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>安全性 \_ 旗標 \_ 忽略憑證 \_ \_ 日期 \_ 無效</span><span class="sxs-lookup"><span data-stu-id="e24b8-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e24b8-583">0x00002000</span></span>

<span data-ttu-id="e24b8-584">忽略 [error \_ INTERNET \_ SEC \_ CERT \_ DATE \_ 無效](wininet-errors.md) 的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e24b8-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>安全性 \_ 旗標 \_ 忽略重新 \_ 導向 \_ 至 \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="e24b8-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="e24b8-586">0x00008000</span></span>

<span data-ttu-id="e24b8-587">在 REDIR 錯誤訊息時，忽略 [ \_ 網際網路 \_ HTTPS \_ 對 \_ HTTP \_ \_ 的錯誤](wininet-errors.md) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>安全性 \_ 旗標 \_ 忽略重新 \_ 導向 \_ 至 \_ HTTPS</span><span class="sxs-lookup"><span data-stu-id="e24b8-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="e24b8-589">0x00004000</span></span>

<span data-ttu-id="e24b8-590">忽略 REDIR 錯誤訊息 [ \_ 上的網際網路 \_ HTTP \_ \_ HTTPS 至 HTTPS \_ \_ 錯誤](wininet-errors.md) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>安全性 \_ 旗標 \_ 忽略 \_ 撤銷</span><span class="sxs-lookup"><span data-stu-id="e24b8-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e24b8-592">0x00000080</span></span>

<span data-ttu-id="e24b8-593">忽略憑證撤銷問題。</span><span class="sxs-lookup"><span data-stu-id="e24b8-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>安全性 \_ 旗標 \_ 忽略 \_ 未知的 \_ CA</span><span class="sxs-lookup"><span data-stu-id="e24b8-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e24b8-595">0x00000100</span></span>

<span data-ttu-id="e24b8-596">忽略未知的憑證授權單位單位問題。</span><span class="sxs-lookup"><span data-stu-id="e24b8-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>安全性 \_ 旗標 \_ 忽略 \_ 弱 \_ 式簽章</span><span class="sxs-lookup"><span data-stu-id="e24b8-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e24b8-598">0x00010000</span></span>

<span data-ttu-id="e24b8-599">忽略弱式憑證簽章問題。</span><span class="sxs-lookup"><span data-stu-id="e24b8-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>安全性 \_ 旗標 \_ 忽略 \_ 錯誤的 \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="e24b8-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="e24b8-601">0x00000200</span></span>

<span data-ttu-id="e24b8-602">忽略不正確的使用問題。</span><span class="sxs-lookup"><span data-stu-id="e24b8-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>安全性 \_ 旗標 \_ NORMALBITNESS</span><span class="sxs-lookup"><span data-stu-id="e24b8-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-604">0x10000000</span></span>

<span data-ttu-id="e24b8-605">與值 [安全性旗標 \_ \_ 強度 \_ 弱](/windows)。</span><span class="sxs-lookup"><span data-stu-id="e24b8-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="e24b8-606">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>安全性 \_ 旗標 \_ PCT</span><span class="sxs-lookup"><span data-stu-id="e24b8-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e24b8-608">0x00000008</span></span>

<span data-ttu-id="e24b8-609">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>安全性 \_ 旗標 \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="e24b8-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e24b8-611">0x00000010</span></span>

<span data-ttu-id="e24b8-612">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>安全性 \_ 旗標 \_ 安全</span><span class="sxs-lookup"><span data-stu-id="e24b8-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e24b8-614">0x00000001</span></span>

<span data-ttu-id="e24b8-615">使用安全傳輸。</span><span class="sxs-lookup"><span data-stu-id="e24b8-615">Uses secure transfers.</span></span> <span data-ttu-id="e24b8-616">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>安全性 \_ 旗標 \_ SSL</span><span class="sxs-lookup"><span data-stu-id="e24b8-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e24b8-618">0x00000002</span></span>

<span data-ttu-id="e24b8-619">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>安全性 \_ 旗標 \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="e24b8-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e24b8-621">0x00000004</span></span>

<span data-ttu-id="e24b8-622">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>安全性 \_ 旗標 \_ 強度 \_ 中</span><span class="sxs-lookup"><span data-stu-id="e24b8-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-624">0x40000000</span></span>

<span data-ttu-id="e24b8-625">使用中型 (56 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="e24b8-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="e24b8-626">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>安全性 \_ 旗標 \_ 強度 \_ 強</span><span class="sxs-lookup"><span data-stu-id="e24b8-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-628">0x20000000</span></span>

<span data-ttu-id="e24b8-629">使用強式 (128 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="e24b8-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="e24b8-630">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>安全性 \_ 旗標 \_ 強度 \_ 弱</span><span class="sxs-lookup"><span data-stu-id="e24b8-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-632">0x10000000</span></span>

<span data-ttu-id="e24b8-633">使用弱式 (40 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="e24b8-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="e24b8-634">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>安全性 \_ 旗標 \_ UNKNOWNBIT</span><span class="sxs-lookup"><span data-stu-id="e24b8-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="e24b8-636">0x80000000</span></span>

<span data-ttu-id="e24b8-637">加密中使用的位大小不明。</span><span class="sxs-lookup"><span data-stu-id="e24b8-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="e24b8-638">這只會在呼叫 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)時傳回。</span><span class="sxs-lookup"><span data-stu-id="e24b8-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="e24b8-639">請注意，以這種方式抓取的資料會與已發生的交易產生關聯，而其安全性等級無法再變更。</span><span class="sxs-lookup"><span data-stu-id="e24b8-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="e24b8-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**網際網路 \_ 選項 \_ 安全性 \_ 金鑰 \_ 位數**</span><span class="sxs-lookup"><span data-stu-id="e24b8-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-641">36</span><span class="sxs-lookup"><span data-stu-id="e24b8-641">36</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-642">抓取包含加密金鑰之位大小的不帶正負號長整數值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="e24b8-643">數位愈大，使用的加密強度就愈大。</span><span class="sxs-lookup"><span data-stu-id="e24b8-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="e24b8-644">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="e24b8-645">請注意，以這種方式抓取的資料會與已發生的交易產生關聯，而其安全性等級無法再變更。</span><span class="sxs-lookup"><span data-stu-id="e24b8-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**網際網路 \_ 選項 \_ 傳送 \_ 輸送量**</span><span class="sxs-lookup"><span data-stu-id="e24b8-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-647">56</span><span class="sxs-lookup"><span data-stu-id="e24b8-647">56</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-648">未實作。</span><span class="sxs-lookup"><span data-stu-id="e24b8-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**網際網路 \_ 選項 \_ 傳送 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="e24b8-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-650">5</span><span class="sxs-lookup"><span data-stu-id="e24b8-650">5</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-651">設定或抓取不帶正負號的長整數值（以毫秒為單位），其中包含要傳送要求的超時值。</span><span class="sxs-lookup"><span data-stu-id="e24b8-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="e24b8-652">如果傳送花費的時間超過這個超時值，就會取消傳送。</span><span class="sxs-lookup"><span data-stu-id="e24b8-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="e24b8-653">此選項可用於任何 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼，包括 **Null** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="e24b8-654">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="e24b8-655">使用於參考 FTP 交易時，這個選項會參考控制通道。</span><span class="sxs-lookup"><span data-stu-id="e24b8-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**網際網路 \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e24b8-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-657">105</span><span class="sxs-lookup"><span data-stu-id="e24b8-657">105</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-658">以重複的 [PCCERT \_ 鏈 \_ 內容](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)形式抓取伺服器的憑證鏈內容。</span><span class="sxs-lookup"><span data-stu-id="e24b8-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="e24b8-659">您可以將此重複的內容傳遞至採用 [PCCERT \_ 鏈 \_ 內容](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)的任何密碼編譯 API 函數。</span><span class="sxs-lookup"><span data-stu-id="e24b8-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="e24b8-660">當您完成憑證鏈內容時，必須在傳回的 [PCCERT \_ 鏈 \_ 內容](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)上呼叫 [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="e24b8-661">**版本：** 需要 Internet Explorer 8.0。</span><span class="sxs-lookup"><span data-stu-id="e24b8-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**\_ \_ 已變更網際網路選項設定 \_**</span><span class="sxs-lookup"><span data-stu-id="e24b8-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-663">39</span><span class="sxs-lookup"><span data-stu-id="e24b8-663">39</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-664">通知系統，登錄設定已變更，因此它會在下一次呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)時驗證設定。</span><span class="sxs-lookup"><span data-stu-id="e24b8-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="e24b8-665">這是由 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**網際網路 \_ 選項 \_ 抑制 \_ 伺服器 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="e24b8-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-667">104</span><span class="sxs-lookup"><span data-stu-id="e24b8-667">104</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-668">設定 HTTP 要求物件，使其不會登入源伺服器，但會對 HTTP proxy 伺服器執行自動登入。</span><span class="sxs-lookup"><span data-stu-id="e24b8-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="e24b8-669">此選項與「要求旗標 **網際網路 \_ 旗標 \_ 無 \_ 驗證**」不同，這會防止對 proxy 伺服器和源伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e24b8-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="e24b8-670">設定此模式將會抑制使用任何認證材質 (先前提供的使用者名稱/密碼或用戶端 SSL 憑證) 在與源伺服器通訊時使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="e24b8-671">但是，如果要求必須透過驗證 proxy 傳輸，WinINet 仍會根據使用者的內部網路區域設定，對 HTTP proxy 執行自動驗證。</span><span class="sxs-lookup"><span data-stu-id="e24b8-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="e24b8-672">預設內部網路區域設定是允許使用使用者的預設認證進行自動登入。</span><span class="sxs-lookup"><span data-stu-id="e24b8-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="e24b8-673">為了確保隱藏所有識別資訊，呼叫端應該將 [ **網際網路 \_ 選項 \_ 抑制 \_ 伺服器 \_ 驗證** ] 與 [ **網際網路 \_ 旗標 \_ 無 \_ cookie** 要求] 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="e24b8-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="e24b8-674">此選項只能在要求物件上設定，然後才會傳送。</span><span class="sxs-lookup"><span data-stu-id="e24b8-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="e24b8-675">在傳送要求之後嘗試設定此選項，將會傳回 **錯誤的 \_ 網際網路 \_ 錯誤 \_ 控制碼 \_ 狀態**。</span><span class="sxs-lookup"><span data-stu-id="e24b8-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="e24b8-676">此選項不需要任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e24b8-676">No buffer is required for this option.</span></span> <span data-ttu-id="e24b8-677">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)只會在 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所傳回的控制碼上使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="e24b8-678">**版本：** 需要 Internet Explorer 8.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**網際網路 \_ 選項 \_ 隱藏 \_ 行為**</span><span class="sxs-lookup"><span data-stu-id="e24b8-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-680">81</span><span class="sxs-lookup"><span data-stu-id="e24b8-680">81</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-681">一般用途選項，可用來隱藏整個進程的行為。</span><span class="sxs-lookup"><span data-stu-id="e24b8-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="e24b8-682">函數的 *lpBuffer* 參數必須是 DWORD 的指標，其中包含要隱藏的特定行為。</span><span class="sxs-lookup"><span data-stu-id="e24b8-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="e24b8-683">此選項無法使用 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)進行查詢。</span><span class="sxs-lookup"><span data-stu-id="e24b8-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="e24b8-684">允許的值為：</span><span class="sxs-lookup"><span data-stu-id="e24b8-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>網際網路 \_ 隱藏 \_ 全部重設 \_</span><span class="sxs-lookup"><span data-stu-id="e24b8-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-686">0</span><span class="sxs-lookup"><span data-stu-id="e24b8-686">0</span></span>

<span data-ttu-id="e24b8-687">停用所有隱藏，並重新啟用預設和設定的行為。</span><span class="sxs-lookup"><span data-stu-id="e24b8-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="e24b8-688">此選項等同于設定 **網際網路 \_ 隱藏 \_ cookie \_ 原則 \_ 重設** ，以及 **個別 \_ \_ \_ \_ 重設網際網路隱藏 cookie 保存** 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="e24b8-689">**版本：** 需要 Internet Explorer 6.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>網際網路 \_ 隱藏 \_ COOKIE \_ 原則</span><span class="sxs-lookup"><span data-stu-id="e24b8-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="e24b8-691">1</span><span class="sxs-lookup"><span data-stu-id="e24b8-691">1</span></span>

<span data-ttu-id="e24b8-692">忽略任何已設定的 cookie 原則，並允許設定 cookie。</span><span class="sxs-lookup"><span data-stu-id="e24b8-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="e24b8-693">**版本：** 需要 Internet Explorer 6.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>網際網路 \_ 抑制 \_ COOKIE \_ 原則 \_ 重設</span><span class="sxs-lookup"><span data-stu-id="e24b8-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="e24b8-695">2</span><span class="sxs-lookup"><span data-stu-id="e24b8-695">2</span></span>

<span data-ttu-id="e24b8-696">停用 **網際網路 \_ 隱藏 \_ cookie \_ 原則** 隱藏，允許根據設定的 cookie 原則來評估 cookie。</span><span class="sxs-lookup"><span data-stu-id="e24b8-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="e24b8-697">**版本：** 需要 Internet Explorer 6.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> 網際網路 \_ 隱藏 \_ COOKIE \_ 保存</span><span class="sxs-lookup"><span data-stu-id="e24b8-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-699">3</span><span class="sxs-lookup"><span data-stu-id="e24b8-699">3</span></span>

<span data-ttu-id="e24b8-700">隱藏 cookie 的持續性，即使伺服器已將它們指定為持續性。</span><span class="sxs-lookup"><span data-stu-id="e24b8-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="e24b8-701">**版本：** 需要 Internet Explorer 8.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>網際網路 \_ 抑制 \_ COOKIE \_ 保存 \_ 重設</span><span class="sxs-lookup"><span data-stu-id="e24b8-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-703">4</span><span class="sxs-lookup"><span data-stu-id="e24b8-703">4</span></span>

<span data-ttu-id="e24b8-704">停用 **網際網路 \_ 隱藏 \_ cookie \_ 保存** 隱藏，並重新啟用 cookie 的持續性。</span><span class="sxs-lookup"><span data-stu-id="e24b8-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="e24b8-705">任何先前隱藏的 cookie 都不會變成持續性。</span><span class="sxs-lookup"><span data-stu-id="e24b8-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="e24b8-706">**版本：** 需要 Internet Explorer 8.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e24b8-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="e24b8-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**網際網路 \_ 選項 \_ URL**</span><span class="sxs-lookup"><span data-stu-id="e24b8-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-708">34</span><span class="sxs-lookup"><span data-stu-id="e24b8-708">34</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-709">抓取字串值，其中包含已下載資源的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="e24b8-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="e24b8-710">如果原始 URL 包含任何額外的資料（例如搜尋字串或錨點），或重新導向呼叫，則傳回的 URL 會與原始的 URL 不同。</span><span class="sxs-lookup"><span data-stu-id="e24b8-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="e24b8-711">這個選項在 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)或 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼上是有效的。</span><span class="sxs-lookup"><span data-stu-id="e24b8-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="e24b8-712">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**網際網路 \_ 選項 \_ 使用者 \_ 代理程式**</span><span class="sxs-lookup"><span data-stu-id="e24b8-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-714">41</span><span class="sxs-lookup"><span data-stu-id="e24b8-714">41</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-715">設定或抓取 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 提供的控制碼上的使用者代理程式字串，並在後續的 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 函式中使用，但前提是它不是由 [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) 或 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)所加入的標頭所覆寫。</span><span class="sxs-lookup"><span data-stu-id="e24b8-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="e24b8-716">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**網際網路 \_ 選項使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="e24b8-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-718">28</span><span class="sxs-lookup"><span data-stu-id="e24b8-718">28</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-719">設定或抓取包含與 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回之控制碼相關聯之使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="e24b8-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="e24b8-720">這是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**網際網路 \_ 選項 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="e24b8-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-722">40</span><span class="sxs-lookup"><span data-stu-id="e24b8-722">40</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-723">抓取包含 Wininet.dll 之版本號碼的 **網際網路 \_ 版本 \_ 資訊** 結構。</span><span class="sxs-lookup"><span data-stu-id="e24b8-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="e24b8-724">此選項可用於 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)的 **Null**[**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="e24b8-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e24b8-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**網際網路 \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="e24b8-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e24b8-726">13</span><span class="sxs-lookup"><span data-stu-id="e24b8-726">13</span></span>
</dt> <dt>



<span data-ttu-id="e24b8-727">設定或抓取不帶正負號的長整數值，其中包含寫入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e24b8-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="e24b8-728">此選項只能用於 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)和 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP 會話所傳回的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼) 。</span><span class="sxs-lookup"><span data-stu-id="e24b8-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="e24b8-729">它是由 [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) 和 [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)所使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e24b8-730">備註</span><span class="sxs-lookup"><span data-stu-id="e24b8-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e24b8-731">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="e24b8-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="e24b8-732">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="e24b8-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e24b8-733">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="e24b8-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e24b8-734">規格需求</span><span class="sxs-lookup"><span data-stu-id="e24b8-734">Requirements</span></span>



| <span data-ttu-id="e24b8-735">需求</span><span class="sxs-lookup"><span data-stu-id="e24b8-735">Requirement</span></span> | <span data-ttu-id="e24b8-736">值</span><span class="sxs-lookup"><span data-stu-id="e24b8-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e24b8-737">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e24b8-737">Minimum supported client</span></span><br/> | <span data-ttu-id="e24b8-738">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e24b8-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="e24b8-739">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e24b8-739">Minimum supported server</span></span><br/> | <span data-ttu-id="e24b8-740">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e24b8-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="e24b8-741">標頭</span><span class="sxs-lookup"><span data-stu-id="e24b8-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24b8-742"><dt>Wininet. h;</dt><dt>Winineti .h</dt></span><span class="sxs-lookup"><span data-stu-id="e24b8-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

