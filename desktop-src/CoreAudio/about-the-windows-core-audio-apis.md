---
description: 關於 Windows Core 音訊 Api
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: 關於 Windows Core 音訊 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847579"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="e43e9-103">關於 Windows Core 音訊 Api</span><span class="sxs-lookup"><span data-stu-id="e43e9-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="e43e9-104">本檔提供 Microsoft Windows 系列作業系統的核心音訊 Api 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e43e9-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="e43e9-105">核心音訊 Api 是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="e43e9-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="e43e9-106">這是一組新的使用者模式音訊元件，可為用戶端應用程式提供改良的音訊功能。</span><span class="sxs-lookup"><span data-stu-id="e43e9-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="e43e9-107">這些功能包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="e43e9-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="e43e9-108">低延遲、無問題的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e43e9-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="e43e9-109">改良的可靠性 (許多音訊函式已從核心模式移至使用者模式) 。</span><span class="sxs-lookup"><span data-stu-id="e43e9-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="e43e9-110">增強的安全性 (處理受保護的音訊內容，會在安全、低許可權的程式) 中進行。</span><span class="sxs-lookup"><span data-stu-id="e43e9-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="e43e9-111">將特定全系統角色指派給個別音訊裝置 (主控台、多媒體和通訊) 。</span><span class="sxs-lookup"><span data-stu-id="e43e9-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="e43e9-112">音訊端點裝置的軟體抽象 (例如，喇叭、耳機和麥克風) 使用者直接操作。</span><span class="sxs-lookup"><span data-stu-id="e43e9-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="e43e9-113">在 Windows 7 中已改善核心音訊 Api。</span><span class="sxs-lookup"><span data-stu-id="e43e9-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="e43e9-114">如需有關新增之增強功能和新功能的詳細資訊，請參閱 [Windows 7 中適用于 Core Audio api 的新](what-s-new-for-core-audio-apis-in-windows-7.md)功能。</span><span class="sxs-lookup"><span data-stu-id="e43e9-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="e43e9-115">本檔說明核心音訊 Api。</span><span class="sxs-lookup"><span data-stu-id="e43e9-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="e43e9-116">這些 Api 可作為下列較高層級 Api 的基礎：</span><span class="sxs-lookup"><span data-stu-id="e43e9-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="e43e9-117">DirectSound</span><span class="sxs-lookup"><span data-stu-id="e43e9-117">DirectSound</span></span>
-   <span data-ttu-id="e43e9-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="e43e9-118">DirectMusic</span></span>
-   <span data-ttu-id="e43e9-119">Windows 多媒體 **waveXxx** 和 **mixerXxx** 功能</span><span class="sxs-lookup"><span data-stu-id="e43e9-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="e43e9-120">媒體基礎</span><span class="sxs-lookup"><span data-stu-id="e43e9-120">Media Foundation</span></span>

<span data-ttu-id="e43e9-121">這些較高層級的 Api 使用核心音訊 Api 來共用音訊裝置的存取權。</span><span class="sxs-lookup"><span data-stu-id="e43e9-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="e43e9-122">媒體基礎是 Windows Vista 的新功能，而 windows 98、Windows Millennium Edition 及 Windows 2000 和更新版本支援 DirectSound、DirectMusic 和 **waveXxx** 和 **mixerXxx** 功能。</span><span class="sxs-lookup"><span data-stu-id="e43e9-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="e43e9-123">大部分的音訊應用程式都會與較高層級的 Api 通訊，而不是直接與核心音訊 Api 通訊。</span><span class="sxs-lookup"><span data-stu-id="e43e9-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="e43e9-124">使用較高層級 Api 的一些應用程式範例如下：</span><span class="sxs-lookup"><span data-stu-id="e43e9-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="e43e9-125">媒體播放機</span><span class="sxs-lookup"><span data-stu-id="e43e9-125">Media players</span></span>
-   <span data-ttu-id="e43e9-126">DVD 播放機</span><span class="sxs-lookup"><span data-stu-id="e43e9-126">DVD players</span></span>
-   <span data-ttu-id="e43e9-127">遊戲</span><span class="sxs-lookup"><span data-stu-id="e43e9-127">Games</span></span>
-   <span data-ttu-id="e43e9-128">播放音效檔的商務應用程式，例如 Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="e43e9-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="e43e9-129">這些應用程式通常會與 DirectSound 或媒體基礎 Api 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e43e9-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="e43e9-130">與核心音訊 Api 的直接通訊可能不適合許多一般用途的音訊應用程式。</span><span class="sxs-lookup"><span data-stu-id="e43e9-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="e43e9-131">例如，核心音訊 Api 需要音訊串流才能使用音訊裝置的原生資料格式。</span><span class="sxs-lookup"><span data-stu-id="e43e9-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="e43e9-132">不過，開發下列產品類型的協力廠商軟體發展人員可能需要核心音訊 Api 的特殊功能：</span><span class="sxs-lookup"><span data-stu-id="e43e9-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="e43e9-133">專業音訊 ( 「pro 音訊」 ) 應用程式</span><span class="sxs-lookup"><span data-stu-id="e43e9-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="e43e9-134"> (RTC) 應用程式的即時通訊</span><span class="sxs-lookup"><span data-stu-id="e43e9-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="e43e9-135">協力廠商音訊 Api</span><span class="sxs-lookup"><span data-stu-id="e43e9-135">Third-party audio APIs</span></span>

