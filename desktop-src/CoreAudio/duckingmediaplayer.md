---
description: 這個範例應用程式會藉由執行媒體播放程式來示範串流衰減，以顯示系統提供的預設衰減行為、退出回避事件，以及在收到回避事件時執行自訂處理。
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992230"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="ed8b0-103">DuckingMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ed8b0-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="ed8b0-104">這個範例應用程式會藉由執行媒體播放程式來示範串流衰減，以顯示系統提供的預設衰減行為、退出回避事件，以及在收到回避事件時執行自訂處理。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="ed8b0-105">此範例必須在 conjuction with [DuckingCaptureSample](duckingcapturesample.md)中使用。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="ed8b0-106">如需回避或串流衰減的詳細資訊，請參閱 [預設回避體驗](stream-attenuation.md)。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="ed8b0-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ed8b0-108">說明</span><span class="sxs-lookup"><span data-stu-id="ed8b0-108">Description</span></span>](#description)
-   [<span data-ttu-id="ed8b0-109">需求</span><span class="sxs-lookup"><span data-stu-id="ed8b0-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ed8b0-110">下載範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ed8b0-111">建立範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ed8b0-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="ed8b0-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed8b0-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ed8b0-114">Description</span><span class="sxs-lookup"><span data-stu-id="ed8b0-114">Description</span></span>

<span data-ttu-id="ed8b0-115">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="ed8b0-116">DirectShow 播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="ed8b0-117">串流管理和處理回避事件的[WASAPI](wasapi.md) 。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8b0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed8b0-118">Requirements</span></span>



| <span data-ttu-id="ed8b0-119">產品</span><span class="sxs-lookup"><span data-stu-id="ed8b0-119">Product</span></span>                                                        | <span data-ttu-id="ed8b0-120">版本</span><span class="sxs-lookup"><span data-stu-id="ed8b0-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="ed8b0-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ed8b0-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="ed8b0-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed8b0-122">Windows 7</span></span> |
| <span data-ttu-id="ed8b0-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ed8b0-123">Visual Studio</span></span>                                                  | <span data-ttu-id="ed8b0-124">2008</span><span class="sxs-lookup"><span data-stu-id="ed8b0-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ed8b0-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-125">Downloading the Sample</span></span>

<span data-ttu-id="ed8b0-126">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="ed8b0-127">Location</span><span class="sxs-lookup"><span data-stu-id="ed8b0-127">Location</span></span>    | <span data-ttu-id="ed8b0-128">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="ed8b0-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8b0-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ed8b0-129">Windows SDK</span></span> | <span data-ttu-id="ed8b0-130">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ DuckingMediaPlayer \\ .。。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="ed8b0-131">建立範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-131">Building the Sample</span></span>

<span data-ttu-id="ed8b0-132">若要建立 DuckingMediaPlayer 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="ed8b0-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="ed8b0-133">在 Visual Studio 2008 中開啟 DuckingMediaPlayer .sln。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="ed8b0-134">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="ed8b0-135">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="ed8b0-136">在此情況下，除非您明確設定在專案檔 DuckingMediaPlayer 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ed8b0-137">執行範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-137">Running the Sample</span></span>

<span data-ttu-id="ed8b0-138">如果您成功建立應用程式，則會產生可執行檔（DuckingMediaPlayer.exe）。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="ed8b0-139">若要執行它，請選取 [ **開始調試** ] 或 [ **啟動但不進行調試** ] **，或** `DuckingMediaPlayer` 在命令視窗中輸入。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="ed8b0-140">若要觀看回避的示範，您必須同時執行 DuckingMediaPlayer 和 DuckingCaptureSample。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="ed8b0-141">DuckingCaptureSample 會開啟通訊資料流程，並通知系統產生回避事件。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="ed8b0-142">當回避事件發生時，系統會通知 DuckingMediaPlayer，而 media player 會執行使用者所要求的動作。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="ed8b0-143">若要停用回避行為：</span><span class="sxs-lookup"><span data-stu-id="ed8b0-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="ed8b0-144">在 [DuckingCaptureSample] 視窗中，選取 [ **使用預設輸入裝置**]，然後按一下 [ **啟動** ]，從通訊裝置啟動捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="ed8b0-145">在 DuckingMediaPlayer 上，選取要播放的媒體檔案，並將回避選項指定為 **退出回避**。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="ed8b0-146">請注意，媒體檔案會播放，而不會發生任何中斷。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="ed8b0-147">系統會忽略開啟的通訊資料流程時，系統所產生的事件。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="ed8b0-148">若要示範系統提供的預設回避行為，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="ed8b0-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="ed8b0-149">從 [控制台] 選取 [音效 **] 選項。**</span><span class="sxs-lookup"><span data-stu-id="ed8b0-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="ed8b0-150">在 [ **通訊** ] 索引標籤上，選取 [ **將其他音效的音量減少 80%**]。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="ed8b0-151">在 [DuckingCaptureSample] 視窗中，選取 [ **使用預設輸入裝置**]，然後按一下 [ **啟動** ]，從通訊裝置啟動捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="ed8b0-152">在 DuckingMediaPlayer 上，選取要播放的媒體檔案，而不選擇任何回避選項。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="ed8b0-153">在 [DuckingCaptureSample] 視窗中，按一下 [ **停止** ] 以停止通訊串流。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="ed8b0-154">請注意，當 DuckingCaptureSample 開啟通訊串流時，DuckingMediaPlayer 播放的媒體檔案不會中斷，但音量層級會降低。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="ed8b0-155">當通訊會話停止時，磁片區會重設為原始設定。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="ed8b0-156">此資料流程衰減行為是系統所執行的預設回避行為。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="ed8b0-157">若要查看媒體播放機所實行的自訂回避行為：</span><span class="sxs-lookup"><span data-stu-id="ed8b0-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="ed8b0-158">在 [DuckingCaptureSample] 視窗中，選取 [ **使用預設輸入裝置**]，然後按一下 [ **啟動** ]，從通訊裝置啟動捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="ed8b0-159">在 DuckingMediaPlayer 上，選取要播放的媒體檔案，然後將回避選項指定為 [ **暫停**]。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="ed8b0-160">在 [DuckingCaptureSample] 視窗中，按一下 [ **停止** ] 以停止通訊串流。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="ed8b0-161">請注意，當 DuckingCaptureSample 開啟通訊串流時，DuckingMediaPlayer 所播放的媒體檔案會暫停。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="ed8b0-162">停止通訊會話時，就會繼續播放。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="ed8b0-163">此資料流程衰減行為是媒體播放機所執行的回避行為。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="ed8b0-164">DuckingMediaPlayer 也會示範如何將每個應用程式的音量控制項與磁片區混音器整合。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="ed8b0-165">如需有關資料流程衰減功能的詳細資訊，請參閱 [預設回避體驗](stream-attenuation.md)。</span><span class="sxs-lookup"><span data-stu-id="ed8b0-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed8b0-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed8b0-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed8b0-167">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="ed8b0-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



