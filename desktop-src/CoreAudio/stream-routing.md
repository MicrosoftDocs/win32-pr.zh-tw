---
description: 串流路由是媒體應用程式在裝置之間切換串流的能力，而不會中斷播放或捕捉會話。
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: 串流路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468317"
---
# <a name="stream-routing"></a><span data-ttu-id="4a5d6-103">串流路由</span><span class="sxs-lookup"><span data-stu-id="4a5d6-103">Stream Routing</span></span>

<span data-ttu-id="4a5d6-104">*串流路由* 是媒體應用程式在裝置之間切換串流的能力，而不會中斷播放或捕捉會話。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="4a5d6-105">電腦可以有多個轉譯和捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="4a5d6-106">系統會 **在 [音效** ] 控制台上列出這些裝置。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="4a5d6-107">從這份清單中，使用者可以將裝置設定為每個角色的預設裝置：播放、錄製或四個通訊角色 (主控台轉譯、主控台抓取、通訊轉譯或通訊捕捉) 。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="4a5d6-108">裝置清單可以動態修改，因為有些裝置可以暫時使用，例如 USB 耳機。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="4a5d6-109">當有多個裝置可用時，使用者可以將預設值變更為不同的裝置。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="4a5d6-110">使用者也可以變更裝置的格式 (取樣率、每個樣本的位數，以及在裝置屬性的 [ **Advanced** ] 索引標籤上) 。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="4a5d6-111">試想一個案例，讓使用者選取 **喇叭** 作為轉譯音訊串流的預設裝置。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="4a5d6-112">使用者接著連接 USB 耳機、選取耳機作為新的預設裝置，並將裝置的取樣率從 44.1 kHz 變更為 48 kHz。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="4a5d6-113">使用者想要以新的取樣率在耳機播放音訊串流，最短的串流會話中斷。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="4a5d6-114">在此案例中，媒體應用程式必須處理的案例有兩種：</span><span class="sxs-lookup"><span data-stu-id="4a5d6-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="4a5d6-115">串流必須傳送至新的預設裝置，並在最短的播放中中斷。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="4a5d6-116">新的裝置必須以新的格式繼續播放 (也就是，使用者可以) 的取樣率變更。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="4a5d6-117">在 Windows Vista 中，為了支援此案例，媒體應用程式必須提供資料流程路由的執行。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="4a5d6-118">應用程式負責終止現有的資料流程，並在新的裝置上重新開機串流。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="4a5d6-119">如果使用者變更預設裝置或其混合格式變更，則會關閉所有相關聯的會話，而且應用程式必須處理復原。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="4a5d6-120">在 Windows 7 中，應用程式可以順暢地將現有預設裝置的串流傳送到新的預設音訊端點。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="4a5d6-121">高階音訊 API 集（例如媒體基礎、DirectSound 和 WAVE Api）會執行串流路由功能。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="4a5d6-122">使用這些 API 集合來播放或從預設裝置捕獲串流的媒體應用程式會使用預設的執行，而不需要修改應用程式。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="4a5d6-123">但是，如果您的媒體應用程式直接使用 MMDeviceAPI 或 WASAPI，應用程式就必須提供資料流程路由執行。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="4a5d6-124">MMDeviceAPI 和 WASAPI 是核心音訊 API 元件，可供應用程式用來在裝置上轉譯或捕獲串流。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="4a5d6-125">MMDeviceAPI 會探索新的音訊端點裝置，而 WASAPI 會管理媒體應用程式和音訊端點裝置之間的音訊資料流程程。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="4a5d6-126">若要執行串流路由功能，應用程式必須在下列情況下接聽 MMDeviceAPI 和 WASAPI 所傳送的通知：</span><span class="sxs-lookup"><span data-stu-id="4a5d6-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="4a5d6-127">使用者會變更預設裝置。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="4a5d6-128">移除現有的預設裝置，並新增預設裝置。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="4a5d6-129">裝置格式已變更。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-129">The device format is changed.</span></span>

<span data-ttu-id="4a5d6-130">藉由處理這些通知，應用程式可以在傳送串流至新的預設裝置時執行必要的串流管理作業。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="4a5d6-131">此外，應用程式可以在轉譯會話為作用中時，使用使用者所指定的新格式來轉譯或捕捉現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="4a5d6-132">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="4a5d6-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="4a5d6-133">取得串流路由的裝置端點</span><span class="sxs-lookup"><span data-stu-id="4a5d6-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="4a5d6-134">串流路由的相關通知</span><span class="sxs-lookup"><span data-stu-id="4a5d6-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="4a5d6-135">串流路由的執行考慮</span><span class="sxs-lookup"><span data-stu-id="4a5d6-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="4a5d6-136">Windows SDK 中包含的下列範例會示範應用程式如何處理串流路由通知。</span><span class="sxs-lookup"><span data-stu-id="4a5d6-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="4a5d6-137">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="4a5d6-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="4a5d6-138">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="4a5d6-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="4a5d6-139">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="4a5d6-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="4a5d6-140">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="4a5d6-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="4a5d6-141">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="4a5d6-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="4a5d6-142">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="4a5d6-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="4a5d6-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a5d6-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a5d6-144">串流管理</span><span class="sxs-lookup"><span data-stu-id="4a5d6-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="4a5d6-145">關於 MMDevice API</span><span class="sxs-lookup"><span data-stu-id="4a5d6-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="4a5d6-146">關於 WASAPI</span><span class="sxs-lookup"><span data-stu-id="4a5d6-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



