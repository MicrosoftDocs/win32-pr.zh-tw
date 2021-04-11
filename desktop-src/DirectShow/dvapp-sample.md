---
description: DVApp 範例
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: DVApp 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109385"
---
# <a name="dvapp-sample"></a><span data-ttu-id="0b098-103">DVApp 範例</span><span class="sxs-lookup"><span data-stu-id="0b098-103">DVApp Sample</span></span>

## <a name="description"></a><span data-ttu-id="0b098-104">Description</span><span class="sxs-lookup"><span data-stu-id="0b098-104">Description</span></span>

<span data-ttu-id="0b098-105">數位視訊 (DV) capture 應用程式。</span><span class="sxs-lookup"><span data-stu-id="0b098-105">Digital Video (DV) capture application.</span></span>

<span data-ttu-id="0b098-106">這個範例示範如何建立各種類型的篩選圖形來控制 DV 攝影機。</span><span class="sxs-lookup"><span data-stu-id="0b098-106">This sample demonstrates how to build various types of filter graphs for controlling DV camcorders.</span></span> <span data-ttu-id="0b098-107">它也會示範如何使用 DV 攝影機來執行捕捉、預覽、傳輸和裝置控制。</span><span class="sxs-lookup"><span data-stu-id="0b098-107">It also shows how to perform capture, preview, transmit, and device control with a DV camcorder.</span></span>

### <a name="usage"></a><span data-ttu-id="0b098-108">使用方式</span><span class="sxs-lookup"><span data-stu-id="0b098-108">Usage</span></span>

<span data-ttu-id="0b098-109">DVApp 應用程式支援下列模式：</span><span class="sxs-lookup"><span data-stu-id="0b098-109">The DVApp application supports the following modes:</span></span>

-   <span data-ttu-id="0b098-110">預覽：將 DV 從攝影機轉譯成影片視窗。</span><span class="sxs-lookup"><span data-stu-id="0b098-110">Preview: Renders DV from the camcorder to a video window.</span></span>
-   <span data-ttu-id="0b098-111">DV 至類型1檔案：將 DV 資料從攝影機捕獲到類型 1 DV 檔案。</span><span class="sxs-lookup"><span data-stu-id="0b098-111">DV to type-1 file: Captures DV data from the camcorder to a type-1 DV file.</span></span>
-   <span data-ttu-id="0b098-112">輸入-1 檔案至 DV：將資料從類型 1 DV 檔案傳送至攝影機。</span><span class="sxs-lookup"><span data-stu-id="0b098-112">Type-1 file to DV: Transmits data from a type-1 DV file to the camcorder.</span></span>
-   <span data-ttu-id="0b098-113">DV 至類型2的檔案：從攝影機捕獲 DV 資料到類型2的 DV 檔案。</span><span class="sxs-lookup"><span data-stu-id="0b098-113">DV to type-2 file: Captures DV data from the camcorder to a type-2 DV file.</span></span>
-   <span data-ttu-id="0b098-114">Type-2 file to DV：將資料從類型2的 DV 檔案傳送至攝像機。</span><span class="sxs-lookup"><span data-stu-id="0b098-114">Type-2 file to DV: Transmits data from a type-2 DV file to the camcorder.</span></span>

<span data-ttu-id="0b098-115">「捕捉」和「傳輸」模式也會執行預覽。</span><span class="sxs-lookup"><span data-stu-id="0b098-115">The capture and transmit modes also perform preview.</span></span> <span data-ttu-id="0b098-116">這兩種模式也都 **沒有預覽** 選項，可停用預覽。</span><span class="sxs-lookup"><span data-stu-id="0b098-116">Each of those modes has a **No Preview** option as well, which disables preview.</span></span> <span data-ttu-id="0b098-117">沒有預覽的捕獲會更有效率，而且可以減少捨棄的畫面格數。</span><span class="sxs-lookup"><span data-stu-id="0b098-117">Capturing without preview is more efficient and can reduce the number of dropped frames.</span></span>

