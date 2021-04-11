---
title: 'MpScanStart 函式 (MpClient) '
description: 啟動掃描工作。
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- MpScanStart 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934643"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="73f6e-104">MpScanStart 函式</span><span class="sxs-lookup"><span data-stu-id="73f6e-104">MpScanStart function</span></span>

<span data-ttu-id="73f6e-105">啟動掃描工作。</span><span class="sxs-lookup"><span data-stu-id="73f6e-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f6e-106">語法</span><span class="sxs-lookup"><span data-stu-id="73f6e-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="73f6e-107">參數</span><span class="sxs-lookup"><span data-stu-id="73f6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73f6e-108">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73f6e-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="73f6e-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="73f6e-110">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="73f6e-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="73f6e-111">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="73f6e-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="73f6e-112">*ScanType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73f6e-113">類型： **[ **MPSCAN \_ 類型**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="73f6e-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="73f6e-114">指定掃描的類型。</span><span class="sxs-lookup"><span data-stu-id="73f6e-114">Specifies the type of scan.</span></span> <span data-ttu-id="73f6e-115">此參數必須是 [**MPSCAN \_ 類型**](mpscan-type.md) enueration 的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="73f6e-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="73f6e-116">*dwScanOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73f6e-117">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="73f6e-117">Type: **DWORD**</span></span>

