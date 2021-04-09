---
title: 傳回值
description: 下列常數代表傳遞最佳化 () 產生的傳回值，以及會捕捉的 HTTP 傳回值。
ms.assetid: 68AC4581-C748-49AB-A588-15816E534756
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e58d66587061cc44fc441249407b73653153322
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023835"
---
# <a name="do-return-values"></a><span data-ttu-id="6d2a2-103">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d2a2-103">DO Return Values</span></span>

<span data-ttu-id="6d2a2-104">下列常數代表傳遞最佳化 () 產生的傳回值，以及會捕捉的 HTTP 傳回值。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-104">The below constants represent return values that Delivery Optimization (DO) generates and HTTP return values that DO captures.</span></span> <span data-ttu-id="6d2a2-105">您可以接收的所有其他傳回值為 COM、RPC 或轉換的 Windows 傳回值 (使用 [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) 宏將 windows 傳回值轉換成 HRESULT 值) 。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-105">All other return values that you can receive are COM, RPC, or converted Windows return values (DO uses the [HRESULT_FROM_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<dl> <dt>

<span data-ttu-id="6d2a2-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-106"><span id="DO_E_NO_SERVICE__0x80d01001_"></span><span id="do_e_no_service__0x80d01001_"></span><span id="DO_E_NO_SERVICE__0X80D01001_"></span>DO_E_NO_SERVICE (0x80d01001)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-107">傳遞最佳化無法提供服務。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-107">Delivery Optimization was unable to provide the service.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-108"><span id="DO_E_DOWNLOAD_NO_PROGRESS__0x80d02002_"></span><span id="do_e_download_no_progress__0x80d02002_"></span><span id="DO_E_DOWNLOAD_NO_PROGRESS__0X80D02002_"></span>DO_E_DOWNLOAD_NO_PROGRESS (0x80d02002)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-109">下載檔案在定義的期間內未看到任何進度。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-109">Download of a file saw no progress within the defined period.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-110"><span id="DO_E_JOB_NOT_FOUND__0x80d02003_"></span><span id="do_e_job_not_found__0x80d02003_"></span><span id="DO_E_JOB_NOT_FOUND__0X80D02003_"></span>DO_E_JOB_NOT_FOUND (0x80d02003)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-111">找不到作業，預期會有作業。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-111">Job was not found, expecting a job to be present.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-112"><span id="DO_E_JOB_EMPTY__0x80d02004_"></span><span id="do_e_job_empty__0x80d02004_"></span><span id="DO_E_JOB_EMPTY__0X80D02004_"></span>DO_E_JOB_EMPTY (0x80d02004)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-113">作業中沒有任何檔案，至少需要一個檔案。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-113">There was no file in the job, expecting at least one file.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-114"><span id="DO_E_LOCALPATH_NOT_SET__0x80d0200d_"></span><span id="do_e_localpath_not_set__0x80d0200d_"></span><span id="DO_E_LOCALPATH_NOT_SET__0X80D0200D_"></span>DO_E_LOCALPATH_NOT_SET (0x80d0200d)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-115">未指定此下載的本機檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-115">There is no local file path specified for this download.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-116"><span id="DO_E_FILE_NOT_AVAILABLE__0x80d02010_"></span><span id="do_e_file_not_available__0x80d02010_"></span><span id="DO_E_FILE_NOT_AVAILABLE__0X80D02010_"></span>DO_E_FILE_NOT_AVAILABLE (0x80d02010)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-117">沒有任何檔案可供使用，因為沒有任何 URL 產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-117">No file is available because no URL generated an error.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-118"><span id="DO_E_UNKNOWN_PROPERTY_ID__0x80d02011_"></span><span id="do_e_unknown_property_id__0x80d02011_"></span><span id="DO_E_UNKNOWN_PROPERTY_ID__0X80D02011_"></span>DO_E_UNKNOWN_PROPERTY_ID (0x80d02011)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-119">使用未知的屬性識別碼呼叫 SetProperty () 或 GetProperty () 。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-119">SetProperty() or GetProperty() called with an unknown property ID.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-120"><span id="DO_E_READ_ONLY_PROPERTY__0x80d02012_"></span><span id="do_e_read_only_property__0x80d02012_"></span><span id="DO_E_READ_ONLY_PROPERTY__0X80D02012_"></span>DO_E_READ_ONLY_PROPERTY (0x80d02012)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-121">無法在唯讀屬性上呼叫 SetProperty () 。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-121">Unable to call SetProperty() on a read-only property.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-122"><span id="DO_E_INVALID_STATE__0x80d02013_"></span><span id="do_e_invalid_state__0x80d02013_"></span><span id="DO_E_INVALID_STATE__0X80D02013_"></span>DO_E_INVALID_STATE (0x80d02013)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-123">目前的作業狀態不允許要求的動作。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-123">The requested action is not allowed in the current job state.</span></span> <span data-ttu-id="6d2a2-124">作業可能已取消或已完成傳輸。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-124">The job might have been canceled or completed transferring.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-125"><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0x80d02014_"></span><span id="do_e_error_information_unavailable__0x80d02014_"></span><span id="DO_E_ERROR_INFORMATION_UNAVAILABLE__0X80D02014_"></span>DO_E_ERROR_INFORMATION_UNAVAILABLE (0x80d02014)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-126">未發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-126">No errors have occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-127"><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0x80d03002_"></span><span id="do_e_no_download_extsettings__0x80d03002_"></span><span id="DO_E_NO_DOWNLOAD_EXTSETTINGS__0X80D03002_"></span>DO_E_NO_DOWNLOAD_EXTSETTINGS (0x80d03002)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-128">因為使用者/系統管理員設定，所以不允許下載作業。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-128">Download job not allowed due to user/admin settings.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-129"><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0x80d03801_"></span><span id="do_e_blocked_by_cost_transfer_policy__0x80d03801_"></span><span id="DO_E_BLOCKED_BY_COST_TRANSFER_POLICY__0X80D03801_"></span>DO_E_BLOCKED_BY_COST_TRANSFER_POLICY (0x80d03801)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-130">因為成本原則限制而暫停工作。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-130">DO paused the job due to cost policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-131"><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0x80d03803_"></span><span id="do_e_blocked_by_cellular_policy__0x80d03803_"></span><span id="DO_E_BLOCKED_BY_CELLULAR_POLICY__0X80D03803_"></span>DO_E_BLOCKED_BY_CELLULAR_POLICY (0x80d03803)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-132">因為偵測到行動電話通訊網路和原則限制，所以已暫停工作。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-132">DO paused the job due to detection of cellular network and policy restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-133"><span id="DO_E_BLOCKED_BY_POWER_STATE__0x80d03804_"></span><span id="do_e_blocked_by_power_state__0x80d03804_"></span><span id="DO_E_BLOCKED_BY_POWER_STATE__0X80D03804_"></span>DO_E_BLOCKED_BY_POWER_STATE (0x80d03804)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-134">因為偵測到電源狀態變更為非 AC 模式，所以請暫停作業。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-134">DO paused the job due to detection of power state change into non-AC mode.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-135"><span id="DO_E_BLOCKED_BY_NO_NETWORK__0x80d03805_"></span><span id="do_e_blocked_by_no_network__0x80d03805_"></span><span id="DO_E_BLOCKED_BY_NO_NETWORK__0X80D03805_"></span>DO_E_BLOCKED_BY_NO_NETWORK (0x80d03805)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-136">因為網路連線中斷，所以請暫停作業。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-136">DO paused the job due to loss of network connectivity.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-137"><span id="DO_E_BLOCKED_BY_VPN_POLICY__0x80d03807_"></span><span id="do_e_blocked_by_vpn_policy__0x80d03807_"></span><span id="DO_E_BLOCKED_BY_VPN_POLICY__0X80D03807_"></span>DO_E_BLOCKED_BY_VPN_POLICY (0x80d03807)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-138">因為偵測到 VPN 網路，所以已暫停完成的工作。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-138">DO paused the completed job due to detection of VPN network.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-139"><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0x80d03808_"></span><span id="do_e_blocked_by_critical_memory_usage__0x80d03808_"></span><span id="DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE__0X80D03808_"></span>DO_E_BLOCKED_BY_CRITICAL_MEMORY_USAGE (0x80d03808)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-140">因為偵測到系統上的嚴重記憶體使用量，所以已暫停完成的工作。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-140">DO paused the completed job due to detection of critical memory usage on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-141"><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0x80d05001_"></span><span id="do_e_http_blocksize_mismatch__0x80d05001_"></span><span id="DO_E_HTTP_BLOCKSIZE_MISMATCH__0X80D05001_"></span>DO_E_HTTP_BLOCKSIZE_MISMATCH (0x80d05001)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-142">HTTP 伺服器傳回資料大小不等於所要求的回應。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-142">HTTP server returned a response with data size not equal to what was requested.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-143"><span id="DO_E_INVALID_RANGE__0x80d05010_"></span><span id="do_e_invalid_range__0x80d05010_"></span><span id="DO_E_INVALID_RANGE__0X80D05010_"></span>DO_E_INVALID_RANGE (0x80d05010)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-144">指定的位元組範圍無效。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-144">The specified byte range is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-145"><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0x80d05011_"></span><span id="do_e_insufficient_range_support__0x80d05011_"></span><span id="DO_E_INSUFFICIENT_RANGE_SUPPORT__0X80D05011_"></span>DO_E_INSUFFICIENT_RANGE_SUPPORT (0x80d05011)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-146">伺服器不支援必要的 HTTP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-146">The server does not support the necessary HTTP protocol.</span></span> <span data-ttu-id="6d2a2-147">傳遞最佳化 () 需要伺服器支援範圍通訊協定標頭。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-147">Delivery Optimization (DO) requires that the server support the Range protocol header.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-148"><span id="DO_E_OVERLAPPING_RANGES__0x80d05012_"></span><span id="do_e_overlapping_ranges__0x80d05012_"></span><span id="DO_E_OVERLAPPING_RANGES__0X80D05012_"></span>DO_E_OVERLAPPING_RANGES (0x80d05012)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-149">位元組範圍清單包含一些重迭的範圍，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-149">The list of byte ranges contains some overlapping ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6d2a2-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802) </span><span class="sxs-lookup"><span data-stu-id="6d2a2-150"><span id="DO_E_FATAL_CORE_ERROR__0x80d06802_"></span><span id="do_e_fatal_core_error__0x80d06802_"></span><span id="DO_E_FATAL_CORE_ERROR__0X80D06802_"></span>DO_E_FATAL_CORE_ERROR (0x80d06802)</span></span>
</dt> <dd>

<span data-ttu-id="6d2a2-151">核心發生嚴重錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d2a2-151">Fatal error encountered in core.</span></span>

</dd> </dl>

 

 