<span data-ttu-id="0b098-118">應用程式會在預覽模式下啟動。</span><span class="sxs-lookup"><span data-stu-id="0b098-118">The application starts in preview mode.</span></span> <span data-ttu-id="0b098-119">若要選取其他模式，請從 [ **圖形模式]** 功能表選擇模式。</span><span class="sxs-lookup"><span data-stu-id="0b098-119">To select another mode, choose a mode from the **Graph Mode** menu.</span></span> <span data-ttu-id="0b098-120">針對每個模式，DVApp 會建立支援該模式功能的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0b098-120">For each mode, DVApp builds a filter graph that supports the functionality of that mode.</span></span> <span data-ttu-id="0b098-121">若要將圖形另存為 GraphEdit (. grf) 檔案，請 **從 [檔案**] 功能表中選取 [**將圖形儲存至檔案]** 。</span><span class="sxs-lookup"><span data-stu-id="0b098-121">To save the graph as a GraphEdit (.grf) file, select **Save Graph to File** from the **File** menu.</span></span> <span data-ttu-id="0b098-122">在 GraphEdit 中開啟檔案之前，請先結束 DVApp。</span><span class="sxs-lookup"><span data-stu-id="0b098-122">Quit DVApp before opening the file in GraphEdit.</span></span>

<span data-ttu-id="0b098-123">若要捕捉至檔案：</span><span class="sxs-lookup"><span data-stu-id="0b098-123">To capture to a file:</span></span>

