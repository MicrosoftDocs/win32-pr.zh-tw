---
title: 'MpUpdateStart 函式 (MpClient) '
description: 開始簽名更新作業。
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- MpUpdateStart 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466653"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="6099a-104">MpUpdateStart 函式</span><span class="sxs-lookup"><span data-stu-id="6099a-104">MpUpdateStart function</span></span>

<span data-ttu-id="6099a-105">開始簽名更新作業。</span><span class="sxs-lookup"><span data-stu-id="6099a-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6099a-106">語法</span><span class="sxs-lookup"><span data-stu-id="6099a-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="6099a-107">參數</span><span class="sxs-lookup"><span data-stu-id="6099a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6099a-108">*hMpHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6099a-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6099a-109">類型： **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="6099a-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="6099a-110">惡意程式碼防護管理員介面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6099a-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="6099a-111">[**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="6099a-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6099a-112">*dwUpdateOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6099a-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6099a-113">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6099a-113">Type: **DWORD**</span></span>

<span data-ttu-id="6099a-114">指定簽章更新作業的選項。</span><span class="sxs-lookup"><span data-stu-id="6099a-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="6099a-115">它可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="6099a-115">It can be one of the following values:</span></span>



| <span data-ttu-id="6099a-116">值</span><span class="sxs-lookup"><span data-stu-id="6099a-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="6099a-117">意義</span><span class="sxs-lookup"><span data-stu-id="6099a-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="6099a-118"><dt>**MPUPDATE \_ 選項 \_ NONE**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="6099a-119">未要求特定的選項。</span><span class="sxs-lookup"><span data-stu-id="6099a-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="6099a-120"><dt>**MPUPDATE \_ 選項 \_ ASYNC**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="6099a-121">更新作業是非同步，在此情況下， **MpUpdateStart** 會在成功初始化簽章更新之後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="6099a-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="6099a-122"> (根據預設，更新作業是同步的，這表示只有在簽章更新完成後才會傳回 **MpUpdateStart** 。 ) </span><span class="sxs-lookup"><span data-stu-id="6099a-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="6099a-123"><dt>**MPUPDATE \_ 選項 \_ 進度**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="6099a-124">呼叫端想要透過回呼接收簽章更新進度資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="6099a-125"><dt>**MPUPDATE \_ 選項 \_ HTTP**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="6099a-126">您可以從 Microsoft security 入口網站下載完整的簽章套件來執行簽章更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="6099a-127">如果用戶端透過 Microsoft Update 遇到簽章下載問題，則可以使用此選項做為回復選項。</span><span class="sxs-lookup"><span data-stu-id="6099a-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="6099a-128"><dt>**MPUPDATE \_ 選項 \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="6099a-129">使用 UNC 共用的直接下載來執行簽章更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="6099a-130"><dt>**MPUPDATE \_ 選項 \_ 管理**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="6099a-131">使用受管理的服務 WSUS 執行簽章更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="6099a-132"><dt>**\_ \_ 未受管理的 MPUPDATE 選項**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="6099a-133">使用非受控服務 MU/WU 執行簽章更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="6099a-134">*pCallbackInfo* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6099a-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6099a-135">類型： **PMPCALLBACK \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="6099a-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="6099a-136">用來以簽章更新狀態變更饋送用戶端的回呼資訊指標 (例如開始和完成) 和進度資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="6099a-137">回呼函數中傳回的 [**MPCALLBACK \_ 資料**](mpcallback-data.md) 會報告實際的更新狀態和進度相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="6099a-138">以下是可能的回呼清單：</span><span class="sxs-lookup"><span data-stu-id="6099a-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="6099a-139">值</span><span class="sxs-lookup"><span data-stu-id="6099a-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="6099a-140">意義</span><span class="sxs-lookup"><span data-stu-id="6099a-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="6099a-141"><dt>**MPNOTIFY \_ SIGUPDATE \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="6099a-142">更新作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="6099a-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="6099a-143"><dt>**MPNOTIFY \_ SIGUPDATE \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="6099a-144">更新作業已完成。</span><span class="sxs-lookup"><span data-stu-id="6099a-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="6099a-145"><dt>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="6099a-146">開始搜尋更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="6099a-147"><dt>**MPNOTIFY \_ SIGUPDATE \_ 搜尋 \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="6099a-148">搜尋已完成的更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-148">Search for updates completed.</span></span> <span data-ttu-id="6099a-149">您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="6099a-150"><dt>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="6099a-151">已開始更新下載。</span><span class="sxs-lookup"><span data-stu-id="6099a-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="6099a-152"><dt>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 進度**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="6099a-153">下載進度資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-153">Download progress information.</span></span> <span data-ttu-id="6099a-154">您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="6099a-155"><dt>**MPNOTIFY \_ SIGUPDATE \_ 下載 \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="6099a-156">下載更新完成。</span><span class="sxs-lookup"><span data-stu-id="6099a-156">Download for update complete.</span></span> <span data-ttu-id="6099a-157">您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="6099a-158"><dt>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 開始**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="6099a-159">已開始安裝更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="6099a-160"><dt>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 進度**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="6099a-161">安裝進度資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-161">Installation progress information.</span></span> <span data-ttu-id="6099a-162">您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="6099a-163"><dt>**MPNOTIFY \_ SIGUPDATE \_ 安裝 \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="6099a-164">已完成安裝更新。</span><span class="sxs-lookup"><span data-stu-id="6099a-164">Installation of update completed.</span></span> <span data-ttu-id="6099a-165">您可以透過 [**MPSIGUPDATE \_ 資料**](mpsigupdate-data.md) 結構取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6099a-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="6099a-166"><dt>**已 \_ 處理 MPNOTIFY SIGUPDATE \_ 要求 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="6099a-167">反惡意程式碼服務已處理簽名更新要求。</span><span class="sxs-lookup"><span data-stu-id="6099a-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="6099a-168">[**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 會指出失敗或成功。</span><span class="sxs-lookup"><span data-stu-id="6099a-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="6099a-169"><dt>**\_ \_ 需要重新開機 MPNOTIFY SIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="6099a-170">需要重新開機才能完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="6099a-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="6099a-171">[**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 會指出失敗或成功。</span><span class="sxs-lookup"><span data-stu-id="6099a-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="6099a-172"><dt>**MPNOTIFY \_ 內部 \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="6099a-173">簽章更新作業遇到一般失敗。</span><span class="sxs-lookup"><span data-stu-id="6099a-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="6099a-174">[**MPCALLBACK \_ 資料**](mpcallback-data.md)中的 *hResult* 具有特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6099a-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="6099a-175">*phUpdateHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6099a-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6099a-176">類型： **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="6099a-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="6099a-177">傳回的更新控制碼，識別目前起始的簽章更新作業。</span><span class="sxs-lookup"><span data-stu-id="6099a-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="6099a-178">這個控制碼可用於後續的函式呼叫，例如控制簽章更新作業。</span><span class="sxs-lookup"><span data-stu-id="6099a-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="6099a-179">控制碼必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉。</span><span class="sxs-lookup"><span data-stu-id="6099a-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6099a-180">傳回值</span><span class="sxs-lookup"><span data-stu-id="6099a-180">Return value</span></span>

<span data-ttu-id="6099a-181">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6099a-181">Type: **HRESULT**</span></span>

<span data-ttu-id="6099a-182">如果函式成功，則傳回值為 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6099a-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="6099a-183">如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="6099a-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="6099a-184">呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。</span><span class="sxs-lookup"><span data-stu-id="6099a-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6099a-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="6099a-185">Requirements</span></span>



| <span data-ttu-id="6099a-186">需求</span><span class="sxs-lookup"><span data-stu-id="6099a-186">Requirement</span></span> | <span data-ttu-id="6099a-187">值</span><span class="sxs-lookup"><span data-stu-id="6099a-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6099a-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6099a-188">Minimum supported client</span></span><br/> | <span data-ttu-id="6099a-189">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6099a-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6099a-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6099a-190">Minimum supported server</span></span><br/> | <span data-ttu-id="6099a-191">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6099a-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6099a-192">標頭</span><span class="sxs-lookup"><span data-stu-id="6099a-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="6099a-193"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6099a-194">DLL</span><span class="sxs-lookup"><span data-stu-id="6099a-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6099a-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6099a-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6099a-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6099a-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6099a-197">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="6099a-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="6099a-198">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="6099a-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="6099a-199">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="6099a-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="6099a-200">**MPCALLBACK \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6099a-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="6099a-201">**MPSIGUPDATE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6099a-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





