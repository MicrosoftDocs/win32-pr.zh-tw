---
description: 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。 這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468328"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="6450f-104">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="6450f-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="6450f-105">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="6450f-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="6450f-106">這個範例會示範在獨佔模式中呈現用戶端的計時器驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="6450f-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="6450f-107">如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6450f-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="6450f-108">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6450f-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6450f-109">說明</span><span class="sxs-lookup"><span data-stu-id="6450f-109">Description</span></span>](#description)
-   [<span data-ttu-id="6450f-110">需求</span><span class="sxs-lookup"><span data-stu-id="6450f-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6450f-111">下載範例</span><span class="sxs-lookup"><span data-stu-id="6450f-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6450f-112">建立範例</span><span class="sxs-lookup"><span data-stu-id="6450f-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6450f-113">查看範例檔案</span><span class="sxs-lookup"><span data-stu-id="6450f-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="6450f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="6450f-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="6450f-115">Description</span><span class="sxs-lookup"><span data-stu-id="6450f-115">Description</span></span>

<span data-ttu-id="6450f-116">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="6450f-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="6450f-117">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="6450f-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="6450f-118">串流管理作業的 WASAPI。</span><span class="sxs-lookup"><span data-stu-id="6450f-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="6450f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6450f-119">Requirements</span></span>



| <span data-ttu-id="6450f-120">產品</span><span class="sxs-lookup"><span data-stu-id="6450f-120">Product</span></span>                                                        | <span data-ttu-id="6450f-121">版本</span><span class="sxs-lookup"><span data-stu-id="6450f-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="6450f-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6450f-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="6450f-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6450f-123">Windows 7</span></span> |
| <span data-ttu-id="6450f-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6450f-124">Visual Studio</span></span>                                                  | <span data-ttu-id="6450f-125">2008</span><span class="sxs-lookup"><span data-stu-id="6450f-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6450f-126">下載範例</span><span class="sxs-lookup"><span data-stu-id="6450f-126">Downloading the Sample</span></span>

<span data-ttu-id="6450f-127">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="6450f-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="6450f-128">Location</span><span class="sxs-lookup"><span data-stu-id="6450f-128">Location</span></span>    | <span data-ttu-id="6450f-129">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="6450f-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6450f-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="6450f-130">Windows SDK</span></span> | <span data-ttu-id="6450f-131">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ RenderExclusiveTimerDriven \\ .。。</span><span class="sxs-lookup"><span data-stu-id="6450f-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="6450f-132">建立範例</span><span class="sxs-lookup"><span data-stu-id="6450f-132">Building the Sample</span></span>

<span data-ttu-id="6450f-133">若要建立 RenderExclusiveTimerDriven 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="6450f-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="6450f-134">開啟 Windows SDK 的 CMD shell，並變更為 RenderExclusiveTimerDriven 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="6450f-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="6450f-135">在 RenderExclusiveTimerDriven 目錄中執行命令 `start WASAPIRenderExclusiveTimerDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPIRenderExclusiveTimerDriven 專案。</span><span class="sxs-lookup"><span data-stu-id="6450f-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="6450f-136">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="6450f-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="6450f-137">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="6450f-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="6450f-138">在此情況下，除非您明確設定在專案檔 WASAPIRenderExclusiveTimerDriven 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="6450f-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="6450f-139">查看範例檔案</span><span class="sxs-lookup"><span data-stu-id="6450f-139">View the Sample Files</span></span>

<span data-ttu-id="6450f-140">如果您成功建立示範應用程式，則會產生可執行檔（WASAPIRenderExclusiveTimerDriven.exe）。</span><span class="sxs-lookup"><span data-stu-id="6450f-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="6450f-141">若要執行它，請 `WASAPIRenderExclusiveTimerDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。</span><span class="sxs-lookup"><span data-stu-id="6450f-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="6450f-142">下列範例顯示如何在預設主控台裝置上指定播放持續時間來執行範例。</span><span class="sxs-lookup"><span data-stu-id="6450f-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="6450f-143">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="6450f-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="6450f-144">引數</span><span class="sxs-lookup"><span data-stu-id="6450f-144">Argument</span></span>        | <span data-ttu-id="6450f-145">描述</span><span class="sxs-lookup"><span data-stu-id="6450f-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="6450f-146">-?</span><span class="sxs-lookup"><span data-stu-id="6450f-146">-?</span></span>              | <span data-ttu-id="6450f-147">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="6450f-147">Shows help.</span></span>                                                |
| <span data-ttu-id="6450f-148">-H</span><span class="sxs-lookup"><span data-stu-id="6450f-148">-h</span></span>              | <span data-ttu-id="6450f-149">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="6450f-149">Shows help.</span></span>                                                |
| <span data-ttu-id="6450f-150">-f</span><span class="sxs-lookup"><span data-stu-id="6450f-150">-f</span></span>              | <span data-ttu-id="6450f-151">以 Hz 為間隔的正弦波頻率。</span><span class="sxs-lookup"><span data-stu-id="6450f-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="6450f-152">-l</span><span class="sxs-lookup"><span data-stu-id="6450f-152">-l</span></span>              | <span data-ttu-id="6450f-153">音訊轉譯延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6450f-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="6450f-154">-d</span><span class="sxs-lookup"><span data-stu-id="6450f-154">-d</span></span>              | <span data-ttu-id="6450f-155">正弦波持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6450f-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="6450f-156">-M</span><span class="sxs-lookup"><span data-stu-id="6450f-156">-m</span></span>              | <span data-ttu-id="6450f-157">停用 MMCSS。</span><span class="sxs-lookup"><span data-stu-id="6450f-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="6450f-158">-主控台</span><span class="sxs-lookup"><span data-stu-id="6450f-158">-console</span></span>        | <span data-ttu-id="6450f-159">使用預設的主控台裝置。</span><span class="sxs-lookup"><span data-stu-id="6450f-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="6450f-160">-通訊</span><span class="sxs-lookup"><span data-stu-id="6450f-160">-communications</span></span> | <span data-ttu-id="6450f-161">使用預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="6450f-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="6450f-162">-多媒體</span><span class="sxs-lookup"><span data-stu-id="6450f-162">-multimedia</span></span>     | <span data-ttu-id="6450f-163">使用預設的多媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="6450f-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="6450f-164">-端點</span><span class="sxs-lookup"><span data-stu-id="6450f-164">-endpoint</span></span>       | <span data-ttu-id="6450f-165">使用參數值中指定的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="6450f-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="6450f-166">如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取轉譯會話的裝置。</span><span class="sxs-lookup"><span data-stu-id="6450f-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="6450f-167">當使用者指定裝置之後，應用程式會以 440 Hz 轉譯正弦波，以達10秒。</span><span class="sxs-lookup"><span data-stu-id="6450f-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="6450f-168">您可以藉由指定-f 和-d 參數值來修改這些值。</span><span class="sxs-lookup"><span data-stu-id="6450f-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="6450f-169">RenderExclusiveTimerDriven 示範計時器驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="6450f-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="6450f-170">在此模式中，用戶端必須等待一段時間， (-d 參數值所指定的時間長度（以毫秒為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="6450f-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="6450f-171">當用戶端喚醒時，會從引擎提取下一組範例。</span><span class="sxs-lookup"><span data-stu-id="6450f-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="6450f-172">在緩衝迴圈中的每個處理階段之前，用戶端必須找出要轉譯的資料量，讓資料不會溢出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6450f-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="6450f-173">要在指定的裝置上播放的音訊資料，可透過啟用事件驅動的緩衝處理來處理。</span><span class="sxs-lookup"><span data-stu-id="6450f-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="6450f-174">RenderExclusiveTimerDriven 範例會示範這個模式。</span><span class="sxs-lookup"><span data-stu-id="6450f-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="6450f-175">如需呈現資料流程的詳細資訊，請參閱轉譯 [資料流程](rendering-a-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="6450f-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6450f-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="6450f-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6450f-177">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="6450f-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



