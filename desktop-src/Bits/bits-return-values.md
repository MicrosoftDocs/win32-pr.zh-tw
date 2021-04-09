---
title: BITS 傳回值
description: Bitsmsg 檔案包含下列傳回值常數。
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- 錯誤位
- 錯誤位，代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933485"
---
# <a name="bits-return-values"></a><span data-ttu-id="58d46-105">BITS 傳回值</span><span class="sxs-lookup"><span data-stu-id="58d46-105">BITS Return Values</span></span>

<span data-ttu-id="58d46-106">Bitsmsg 檔案包含下列傳回值常數。</span><span class="sxs-lookup"><span data-stu-id="58d46-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="58d46-107">常數代表 BITS 產生的傳回值，以及 BITS 所捕捉的 HTTP 傳回值。</span><span class="sxs-lookup"><span data-stu-id="58d46-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="58d46-108">您可以接收的所有其他傳回值為 COM、RPC 或轉換的 Windows 傳回值 (位使用 [ \_ \_ WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) 宏的 hresult 將 windows 傳回值轉換成 hresult 值) 。</span><span class="sxs-lookup"><span data-stu-id="58d46-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="58d46-109">請注意，Bitsmsg 檔案包含以下未列出的其他傳回值。</span><span class="sxs-lookup"><span data-stu-id="58d46-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="58d46-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG \_ S \_ 部分 \_ 完整 (0x00200017) </span><span class="sxs-lookup"><span data-stu-id="58d46-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-111">在呼叫 [**IBackgroundCopyJob：： Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) 方法之前，已成功傳輸作業檔案的子集。</span><span class="sxs-lookup"><span data-stu-id="58d46-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="58d46-112">未完成的已刪除。</span><span class="sxs-lookup"><span data-stu-id="58d46-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ \_ 無法 \_ 刪除檔案 \_ \_ (0x0020001A) </span><span class="sxs-lookup"><span data-stu-id="58d46-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-114">無法刪除與作業相關聯的所有暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="58d46-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>\_ \_ \_ 由原則覆寫的 BG \_ (0x00200055) </span><span class="sxs-lookup"><span data-stu-id="58d46-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-116">已成功儲存設定喜好設定，但因為設定的群組原則設定會覆寫喜好設定，所以不會使用喜好設定。</span><span class="sxs-lookup"><span data-stu-id="58d46-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>\_ \_ \_ (0x80200001) 找不到 BG E</span><span class="sxs-lookup"><span data-stu-id="58d46-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-118">找不到要求的作業。</span><span class="sxs-lookup"><span data-stu-id="58d46-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG \_ E \_ 不正確 \_ 狀態 (0x80200002) </span><span class="sxs-lookup"><span data-stu-id="58d46-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-120">目前的作業狀態不允許要求的動作。</span><span class="sxs-lookup"><span data-stu-id="58d46-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ EMPTY (0x80200003) </span><span class="sxs-lookup"><span data-stu-id="58d46-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-122">作業必須包含一或多個檔案，您才能繼續作業。</span><span class="sxs-lookup"><span data-stu-id="58d46-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>\_無法使用 BG E 檔案 \_ \_ \_ (0x80200004) </span><span class="sxs-lookup"><span data-stu-id="58d46-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-124">因為錯誤未與本機或遠端檔案相關聯，所以無法使用檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="58d46-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG \_ E \_ 通訊協定 \_ 無法 \_ 使用 (0x80200005) </span><span class="sxs-lookup"><span data-stu-id="58d46-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-126">因為錯誤未與指定的傳輸通訊協定相關聯，所以無法使用通訊協定資訊。</span><span class="sxs-lookup"><span data-stu-id="58d46-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E \_ 目的地已 \_ 鎖定 (0x8020000D) </span><span class="sxs-lookup"><span data-stu-id="58d46-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-128">本機檔案名中指定的目的地檔案系統磁片區已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="58d46-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG \_ E \_ 磁片區 \_ 變更 (0x8020000E) </span><span class="sxs-lookup"><span data-stu-id="58d46-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-130">本機檔案名中指定的目的地磁片區已變更。</span><span class="sxs-lookup"><span data-stu-id="58d46-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="58d46-131">例如，原始磁片磁碟機已被不同的磁片磁碟機取代。</span><span class="sxs-lookup"><span data-stu-id="58d46-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_ \_ \_ \_ (0X8020000F) 無法使用 BG E 錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="58d46-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-133">只有當作業的狀態為 [BG 作業狀態] 錯誤時，才可使用錯誤資訊 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="58d46-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="58d46-134">在 BITS 開始傳送作業的資料或用戶端結束之後，無法使用錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="58d46-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ 網路已 \_ 中斷連線 (0x80200010) </span><span class="sxs-lookup"><span data-stu-id="58d46-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-136">網路介面卡為非使用中或已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="58d46-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="58d46-137">所有作業都會處於「BG \_ 作業 \_ 狀態」 \_ 暫時性 \_ 錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="58d46-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ 遺失 \_ 檔案 \_ 大小 (0x80200011) </span><span class="sxs-lookup"><span data-stu-id="58d46-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-139">伺服器未傳回檔案大小。</span><span class="sxs-lookup"><span data-stu-id="58d46-139">The server did not return the file size.</span></span> <span data-ttu-id="58d46-140">BITS 只會傳送靜態內容，而且需要 HTTP 伺服器傳回內容長度標頭。</span><span class="sxs-lookup"><span data-stu-id="58d46-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="58d46-141">如果 URL 指向動態內容，傳送要求就會失敗。</span><span class="sxs-lookup"><span data-stu-id="58d46-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG \_ E \_ \_ HTTP \_ 支援 (0x80200012) </span><span class="sxs-lookup"><span data-stu-id="58d46-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-143">伺服器不支援 HTTP/1.1 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="58d46-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG \_ E \_ 的 \_ 範圍 \_ 支援 (0x80200013) </span><span class="sxs-lookup"><span data-stu-id="58d46-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-145">伺服器不支援內容約制標頭。</span><span class="sxs-lookup"><span data-stu-id="58d46-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="58d46-146">一般來說，當您嘗試下載動態內容時，您會收到這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="58d46-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="58d46-147">如果中繼 proxy 正在移除內容約制或內容長度標頭，您也可能會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="58d46-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>\_ \_ 不支援 BG E 遠端 \_ \_ (0x80200014) </span><span class="sxs-lookup"><span data-stu-id="58d46-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-149">不支援 BITS 的遠端使用。</span><span class="sxs-lookup"><span data-stu-id="58d46-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="58d46-150">如需詳細資訊，請參閱 [使用者和網路連接](users-and-network-connections.md)。</span><span class="sxs-lookup"><span data-stu-id="58d46-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="58d46-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ 新的 \_ 擁有者 \_ 差異 \_ 對應 (0x80200015) </span><span class="sxs-lookup"><span data-stu-id="58d46-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-152">本機檔案的網路磁碟機機對應與先前擁有者的目前擁有者不同。</span><span class="sxs-lookup"><span data-stu-id="58d46-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ 新 \_ 擁有 \_ 者 \_ 沒有 \_ (0x80200016) 的檔案存取權</span><span class="sxs-lookup"><span data-stu-id="58d46-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-154">新擁有者的許可權不足，無法暫存工作檔案。</span><span class="sxs-lookup"><span data-stu-id="58d46-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG \_ E \_ PROXY \_ 列出 \_ 太 \_ 大的 (0x80200018) </span><span class="sxs-lookup"><span data-stu-id="58d46-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-156">HTTP proxy 清單太長。</span><span class="sxs-lookup"><span data-stu-id="58d46-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="58d46-157">清單不得超過 32 KB。</span><span class="sxs-lookup"><span data-stu-id="58d46-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG \_ E \_ PROXY \_ 略過 \_ 清單 \_ 太 \_ 大 (0x80200019) </span><span class="sxs-lookup"><span data-stu-id="58d46-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-159">HTTP proxy 略過清單太長。</span><span class="sxs-lookup"><span data-stu-id="58d46-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="58d46-160">清單不得超過 32 KB。</span><span class="sxs-lookup"><span data-stu-id="58d46-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ % \_ \_ \_ (0x8020001C) 的檔太多</span><span class="sxs-lookup"><span data-stu-id="58d46-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-162">您無法將一個以上的檔案新增至上傳作業。</span><span class="sxs-lookup"><span data-stu-id="58d46-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG \_ E \_ 本機 \_ 檔 \_ 已變更 (0x8020001D) </span><span class="sxs-lookup"><span data-stu-id="58d46-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-164">本機檔案的內容會在傳送程式開始之後變更。</span><span class="sxs-lookup"><span data-stu-id="58d46-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="58d46-165">在上傳或上傳回復作業開始傳送程式之後，無法變更本機檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="58d46-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ 太 \_ 大 (0x80200020) </span><span class="sxs-lookup"><span data-stu-id="58d46-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-167">上傳檔案的大小超過伺服器上指定的允許上傳大小上限。</span><span class="sxs-lookup"><span data-stu-id="58d46-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG \_ E \_ 字串 \_ 太 \_ 長 (0x80200021) </span><span class="sxs-lookup"><span data-stu-id="58d46-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-169">指定的字串太長。</span><span class="sxs-lookup"><span data-stu-id="58d46-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG \_ E \_ 用戶端 \_ 伺服器 \_ 通訊協定 \_ 不相符 (0x80200022) </span><span class="sxs-lookup"><span data-stu-id="58d46-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-171">用戶端和伺服器無法協商要用於上傳作業的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="58d46-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_ \_ 已啟用 BG E SERVER \_ 執行 \_ (0x80200023) </span><span class="sxs-lookup"><span data-stu-id="58d46-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-173">腳本或執行許可權會在與作業相關聯的 IIS 虛擬目錄上啟用。</span><span class="sxs-lookup"><span data-stu-id="58d46-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="58d46-174">若要將檔案上傳至虛擬目錄，請停用虛擬目錄的腳本和執行許可權。</span><span class="sxs-lookup"><span data-stu-id="58d46-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E 使用者 \_ 名稱 \_ 太 \_ 大 (0x80200025) </span><span class="sxs-lookup"><span data-stu-id="58d46-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-176">使用者名稱不能超過300個字元。</span><span class="sxs-lookup"><span data-stu-id="58d46-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E \_ 密碼 \_ 太 \_ 大 (0x80200026) </span><span class="sxs-lookup"><span data-stu-id="58d46-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-178">密碼不能超過65535個字元。</span><span class="sxs-lookup"><span data-stu-id="58d46-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ 不正確 \_ 驗證 \_ 目標 (0x80200027) </span><span class="sxs-lookup"><span data-stu-id="58d46-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-180">指定的驗證目標無效。</span><span class="sxs-lookup"><span data-stu-id="58d46-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ 不正確 \_ 驗證 \_ 配置 (0x80200028) </span><span class="sxs-lookup"><span data-stu-id="58d46-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-182">指定的驗證配置無效。</span><span class="sxs-lookup"><span data-stu-id="58d46-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E \_ 不正確 \_ 範圍 (0x8020002B) </span><span class="sxs-lookup"><span data-stu-id="58d46-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-184">指定的位元組範圍無效。</span><span class="sxs-lookup"><span data-stu-id="58d46-184">The specified byte range is invalid.</span></span> <span data-ttu-id="58d46-185">位元組範圍必須存在於指定的遠端檔案中。</span><span class="sxs-lookup"><span data-stu-id="58d46-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG \_ E 重 \_ 迭 \_ 範圍 (0x8020002C) </span><span class="sxs-lookup"><span data-stu-id="58d46-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-187">位元組範圍清單包含重迭或重複的範圍，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="58d46-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ \_ \_ (0x8020003E) 的原則封鎖</span><span class="sxs-lookup"><span data-stu-id="58d46-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-189">群組原則設定會防止背景工作在此時間執行。</span><span class="sxs-lookup"><span data-stu-id="58d46-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="58d46-190">如需詳細資訊，請參閱 [MaxInternetBandwidth](group-policies.md) 原則。</span><span class="sxs-lookup"><span data-stu-id="58d46-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E \_ 不正確 \_ PROXY \_ 資訊 (0x8020003F) </span><span class="sxs-lookup"><span data-stu-id="58d46-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-192">指出您使用 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 方法指定的 proxy 清單或 proxy 略過清單不正確執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="58d46-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ 不正確 \_ 認證 (0x80200040) </span><span class="sxs-lookup"><span data-stu-id="58d46-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-194">提供的安全性認證格式無效。</span><span class="sxs-lookup"><span data-stu-id="58d46-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_ \_ 已刪除 BG E 記錄 \_ (0x80200042) </span><span class="sxs-lookup"><span data-stu-id="58d46-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-196">快取記錄已刪除。</span><span class="sxs-lookup"><span data-stu-id="58d46-196">The cache record has been deleted.</span></span> <span data-ttu-id="58d46-197">嘗試更新它已被放棄。</span><span class="sxs-lookup"><span data-stu-id="58d46-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG \_ E \_ UPNP \_ 錯誤 (0x80200045) </span><span class="sxs-lookup"><span data-stu-id="58d46-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-199">發生通用隨插即用 (UPnP) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="58d46-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="58d46-200">請檢查您的網際網路閘道裝置。</span><span class="sxs-lookup"><span data-stu-id="58d46-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>\_已停用 BG E 對等 \_ \_ (0x80200047) </span><span class="sxs-lookup"><span data-stu-id="58d46-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-202">對等快取已停用。</span><span class="sxs-lookup"><span data-stu-id="58d46-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048) </span><span class="sxs-lookup"><span data-stu-id="58d46-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-204">快取記錄正在使用中，無法變更或刪除。</span><span class="sxs-lookup"><span data-stu-id="58d46-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="58d46-205">請在幾秒後再試一次。</span><span class="sxs-lookup"><span data-stu-id="58d46-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ \_ \_ \_ \_ \_ (0x80200049) 的每位使用者太多作業</span><span class="sxs-lookup"><span data-stu-id="58d46-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-207">使用者的作業計數已超過 MaxJobsPerUser 群組原則設定所設定的每個使用者作業限制。</span><span class="sxs-lookup"><span data-stu-id="58d46-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ \_ \_ \_ \_ 每 \_ 台電腦 (0x80200050) 的作業太多</span><span class="sxs-lookup"><span data-stu-id="58d46-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-209">電腦的工作計數已超過 MaxJobsPerMachine 群組原則設定所設定的每一電腦作業限制。</span><span class="sxs-lookup"><span data-stu-id="58d46-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ \_ \_ \_ \_ (0x80200051) 中有太多檔案在 \_ 工作中</span><span class="sxs-lookup"><span data-stu-id="58d46-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-211">作業的檔案計數已超過 MaxFilesPerJob 群組原則設定所設定的每個作業檔限制。</span><span class="sxs-lookup"><span data-stu-id="58d46-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG% 檔案 \_ \_ \_ \_ \_ (0x80200052 中有太多範圍 \_) </span><span class="sxs-lookup"><span data-stu-id="58d46-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-213">檔案的範圍計數已超過 MaxRangesPerFile 群組原則設定所設定的每個檔案範圍限制。</span><span class="sxs-lookup"><span data-stu-id="58d46-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG \_ E \_ 驗證 \_ 失敗 (0x80200053) </span><span class="sxs-lookup"><span data-stu-id="58d46-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-215">應用程式要求來自網站的資料，但回應無效。</span><span class="sxs-lookup"><span data-stu-id="58d46-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="58d46-216">如需詳細資訊，請使用事件檢視器來查看 \\ Microsoft \\ Windows \\ Bits-用戶端作業記錄檔的應用程式記錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="58d46-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG \_ E \_ MAXDOWNLOAD \_ TIMEOUT (0x80200054) </span><span class="sxs-lookup"><span data-stu-id="58d46-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-218">BITS 的下載作業已超時。</span><span class="sxs-lookup"><span data-stu-id="58d46-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="58d46-219">下載作業未在作業或 MaxDownloadTime 群組原則設定上設定的下載時間上限內完成。</span><span class="sxs-lookup"><span data-stu-id="58d46-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 400 (0x80190190) </span><span class="sxs-lookup"><span data-stu-id="58d46-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-221">伺服器無法處理傳送要求，因為遠端檔案名的語法無效。</span><span class="sxs-lookup"><span data-stu-id="58d46-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 401 (0x80190191) </span><span class="sxs-lookup"><span data-stu-id="58d46-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-223">使用者沒有存取遠端檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="58d46-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="58d46-224">要求的資源需要進行使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="58d46-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 404 (0x80190194) </span><span class="sxs-lookup"><span data-stu-id="58d46-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-226">要求的 URL 不存在於伺服器上。</span><span class="sxs-lookup"><span data-stu-id="58d46-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="58d46-227">在 IIS 7 中，此錯誤可能表示</span><span class="sxs-lookup"><span data-stu-id="58d46-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="58d46-228">在伺服器上 (vdir) 的虛擬目錄上，不會啟用該位上傳。</span><span class="sxs-lookup"><span data-stu-id="58d46-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="58d46-229">上傳大小超過最大上傳限制 (如需詳細資訊，請參閱 [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS 延伸模組屬性) 。</span><span class="sxs-lookup"><span data-stu-id="58d46-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="58d46-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 407 (0x80190197) </span><span class="sxs-lookup"><span data-stu-id="58d46-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-231">使用者沒有存取 proxy 的許可權。</span><span class="sxs-lookup"><span data-stu-id="58d46-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="58d46-232">Proxy 需要使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="58d46-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 414 (0x8019019E) </span><span class="sxs-lookup"><span data-stu-id="58d46-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-234">伺服器無法處理傳送要求。</span><span class="sxs-lookup"><span data-stu-id="58d46-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="58d46-235">遠端檔案名 (URI) 的統一資源識別項長度超過伺服器可解讀的長度。</span><span class="sxs-lookup"><span data-stu-id="58d46-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 501 (0x801901F5) </span><span class="sxs-lookup"><span data-stu-id="58d46-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-237">伺服器不支援完成要求所需的功能。</span><span class="sxs-lookup"><span data-stu-id="58d46-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="58d46-238">在 IIS 6 中，此錯誤表示伺服器上 (vdir) 的虛擬目錄上未啟用 BITS 上傳。</span><span class="sxs-lookup"><span data-stu-id="58d46-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 503 (0x801901F7) </span><span class="sxs-lookup"><span data-stu-id="58d46-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-240">服務暫時超載，無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="58d46-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="58d46-241">稍後再繼續作業。</span><span class="sxs-lookup"><span data-stu-id="58d46-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 504 (0x801901F8) </span><span class="sxs-lookup"><span data-stu-id="58d46-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-243">等候閘道時，傳送要求超時。</span><span class="sxs-lookup"><span data-stu-id="58d46-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="58d46-244">稍後再繼續作業。</span><span class="sxs-lookup"><span data-stu-id="58d46-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="58d46-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E \_ HTTP \_ 錯誤 \_ 505 (0x801901F9) </span><span class="sxs-lookup"><span data-stu-id="58d46-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="58d46-246">伺服器不支援遠端檔案名中指定的 HTTP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="58d46-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="58d46-247">Bitsmsg 標頭檔包含上面未列出的額外 HTTP 傳回值，位在內部使用。</span><span class="sxs-lookup"><span data-stu-id="58d46-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="58d46-248">如需這些和其他您可以接收之 HTTP 傳回值的相關資訊，請參閱來自網際網路工程任務推動小組的 RFC 2616 規格 [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) 。</span><span class="sxs-lookup"><span data-stu-id="58d46-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 