<span data-ttu-id="e43e9-136">「Pro 音訊」或 RTC 應用程式可能需要直接存取核心音訊 Api 的低層級功能，藉由取得音訊硬體的獨佔存取權來達到最低延遲。</span><span class="sxs-lookup"><span data-stu-id="e43e9-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="e43e9-137">協力廠商音訊 API 可能需要直接存取核心音訊 Api，才能執行一組功能，這些功能可能不會由 Windows 提供的任何單一高階音訊 API 完全支援。</span><span class="sxs-lookup"><span data-stu-id="e43e9-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="e43e9-138">使用舊版音訊 API 來播放或錄製音訊的應用程式可能需要舊版音訊 API 不支援的其他功能，但核心音訊 api 支援此功能。</span><span class="sxs-lookup"><span data-stu-id="e43e9-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="e43e9-139">在許多情況下，應用程式可以直接透過核心音訊 Api 來存取這些功能，而這些 Api 可與舊版音訊 API 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e43e9-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="e43e9-140">核心音訊 Api 如下：</span><span class="sxs-lookup"><span data-stu-id="e43e9-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="e43e9-141">[多媒體裝置 (MMDevice) API](mmdevice-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e43e9-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="e43e9-142">用戶端會使用此 API 來列舉系統中的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="e43e9-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="e43e9-143">[Windows 音訊會話 API (WASAPI) ](wasapi.md)。</span><span class="sxs-lookup"><span data-stu-id="e43e9-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="e43e9-144">用戶端會使用此 API 來建立和管理音訊端點裝置的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e43e9-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="e43e9-145">[DEVICETOPOLOGY API](devicetopology-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e43e9-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="e43e9-146">用戶端會使用此 API 來直接存取拓撲功能 (例如，磁片區控制項，以及位於音訊介面卡內硬體裝置內資料路徑的 multiplexers) 。</span><span class="sxs-lookup"><span data-stu-id="e43e9-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="e43e9-147">[ENDPOINTVOLUME API](endpointvolume-api.md)。</span><span class="sxs-lookup"><span data-stu-id="e43e9-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="e43e9-148">用戶端會使用此 API 直接存取音訊端點裝置上的磁片區控制項。</span><span class="sxs-lookup"><span data-stu-id="e43e9-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="e43e9-149">此 API 主要是由管理專用模式音訊串流的應用程式所使用。</span><span class="sxs-lookup"><span data-stu-id="e43e9-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="e43e9-150">這些 Api 支援使用者易記的端點裝置概念，如 [音訊端點裝置](audio-endpoint-devices.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e43e9-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="e43e9-151">Microsoft 不打算將此處所述的核心音訊 Api 提供給舊版 Windows 使用，包括 Microsoft Windows Server 2003、Windows XP、Windows Millennium Edition、Windows 2000 及 Windows 98。</span><span class="sxs-lookup"><span data-stu-id="e43e9-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="e43e9-152">本總覽包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="e43e9-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="e43e9-153">**主題**</span><span class="sxs-lookup"><span data-stu-id="e43e9-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="e43e9-154">**說明**</span><span class="sxs-lookup"><span data-stu-id="e43e9-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e43e9-155">Windows 7 中 Core Audio Api 的新功能</span><span class="sxs-lookup"><span data-stu-id="e43e9-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="e43e9-156">摘要說明核心音訊 Api 的新功能和增強功能</span><span class="sxs-lookup"><span data-stu-id="e43e9-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="e43e9-157">標頭檔和系統元件</span><span class="sxs-lookup"><span data-stu-id="e43e9-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="e43e9-158">描述核心音訊 Api 的標頭檔和系統元件。</span><span class="sxs-lookup"><span data-stu-id="e43e9-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="e43e9-159">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="e43e9-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="e43e9-160">列出 Windows SDK 中使用核心音訊 Api 的範例。</span><span class="sxs-lookup"><span data-stu-id="e43e9-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="e43e9-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="e43e9-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e43e9-162">核心音訊 Api</span><span class="sxs-lookup"><span data-stu-id="e43e9-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



