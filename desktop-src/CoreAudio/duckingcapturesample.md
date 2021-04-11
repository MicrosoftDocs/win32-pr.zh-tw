---
description: 這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847577"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="383d0-103">DuckingCaptureSample</span><span class="sxs-lookup"><span data-stu-id="383d0-103">DuckingCaptureSample</span></span>

<span data-ttu-id="383d0-104">這個範例應用程式會示範如何開啟和關閉通訊資料流程，以及造成應用程式可取得以執行資料流程衰減的回避事件。</span><span class="sxs-lookup"><span data-stu-id="383d0-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="383d0-105">此應用程式會執行聊天用戶端，此用戶端會使用核心音訊 Api 從通訊裝置讀取音訊資料，並在輸出裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="383d0-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="383d0-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="383d0-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="383d0-107">說明</span><span class="sxs-lookup"><span data-stu-id="383d0-107">Description</span></span>](#description)
-   [<span data-ttu-id="383d0-108">需求</span><span class="sxs-lookup"><span data-stu-id="383d0-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="383d0-109">下載範例</span><span class="sxs-lookup"><span data-stu-id="383d0-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="383d0-110">建立範例</span><span class="sxs-lookup"><span data-stu-id="383d0-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="383d0-111">執行範例</span><span class="sxs-lookup"><span data-stu-id="383d0-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="383d0-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="383d0-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="383d0-113">Description</span><span class="sxs-lookup"><span data-stu-id="383d0-113">Description</span></span>

<span data-ttu-id="383d0-114">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="383d0-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="383d0-115">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="383d0-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="383d0-116">用來存取通訊捕捉和轉譯裝置、串流管理作業，以及處理回避事件的[WASAPI](wasapi.md) 。</span><span class="sxs-lookup"><span data-stu-id="383d0-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="383d0-117">用於存取通訊裝置和捕獲音訊輸入的[WAVE api](/previous-versions//ms713499(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="383d0-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="383d0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="383d0-118">Requirements</span></span>



| <span data-ttu-id="383d0-119">產品</span><span class="sxs-lookup"><span data-stu-id="383d0-119">Product</span></span>                                                        | <span data-ttu-id="383d0-120">版本</span><span class="sxs-lookup"><span data-stu-id="383d0-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="383d0-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="383d0-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="383d0-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="383d0-122">Windows 7</span></span> |
| <span data-ttu-id="383d0-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="383d0-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="383d0-124">下載範例</span><span class="sxs-lookup"><span data-stu-id="383d0-124">Downloading the Sample</span></span>

<span data-ttu-id="383d0-125">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="383d0-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="383d0-126">Location</span><span class="sxs-lookup"><span data-stu-id="383d0-126">Location</span></span>    | <span data-ttu-id="383d0-127">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="383d0-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="383d0-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="383d0-128">Windows SDK</span></span> | <span data-ttu-id="383d0-129">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ DuckingCaptureSample \\ .。。</span><span class="sxs-lookup"><span data-stu-id="383d0-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="383d0-130">建立範例</span><span class="sxs-lookup"><span data-stu-id="383d0-130">Building the Sample</span></span>

<span data-ttu-id="383d0-131">若要建立 DuckingCaptureSample 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="383d0-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="383d0-132">在 Visual Studio 2008 中開啟 DuckingCaptureSample .sln。</span><span class="sxs-lookup"><span data-stu-id="383d0-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="383d0-133">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="383d0-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="383d0-134">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="383d0-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="383d0-135">在此情況下，除非您明確設定在專案檔 DuckingCaptureSample 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="383d0-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="383d0-136">執行範例</span><span class="sxs-lookup"><span data-stu-id="383d0-136">Running the Sample</span></span>

<span data-ttu-id="383d0-137">如果您成功建立應用程式，則會產生可執行檔（DuckingCaptureSample.exe）。</span><span class="sxs-lookup"><span data-stu-id="383d0-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="383d0-138">若要執行它，請選取 [ **開始調試** ] 或 [ **啟動但不進行調試** ] **，或** `DuckingCaptureSample` 在命令視窗中輸入。</span><span class="sxs-lookup"><span data-stu-id="383d0-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="383d0-139">DuckingCaptureSample 會為使用者提供兩個從預設主控台裝置（WASAPI 和 Wave Api）捕獲音訊的實施。</span><span class="sxs-lookup"><span data-stu-id="383d0-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="383d0-140">若要啟動捕獲會話，請選取模式，然後按一下應用程式使用者介面上的 [ **啟動** ]。</span><span class="sxs-lookup"><span data-stu-id="383d0-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="383d0-141">若要結束會話，請按一下 [ **停止**]。</span><span class="sxs-lookup"><span data-stu-id="383d0-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="383d0-142">根據使用者指定 (輸入或輸出) 的裝置，應用程式會使用 MMDevice API 來取得預設轉譯或捕捉通訊裝置的參考。</span><span class="sxs-lookup"><span data-stu-id="383d0-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="383d0-143">當使用者啟動聊天會話之後，應用程式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="383d0-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="383d0-144">在事件驅動模式中建立並初始化音訊用戶端。</span><span class="sxs-lookup"><span data-stu-id="383d0-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="383d0-145">將用戶端與事件處理常式產生關聯，該控制碼表示範例已準備好進行捕捉或轉譯。</span><span class="sxs-lookup"><span data-stu-id="383d0-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="383d0-146">設定傳輸的捕獲用戶端和轉譯用戶端。</span><span class="sxs-lookup"><span data-stu-id="383d0-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="383d0-147">建立聊天線程，並啟動音訊引擎。</span><span class="sxs-lookup"><span data-stu-id="383d0-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="383d0-148">為了捕獲音訊資料，在每次處理階段中，此範例會使用 capture 用戶端來取得緩衝區中可用的已捕獲資料量、從預設輸入裝置讀取資料，以及釋出封包，並讓緩衝區可用來讀取下一組已捕獲的資料。</span><span class="sxs-lookup"><span data-stu-id="383d0-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="383d0-149">針對轉譯，應用程式會決定已排入佇列以在 capture 端點緩衝區中播放的資料量。</span><span class="sxs-lookup"><span data-stu-id="383d0-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="383d0-150">它會視情況寫入緩衝區，並釋出緩衝區，以準備下一次處理行程，直到所有資料都已寫入為止。</span><span class="sxs-lookup"><span data-stu-id="383d0-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="383d0-151">若是轉譯，則會 prerolled 無訊息框架，以防止音訊引擎在啟動時瑕疵。</span><span class="sxs-lookup"><span data-stu-id="383d0-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="383d0-152">DuckingCaptureSample 也會顯示如何從磁片區混音器隱藏轉譯資料流程。</span><span class="sxs-lookup"><span data-stu-id="383d0-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="383d0-153">如需資料流程衰減功能的詳細資訊，請參閱 [使用通訊裝置](using-the-communication-device.md)。</span><span class="sxs-lookup"><span data-stu-id="383d0-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="383d0-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="383d0-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="383d0-155">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="383d0-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
