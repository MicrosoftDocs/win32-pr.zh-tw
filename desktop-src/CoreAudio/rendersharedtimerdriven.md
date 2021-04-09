---
description: 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688947"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="72b3a-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="72b3a-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="72b3a-104">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="72b3a-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="72b3a-105">這個範例會示範在共用模式中呈現用戶端的計時器驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="72b3a-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="72b3a-106">若是共用模式資料流程，用戶端會與音訊引擎共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72b3a-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="72b3a-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="72b3a-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="72b3a-108">說明</span><span class="sxs-lookup"><span data-stu-id="72b3a-108">Description</span></span>](#description)
-   [<span data-ttu-id="72b3a-109">需求</span><span class="sxs-lookup"><span data-stu-id="72b3a-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="72b3a-110">下載範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="72b3a-111">建立範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="72b3a-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="72b3a-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="72b3a-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="72b3a-114">Description</span><span class="sxs-lookup"><span data-stu-id="72b3a-114">Description</span></span>

<span data-ttu-id="72b3a-115">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="72b3a-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="72b3a-116">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="72b3a-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="72b3a-117">串流管理作業的 WASAPI。</span><span class="sxs-lookup"><span data-stu-id="72b3a-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b3a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="72b3a-118">Requirements</span></span>



| <span data-ttu-id="72b3a-119">產品</span><span class="sxs-lookup"><span data-stu-id="72b3a-119">Product</span></span>                                                        | <span data-ttu-id="72b3a-120">版本</span><span class="sxs-lookup"><span data-stu-id="72b3a-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="72b3a-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="72b3a-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="72b3a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="72b3a-122">Windows 7</span></span> |
| <span data-ttu-id="72b3a-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="72b3a-123">Visual Studio</span></span>                                                  | <span data-ttu-id="72b3a-124">2008</span><span class="sxs-lookup"><span data-stu-id="72b3a-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="72b3a-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-125">Downloading the Sample</span></span>

<span data-ttu-id="72b3a-126">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="72b3a-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="72b3a-127">Location</span><span class="sxs-lookup"><span data-stu-id="72b3a-127">Location</span></span>    | <span data-ttu-id="72b3a-128">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="72b3a-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b3a-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="72b3a-129">Windows SDK</span></span> | <span data-ttu-id="72b3a-130">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ RenderSharedTimerDriven \\ .。。</span><span class="sxs-lookup"><span data-stu-id="72b3a-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="72b3a-131">建立範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-131">Building the Sample</span></span>

<span data-ttu-id="72b3a-132">若要建立 RenderSharedTimerDriven 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="72b3a-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="72b3a-133">開啟 Windows SDK 的 CMD shell，並變更為 RenderSharedTimerDriven 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="72b3a-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="72b3a-134">在 RenderSharedTimerDriven 目錄中執行命令 `start WASAPIRenderSharedTimerDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPIRenderSharedTimerDriven 專案。</span><span class="sxs-lookup"><span data-stu-id="72b3a-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="72b3a-135">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="72b3a-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="72b3a-136">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="72b3a-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="72b3a-137">在此情況下，除非您明確設定在專案檔 WASAPIRenderSharedTimerDriven 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="72b3a-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="72b3a-138">執行範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-138">Running the Sample</span></span>

<span data-ttu-id="72b3a-139">如果您成功建立示範應用程式，則會產生可執行檔（WASAPIRenderSharedTimerDriven.exe）。</span><span class="sxs-lookup"><span data-stu-id="72b3a-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="72b3a-140">若要執行它，請 `WASAPIRenderSharedTimerDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。</span><span class="sxs-lookup"><span data-stu-id="72b3a-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="72b3a-141">下列範例顯示如何在預設的多媒體裝置上指定播放持續時間來執行範例。</span><span class="sxs-lookup"><span data-stu-id="72b3a-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="72b3a-142">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="72b3a-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="72b3a-143">引數</span><span class="sxs-lookup"><span data-stu-id="72b3a-143">Argument</span></span>        | <span data-ttu-id="72b3a-144">描述</span><span class="sxs-lookup"><span data-stu-id="72b3a-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="72b3a-145">-?</span><span class="sxs-lookup"><span data-stu-id="72b3a-145">-?</span></span>              | <span data-ttu-id="72b3a-146">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="72b3a-146">Shows help.</span></span>                                                |
| <span data-ttu-id="72b3a-147">-H</span><span class="sxs-lookup"><span data-stu-id="72b3a-147">-h</span></span>              | <span data-ttu-id="72b3a-148">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="72b3a-148">Shows help.</span></span>                                                |
| <span data-ttu-id="72b3a-149">-f</span><span class="sxs-lookup"><span data-stu-id="72b3a-149">-f</span></span>              | <span data-ttu-id="72b3a-150">以 Hz 為間隔的正弦波頻率。</span><span class="sxs-lookup"><span data-stu-id="72b3a-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="72b3a-151">-l</span><span class="sxs-lookup"><span data-stu-id="72b3a-151">-l</span></span>              | <span data-ttu-id="72b3a-152">音訊轉譯延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="72b3a-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="72b3a-153">-d</span><span class="sxs-lookup"><span data-stu-id="72b3a-153">-d</span></span>              | <span data-ttu-id="72b3a-154">正弦波持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="72b3a-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="72b3a-155">-M</span><span class="sxs-lookup"><span data-stu-id="72b3a-155">-m</span></span>              | <span data-ttu-id="72b3a-156">停用 MMCSS。</span><span class="sxs-lookup"><span data-stu-id="72b3a-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="72b3a-157">-主控台</span><span class="sxs-lookup"><span data-stu-id="72b3a-157">-console</span></span>        | <span data-ttu-id="72b3a-158">使用預設的主控台裝置。</span><span class="sxs-lookup"><span data-stu-id="72b3a-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="72b3a-159">-通訊</span><span class="sxs-lookup"><span data-stu-id="72b3a-159">-communications</span></span> | <span data-ttu-id="72b3a-160">使用預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="72b3a-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="72b3a-161">-多媒體</span><span class="sxs-lookup"><span data-stu-id="72b3a-161">-multimedia</span></span>     | <span data-ttu-id="72b3a-162">使用預設的多媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="72b3a-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="72b3a-163">-端點</span><span class="sxs-lookup"><span data-stu-id="72b3a-163">-endpoint</span></span>       | <span data-ttu-id="72b3a-164">使用參數值中指定的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="72b3a-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="72b3a-165">如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取轉譯會話的裝置。</span><span class="sxs-lookup"><span data-stu-id="72b3a-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="72b3a-166">當使用者指定裝置之後，應用程式會以 440 Hz 轉譯正弦波，以達10秒。</span><span class="sxs-lookup"><span data-stu-id="72b3a-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="72b3a-167">您可以藉由指定-f 和-d 參數值來修改這些值。</span><span class="sxs-lookup"><span data-stu-id="72b3a-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="72b3a-168">RenderSharedTimerDriven 示範計時器驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="72b3a-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="72b3a-169">在此模式中，用戶端必須等待一段時間， (-d 參數值所指定的時間長度（以毫秒為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="72b3a-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="72b3a-170">當用戶端喚醒時，會從引擎提取下一組範例。</span><span class="sxs-lookup"><span data-stu-id="72b3a-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="72b3a-171">在緩衝迴圈中的每個處理階段之前，用戶端必須找出要轉譯的資料量，讓資料不會溢出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72b3a-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="72b3a-172">要在指定的裝置上播放的音訊資料，可透過啟用事件驅動的緩衝處理來處理。</span><span class="sxs-lookup"><span data-stu-id="72b3a-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="72b3a-173">[RenderSharedEventDriven](rendersharedeventdriven.md)範例會示範這個模式。</span><span class="sxs-lookup"><span data-stu-id="72b3a-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="72b3a-174">如需呈現資料流程的詳細資訊，請參閱轉譯 [資料流程](rendering-a-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="72b3a-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="72b3a-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="72b3a-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72b3a-176">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="72b3a-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



