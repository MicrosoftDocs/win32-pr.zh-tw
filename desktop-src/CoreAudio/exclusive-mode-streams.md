---
description: Exclusive-Mode 資料流程
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Exclusive-Mode 資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677efa83d099bd32ddb0674414e25a9af219bd1a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068584"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="e6205-103">Exclusive-Mode 資料流程</span><span class="sxs-lookup"><span data-stu-id="e6205-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="e6205-104">如先前所述，如果應用程式在獨佔模式中開啟資料流程，應用程式就會獨佔使用播放或記錄串流的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="e6205-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="e6205-105">相反地，有數個應用程式可以在裝置上開啟共用模式串流，藉以共用音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="e6205-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="e6205-106">音訊裝置的獨佔模式存取可以封鎖重要的系統音效、防止與其他應用程式的互通性，也會降低使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="e6205-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="e6205-107">若要減輕這些問題，使用獨佔模式資料流程的應用程式通常會在應用程式不是前景進程或未主動串流時，會讓出音訊裝置的控制權。</span><span class="sxs-lookup"><span data-stu-id="e6205-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="e6205-108">資料流程延遲是資料路徑固有的延遲，可將應用程式的端點緩衝區與音訊端點裝置連接在一起。</span><span class="sxs-lookup"><span data-stu-id="e6205-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="e6205-109">若為轉譯資料流程，延遲是指應用程式將範例寫入端點緩衝區至範例透過喇叭聽到的時間所造成的最大延遲。</span><span class="sxs-lookup"><span data-stu-id="e6205-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="e6205-110">針對 capture 資料流程，延遲是從音效進入麥克風到應用程式可以從端點緩衝區讀取該音效之樣本的時間最大延遲。</span><span class="sxs-lookup"><span data-stu-id="e6205-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="e6205-111">使用獨佔模式資料流程的應用程式通常會這麼做，因為它們需要在音訊端點裝置與存取端點緩衝區的應用程式執行緒之間的資料路徑中有低延遲的情況。</span><span class="sxs-lookup"><span data-stu-id="e6205-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="e6205-112">一般而言，這些執行緒會以相對較高的優先順序執行，並將其本身排程為定期間隔執行，其接近或與定期間隔分開，以將連續處理傳遞給音訊硬體。</span><span class="sxs-lookup"><span data-stu-id="e6205-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="e6205-113">在每次通過時，音訊硬體都會處理端點緩衝區中的新資料。</span><span class="sxs-lookup"><span data-stu-id="e6205-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="e6205-114">若要達到最小的串流延遲，應用程式可能需要兩個特殊的音訊硬體，以及一個輕微載入的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="e6205-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="e6205-115">驅動音訊硬體超過其時間限制，或使用競爭的高優先順序工作載入系統，可能會導致低延遲音訊串流發生問題。</span><span class="sxs-lookup"><span data-stu-id="e6205-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="e6205-116">例如，針對轉譯資料流程，如果應用程式無法在音訊硬體讀取緩衝區之前寫入至端點緩衝區，或如果硬體無法在緩衝區預定播放的時間之前讀取緩衝區，就會發生問題。</span><span class="sxs-lookup"><span data-stu-id="e6205-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="e6205-117">一般來說，要在各種不同的音訊硬體上執行的應用程式，以及廣泛的系統，都應該放寬其時間需求，以避免所有目標環境發生問題。</span><span class="sxs-lookup"><span data-stu-id="e6205-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="e6205-118">Windows Vista 有數項功能，可支援需要低延遲音訊串流的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6205-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="e6205-119">如 [使用者模式音訊元件](user-mode-audio-components.md)中所述，執行時間關鍵作業的應用程式可以呼叫多媒體類別排程器服務 (MMCSS) 函式來提高執行緒優先順序，而不會將 CPU 資源拒絕到較低優先順序的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6205-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="e6205-120">此外， [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法支援 AUDCLNT \_ STREAMFLAGS \_ >app >eventcallback 旗標，可讓應用程式的緩衝區服務執行緒在新的緩衝區變成可供音訊裝置使用時，排程執行。</span><span class="sxs-lookup"><span data-stu-id="e6205-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="e6205-121">藉由使用這些功能，應用程式執行緒可以降低其執行時間的不確定性，進而降低低延遲音訊串流中發生問題的風險。</span><span class="sxs-lookup"><span data-stu-id="e6205-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="e6205-122">舊版音訊介面卡的驅動程式可能會使用 WaveCyclic 或 WavePci 設備磁碟機介面 (的 DDI) ，而較新的音訊介面卡驅動程式較有可能支援 WaveRT 的 DDI。</span><span class="sxs-lookup"><span data-stu-id="e6205-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="e6205-123">針對獨佔模式應用程式，WaveRT 驅動程式可提供比 WaveCyclic 或 WavePci 驅動程式更好的效能，但 WaveRT 驅動程式需要額外的硬體功能。</span><span class="sxs-lookup"><span data-stu-id="e6205-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="e6205-124">這些功能包括能夠直接與應用程式共用硬體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6205-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="e6205-125">使用直接共用時，不需要系統介入，就能在獨佔模式應用程式和音訊硬體之間傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="e6205-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="e6205-126">相反地，WaveCyclic 和 WavePci 驅動程式適用于較舊且較不支援的音訊介面卡。</span><span class="sxs-lookup"><span data-stu-id="e6205-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="e6205-127">這些介面卡依賴系統軟體來傳輸 (連接到系統 i/o 要求封包的資料區塊，或應用程式緩衝區與硬體緩衝區之間的 Irp) 。</span><span class="sxs-lookup"><span data-stu-id="e6205-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="e6205-128">此外，USB 音訊裝置也依賴系統軟體在應用程式緩衝區和硬體緩衝區之間傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="e6205-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="e6205-129">為了改善連接到依賴系統進行資料傳輸之音訊裝置的獨佔模式應用程式效能，WASAPI 會自動增加系統執行緒的優先順序，以便在應用程式和硬體之間傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="e6205-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="e6205-130">WASAPI 會使用 MMCSS 來提高執行緒優先順序。</span><span class="sxs-lookup"><span data-stu-id="e6205-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="e6205-131">在 Windows Vista 中，如果系統執行緒針對 PCM 格式和裝置期限小於10毫秒的獨佔模式音訊播放串流管理資料傳輸，WASAPI 會將 MMCSS 工作名稱 "Pro Audio" 指派給執行緒。</span><span class="sxs-lookup"><span data-stu-id="e6205-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="e6205-132">如果串流的裝置期間大於或等於10毫秒，WASAPI 會將 MMCSS 工作名稱 "Audio" 指派給執行緒。</span><span class="sxs-lookup"><span data-stu-id="e6205-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="e6205-133">如需有關 WaveCyclic、WavePci 和 WaveRT DDIs 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="e6205-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="e6205-134">如需有關選取適當裝置期間的詳細資訊，請參閱 [**IAudioClient：： GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)。</span><span class="sxs-lookup"><span data-stu-id="e6205-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="e6205-135">如 [會話磁片區控制項](session-volume-controls.md)中所述， [WASAPI](wasapi.md) 會提供 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)、 [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)和 [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) 介面，以控制共用模式音訊串流的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="e6205-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="e6205-136">不過，這些介面中的控制項對獨佔模式資料流程沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="e6205-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="e6205-137">相反地，管理獨佔模式串流的應用程式通常會使用 [ENDPOINTVOLUME API](endpointvolume-api.md)中的 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)介面來控制這些資料流程的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="e6205-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="e6205-138">如需此介面的詳細資訊，請參閱 [端點磁片區控制項](endpoint-volume-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="e6205-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="e6205-139">針對系統中的每個播放裝置和捕獲裝置，使用者可以控制裝置是否可以在獨佔模式中使用。</span><span class="sxs-lookup"><span data-stu-id="e6205-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="e6205-140">如果使用者停用裝置的獨佔模式使用，則裝置可用來播放或只記錄共用模式串流。</span><span class="sxs-lookup"><span data-stu-id="e6205-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="e6205-141">如果使用者啟用裝置的獨佔模式使用，則使用者也可以控制應用程式在獨佔模式中使用裝置的要求，是否會由目前透過裝置播放或記錄共用模式串流的應用程式來執行裝置。</span><span class="sxs-lookup"><span data-stu-id="e6205-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="e6205-142">如果已啟用 [先占]，則如果裝置目前不在使用中，或如果裝置是在共用模式中使用，則應用程式對裝置進行獨佔控制權的要求將會成功，但如果另一個應用程式已經有裝置的獨佔控制權，則要求會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6205-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="e6205-143">如果停用了 [已停用]，則如果裝置目前不在使用中，則應用程式對裝置進行獨佔控制權的要求將會成功，但如果裝置已在共用模式或獨佔模式中使用，則要求會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6205-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="e6205-144">在 Windows Vista 中，音訊端點裝置的預設設定如下：</span><span class="sxs-lookup"><span data-stu-id="e6205-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="e6205-145">裝置可用來播放或記錄獨佔模式的串流。</span><span class="sxs-lookup"><span data-stu-id="e6205-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="e6205-146">使用裝置來播放或記錄獨佔模式串流的要求 shutdown 任何目前透過裝置播放或錄製的共用模式串流。</span><span class="sxs-lookup"><span data-stu-id="e6205-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="e6205-147">**變更播放或錄製裝置的獨佔模式設定**</span><span class="sxs-lookup"><span data-stu-id="e6205-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="e6205-148">以滑鼠右鍵按一下通知區域中位於工作列右邊的喇叭圖示，然後選取 [ **播放裝置** ] 或 [ **錄製裝置**]。</span><span class="sxs-lookup"><span data-stu-id="e6205-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="e6205-149"> (，請從命令提示字元視窗執行 [Windows 多媒體] 控制台 Mmsys.cpl。</span><span class="sxs-lookup"><span data-stu-id="e6205-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="e6205-150">如需詳細資訊，請參閱 [裝置 \_ 狀態 \_ XXX 常數](device-state-xxx-constants.md)中的備註。 ) </span><span class="sxs-lookup"><span data-stu-id="e6205-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="e6205-151">在 [ **音效** ] 視窗出現後，選取 [ **播放** ] 或 [ **錄製**]。</span><span class="sxs-lookup"><span data-stu-id="e6205-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="e6205-152">接下來，選取裝置名稱清單中的專案， **然後按一下 [** 內容]。</span><span class="sxs-lookup"><span data-stu-id="e6205-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="e6205-153">在 [ **屬性** ] 視窗出現後，按一下 [ **Advanced**]。</span><span class="sxs-lookup"><span data-stu-id="e6205-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="e6205-154">若要讓應用程式在獨佔模式中使用裝置，請核取標示為 [ **允許應用程式對此裝置進行獨佔控制**] 的方塊。</span><span class="sxs-lookup"><span data-stu-id="e6205-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="e6205-155">若要停用裝置的獨佔模式使用，請清除該核取方塊。</span><span class="sxs-lookup"><span data-stu-id="e6205-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="e6205-156">如果已啟用裝置的專用模式使用，則您可以指定如果裝置目前現正播放或記錄共用模式串流，則對裝置的獨佔控制要求是否會成功。</span><span class="sxs-lookup"><span data-stu-id="e6205-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="e6205-157">若要讓獨佔模式應用程式優先于共用模式應用程式，請核取標示 **為 [提供獨佔模式應用程式優先順序]** 的方塊。</span><span class="sxs-lookup"><span data-stu-id="e6205-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="e6205-158">若要在共用模式應用程式上拒絕獨佔模式應用程式優先順序，請清除核取方塊。</span><span class="sxs-lookup"><span data-stu-id="e6205-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="e6205-159">下列程式碼範例示範如何在設定為在獨佔模式中使用的音訊轉譯裝置上播放低延遲音訊串流：</span><span class="sxs-lookup"><span data-stu-id="e6205-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;
    DWORD taskIndex = 0;
    
    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="e6205-160">在上述程式碼範例中，PlayExclusiveStream 函式會在應用程式執行緒中執行，該執行緒會在播放轉譯資料流程時服務端點的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6205-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="e6205-161">函數會採用單一參數 pMySource，它是屬於用戶端定義之類別 MyAudioSource 的物件指標。</span><span class="sxs-lookup"><span data-stu-id="e6205-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="e6205-162">此類別具有兩個在程式碼範例中呼叫的成員函式，LoadData 和 SetFormat。</span><span class="sxs-lookup"><span data-stu-id="e6205-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="e6205-163">轉譯 [資料流程](rendering-a-stream.md)中描述的是 MyAudioSource。</span><span class="sxs-lookup"><span data-stu-id="e6205-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="e6205-164">PlayExclusiveStream 函式會呼叫協助程式函式（GetStreamFormat），該函式會與預設轉譯裝置協調以判斷裝置是否支援適合應用程式使用的獨佔模式串流格式。</span><span class="sxs-lookup"><span data-stu-id="e6205-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="e6205-165">GetStreamFormat 函式的程式碼不會出現在程式碼範例中;這是因為其執行的詳細資料完全取決於應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="e6205-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="e6205-166">不過，您可以直接描述 GetStreamFormat 函式的作業，它會呼叫 [**IAudioClient：： IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) 方法一或多次，以判斷裝置是否支援適當的格式。</span><span class="sxs-lookup"><span data-stu-id="e6205-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="e6205-167">應用程式的需求會決定 GetStreamFormat 呈現給 **IsFormatSupported** 方法的格式，以及呈現這些格式的順序。</span><span class="sxs-lookup"><span data-stu-id="e6205-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="e6205-168">如需 **IsFormatSupported** 的詳細資訊，請參閱 [裝置格式](device-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="e6205-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="e6205-169">在 GetStreamFormat 呼叫之後，PlayExclusiveStream 函式會呼叫 [**IAudioClient：： GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) 方法，以取得音訊硬體所支援的最小裝置期限。</span><span class="sxs-lookup"><span data-stu-id="e6205-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="e6205-170">接下來，此函式會呼叫 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法，要求等於最小期間的緩衝區持續時間。</span><span class="sxs-lookup"><span data-stu-id="e6205-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="e6205-171">如果呼叫成功， **Initialize** 方法會配置兩個端點緩衝區，而每個緩衝區都等於最短期間的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e6205-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="e6205-172">之後，當音訊串流開始執行時，應用程式和音訊硬體將會以 "乒乓球" 的方式共用兩個緩衝區，也就是當應用程式寫入某個緩衝區時，硬體會從其他緩衝區讀取。</span><span class="sxs-lookup"><span data-stu-id="e6205-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="e6205-173">在啟動資料流程之前，PlayExclusiveStream 函式會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e6205-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="e6205-174">建立並註冊事件控制碼，當緩衝區變成可供填滿時，它會接收通知。</span><span class="sxs-lookup"><span data-stu-id="e6205-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="e6205-175">使用來自音訊來源的資料填滿第一個緩衝區，以減少當聽到初始音效時，從資料流程開始執行的延遲。</span><span class="sxs-lookup"><span data-stu-id="e6205-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="e6205-176">呼叫 **AvSetMmThreadCharacteristics** 函式，要求 MMCSS 提高 PlayExclusiveStream 執行所線上程的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e6205-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="e6205-177"> (當資料流程停止執行時， **AvRevertMmThreadCharacteristics** 函式呼叫會還原原始的執行緒優先順序。 ) </span><span class="sxs-lookup"><span data-stu-id="e6205-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="e6205-178">如需 **AvSetMmThreadCharacteristics** 和 **AvRevertMmThreadCharacteristics** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="e6205-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="e6205-179">當資料流程正在執行時，上述程式碼範例中 **while** 迴圈的每個反復專案都會填滿一個端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6205-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="e6205-180">在反復專案之間， **WaitForSingleObject** 函式呼叫會等待事件控制碼收到信號。</span><span class="sxs-lookup"><span data-stu-id="e6205-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="e6205-181">當控制碼收到信號時，迴圈主體會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="e6205-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="e6205-182">呼叫 [**IAudioRenderClient：： GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) 方法以取得下一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6205-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="e6205-183">填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6205-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="e6205-184">呼叫 [**IAudioRenderClient：： ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) 方法以釋放緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6205-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="e6205-185">如需 **WaitForSingleObject** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="e6205-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="e6205-186">如果音訊介面卡是由 WaveRT 驅動程式所控制，則事件處理常式的信號會系結至來自音訊硬體的 DMA-傳輸通知。</span><span class="sxs-lookup"><span data-stu-id="e6205-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="e6205-187">若是 USB 音訊裝置，或由 WaveCyclic 或 WavePci 驅動程式控制的音訊裝置，事件控制碼的信號會系結至將資料從應用程式緩衝區傳輸到硬體緩衝區的 Irp 完成。</span><span class="sxs-lookup"><span data-stu-id="e6205-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="e6205-188">上述程式碼範例會將音訊硬體和電腦系統推送至其效能限制。</span><span class="sxs-lookup"><span data-stu-id="e6205-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="e6205-189">首先，為了減少資料流程延遲，應用程式會排程緩衝區服務執行緒，以使用音訊硬體將支援的最短裝置期限。</span><span class="sxs-lookup"><span data-stu-id="e6205-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="e6205-190">其次，為了確保執行緒可靠地在每個裝置期間內執行， **AvSetMmThreadCharacteristics** 函式呼叫會將 TaskName 參數設定為 "Pro Audio"，也就是在 Windows Vista 中，預設工作名稱的優先順序最高。</span><span class="sxs-lookup"><span data-stu-id="e6205-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="e6205-191">請考慮應用程式的時間需求是否可能會被放寬，而不會危及其實用性。</span><span class="sxs-lookup"><span data-stu-id="e6205-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="e6205-192">例如，應用程式可能會將其緩衝區服務執行緒排程為使用長度超過最小值的期間。</span><span class="sxs-lookup"><span data-stu-id="e6205-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="e6205-193">較長的期間可能會安全地允許使用較低的執行緒優先順序。</span><span class="sxs-lookup"><span data-stu-id="e6205-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6205-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6205-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6205-195">串流管理</span><span class="sxs-lookup"><span data-stu-id="e6205-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



