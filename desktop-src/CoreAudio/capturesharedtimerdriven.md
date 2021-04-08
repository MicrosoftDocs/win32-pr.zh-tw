---
description: 這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。 這個範例示範計時器驅動的緩衝。
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025932"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="0b325-104">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="0b325-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="0b325-105">這個範例應用程式會使用核心音訊 Api，從使用者指定的輸入裝置捕獲音訊資料，並將其寫入至目前目錄中唯一命名的 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="0b325-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="0b325-106">這個範例示範計時器驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="0b325-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="0b325-107">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0b325-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0b325-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b325-108">Description</span></span>](#description)
-   [<span data-ttu-id="0b325-109">需求</span><span class="sxs-lookup"><span data-stu-id="0b325-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0b325-110">下載範例</span><span class="sxs-lookup"><span data-stu-id="0b325-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="0b325-111">建立範例</span><span class="sxs-lookup"><span data-stu-id="0b325-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="0b325-112">執行範例</span><span class="sxs-lookup"><span data-stu-id="0b325-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="0b325-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b325-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="0b325-114">Description</span><span class="sxs-lookup"><span data-stu-id="0b325-114">Description</span></span>

<span data-ttu-id="0b325-115">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="0b325-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="0b325-116">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b325-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="0b325-117">串流管理作業的[WASAPI](wasapi.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b325-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b325-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b325-118">Requirements</span></span>



| <span data-ttu-id="0b325-119">產品</span><span class="sxs-lookup"><span data-stu-id="0b325-119">Product</span></span>                                                        | <span data-ttu-id="0b325-120">版本</span><span class="sxs-lookup"><span data-stu-id="0b325-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0b325-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0b325-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0b325-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b325-122">Windows 7</span></span> |
| <span data-ttu-id="0b325-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0b325-123">Visual Studio</span></span>                                                  | <span data-ttu-id="0b325-124">2008</span><span class="sxs-lookup"><span data-stu-id="0b325-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0b325-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="0b325-125">Downloading the Sample</span></span>

<span data-ttu-id="0b325-126">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="0b325-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="0b325-127">Location</span><span class="sxs-lookup"><span data-stu-id="0b325-127">Location</span></span>    | <span data-ttu-id="0b325-128">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="0b325-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b325-129">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0b325-129">Windows SDK</span></span> | <span data-ttu-id="0b325-130">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ CaptureSharedTimerDriven \\ .。。</span><span class="sxs-lookup"><span data-stu-id="0b325-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="0b325-131">建立範例</span><span class="sxs-lookup"><span data-stu-id="0b325-131">Building the Sample</span></span>

<span data-ttu-id="0b325-132">若要建立 CaptureSharedTimerDriven 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="0b325-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="0b325-133">開啟 Windows SDK 的 CMD shell，並變更為 CaptureSharedTimerDriven 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="0b325-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="0b325-134">在 CaptureSharedTimerDriven 目錄中執行命令 `start WASAPICaptureSharedTimerDriven.sln` ，以在 Visual Studio 視窗中開啟 WASAPICaptureSharedTimerDriven 專案。</span><span class="sxs-lookup"><span data-stu-id="0b325-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="0b325-135">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="0b325-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="0b325-136">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="0b325-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="0b325-137">在此情況下，除非您明確設定在專案檔 WASAPICaptureSharedTimerDriven 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="0b325-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0b325-138">執行範例</span><span class="sxs-lookup"><span data-stu-id="0b325-138">Running the Sample</span></span>

<span data-ttu-id="0b325-139">如果您成功建立示範應用程式，則會產生可執行檔（WASAPICaptureSharedTimerDriven.exe）。</span><span class="sxs-lookup"><span data-stu-id="0b325-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="0b325-140">若要執行它，請 `WASAPICaptureSharedTimerDriven` 在命令視窗中輸入，後面接著必要或選擇性的引數。</span><span class="sxs-lookup"><span data-stu-id="0b325-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="0b325-141">下列範例顯示如何在預設的多媒體裝置上指定捕捉持續時間來執行範例。</span><span class="sxs-lookup"><span data-stu-id="0b325-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="0b325-142">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="0b325-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="0b325-143">引數</span><span class="sxs-lookup"><span data-stu-id="0b325-143">Argument</span></span>        | <span data-ttu-id="0b325-144">描述</span><span class="sxs-lookup"><span data-stu-id="0b325-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="0b325-145">-?</span><span class="sxs-lookup"><span data-stu-id="0b325-145">-?</span></span>              | <span data-ttu-id="0b325-146">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="0b325-146">Shows help.</span></span>                                                |
| <span data-ttu-id="0b325-147">-H</span><span class="sxs-lookup"><span data-stu-id="0b325-147">-h</span></span>              | <span data-ttu-id="0b325-148">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="0b325-148">Shows help.</span></span>                                                |
| <span data-ttu-id="0b325-149">-l</span><span class="sxs-lookup"><span data-stu-id="0b325-149">-l</span></span>              | <span data-ttu-id="0b325-150">音訊捕獲延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0b325-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="0b325-151">-d</span><span class="sxs-lookup"><span data-stu-id="0b325-151">-d</span></span>              | <span data-ttu-id="0b325-152">音訊捕獲持續時間（秒）。</span><span class="sxs-lookup"><span data-stu-id="0b325-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="0b325-153">-M</span><span class="sxs-lookup"><span data-stu-id="0b325-153">-m</span></span>              | <span data-ttu-id="0b325-154">停用 MMCSS。</span><span class="sxs-lookup"><span data-stu-id="0b325-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="0b325-155">-主控台</span><span class="sxs-lookup"><span data-stu-id="0b325-155">-console</span></span>        | <span data-ttu-id="0b325-156">使用預設的主控台裝置。</span><span class="sxs-lookup"><span data-stu-id="0b325-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="0b325-157">-通訊</span><span class="sxs-lookup"><span data-stu-id="0b325-157">-communications</span></span> | <span data-ttu-id="0b325-158">使用預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="0b325-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="0b325-159">-多媒體</span><span class="sxs-lookup"><span data-stu-id="0b325-159">-multimedia</span></span>     | <span data-ttu-id="0b325-160">使用預設的多媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="0b325-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="0b325-161">-端點</span><span class="sxs-lookup"><span data-stu-id="0b325-161">-endpoint</span></span>       | <span data-ttu-id="0b325-162">使用參數值中指定的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b325-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="0b325-163">如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取要用於捕獲會話的裝置。</span><span class="sxs-lookup"><span data-stu-id="0b325-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="0b325-164">預設的主控台、通訊和多媒體裝置會列出，後面接著 [裝置] 和 [端點識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0b325-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="0b325-165">如果未指定持續時間，則會從指定的裝置捕獲音訊串流10秒。</span><span class="sxs-lookup"><span data-stu-id="0b325-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="0b325-166">應用程式會將已捕捉的資料寫入至唯一命名的 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="0b325-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="0b325-167">CaptureSharedTimerDriven 示範計時器驅動的緩衝。</span><span class="sxs-lookup"><span data-stu-id="0b325-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="0b325-168">在此模式中，用戶端必須等待一段時間， (-d 參數值所指定的時間長度（以毫秒為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="0b325-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="0b325-169">當用戶端喚醒時，會從引擎提取下一組範例。</span><span class="sxs-lookup"><span data-stu-id="0b325-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="0b325-170">用戶端必須先找出可用的捕獲資料量，讓資料不會溢出擷取緩衝區，才能在每次處理的緩衝迴圈中傳遞。</span><span class="sxs-lookup"><span data-stu-id="0b325-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="0b325-171">您可以藉由啟用事件驅動的緩衝處理，來處理從指定的裝置所捕捉的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="0b325-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="0b325-172">[CaptureSharedEventDriven](capturesharedeventdriven.md)範例會示範這個模式。</span><span class="sxs-lookup"><span data-stu-id="0b325-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b325-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b325-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b325-174">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="0b325-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