<span data-ttu-id="73f6e-118">指定掃描操作的各種選項。</span><span class="sxs-lookup"><span data-stu-id="73f6e-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="73f6e-119">值</span><span class="sxs-lookup"><span data-stu-id="73f6e-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="73f6e-120">意義</span><span class="sxs-lookup"><span data-stu-id="73f6e-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="73f6e-121"><dt>**MPSCAN \_ 選項 \_ NONE**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="73f6e-122">未要求特定的選項。</span><span class="sxs-lookup"><span data-stu-id="73f6e-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="73f6e-123"><dt>**MPSCAN \_ 選項 \_ ASYNC**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="73f6e-124">掃描工作是非同步，其中 **MpScanStart** 會在成功啟動掃描後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="73f6e-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="73f6e-125"> (預設掃描工作是同步的，這表示只有在掃描完成後才會傳回 **MpScanStart** 。 ) </span><span class="sxs-lookup"><span data-stu-id="73f6e-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="73f6e-126"><dt>**MPSCAN \_ 選項 \_ 進度**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="73f6e-127">呼叫端想要透過回呼接收掃描進度資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="73f6e-128"><dt>**MPSCAN \_ 選項 \_ LOWPRIORITY**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="73f6e-129">以低優先順序執行掃描。</span><span class="sxs-lookup"><span data-stu-id="73f6e-129">Perform the scan with low priority.</span></span> <span data-ttu-id="73f6e-130"> (預設會以一般優先順序執行掃描工作。 ) </span><span class="sxs-lookup"><span data-stu-id="73f6e-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="73f6e-131"><dt>**MPSCAN \_ 選項 \_ PACKEDEXES**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="73f6e-132">掃描封裝的可執行檔是否有可能的威脅。</span><span class="sxs-lookup"><span data-stu-id="73f6e-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="73f6e-133"><dt>**MPSCAN \_ 選項 \_ 封存**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="73f6e-134">掃描封存內容是否有可能的威脅。</span><span class="sxs-lookup"><span data-stu-id="73f6e-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="73f6e-135">封存是副檔名為 .zip、.cab 或 tar 的檔案。</span><span class="sxs-lookup"><span data-stu-id="73f6e-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="73f6e-136"><dt>**MPSCAN \_ 選項 \_ 啟發學習法**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="73f6e-137">啟用以啟發學習法為基礎的掃描。</span><span class="sxs-lookup"><span data-stu-id="73f6e-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="73f6e-138">這會掃描偵測類型設定為啟發學習法的威脅。</span><span class="sxs-lookup"><span data-stu-id="73f6e-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="73f6e-139"><dt>**MPSCAN \_ 選項 \_ REPORTFRIENDLY**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="73f6e-140">在資源掃描中報告易記專案。</span><span class="sxs-lookup"><span data-stu-id="73f6e-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="73f6e-141">這僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="73f6e-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="73f6e-142"><dt>**MPSCAN \_ 選項 \_ REPORTUNKNOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="73f6e-143">在資源掃描中報告未知的專案。</span><span class="sxs-lookup"><span data-stu-id="73f6e-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="73f6e-144">這僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="73f6e-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="73f6e-145"><dt>**MPSCAN \_ 選項 \_ NOCONSOLIDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="73f6e-146">請勿將掃描結果與全域威脅視圖合併。</span><span class="sxs-lookup"><span data-stu-id="73f6e-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="73f6e-147">這適用于用戶端 (例如，電子郵件客戶程式) 想要自行控制清理 UX，而不允許預設反惡意程式碼清理 UX。</span><span class="sxs-lookup"><span data-stu-id="73f6e-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="73f6e-148">這僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="73f6e-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73f6e-149">*pScanResources* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73f6e-150">類型： **PMPSCAN \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="73f6e-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="73f6e-151">掃描資源資訊的指標。</span><span class="sxs-lookup"><span data-stu-id="73f6e-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="73f6e-152">此參數必須是 **Null** ，才能進行快速掃描。</span><span class="sxs-lookup"><span data-stu-id="73f6e-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="73f6e-153">這是完整掃描的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="73f6e-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="73f6e-154">若為資源掃描，必須至少使用一個資源資訊結構來指定此參數。</span><span class="sxs-lookup"><span data-stu-id="73f6e-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="73f6e-155">若要掃描特定資源，呼叫端必須具有該資源的 **一般 \_ 讀取** 許可權。</span><span class="sxs-lookup"><span data-stu-id="73f6e-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="73f6e-156">請參閱 [**MPSCAN \_ 資源**](mpscan-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="73f6e-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="73f6e-157">*pCallbackInfo* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73f6e-158">類型： **PMPCALLBACK \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="73f6e-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="73f6e-159">用來將掃描狀態變更饋送至用戶端的回呼資訊指標 (例如開始和完成) 和進度資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="73f6e-160">回呼函式中傳回的 [**MPCALLBACK \_ 資料**](mpcallback-data.md) 會報告實際的掃描狀態和進度相關資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="73f6e-161">以下是可能的回呼清單：</span><span class="sxs-lookup"><span data-stu-id="73f6e-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="73f6e-162">值</span><span class="sxs-lookup"><span data-stu-id="73f6e-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="73f6e-163">意義</span><span class="sxs-lookup"><span data-stu-id="73f6e-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="73f6e-164"><dt>**MPNOTIFY \_ 掃描 \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="73f6e-165">掃描工作已啟動。</span><span class="sxs-lookup"><span data-stu-id="73f6e-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="73f6e-166"><dt>**MPNOTIFY \_ 掃描 \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="73f6e-167">掃描工作已完成。</span><span class="sxs-lookup"><span data-stu-id="73f6e-167">Scan operation completed.</span></span> <span data-ttu-id="73f6e-168">您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="73f6e-169"><dt>**MPNOTIFY \_ 掃描 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="73f6e-170">掃描操作已暫停。</span><span class="sxs-lookup"><span data-stu-id="73f6e-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="73f6e-171"><dt>**MPNOTIFY \_ 掃描已 \_ 繼續**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="73f6e-172">掃描工作已從暫停繼續。</span><span class="sxs-lookup"><span data-stu-id="73f6e-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="73f6e-173"><dt>**MPNOTIFY \_ 掃描 \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="73f6e-174">掃描操作已取消。</span><span class="sxs-lookup"><span data-stu-id="73f6e-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="73f6e-175"><dt>**MPNOTIFY \_ 掃描 \_ 進度**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="73f6e-176">掃描進度資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-176">Scan progress information.</span></span> <span data-ttu-id="73f6e-177">您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得額外的資訊 (例如資源統計資料) 。</span><span class="sxs-lookup"><span data-stu-id="73f6e-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="73f6e-178"><dt>**MPNOTIFY \_ 掃描 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="73f6e-179">掃描特定資源的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="73f6e-180">您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得特定的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="73f6e-181"><dt>**\_ \_ 受感染的 MPNOTIFY 掃描**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="73f6e-182">掃描找到受感染的資源。</span><span class="sxs-lookup"><span data-stu-id="73f6e-182">Scan found an infected resource.</span></span> <span data-ttu-id="73f6e-183">請注意，在大部分情況下，這會導致掃描結束時回報某些威脅。</span><span class="sxs-lookup"><span data-stu-id="73f6e-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="73f6e-184">有時候，由於排除專案的原因，可能無法具體化為威脅。</span><span class="sxs-lookup"><span data-stu-id="73f6e-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="73f6e-185">您可以透過 [**MPSCAN \_ 資料**](mpscan-data.md) 結構取得其他受感染的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="73f6e-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="73f6e-186"><dt>**MPNOTIFY \_ 掃描 \_ MEMORYSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="73f6e-187">完整掃描的快速掃描部分已開始。</span><span class="sxs-lookup"><span data-stu-id="73f6e-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="73f6e-188"><dt>**MPNOTIFY \_ 掃描 \_ MEMORYCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="73f6e-189">完整掃描的快速掃描部分已完成。</span><span class="sxs-lookup"><span data-stu-id="73f6e-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="73f6e-190"><dt>**MPNOTIFY \_ 內部 \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="73f6e-191">掃描工作遇到一般失敗。</span><span class="sxs-lookup"><span data-stu-id="73f6e-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="73f6e-192">[**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 具有特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73f6e-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="73f6e-193">*phScanHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73f6e-194">類型： **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="73f6e-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="73f6e-195">傳回的掃描控制碼，識別目前起始的掃描。</span><span class="sxs-lookup"><span data-stu-id="73f6e-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="73f6e-196">這個控制碼可用於後續的函式呼叫，例如取出掃描結果。</span><span class="sxs-lookup"><span data-stu-id="73f6e-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="73f6e-197">控制碼必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉。</span><span class="sxs-lookup"><span data-stu-id="73f6e-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73f6e-198">傳回值</span><span class="sxs-lookup"><span data-stu-id="73f6e-198">Return value</span></span>

