---
description: 端點資料遺失防止 (DLP) Api 可讓應用程式在特定作業之前和之後通知作業系統，例如開啟或儲存檔案。
title: 端點資料遺失防止
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495446"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="80531-103">端點資料遺失防止</span><span class="sxs-lookup"><span data-stu-id="80531-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="80531-104">Windows 10 會實行有助於防止機密檔案遺失資料的機制。</span><span class="sxs-lookup"><span data-stu-id="80531-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="80531-105">端點資料遺失防止 (DLP) Api 可讓應用程式在特定作業之前和之後通知作業系統，例如開啟或儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="80531-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="80531-106">這些通知會作為「提示」，可讓系統將資料遺失作業優化。</span><span class="sxs-lookup"><span data-stu-id="80531-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="80531-107">DLP dll 的位置</span><span class="sxs-lookup"><span data-stu-id="80531-107">Location of the DLP dll</span></span>

<span data-ttu-id="80531-108">由於端點 DLP dll 未與 Windows SDK 配套，因此應用程式必須在執行時間手動載入 dll。</span><span class="sxs-lookup"><span data-stu-id="80531-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="80531-109">Dll 位置的路徑會儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="80531-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="80531-110">下表列出儲存這項資訊的登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="80531-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="80531-111">這些路徑在下面提供的範例 endpointdlp 程式代碼清單中會定義為常數，以方便開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="80531-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="80531-112">常數</span><span class="sxs-lookup"><span data-stu-id="80531-112">Constant</span></span> | <span data-ttu-id="80531-113">值</span><span class="sxs-lookup"><span data-stu-id="80531-113">Value</span></span> | <span data-ttu-id="80531-114">描述</span><span class="sxs-lookup"><span data-stu-id="80531-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="80531-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="80531-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="80531-116">"EndpointDlp.dll"</span><span class="sxs-lookup"><span data-stu-id="80531-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="80531-117">提供 API 的端點 DLP DLL 名稱</span><span class="sxs-lookup"><span data-stu-id="80531-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="80531-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="80531-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="80531-119">"SOFTWARE \\ Microsoft \\ Windows Defender"</span><span class="sxs-lookup"><span data-stu-id="80531-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="80531-120">Windows Defender 在 HKLM 下儲存某些端點 DLP 設定的登錄機碼</span><span class="sxs-lookup"><span data-stu-id="80531-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="80531-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="80531-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="80531-122">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY 的值</span><span class="sxs-lookup"><span data-stu-id="80531-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="80531-123">可從中取得 EndpointDlp.dll 安裝位置的 HKLM 機碼底下的登錄路徑</span><span class="sxs-lookup"><span data-stu-id="80531-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="80531-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="80531-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="80531-125">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="80531-125">"InstallLocation"</span></span> | <span data-ttu-id="80531-126">在 ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY 的登錄值，在其中儲存 EndpointDlp.dll 安裝位置</span><span class="sxs-lookup"><span data-stu-id="80531-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="80531-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="80531-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="80531-128">x86</span><span class="sxs-lookup"><span data-stu-id="80531-128">"x86"</span></span> | <span data-ttu-id="80531-129">在 x64 平臺上，將此目錄串連以取得 x86 版本的 EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="80531-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="80531-130">檢查是否已啟用 endpoint DLP</span><span class="sxs-lookup"><span data-stu-id="80531-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="80531-131">若要判斷是否已在系統上啟用 endpoint DLP，請檢查下列登錄機碼值。</span><span class="sxs-lookup"><span data-stu-id="80531-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="80531-132">常數</span><span class="sxs-lookup"><span data-stu-id="80531-132">Constant</span></span> | <span data-ttu-id="80531-133">值</span><span class="sxs-lookup"><span data-stu-id="80531-133">Value</span></span> | <span data-ttu-id="80531-134">描述</span><span class="sxs-lookup"><span data-stu-id="80531-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="80531-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="80531-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="80531-136">「 \\ 功能」</span><span class="sxs-lookup"><span data-stu-id="80531-136">"\\Features"</span></span> | <span data-ttu-id="80531-137"> (HKLM) 下的 Endpoint DLP 啟用旗標金鑰的路徑 ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="80531-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="80531-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="80531-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="80531-139">"SenseDlpEnabled"</span><span class="sxs-lookup"><span data-stu-id="80531-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="80531-140">包含 DLP ENABLED 旗標登錄機碼的 ENDPOINTDLP_ENABLED_FLAG_REGKEY 下的登錄值</span><span class="sxs-lookup"><span data-stu-id="80531-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="80531-141">端點 DLP Api</span><span class="sxs-lookup"><span data-stu-id="80531-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="80531-142">下表列出端點 DLP dll 提供的 Api。</span><span class="sxs-lookup"><span data-stu-id="80531-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="80531-143">初始化和版本控制</span><span class="sxs-lookup"><span data-stu-id="80531-143">Initialization and versioning</span></span>