1.  <span data-ttu-id="0b098-124">**在 [檔案] 功能表中**，選擇 [**設定輸出** 檔]，然後輸入檔案名。</span><span class="sxs-lookup"><span data-stu-id="0b098-124">From the **File** menu, choose **Set Output File** and enter a file name.</span></span>
2.  <span data-ttu-id="0b098-125">從 [ **圖形模式]** 功能表中，選取 [ *DV 至* 檔案模式] (類型1或 [類型 2]，不論是否有預覽) 。</span><span class="sxs-lookup"><span data-stu-id="0b098-125">From the **Graph Mode** menu, select a *DV to File* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="0b098-126">按一下 [ **記錄**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-126">Click **Record**.</span></span>
4.  <span data-ttu-id="0b098-127">如果攝像機處於 VTR 模式，請按一下 [ **播放**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-127">If the camcorder is in VTR mode, click **Play**.</span></span>
5.  <span data-ttu-id="0b098-128">若要停止捕捉，請按一下 [ **停止**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-128">To stop capturing, click **Stop**.</span></span>

<span data-ttu-id="0b098-129">若要從檔案傳輸至攝像機：</span><span class="sxs-lookup"><span data-stu-id="0b098-129">To transmit from a file to the camcorder:</span></span>

1.  <span data-ttu-id="0b098-130">**在 [檔案**] 功能表中，按一下 [**設定輸入** 檔]，然後選取一個 DV 檔案。</span><span class="sxs-lookup"><span data-stu-id="0b098-130">From the **File** menu, click **Set Input File** and select a DV file.</span></span> <span data-ttu-id="0b098-131">檔案必須符合選取的模式 (類型1或類型 2) 。</span><span class="sxs-lookup"><span data-stu-id="0b098-131">The file must match the selected mode (type 1 or type 2).</span></span>
2.  <span data-ttu-id="0b098-132">從 [ **圖形模式]** 功能表中，選取 [ *DV* 模式] (類型1或 [類型 2]，不論是否有預覽) 。</span><span class="sxs-lookup"><span data-stu-id="0b098-132">From the **Graph Mode** menu, select a *File to DV* mode (type 1 or type 2, with or without preview).</span></span>
3.  <span data-ttu-id="0b098-133">按一下 [播放]。</span><span class="sxs-lookup"><span data-stu-id="0b098-133">Click **Play**.</span></span>
4.  <span data-ttu-id="0b098-134">若要將資料記錄到磁帶，請按一下 [ **記錄**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-134">To record the data to tape, click **Record**.</span></span>
5.  <span data-ttu-id="0b098-135">若要停止傳輸，請按一下 [ **停止**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-135">To stop transmitting, click **Stop**.</span></span>

<span data-ttu-id="0b098-136">如果攝影機處於 VTR 模式，則使用者可以透過應用程式的 VCR 樣式按鈕來控制傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="0b098-136">If the camcorder is in VTR mode, the user can control the transport mechanism through the application's VCR-style buttons.</span></span> <span data-ttu-id="0b098-137">若要搜尋磁帶，請輸入目標時間碼，然後按一下 [搜尋] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="0b098-137">To seek the tape, enter the target timecode and click the seek button.</span></span>

<span data-ttu-id="0b098-138">若要限制應用程式所捕獲的資料量，請從 [檔案 **] 功能表中選擇 [** **捕捉大小**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-138">To limit how much data the application captures, choose **Capture Size** from the **File** menu.</span></span>

<span data-ttu-id="0b098-139">若要檢查磁帶格式 (NTSC 或 PAL) ，請從 [**選項**] 功能表選擇 [**檢查磁帶**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-139">To check the tape format (NTSC or PAL), choose **Check Tape** from the **Options** menu.</span></span>

<span data-ttu-id="0b098-140">若要變更預覽視窗的大小，請從 [**選項**] 功能表選擇 [**變更解碼大小**]。</span><span class="sxs-lookup"><span data-stu-id="0b098-140">To change the size of the preview window, choose **Change Decode Size** from the **Options** menu.</span></span>

### <a name="programming-notes"></a><span data-ttu-id="0b098-141">程式設計附注</span><span class="sxs-lookup"><span data-stu-id="0b098-141">Programming Notes</span></span>

<span data-ttu-id="0b098-142">此應用程式的主要目的是要說明如何建立各種 DV 捕捉和傳輸圖形。</span><span class="sxs-lookup"><span data-stu-id="0b098-142">The main purpose of this application is to show how to build various DV capture and transmit graphs.</span></span>

### <a name="device-arrival-and-removal"></a><span data-ttu-id="0b098-143">裝置抵達和移除</span><span class="sxs-lookup"><span data-stu-id="0b098-143">Device Arrival and Removal</span></span>

<span data-ttu-id="0b098-144">應用程式會使用兩種不同的技術來處理裝置抵達和移除。</span><span class="sxs-lookup"><span data-stu-id="0b098-144">The application handles device arrival and removal, using two different techniques.</span></span> <span data-ttu-id="0b098-145">針對裝置抵達，應用程式的訊息迴圈會回應 WM \_ DEVICECHANGE 訊息。</span><span class="sxs-lookup"><span data-stu-id="0b098-145">For device arrival, the application's message loop responds to WM\_DEVICECHANGE messages.</span></span> <span data-ttu-id="0b098-146">移除裝置時，應用程式會從篩選圖形管理員回應 [**EC \_ 裝置 \_ 遺失**](ec-device-lost.md) 的事件。</span><span class="sxs-lookup"><span data-stu-id="0b098-146">For device removal, the application responds to [**EC\_DEVICE\_LOST**](ec-device-lost.md) events from the filter graph manager.</span></span> <span data-ttu-id="0b098-147">這兩種方法都可以運作，但 EC \_ 裝置 \_ 遺失事件則取決於是否存在篩選圖形中的裝置。</span><span class="sxs-lookup"><span data-stu-id="0b098-147">Either approach works, although the EC\_DEVICE\_LOST event depends on the existence of the device in the filter graph.</span></span>

<span data-ttu-id="0b098-148">應用程式一次只能處理一個裝置。</span><span class="sxs-lookup"><span data-stu-id="0b098-148">The application only handles one device at a time.</span></span> <span data-ttu-id="0b098-149">如果移除目前的裝置，應用程式會在系統上尋找另一個 DV 裝置。</span><span class="sxs-lookup"><span data-stu-id="0b098-149">If the current device is removed, the application looks for another DV device on the system.</span></span>

<span data-ttu-id="0b098-150">在某些 DV 攝影機上，使用者必須在相機模式與 VTR 模式之間切換時，關閉裝置，以觸發裝置遺失的訊息。</span><span class="sxs-lookup"><span data-stu-id="0b098-150">On some DV camcorders, the user must shut off the device when switching it between camera mode and VTR mode, which triggers a device-lost message.</span></span> <span data-ttu-id="0b098-151">應用程式會藉由啟用或停用適當的功能表命令來回應。</span><span class="sxs-lookup"><span data-stu-id="0b098-151">The application responds by enabling or disabling the appropriate menu commands.</span></span> <span data-ttu-id="0b098-152">不過，如果使用者在模式之間快速切換，則此攝影機可能不會產生裝置遺失的訊息。</span><span class="sxs-lookup"><span data-stu-id="0b098-152">However, if the user toggles rapidly between modes, the camcorder might not generate a device-lost message.</span></span> <span data-ttu-id="0b098-153">您可以從 [**選項**] 功能表選擇 [重新整理 **模式]** ，以強制更新功能表。</span><span class="sxs-lookup"><span data-stu-id="0b098-153">You can force the menus to update by choosing **Refresh Mode** from the **Options** menu.</span></span> <span data-ttu-id="0b098-154">有些 DV 攝影機可以在不關閉的情況下切換模式，但只有在切換到 VTR 模式時，才會傳送裝置遺失的訊息。</span><span class="sxs-lookup"><span data-stu-id="0b098-154">Some DV camcorders can toggle modes without shutting off, but send a device-lost message only when they switch to VTR mode.</span></span>

### <a name="device-control"></a><span data-ttu-id="0b098-155">裝置控制</span><span class="sxs-lookup"><span data-stu-id="0b098-155">Device Control</span></span>

<span data-ttu-id="0b098-156">[ **播放** 和 **錄製** ] 按鈕的功能取決於目前的模式：</span><span class="sxs-lookup"><span data-stu-id="0b098-156">The functionality of the **Play** and **Record** button depends on the current mode:</span></span>

-   <span data-ttu-id="0b098-157">預覽：篩選圖形會自動執行。</span><span class="sxs-lookup"><span data-stu-id="0b098-157">Preview: The filter graph runs automatically.</span></span> <span data-ttu-id="0b098-158">[ **播放** ] 按鈕會啟動傳輸。</span><span class="sxs-lookup"><span data-stu-id="0b098-158">The **Play** button starts the transport.</span></span>
-   <span data-ttu-id="0b098-159">捕捉至檔案： [ **記錄** ] 按鈕會執行圖形，而 [ **播放** ] 按鈕會啟動傳輸。</span><span class="sxs-lookup"><span data-stu-id="0b098-159">Capture to file: The **Record** button runs the graph, and the **Play** button starts the transport.</span></span>
-   <span data-ttu-id="0b098-160">傳送至裝置： [ **播放** ] 按鈕會執行圖形，而 [ **記錄** ] 按鈕會啟動傳輸。</span><span class="sxs-lookup"><span data-stu-id="0b098-160">Transmit to device: The **Play** button runs the graph, and the **Record** button starts the transport.</span></span>

<span data-ttu-id="0b098-161">範例應用程式不會執行框架精確的捕獲。</span><span class="sxs-lookup"><span data-stu-id="0b098-161">The sample application does not perform frame-accurate capture.</span></span> <span data-ttu-id="0b098-162">在不同的點上，應用程式會呼叫 **Sleep** 函式來等候裝置回應。</span><span class="sxs-lookup"><span data-stu-id="0b098-162">At various points, the application calls the **Sleep** function to wait for the device to respond.</span></span> <span data-ttu-id="0b098-163">較新的 DV 攝影機會在裝置狀態變更時傳送通知。</span><span class="sxs-lookup"><span data-stu-id="0b098-163">Newer DV camcorders send a notification when the state of the device changes.</span></span> <span data-ttu-id="0b098-164">較舊的裝置可能不支援通知;基於範例的目的，呼叫 **睡眠** 是較簡單的解決方案。</span><span class="sxs-lookup"><span data-stu-id="0b098-164">Older devices might not support notification; for the purposes of a sample, calling **Sleep** is a simpler solution.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="0b098-165">下載範例</span><span class="sxs-lookup"><span data-stu-id="0b098-165">Downloading the Sample</span></span>

<span data-ttu-id="0b098-166">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0b098-166">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="0b098-167">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 捕獲 \\ DVApp。</span><span class="sxs-lookup"><span data-stu-id="0b098-167">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Capture\\DVApp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b098-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b098-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b098-169">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="0b098-169">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="0b098-170">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="0b098-170">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0b098-171">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="0b098-171">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