<span data-ttu-id="73f6e-199">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="73f6e-199">Type: **HRESULT**</span></span>

<span data-ttu-id="73f6e-200">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="73f6e-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="73f6e-201">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="73f6e-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="73f6e-202">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="73f6e-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f6e-203">規格需求</span><span class="sxs-lookup"><span data-stu-id="73f6e-203">Requirements</span></span>



| <span data-ttu-id="73f6e-204">需求</span><span class="sxs-lookup"><span data-stu-id="73f6e-204">Requirement</span></span> | <span data-ttu-id="73f6e-205">值</span><span class="sxs-lookup"><span data-stu-id="73f6e-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73f6e-206">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73f6e-206">Minimum supported client</span></span><br/> | <span data-ttu-id="73f6e-207">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="73f6e-208">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73f6e-208">Minimum supported server</span></span><br/> | <span data-ttu-id="73f6e-209">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73f6e-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73f6e-210">標頭</span><span class="sxs-lookup"><span data-stu-id="73f6e-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="73f6e-211"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="73f6e-212">DLL</span><span class="sxs-lookup"><span data-stu-id="73f6e-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73f6e-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73f6e-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73f6e-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73f6e-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f6e-215">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="73f6e-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="73f6e-216">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="73f6e-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="73f6e-217">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="73f6e-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="73f6e-218">**MPCALLBACK \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="73f6e-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="73f6e-219">**MPSCAN \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="73f6e-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="73f6e-220">**MPSCAN \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="73f6e-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="73f6e-221">**MPSCAN \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="73f6e-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 





