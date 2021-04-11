---
description: 這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b94fa423cd4d4e7dc7121e927696529bfadf9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025942"
---
# <a name="renderexclusiveeventdriven"></a><span data-ttu-id="9ea6e-103">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="9ea6e-103">RenderExclusiveEventDriven</span></span>

<span data-ttu-id="9ea6e-104">這個範例應用程式會使用核心音訊 Api，將音訊資料轉譯為使用者指定的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="9ea6e-105">這個範例會示範在獨佔模式中呈現用戶端的事件驅動緩衝。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-105">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="9ea6e-106">如果是獨佔模式資料流程，用戶端會與音訊裝置共用端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-106">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="9ea6e-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9ea6e-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ea6e-108">Description</span></span>](#description)
-   [<span data-ttu-id="9ea6e-109">需求</span><span class="sxs-lookup"><span data-stu-id="9ea6e-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9ea6e-110">下載範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="9ea6e-111">建立範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="9ea6e-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="9ea6e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ea6e-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="9ea6e-114">Description</span><span class="sxs-lookup"><span data-stu-id="9ea6e-114">Description</span></span>

<span data-ttu-id="9ea6e-115">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="9ea6e-116">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="9ea6e-117">串流管理作業的 WASAPI。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea6e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ea6e-118">Requirements</span></span>



| <span data-ttu-id="9ea6e-119">產品</span><span class="sxs-lookup"><span data-stu-id="9ea6e-119">Product</span></span>                                                        | <span data-ttu-id="9ea6e-120">版本</span><span class="sxs-lookup"><span data-stu-id="9ea6e-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="9ea6e-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9ea6e-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="9ea6e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ea6e-122">Windows 7</span></span> |
| <span data-ttu-id="9ea6e-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9ea6e-123">Visual Studio</span></span>                                                  | <span data-ttu-id="9ea6e-124">2008</span><span class="sxs-lookup"><span data-stu-id="9ea6e-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9ea6e-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-125">Downloading the Sample</span></span>

<span data-ttu-id="9ea6e-126">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="9ea6e-127">Location</span><span class="sxs-lookup"><span data-stu-id="9ea6e-127">Location</span></span>    | <span data-ttu-id="9ea6e-128">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="9ea6e-128">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea6e-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="9ea6e-129">Windows SDK</span></span> | <span data-ttu-id="9ea6e-130">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ RenderExclusiveEventDriven \\ .。。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="9ea6e-131">建立範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-131">Building the Sample</span></span>

<span data-ttu-id="9ea6e-132">若要建立 RenderExclusiveEventDriven 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9ea6e-132">To build the RenderExclusiveEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="9ea6e-133">開啟 Windows SDK 的 CMD shell，並變更為 RenderExclusiveEventDriven 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-133">Open the CMD shell for the Windows SDK and change to the RenderExclusiveEventDriven sample directory.</span></span>
2.  <span data-ttu-id="9ea6e-134">在 RenderExclusiveEventDriven 目錄中執行命令 `start WASAPIRenderExclusiveEventDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPIRenderExclusiveEventDriven 專案。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-134">Run the command `start WASAPIRenderExclusiveEventDriven.sln` in the RenderExclusiveEventDriven directory to open the WASAPIRenderExclusiveEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="9ea6e-135">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="9ea6e-136">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="9ea6e-137">在此情況下，除非您明確設定在專案檔 WASAPIRenderExclusiveEventDriven 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="9ea6e-138">執行範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-138">Running the Sample</span></span>

<span data-ttu-id="9ea6e-139">如果您成功建立示範應用程式，則會產生可執行檔（WASAPIRenderExclusiveEventDriven.exe）。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-139">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveEventDriven.exe, is generated.</span></span> <span data-ttu-id="9ea6e-140">若要執行它，請 `WASAPIRenderExclusiveEventDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-140">To run it, type `WASAPIRenderExclusiveEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="9ea6e-141">下列範例顯示如何在預設的多媒體裝置上指定播放持續時間來執行範例。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="9ea6e-142">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="9ea6e-143">引數</span><span class="sxs-lookup"><span data-stu-id="9ea6e-143">Argument</span></span>        | <span data-ttu-id="9ea6e-144">描述</span><span class="sxs-lookup"><span data-stu-id="9ea6e-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="9ea6e-145">-?</span><span class="sxs-lookup"><span data-stu-id="9ea6e-145">-?</span></span>              | <span data-ttu-id="9ea6e-146">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-146">Shows help.</span></span>                                                |
| <span data-ttu-id="9ea6e-147">-H</span><span class="sxs-lookup"><span data-stu-id="9ea6e-147">-h</span></span>              | <span data-ttu-id="9ea6e-148">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-148">Shows help.</span></span>                                                |
| <span data-ttu-id="9ea6e-149">-f</span><span class="sxs-lookup"><span data-stu-id="9ea6e-149">-f</span></span>              | <span data-ttu-id="9ea6e-150">以 Hz 為間隔的正弦波頻率。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="9ea6e-151">-l</span><span class="sxs-lookup"><span data-stu-id="9ea6e-151">-l</span></span>              | <span data-ttu-id="9ea6e-152">音訊轉譯延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="9ea6e-153">-d</span><span class="sxs-lookup"><span data-stu-id="9ea6e-153">-d</span></span>              | <span data-ttu-id="9ea6e-154">正弦波持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="9ea6e-155">-M</span><span class="sxs-lookup"><span data-stu-id="9ea6e-155">-m</span></span>              | <span data-ttu-id="9ea6e-156">停用 MMCSS。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="9ea6e-157">-主控台</span><span class="sxs-lookup"><span data-stu-id="9ea6e-157">-console</span></span>        | <span data-ttu-id="9ea6e-158">使用預設的主控台裝置。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="9ea6e-159">-通訊</span><span class="sxs-lookup"><span data-stu-id="9ea6e-159">-communications</span></span> | <span data-ttu-id="9ea6e-160">使用預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="9ea6e-161">-多媒體</span><span class="sxs-lookup"><span data-stu-id="9ea6e-161">-multimedia</span></span>     | <span data-ttu-id="9ea6e-162">使用預設的多媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="9ea6e-163">-端點</span><span class="sxs-lookup"><span data-stu-id="9ea6e-163">-endpoint</span></span>       | <span data-ttu-id="9ea6e-164">使用參數值中指定的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="9ea6e-165">如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取轉譯會話的裝置。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="9ea6e-166">當使用者指定裝置之後，應用程式會以 440 Hz 轉譯正弦波，以達10秒。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="9ea6e-167">您可以藉由指定-f 和-d 參數值來修改這些值。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="9ea6e-168">RenderExclusiveEventDriven 範例會示範事件驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-168">The RenderExclusiveEventDriven sample demonstrates event-driven buffering.</span></span> <span data-ttu-id="9ea6e-169">此範例顯示如何：</span><span class="sxs-lookup"><span data-stu-id="9ea6e-169">The sample shows how to:</span></span>

-   <span data-ttu-id="9ea6e-170">將音訊用戶端具現化，將其設定為在獨佔模式中執行，並在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)的呼叫中設定 **AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback** 旗標，以啟用事件驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="9ea6e-171">藉由呼叫 [**IAudioClient：： SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) 方法，將用戶端與準備好呈現的範例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="9ea6e-172">建立轉譯執行緒，以處理來自音訊引擎的範例。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-172">Create a render thread to process samples from the audio engine.</span></span>
-   <span data-ttu-id="9ea6e-173">在將緩衝區傳送至裝置之前，請先在128位元組界限上適當地對齊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-173">Align the buffers properly on a 128-byte boundary before sending them to the device.</span></span> <span data-ttu-id="9ea6e-174">這是藉由調整引擎的週期來完成。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-174">This is done by adjusting the periodicity of the engine.</span></span>
-   <span data-ttu-id="9ea6e-175">檢查裝置端點的混合格式，以判斷是否可以轉譯樣本。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-175">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="9ea6e-176">如果裝置不支援混合格式，資料會轉換成 PCM。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-176">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="9ea6e-177">處理資料流程切換。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-177">Handle stream switching.</span></span>

<span data-ttu-id="9ea6e-178">當轉譯會話開始且資料流程開始時，音訊引擎會發出通知給用戶端的事件處理常式，以便在每次緩衝區可供用戶端處理時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-178">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="9ea6e-179">音訊資料也可以在計時器驅動迴圈中處理。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-179">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="9ea6e-180">[RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)範例會示範這個模式。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-180">This mode is demonstrated in the [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md) sample.</span></span>

<span data-ttu-id="9ea6e-181">如需呈現資料流程的詳細資訊，請參閱轉譯 [資料流程](rendering-a-stream.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea6e-181">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ea6e-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ea6e-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea6e-183">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="9ea6e-183">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



