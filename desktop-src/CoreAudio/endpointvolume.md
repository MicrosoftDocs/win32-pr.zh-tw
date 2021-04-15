---
description: 這個範例應用程式會使用核心音訊 Api 來變更裝置的音量（由使用者所指定）。
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468332"
---
# <a name="endpointvolume"></a><span data-ttu-id="d8e63-103">EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="d8e63-103">EndpointVolume</span></span>

<span data-ttu-id="d8e63-104">這個範例應用程式會使用核心音訊 Api 來變更裝置的音量（由使用者所指定）。</span><span class="sxs-lookup"><span data-stu-id="d8e63-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="d8e63-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d8e63-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d8e63-106">說明</span><span class="sxs-lookup"><span data-stu-id="d8e63-106">Description</span></span>](#description)
-   [<span data-ttu-id="d8e63-107">需求</span><span class="sxs-lookup"><span data-stu-id="d8e63-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d8e63-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d8e63-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d8e63-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d8e63-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8e63-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d8e63-112">Description</span><span class="sxs-lookup"><span data-stu-id="d8e63-112">Description</span></span>

<span data-ttu-id="d8e63-113">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="d8e63-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="d8e63-114">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="d8e63-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="d8e63-115">[ENDPOINTVOLUME API](endpointvolume-api.md) 來控制裝置端點的音量層級。</span><span class="sxs-lookup"><span data-stu-id="d8e63-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e63-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8e63-116">Requirements</span></span>



| <span data-ttu-id="d8e63-117">產品</span><span class="sxs-lookup"><span data-stu-id="d8e63-117">Product</span></span>                                                        | <span data-ttu-id="d8e63-118">版本</span><span class="sxs-lookup"><span data-stu-id="d8e63-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d8e63-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d8e63-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d8e63-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8e63-120">Windows 7</span></span> |
| <span data-ttu-id="d8e63-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d8e63-121">Visual Studio</span></span>                                                  | <span data-ttu-id="d8e63-122">2008</span><span class="sxs-lookup"><span data-stu-id="d8e63-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d8e63-123">下載範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-123">Downloading the Sample</span></span>

<span data-ttu-id="d8e63-124">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="d8e63-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d8e63-125">Location</span><span class="sxs-lookup"><span data-stu-id="d8e63-125">Location</span></span>    | <span data-ttu-id="d8e63-126">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="d8e63-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e63-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d8e63-127">Windows SDK</span></span> | <span data-ttu-id="d8e63-128">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ EndpointVolume \\ .。。</span><span class="sxs-lookup"><span data-stu-id="d8e63-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="d8e63-129">建立範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-129">Building the Sample</span></span>

<span data-ttu-id="d8e63-130">若要建立 x 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d8e63-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="d8e63-131">若要建立 EndpointVolumeChanger 範例，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d8e63-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="d8e63-132">開啟 Windows SDK 的 CMD shell，並變更為 EndpointVolume 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="d8e63-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="d8e63-133">在 EndpointVolume 目錄中執行命令 `start EndpointVolumeChanger.sln` ，以在 Visual Studio 視窗中開啟 EndpointVolumeChanger 專案。</span><span class="sxs-lookup"><span data-stu-id="d8e63-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="d8e63-134">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="d8e63-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="d8e63-135">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="d8e63-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="d8e63-136">在此情況下，除非您明確設定在專案檔 WASAPIEndpointVolume 中使用的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="d8e63-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d8e63-137">執行範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-137">Running the Sample</span></span>

<span data-ttu-id="d8e63-138">如果您成功建立示範應用程式，則會產生可執行檔（EndpointVolumeChanger.exe）。</span><span class="sxs-lookup"><span data-stu-id="d8e63-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="d8e63-139">若要執行它，請 `EndpointVolumeChanger` 在命令視窗中輸入，後面接著必要或選擇性的引數。</span><span class="sxs-lookup"><span data-stu-id="d8e63-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="d8e63-140">下列範例顯示如何切換預設主控台裝置上的靜音設定。</span><span class="sxs-lookup"><span data-stu-id="d8e63-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="d8e63-141">下表顯示引數。</span><span class="sxs-lookup"><span data-stu-id="d8e63-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="d8e63-142">引數</span><span class="sxs-lookup"><span data-stu-id="d8e63-142">Argument</span></span>        | <span data-ttu-id="d8e63-143">描述</span><span class="sxs-lookup"><span data-stu-id="d8e63-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="d8e63-144">-?</span><span class="sxs-lookup"><span data-stu-id="d8e63-144">-?</span></span>              | <span data-ttu-id="d8e63-145">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="d8e63-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="d8e63-146">-H</span><span class="sxs-lookup"><span data-stu-id="d8e63-146">-h</span></span>              | <span data-ttu-id="d8e63-147">顯示說明。</span><span class="sxs-lookup"><span data-stu-id="d8e63-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="d8e63-148">將音訊端點裝置上的音量層級遞增一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d8e63-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="d8e63-149">.</span><span class="sxs-lookup"><span data-stu-id="d8e63-149">.</span></span> |
| <span data-ttu-id="d8e63-150">-up</span><span class="sxs-lookup"><span data-stu-id="d8e63-150">-up</span></span>             | <span data-ttu-id="d8e63-151">將音訊端點裝置上的音量層級遞增一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d8e63-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="d8e63-152">將音訊端點裝置上的音量層級減少一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d8e63-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="d8e63-153">-down</span><span class="sxs-lookup"><span data-stu-id="d8e63-153">-down</span></span>           | <span data-ttu-id="d8e63-154">將音訊端點裝置上的音量層級減少一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d8e63-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="d8e63-155">-v</span><span class="sxs-lookup"><span data-stu-id="d8e63-155">-v</span></span>              | <span data-ttu-id="d8e63-156">設定音訊端點裝置上的主要磁碟區層級。</span><span class="sxs-lookup"><span data-stu-id="d8e63-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="d8e63-157">-主控台</span><span class="sxs-lookup"><span data-stu-id="d8e63-157">-console</span></span>        | <span data-ttu-id="d8e63-158">使用預設的主控台裝置。</span><span class="sxs-lookup"><span data-stu-id="d8e63-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="d8e63-159">-通訊</span><span class="sxs-lookup"><span data-stu-id="d8e63-159">-communications</span></span> | <span data-ttu-id="d8e63-160">使用預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="d8e63-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="d8e63-161">-多媒體</span><span class="sxs-lookup"><span data-stu-id="d8e63-161">-multimedia</span></span>     | <span data-ttu-id="d8e63-162">使用預設的多媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="d8e63-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="d8e63-163">-端點</span><span class="sxs-lookup"><span data-stu-id="d8e63-163">-endpoint</span></span>       | <span data-ttu-id="d8e63-164">使用參數值中指定的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8e63-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="d8e63-165">如果應用程式執行時沒有引數，它會列舉可用的裝置，並提示使用者選取裝置。</span><span class="sxs-lookup"><span data-stu-id="d8e63-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="d8e63-166">當使用者指定裝置之後，應用程式會顯示端點目前的磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="d8e63-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="d8e63-167">您可以使用上表所述的參數來控制該磁片區。</span><span class="sxs-lookup"><span data-stu-id="d8e63-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="d8e63-168">如需控制音訊端點裝置音量層級的詳細資訊，請參閱 [ENDPOINTVOLUME API](endpointvolume-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d8e63-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8e63-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8e63-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e63-170">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="d8e63-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



