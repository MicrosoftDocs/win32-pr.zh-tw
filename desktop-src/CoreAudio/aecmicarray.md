---
description: 此範例會使用核心音訊 Api 來捕捉高品質的語音串流。 此範例支援聲場 echo 取消 (AEC) 和麥克風陣列處理，方法是使用由 Microsoft 所提供的 AEC （也稱為語音捕獲 DSP）。
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111561"
---
# <a name="aecmicarray"></a><span data-ttu-id="7e6d2-104">AECMicArray</span><span class="sxs-lookup"><span data-stu-id="7e6d2-104">AECMicArray</span></span>

<span data-ttu-id="7e6d2-105">此範例會使用核心音訊 Api 來捕捉高品質的語音串流。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="7e6d2-106">此範例支援聲場 echo 取消 (AEC) 和麥克風陣列處理，方法是使用由 Microsoft 所提供的 AEC （也稱為語音捕獲 DSP）。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="7e6d2-107">本主題將包含以下各節。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="7e6d2-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e6d2-108">Description</span></span>](#description)
-   [<span data-ttu-id="7e6d2-109">需求</span><span class="sxs-lookup"><span data-stu-id="7e6d2-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7e6d2-110">下載範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7e6d2-111">建立範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7e6d2-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7e6d2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e6d2-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="7e6d2-114">Description</span><span class="sxs-lookup"><span data-stu-id="7e6d2-114">Description</span></span>

<span data-ttu-id="7e6d2-115">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="7e6d2-116">[MMDevice](mmdevice-api.md) 多媒體裝置的列舉和選取。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="7e6d2-117">串流管理作業的[WASAPI](wasapi.md) ，例如啟動和停止資料流程、串流切換。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="7e6d2-118">用於列舉音訊介面卡的[DeviceTopology](devicetopology-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="7e6d2-119">[EndpointVolume](endpointvolume-api.md) 控制 [音訊會話](audio-sessions.md)的音量層級。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6d2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e6d2-120">Requirements</span></span>



| <span data-ttu-id="7e6d2-121">產品</span><span class="sxs-lookup"><span data-stu-id="7e6d2-121">Product</span></span>                                                        | <span data-ttu-id="7e6d2-122">版本</span><span class="sxs-lookup"><span data-stu-id="7e6d2-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="7e6d2-123">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e6d2-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7e6d2-124">Windows Vista 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7e6d2-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="7e6d2-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e6d2-125">Visual Studio</span></span>                                                  | <span data-ttu-id="7e6d2-126">2005 (非 express 版本) </span><span class="sxs-lookup"><span data-stu-id="7e6d2-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7e6d2-127">下載範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-127">Downloading the Sample</span></span>

<span data-ttu-id="7e6d2-128">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="7e6d2-129">Location</span><span class="sxs-lookup"><span data-stu-id="7e6d2-129">Location</span></span>    | <span data-ttu-id="7e6d2-130">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="7e6d2-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6d2-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7e6d2-131">Windows SDK</span></span> | <span data-ttu-id="7e6d2-132">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ AECMicArray \\ .。。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="7e6d2-133">建立範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-133">Building the Sample</span></span>

<span data-ttu-id="7e6d2-134">若要建立 AecSDKDemo 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7e6d2-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="7e6d2-135">開啟 [SDK 命令] 視窗。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="7e6d2-136">輸入 **cd% MSSDK% \\ 安裝程式**。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="7e6d2-137">執行 VCIntegrate.exe。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="7e6d2-138">從這裡開始，命令視窗會有適當的環境設定，以建立利用 SDK 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="7e6d2-139">建置範例。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7e6d2-140">執行範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-140">Running the Sample</span></span>

<span data-ttu-id="7e6d2-141">如果您成功建立示範應用程式，則會產生可執行檔 AecSDKDemo.exe。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="7e6d2-142">若要執行它，請 `AecSDKDemo` 在命令視窗中輸入，後面接著必要或選擇性的引數，如下所述。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="7e6d2-143">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="7e6d2-144">引數</span><span class="sxs-lookup"><span data-stu-id="7e6d2-144">Argument</span></span>  | <span data-ttu-id="7e6d2-145">描述</span><span class="sxs-lookup"><span data-stu-id="7e6d2-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6d2-146">-out</span><span class="sxs-lookup"><span data-stu-id="7e6d2-146">-out</span></span>      | <span data-ttu-id="7e6d2-147">必要。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-147">Required.</span></span> <span data-ttu-id="7e6d2-148">指定輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="7e6d2-149">-mod</span><span class="sxs-lookup"><span data-stu-id="7e6d2-149">-mod</span></span>      | <span data-ttu-id="7e6d2-150">必要。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-150">Required.</span></span> <span data-ttu-id="7e6d2-151">指定語音捕獲系統模式。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="7e6d2-152">如需詳細資訊，請參閱範例讀我檔案中的「設定 voice capture」一節。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="7e6d2-153">-特徵</span><span class="sxs-lookup"><span data-stu-id="7e6d2-153">-feat</span></span>     | <span data-ttu-id="7e6d2-154">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-154">Optional.</span></span> <span data-ttu-id="7e6d2-155">開啟 (1) 或 off (0) 的功能模式。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="7e6d2-156">-ns</span><span class="sxs-lookup"><span data-stu-id="7e6d2-156">-ns</span></span>       | <span data-ttu-id="7e6d2-157">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-157">Optional.</span></span> <span data-ttu-id="7e6d2-158">開啟 (1) 或 off (0) 的雜訊抑制。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="7e6d2-159">您必須開啟功能模式，才能指定此功能。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="7e6d2-160">-agc</span><span class="sxs-lookup"><span data-stu-id="7e6d2-160">-agc</span></span>      | <span data-ttu-id="7e6d2-161">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-161">Optional.</span></span> <span data-ttu-id="7e6d2-162">開啟 (1) 或 off (0) 的數位 AGC。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="7e6d2-163">您必須開啟功能模式，才能指定此功能。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="7e6d2-164">-cntrclip</span><span class="sxs-lookup"><span data-stu-id="7e6d2-164">-cntrclip</span></span> | <span data-ttu-id="7e6d2-165">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-165">Optional.</span></span> <span data-ttu-id="7e6d2-166">在 (1) 或 off (0) 上開啟中央剪輯。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="7e6d2-167">您必須開啟功能模式，才能指定此功能。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="7e6d2-168">-spkdev</span><span class="sxs-lookup"><span data-stu-id="7e6d2-168">-spkdev</span></span>   | <span data-ttu-id="7e6d2-169">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-169">Optional.</span></span> <span data-ttu-id="7e6d2-170">指定喇叭裝置索引。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-170">Specifies speaker device index.</span></span> <span data-ttu-id="7e6d2-171">如果未指定，系統會要求使用者選取。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="7e6d2-172">-micdev</span><span class="sxs-lookup"><span data-stu-id="7e6d2-172">-micdev</span></span>   | <span data-ttu-id="7e6d2-173">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-173">Optional.</span></span> <span data-ttu-id="7e6d2-174">指定麥克風裝置索引。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-174">Specifies microphone device index.</span></span> <span data-ttu-id="7e6d2-175">如果未指定，系統會要求使用者選取。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="7e6d2-176">-持續時間</span><span class="sxs-lookup"><span data-stu-id="7e6d2-176">-duration</span></span> | <span data-ttu-id="7e6d2-177">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-177">Optional.</span></span> <span data-ttu-id="7e6d2-178">指定應用程式執行的時間長度。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="7e6d2-179">這個範例應用程式不會播放任何信號。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-179">This sample application does not play any signals.</span></span> <span data-ttu-id="7e6d2-180">若要適當地執行適用于 AEC 的模式 (模式0和 4) ，使用者必須透過指定給 SQL-DMO 的相同喇叭裝置來播放某些音訊信號 (也就是由 "-spkdev" 選項指定的裝置) ，它會在雙向交談案例中模擬最遠的聲音。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="7e6d2-181">使用者可以使用任何玩家來播放任何音訊信號。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="7e6d2-182">如果選取的喇叭裝置上沒有作用中的轉譯資料流程，則將無法處理。</span><span class="sxs-lookup"><span data-stu-id="7e6d2-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e6d2-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e6d2-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e6d2-184">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="7e6d2-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



