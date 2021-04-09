---
description: 這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。 這個範例示範事件驅動的緩衝。
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110789"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="d396f-104">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="d396f-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="d396f-105">這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="d396f-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="d396f-106">這個範例示範事件驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="d396f-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="d396f-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d396f-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d396f-108">說明</span><span class="sxs-lookup"><span data-stu-id="d396f-108">Description</span></span>](#description)
-   [<span data-ttu-id="d396f-109">需求</span><span class="sxs-lookup"><span data-stu-id="d396f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d396f-110">下載範例</span><span class="sxs-lookup"><span data-stu-id="d396f-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d396f-111">建立範例</span><span class="sxs-lookup"><span data-stu-id="d396f-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d396f-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="d396f-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d396f-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="d396f-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d396f-114">Description</span><span class="sxs-lookup"><span data-stu-id="d396f-114">Description</span></span>

<span data-ttu-id="d396f-115">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="d396f-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="d396f-116">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="d396f-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="d396f-117">串流管理作業的[WASAPI](wasapi.md) ，例如啟動和停止資料流程，以及串流切換。</span><span class="sxs-lookup"><span data-stu-id="d396f-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="d396f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d396f-118">Requirements</span></span>



| <span data-ttu-id="d396f-119">產品</span><span class="sxs-lookup"><span data-stu-id="d396f-119">Product</span></span>                                                        | <span data-ttu-id="d396f-120">版本</span><span class="sxs-lookup"><span data-stu-id="d396f-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d396f-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d396f-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d396f-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d396f-122">Windows 7</span></span> |
| <span data-ttu-id="d396f-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d396f-123">Visual Studio</span></span>                                                  | <span data-ttu-id="d396f-124">2008</span><span class="sxs-lookup"><span data-stu-id="d396f-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d396f-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="d396f-125">Downloading the Sample</span></span>

<span data-ttu-id="d396f-126">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="d396f-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d396f-127">Location</span><span class="sxs-lookup"><span data-stu-id="d396f-127">Location</span></span>    | <span data-ttu-id="d396f-128">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="d396f-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d396f-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d396f-129">Windows SDK</span></span> | <span data-ttu-id="d396f-130">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ CaptureSharedEventDriven \\ .。。</span><span class="sxs-lookup"><span data-stu-id="d396f-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="d396f-131">建立範例</span><span class="sxs-lookup"><span data-stu-id="d396f-131">Building the Sample</span></span>

<span data-ttu-id="d396f-132">若要建立 CaptureSharedEventDriven 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d396f-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="d396f-133">開啟 Windows SDK 的 CMD shell，並變更為 CaptureSharedEventDriven 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="d396f-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="d396f-134">在 CaptureSharedEventDriven 目錄中執行命令 `start WASAPICaptureSharedEventDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPICaptureSharedEventDriven 專案。</span><span class="sxs-lookup"><span data-stu-id="d396f-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="d396f-135">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="d396f-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="d396f-136">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="d396f-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="d396f-137">在此情況下，除非您明確設定在專案檔 WASAPICaptureSharedEventDriven 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="d396f-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d396f-138">執行範例</span><span class="sxs-lookup"><span data-stu-id="d396f-138">Running the Sample</span></span>

<span data-ttu-id="d396f-139">如果您成功建立示範應用程式，則會產生可執行檔（WASAPICaptureSharedEventDriven.exe）。</span><span class="sxs-lookup"><span data-stu-id="d396f-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="d396f-140">若要執行它，請 `WASAPICaptureSharedEventDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。</span><span class="sxs-lookup"><span data-stu-id="d396f-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="d396f-141">下列範例顯示如何在預設的多媒體裝置上指定捕捉持續時間來執行範例。</span><span class="sxs-lookup"><span data-stu-id="d396f-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="d396f-142">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="d396f-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="d396f-143">引數</span><span class="sxs-lookup"><span data-stu-id="d396f-143">Argument</span></span>        | <span data-ttu-id="d396f-144">描述</span><span class="sxs-lookup"><span data-stu-id="d396f-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="d396f-145">-?</span><span class="sxs-lookup"><span data-stu-id="d396f-145">-?</span></span>              | <span data-ttu-id="d396f-146">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="d396f-146">Shows help.</span></span>                                                |
| <span data-ttu-id="d396f-147">-H</span><span class="sxs-lookup"><span data-stu-id="d396f-147">-h</span></span>              | <span data-ttu-id="d396f-148">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="d396f-148">Shows help.</span></span>                                                |
| <span data-ttu-id="d396f-149">-l</span><span class="sxs-lookup"><span data-stu-id="d396f-149">-l</span></span>              | <span data-ttu-id="d396f-150">音訊捕獲延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d396f-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="d396f-151">-d</span><span class="sxs-lookup"><span data-stu-id="d396f-151">-d</span></span>              | <span data-ttu-id="d396f-152">音訊捕獲持續時間（秒）。</span><span class="sxs-lookup"><span data-stu-id="d396f-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="d396f-153">-M</span><span class="sxs-lookup"><span data-stu-id="d396f-153">-m</span></span>              | <span data-ttu-id="d396f-154">停用 MMCSS。</span><span class="sxs-lookup"><span data-stu-id="d396f-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="d396f-155">-主控台</span><span class="sxs-lookup"><span data-stu-id="d396f-155">-console</span></span>        | <span data-ttu-id="d396f-156">使用預設的主控台裝置。</span><span class="sxs-lookup"><span data-stu-id="d396f-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="d396f-157">-通訊</span><span class="sxs-lookup"><span data-stu-id="d396f-157">-communications</span></span> | <span data-ttu-id="d396f-158">使用預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="d396f-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="d396f-159">-多媒體</span><span class="sxs-lookup"><span data-stu-id="d396f-159">-multimedia</span></span>     | <span data-ttu-id="d396f-160">使用預設的多媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="d396f-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="d396f-161">-端點</span><span class="sxs-lookup"><span data-stu-id="d396f-161">-endpoint</span></span>       | <span data-ttu-id="d396f-162">使用參數值中指定的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="d396f-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="d396f-163">如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取要用於捕獲會話的裝置。</span><span class="sxs-lookup"><span data-stu-id="d396f-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="d396f-164">預設的主控台、通訊和多媒體裝置會列出，後面接著 [裝置] 和 [端點識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d396f-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="d396f-165">如果未指定持續時間，則會從指定的裝置捕獲音訊串流10秒。</span><span class="sxs-lookup"><span data-stu-id="d396f-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="d396f-166">應用程式會將已捕捉的資料寫入至唯一命名的 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="d396f-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="d396f-167">CaptureSharedEventDriven 示範事件驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="d396f-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="d396f-168">針對此範例具現化的音訊用戶端設定為在共用模式中執行，而用戶端的音訊緩衝區處理是由在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)的呼叫中設定 **AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback** 旗標，使事件成為驅動。</span><span class="sxs-lookup"><span data-stu-id="d396f-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="d396f-169">此範例會顯示用戶端如何藉由呼叫 [**IAudioClient：： SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) 方法，提供事件控制碼給系統。</span><span class="sxs-lookup"><span data-stu-id="d396f-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="d396f-170">當 capture 會話開始且資料流程開始時，音訊引擎會發出通知給用戶端的事件處理常式，每次緩衝區準備好供用戶端處理時使用。</span><span class="sxs-lookup"><span data-stu-id="d396f-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="d396f-171">音訊資料也可以在計時器驅動迴圈中處理。</span><span class="sxs-lookup"><span data-stu-id="d396f-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="d396f-172">這是在 [CaptureSharedTimerDriven](capturesharedtimerdriven.md) 範例中 demostrated 的模式。</span><span class="sxs-lookup"><span data-stu-id="d396f-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d396f-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="d396f-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d396f-174">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="d396f-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



