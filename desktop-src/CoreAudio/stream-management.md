---
description: 串流管理
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: 串流管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110933"
---
# <a name="stream-management"></a><span data-ttu-id="6450a-103">串流管理</span><span class="sxs-lookup"><span data-stu-id="6450a-103">Stream Management</span></span>

<span data-ttu-id="6450a-104">列舉系統中的 [音訊端點裝置](audio-endpoint-devices.md) ，並識別適合的轉譯或捕獲裝置之後，音訊用戶端應用程式的下一項工作就是開啟與端點裝置的連線，並透過該連線管理音訊資料的流程。</span><span class="sxs-lookup"><span data-stu-id="6450a-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="6450a-105">[WASAPI](wasapi.md) 可讓用戶端建立及管理音訊串流。</span><span class="sxs-lookup"><span data-stu-id="6450a-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="6450a-106">WASAPI 會執行數個介面，以提供串流管理服務給音訊用戶端。</span><span class="sxs-lookup"><span data-stu-id="6450a-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="6450a-107">主要介面為 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)。</span><span class="sxs-lookup"><span data-stu-id="6450a-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="6450a-108">用戶端會藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法 (，並將參數 *iid* 設定為端點物件上的 **REFIID** iid IAudioClient) ，藉以取得音訊端點裝置的 **IAudioClient** 介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6450a-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="6450a-109">用戶端會呼叫 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面中的方法來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="6450a-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="6450a-110">探索端點裝置支援的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="6450a-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="6450a-111">取得端點緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="6450a-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="6450a-112">取得資料流程格式和延遲。</span><span class="sxs-lookup"><span data-stu-id="6450a-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="6450a-113">啟動、停止和重設流經端點裝置的串流。</span><span class="sxs-lookup"><span data-stu-id="6450a-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="6450a-114">存取其他音訊服務。</span><span class="sxs-lookup"><span data-stu-id="6450a-114">Access additional audio services.</span></span>

