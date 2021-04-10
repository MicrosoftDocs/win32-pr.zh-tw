---
title: DWM 函數
description: 本節包含桌面視窗管理員 (DWM) 函數的相關資訊。
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- 桌面視窗管理員 (DWM) ，參考
- DWM (桌面視窗管理員) ，參考
- 桌面視窗管理員 (DWM) 、函數
- DWM (桌面視窗管理員) ，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316603"
---
# <a name="dwm-functions"></a><span data-ttu-id="c7956-107">DWM 函數</span><span class="sxs-lookup"><span data-stu-id="c7956-107">DWM Functions</span></span>

<span data-ttu-id="c7956-108">本節包含桌面視窗管理員 (DWM) 函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c7956-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c7956-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="c7956-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7956-110">主題</span><span class="sxs-lookup"><span data-stu-id="c7956-110">Topic</span></span></th>
<th><span data-ttu-id="c7956-111">描述</span><span class="sxs-lookup"><span data-stu-id="c7956-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7956-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-113">此函數並未實作。</span><span class="sxs-lookup"><span data-stu-id="c7956-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-115">非工作區中 DWM 點擊測試的預設視窗程式。</span><span class="sxs-lookup"><span data-stu-id="c7956-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="c7956-116">您也必須確保針對<a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a>訊息呼叫<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c7956-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="c7956-117">如果未針對<strong>WM_NCMOUSELEAVE</strong>訊息呼叫<strong>DwmDefWindowProc</strong> ，當游標離開視窗時，DWM 不會從 [<strong>最大化</strong>]、[<strong>最小化</strong>] 和 [<strong>關閉</strong>] 按鈕中移除反白顯示。</span><span class="sxs-lookup"><span data-stu-id="c7956-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-119">此函數並未實作。</span><span class="sxs-lookup"><span data-stu-id="c7956-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-121">啟用指定之視窗的模糊效果。</span><span class="sxs-lookup"><span data-stu-id="c7956-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="c7956-122">
<b>注意</b> 從 Windows 8 開始，呼叫此函式並不會造成模糊效果，因為轉譯視窗的方式中的樣式變更。</span><span class="sxs-lookup"><span data-stu-id="c7956-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-124">啟用或停用 DWM 組合。</span><span class="sxs-lookup"><span data-stu-id="c7956-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c7956-125">從 Windows 8 起，此函式已被取代。</span><span class="sxs-lookup"><span data-stu-id="c7956-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="c7956-126">DWM 無法再以程式設計的方式停用。</span><span class="sxs-lookup"><span data-stu-id="c7956-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-128">通知 DWM 在呼叫進程運作時，加入宣告或退出多媒體類別排程服務 (MMCSS) 排程。</span><span class="sxs-lookup"><span data-stu-id="c7956-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-130">將視窗框架擴充到工作區。</span><span class="sxs-lookup"><span data-stu-id="c7956-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-132">發出排清呼叫，在所有目前未完成的 Microsoft DirectX 介面更新完成時，封鎖呼叫端直到下一次出現為止。</span><span class="sxs-lookup"><span data-stu-id="c7956-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="c7956-133">這會針對非常複雜的場景進行補償，或以非常低的優先順序呼叫處理常式。</span><span class="sxs-lookup"><span data-stu-id="c7956-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-135">抓取用於 DWM 玻璃組合的目前色彩。</span><span class="sxs-lookup"><span data-stu-id="c7956-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="c7956-136">這個值是以目前的色彩配置為基礎，而且可由使用者進行修改。</span><span class="sxs-lookup"><span data-stu-id="c7956-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="c7956-137">應用程式可以藉由處理 <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> 通知來接聽色彩變更。</span><span class="sxs-lookup"><span data-stu-id="c7956-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-139">抓取所指定視窗的目前組合計時資訊。</span><span class="sxs-lookup"><span data-stu-id="c7956-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-141">此函數並未實作。</span><span class="sxs-lookup"><span data-stu-id="c7956-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-143">此函數並未實作。</span><span class="sxs-lookup"><span data-stu-id="c7956-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-145">捕獲傳輸屬性。</span><span class="sxs-lookup"><span data-stu-id="c7956-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="c7956-147">
<strong>注意</strong>  這個函式是公開可用的，但無法正常運作，Windows 10 版本1803。</span><span class="sxs-lookup"><span data-stu-id="c7956-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="c7956-148">檢查在指定的視窗的應用程式標題列中取得索引標籤所需的需求。</span><span class="sxs-lookup"><span data-stu-id="c7956-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-150">抓取套用至視窗之指定屬性的目前值。</span><span class="sxs-lookup"><span data-stu-id="c7956-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-152">由應用程式呼叫，以指出所有先前從視窗提供的 iconic 點陣圖（縮圖和查看表示）都應該重新整理。</span><span class="sxs-lookup"><span data-stu-id="c7956-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-154">取得值，這個值會指出是否已啟用 DWM 組合。</span><span class="sxs-lookup"><span data-stu-id="c7956-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="c7956-155">執行 Windows 7 或更早版本之電腦上的應用程式，可以藉由處理 <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> 通知，來接聽撰寫狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c7956-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-157">變更將顯示上一個畫面格的監視器重新整理次數。</span><span class="sxs-lookup"><span data-stu-id="c7956-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="c7956-158">不再支援<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c7956-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="c7956-159">從 Windows 8.1 開始，對 <strong>DwmModifyPreviousDxFrameDuration</strong> 的呼叫一律會傳回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c7956-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-161">捕獲 DWM 縮圖的來源大小。</span><span class="sxs-lookup"><span data-stu-id="c7956-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-163">建立目的地和來源視窗之間的 DWM 縮圖關聯性。</span><span class="sxs-lookup"><span data-stu-id="c7956-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-165">通知 DWM，觸控連絡人已被辨識為手勢，而且 DWM 應該繪製該手勢的意見反應。</span><span class="sxs-lookup"><span data-stu-id="c7956-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-167">設定用來顯示所呈現畫面格的監視器重新整理數目。</span><span class="sxs-lookup"><span data-stu-id="c7956-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="c7956-168">不再支援<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c7956-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="c7956-169">從 Windows 8.1 開始，對 <strong>DwmSetDxFrameDuration</strong> 的呼叫一律會傳回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c7956-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-171">設定靜態的 iconic 點陣圖以顯示 <em>即時預覽</em> (也稱為視窗或索引標籤的 [ <em>查看預覽</em> ]) 。工作列可以使用此點陣圖來顯示視窗或索引標籤的完整大小預覽。</span><span class="sxs-lookup"><span data-stu-id="c7956-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-173">在視窗或索引標籤上設定靜態、iconic 點陣圖，以做為縮圖標記法。</span><span class="sxs-lookup"><span data-stu-id="c7956-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="c7956-174">工作列可以使用此點陣圖作為視窗或索引標籤的縮圖切換目標。</span><span class="sxs-lookup"><span data-stu-id="c7956-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-176">設定框架組合的目前參數。</span><span class="sxs-lookup"><span data-stu-id="c7956-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="c7956-177">不再支援<a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c7956-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="c7956-178">從 Windows 8.1 開始，對 <strong>DwmSetPresentParameters</strong> 的呼叫一律會傳回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="c7956-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-180">設定視窗的非用戶端轉譯屬性值。</span><span class="sxs-lookup"><span data-stu-id="c7956-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-182">由應用程式或架構呼叫，以指定要繪製以回應特定觸控或畫筆連絡人的視覺效果意見反應類型。</span><span class="sxs-lookup"><span data-stu-id="c7956-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-184">啟用觸控和拖曳互動至使用者的圖形化意見反應。</span><span class="sxs-lookup"><span data-stu-id="c7956-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-186">使用 DWM 來協調工具視窗的動畫。</span><span class="sxs-lookup"><span data-stu-id="c7956-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7956-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-188">移除 <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> 函數所建立的 DWM 縮圖關聯性。</span><span class="sxs-lookup"><span data-stu-id="c7956-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7956-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="c7956-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="c7956-190">更新 DWM 縮圖的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7956-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