| <span data-ttu-id="80531-144">API</span><span class="sxs-lookup"><span data-stu-id="80531-144">API</span></span> | <span data-ttu-id="80531-145">描述</span><span class="sxs-lookup"><span data-stu-id="80531-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="80531-146">DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="80531-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="80531-147">針對一組端點資料遺失防止 (DLP) 作業，通知系統所需的強制模式。</span><span class="sxs-lookup"><span data-stu-id="80531-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="80531-148">DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="80531-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="80531-149">在目前的裝置上，抓取端點資料遺失防止 (DLP) API 的版本。</span><span class="sxs-lookup"><span data-stu-id="80531-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="80531-150">文件作業</span><span class="sxs-lookup"><span data-stu-id="80531-150">Document operations</span></span>

| <span data-ttu-id="80531-151">API</span><span class="sxs-lookup"><span data-stu-id="80531-151">API</span></span> | <span data-ttu-id="80531-152">描述</span><span class="sxs-lookup"><span data-stu-id="80531-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="80531-153">DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="80531-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="80531-154">在起始開啟作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="80531-155">DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="80531-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="80531-156">在開啟作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="80531-157">DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="80531-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="80531-158">在開機檔案關閉作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="80531-159">DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="80531-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="80531-160">在起始開啟作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="80531-161">DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="80531-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="80531-162">在開啟作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="80531-163">DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="80531-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="80531-164">在開機檔案關閉作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="80531-165">將儲存為 作業</span><span class="sxs-lookup"><span data-stu-id="80531-165">Save as operations</span></span>
| <span data-ttu-id="80531-166">API</span><span class="sxs-lookup"><span data-stu-id="80531-166">API</span></span> | <span data-ttu-id="80531-167">描述</span><span class="sxs-lookup"><span data-stu-id="80531-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="80531-168">DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="80531-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="80531-169">在起始「另存新檔」作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="80531-170">DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="80531-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="80531-171">在 [另存新檔] 作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="80531-172">拖放作業</span><span class="sxs-lookup"><span data-stu-id="80531-172">Drag and drop operations</span></span>

| <span data-ttu-id="80531-173">API</span><span class="sxs-lookup"><span data-stu-id="80531-173">API</span></span> | <span data-ttu-id="80531-174">描述</span><span class="sxs-lookup"><span data-stu-id="80531-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="80531-175">DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="80531-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="80531-176">當輸入放置目標時，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="80531-177">DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="80531-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="80531-178">當卸載目標結束時，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="80531-179">DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="80531-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="80531-180">在起始拖放作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="80531-181">DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="80531-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="80531-182">在拖放作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="80531-183">剪貼簿作業</span><span class="sxs-lookup"><span data-stu-id="80531-183">Clipboard operations</span></span>

| <span data-ttu-id="80531-184">API</span><span class="sxs-lookup"><span data-stu-id="80531-184">API</span></span> | <span data-ttu-id="80531-185">描述</span><span class="sxs-lookup"><span data-stu-id="80531-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="80531-186">DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="80531-187">在起始複製到剪貼簿作業之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="80531-188">DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="80531-189">在複製到剪貼簿作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="80531-190">DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="80531-191">為系統提供檔的相關資訊，再開始貼上剪貼簿作業。</span><span class="sxs-lookup"><span data-stu-id="80531-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="80531-192">DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="80531-193">在貼上剪貼簿作業完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="80531-194">DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="80531-195">提供隱藏專案剪貼簿作業完成後的系統狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="80531-196">DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="80531-197">在起始隱藏剪貼簿作業之前通知系統。</span><span class="sxs-lookup"><span data-stu-id="80531-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="80531-198">DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="80531-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="80531-199">判斷應用程式是否必須從系統剪貼簿提取資料，而不是從其內部快取中取得資料。</span><span class="sxs-lookup"><span data-stu-id="80531-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="80531-200">列印工作</span><span class="sxs-lookup"><span data-stu-id="80531-200">Print operations</span></span>

| <span data-ttu-id="80531-201">API</span><span class="sxs-lookup"><span data-stu-id="80531-201">API</span></span> | <span data-ttu-id="80531-202">描述</span><span class="sxs-lookup"><span data-stu-id="80531-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="80531-203">DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="80531-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="80531-204">在開始列印工作之前，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="80531-205">DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="80531-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="80531-206">在列印工作開始後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="80531-207">DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="80531-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="80531-208">在列印工作完成後，為系統提供檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="80531-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="80531-209">端點 DLP 範例標頭</span><span class="sxs-lookup"><span data-stu-id="80531-209">Endpoint DLP example header</span></span>

<span data-ttu-id="80531-210">因為端點 DLP 標頭未包含在 Windows SDK 中，所以您必須自行建立標頭檔，以取得要在您的執行中使用的 API 簽章。</span><span class="sxs-lookup"><span data-stu-id="80531-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="80531-211">為了方便起見，我們會提供範例程式碼，讓您可以複製並貼到您的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="80531-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="80531-212">除了函式宣告之外，此程式代碼清單也會定義有用的常數，例如版本設定資訊和登錄機碼路徑。</span><span class="sxs-lookup"><span data-stu-id="80531-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