<span data-ttu-id="6450a-115">若要建立資料流程，用戶端會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="6450a-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="6450a-116">透過這個方法，用戶端會指定資料流程的資料格式、端點緩衝區的大小，以及資料流程是否以共用或獨佔模式運作。</span><span class="sxs-lookup"><span data-stu-id="6450a-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="6450a-117">[**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)介面中的其餘方法分為兩個群組：</span><span class="sxs-lookup"><span data-stu-id="6450a-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="6450a-118">只有在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)開啟資料流程之後，才能呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="6450a-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="6450a-119">可以在 [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 呼叫之前或之後的任何時間呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="6450a-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="6450a-120">只有在呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)之後，才能呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="6450a-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="6450a-121">**IAudioClient::GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="6450a-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="6450a-122">**IAudioClient::GetCurrentPadding**</span><span class="sxs-lookup"><span data-stu-id="6450a-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="6450a-123">**IAudioClient：： GetService**</span><span class="sxs-lookup"><span data-stu-id="6450a-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="6450a-124">**IAudioClient::GetStreamLatency**</span><span class="sxs-lookup"><span data-stu-id="6450a-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="6450a-125">**IAudioClient：： Reset**</span><span class="sxs-lookup"><span data-stu-id="6450a-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="6450a-126">**IAudioClient：： Start**</span><span class="sxs-lookup"><span data-stu-id="6450a-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="6450a-127">**IAudioClient：： Stop**</span><span class="sxs-lookup"><span data-stu-id="6450a-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="6450a-128">您可以在 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 呼叫之前或之後呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="6450a-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="6450a-129">**IAudioClient::GetDevicePeriod**</span><span class="sxs-lookup"><span data-stu-id="6450a-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="6450a-130">**IAudioClient::GetMixFormat**</span><span class="sxs-lookup"><span data-stu-id="6450a-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="6450a-131">**IAudioClient::IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="6450a-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="6450a-132">若要存取其他音訊用戶端服務，用戶端會呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法。</span><span class="sxs-lookup"><span data-stu-id="6450a-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="6450a-133">透過這個方法，用戶端可以取得下列介面的參考：</span><span class="sxs-lookup"><span data-stu-id="6450a-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="6450a-134">**IAudioRenderClient**</span><span class="sxs-lookup"><span data-stu-id="6450a-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="6450a-135">將轉譯資料寫入音訊呈現端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6450a-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="6450a-136">**IAudioCaptureClient**</span><span class="sxs-lookup"><span data-stu-id="6450a-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="6450a-137">從音訊捕獲端點緩衝區讀取捕捉到的資料。</span><span class="sxs-lookup"><span data-stu-id="6450a-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="6450a-138">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="6450a-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="6450a-139">與音訊會話管理員通訊，以設定及管理與資料流程相關聯的音訊會話。</span><span class="sxs-lookup"><span data-stu-id="6450a-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="6450a-140">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="6450a-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="6450a-141">控制與資料流程相關聯之音訊會話的音量層級。</span><span class="sxs-lookup"><span data-stu-id="6450a-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="6450a-142">**IChannelAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="6450a-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="6450a-143">控制與資料流程相關聯之音訊會話中個別通道的音量層級。</span><span class="sxs-lookup"><span data-stu-id="6450a-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="6450a-144">**IAudioClock**</span><span class="sxs-lookup"><span data-stu-id="6450a-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="6450a-145">監視資料流程資料速率和資料流程位置。</span><span class="sxs-lookup"><span data-stu-id="6450a-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="6450a-146">此外，需要會話相關事件通知的 WASAPI 用戶端應該會執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="6450a-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="6450a-147">**IAudioSessionEvents**</span><span class="sxs-lookup"><span data-stu-id="6450a-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="6450a-148">若要接收事件通知，用戶端會將其 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) 介面的指標傳遞至 [**IAudioSessionControl：： RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) 方法，作為呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="6450a-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="6450a-149">最後，用戶端可能會使用較高層級的 API 來建立音訊串流，但也需要存取包含該資料流程之會話的會話控制項和磁片區控制項。</span><span class="sxs-lookup"><span data-stu-id="6450a-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="6450a-150">較高層級的 API 通常不會提供此存取權。</span><span class="sxs-lookup"><span data-stu-id="6450a-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="6450a-151">用戶端可以透過 [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) 介面取得特定會話的控制項。</span><span class="sxs-lookup"><span data-stu-id="6450a-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="6450a-152">此介面可讓用戶端取得會話的 [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) 和 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面，而不需要用戶端使用 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面來建立資料流程，以及將串流指派給會話。</span><span class="sxs-lookup"><span data-stu-id="6450a-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="6450a-153">用戶端會藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法 (，並將參數 *iid* 設定為端點物件上的 **REFIID** iid IAudioSessionManager) ，藉以取得音訊端點裝置的 **IAudioSessionManager** 介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6450a-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="6450a-154">[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)、 [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)和 [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager)介面是在標頭檔 Audiopolicy 中定義。</span><span class="sxs-lookup"><span data-stu-id="6450a-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="6450a-155">所有其他 WASAPI 介面都是在標頭檔 Audioclient 中定義。</span><span class="sxs-lookup"><span data-stu-id="6450a-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="6450a-156">下列各節說明如何使用 WASAPI 來管理音訊串流：</span><span class="sxs-lookup"><span data-stu-id="6450a-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="6450a-157">關於 WASAPI</span><span class="sxs-lookup"><span data-stu-id="6450a-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="6450a-158">呈現資料流程</span><span class="sxs-lookup"><span data-stu-id="6450a-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="6450a-159">捕獲資料流程</span><span class="sxs-lookup"><span data-stu-id="6450a-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="6450a-160">回送記錄</span><span class="sxs-lookup"><span data-stu-id="6450a-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="6450a-161">獨佔模式資料流程</span><span class="sxs-lookup"><span data-stu-id="6450a-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="6450a-162">從 Invalid-Device 錯誤中復原</span><span class="sxs-lookup"><span data-stu-id="6450a-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="6450a-163">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="6450a-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="6450a-164">串流路由</span><span class="sxs-lookup"><span data-stu-id="6450a-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="6450a-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="6450a-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6450a-166">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="6450a-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



