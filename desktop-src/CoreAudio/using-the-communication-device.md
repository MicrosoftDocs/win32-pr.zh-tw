---
description: 在 Windows 7 中，[Windows 多媒體] 控制台（Mmsys.cpl）會提供新的 [通訊] 索引標籤。
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: 使用通訊裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847377"
---
# <a name="using-a-communication-device"></a><span data-ttu-id="7017a-103">使用通訊裝置</span><span class="sxs-lookup"><span data-stu-id="7017a-103">Using a Communication Device</span></span>

<span data-ttu-id="7017a-104">在 Windows 7 中，[Windows 多媒體] 控制台（Mmsys.cpl）會提供新的 [ **通訊** ] 索引標籤。此索引標籤包含的選項可讓使用者設定選項，以定義系統管理 *通訊裝置* 的方式。</span><span class="sxs-lookup"><span data-stu-id="7017a-104">In Windows 7, the Windows multimedia control panel, Mmsys.cpl, provides a new **Communications** tab. This tab contains options that enables a user to set options that defines how the system manages a *communication device*.</span></span> <span data-ttu-id="7017a-105">通訊裝置主要用於在電腦上撥打電話或接收電話。</span><span class="sxs-lookup"><span data-stu-id="7017a-105">A communication device is used primarily for placing or receiving telephone calls on the computer.</span></span> <span data-ttu-id="7017a-106">如果電腦只有一個轉譯裝置 (喇叭) 和一個) 裝置 (麥克風，這些音訊裝置也會作為預設通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="7017a-106">For a computer that has only one rendering device (speaker) and one capture device (microphone), these audio devices also act as the default communication devices.</span></span> <span data-ttu-id="7017a-107">當使用者連接新的裝置（例如 USB 耳機）時，系統會藉由查閱 OEM 所填入的設定來執行自動裝置角色偵測。</span><span class="sxs-lookup"><span data-stu-id="7017a-107">When a user connects a new device, such as a USB headset, the system performs automatic device role detection by looking up the configuration settings that are populated by the OEM.</span></span> <span data-ttu-id="7017a-108">如果系統判斷最適合通訊用途的裝置，系統會將 **eCommunications** 角色指派給裝置。</span><span class="sxs-lookup"><span data-stu-id="7017a-108">If the system determines a device to be best suited for communication purposes, the system assigns the **eCommunications** role to the device.</span></span> <span data-ttu-id="7017a-109">針對這些裝置，Windows 7 Mmsys.cpl 提供選項 **預設通訊裝置** ，讓使用者可以選取每個音訊轉譯的通訊裝置， ([ **播放** ] 索引標籤) 以及音訊捕獲 (**錄製** ] 索引標籤) 。</span><span class="sxs-lookup"><span data-stu-id="7017a-109">For these devices, the Windows 7 Mmsys.cpl provides the option **Default Communication Device** that enables a user to select a communication device each for audio rendering (**Playback** tab) and audio capturing (**Recording** tab).</span></span> <span data-ttu-id="7017a-110">系統會執行自動角色偵測，但不會設定要用於通訊的特定裝置。</span><span class="sxs-lookup"><span data-stu-id="7017a-110">The system performs automatic role detection but does not set a particular device to be used for communications.</span></span> <span data-ttu-id="7017a-111">這必須由使用者完成。</span><span class="sxs-lookup"><span data-stu-id="7017a-111">This must be done by the user.</span></span> <span data-ttu-id="7017a-112">新的 **eCommunications** 角色可讓應用程式區分使用者選擇的裝置來處理電話，以及使用裝置作為多媒體裝置， (音樂播放) 。</span><span class="sxs-lookup"><span data-stu-id="7017a-112">The new **eCommunications** role lets an application distinguish between a device that is chosen by the user for handling phone calls and a device to be used as a multimedia device (music playback).</span></span> <span data-ttu-id="7017a-113">例如，如果使用者有連接到電腦的耳機和說話者，系統會將 **eConsole** 角色指派給喇叭，並將 **eCommunications** 角色指派給耳機。</span><span class="sxs-lookup"><span data-stu-id="7017a-113">For example, if the user has a headset and a speaker connected to the computer, the system assigns the **eConsole** role to the speaker and the **eCommunications** role to the headset.</span></span> <span data-ttu-id="7017a-114">當使用者選取用來作為通訊裝置的耳機之後，若要開發通訊應用程式，您可以特別以耳機為目標來呈現音訊串流。</span><span class="sxs-lookup"><span data-stu-id="7017a-114">After the user selects the headset to be used as the communication device, to develop a communication application, you can target the headset specifically for rendering an audio stream.</span></span> <span data-ttu-id="7017a-115">應用程式，使用者無法變更系統指派的裝置角色。</span><span class="sxs-lookup"><span data-stu-id="7017a-115">An application the user cannot change the device role assigned by the system.</span></span> <span data-ttu-id="7017a-116">如需裝置角色的詳細資訊，請參閱 [裝置角色](device-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="7017a-116">For more information about device roles, see [Device Roles](device-roles.md).</span></span>

<span data-ttu-id="7017a-117">通訊應用程式（例如 VoIP 和整合通訊應用程式）會透過電腦撥打電話及接收電話。</span><span class="sxs-lookup"><span data-stu-id="7017a-117">Communication applications, such as VoIP and Unified Communication applications, place and receive phone calls through a computer.</span></span> <span data-ttu-id="7017a-118">例如，VoIP 應用程式可能會將包含環形通知的串流指派給用於轉譯音訊串流的通訊裝置集合端點。</span><span class="sxs-lookup"><span data-stu-id="7017a-118">For example, a VoIP application might assign a stream that contains the ring-in notification to the endpoint of a communication device set for rendering audio streams.</span></span> <span data-ttu-id="7017a-119">此外，應用程式可能會在已設定為通訊裝置的捕獲和轉譯端點裝置上，開啟語音輸入和輸出串流。</span><span class="sxs-lookup"><span data-stu-id="7017a-119">In addition, the application might open the voice input and output streams on the capture and rendering endpoint devices that are set as communication devices.</span></span>

<span data-ttu-id="7017a-120">若要將通訊功能整合到您的應用程式，您可以使用：</span><span class="sxs-lookup"><span data-stu-id="7017a-120">To integrate communication capabilities into your applications, you can use:</span></span>

-   <span data-ttu-id="7017a-121">[MMDEVICE API](mmdevice-api.md)-取得通訊裝置端點的參考。</span><span class="sxs-lookup"><span data-stu-id="7017a-121">[MMDevice API](mmdevice-api.md)—to get a reference to the endpoint of the communication device.</span></span>
-   <span data-ttu-id="7017a-122">[WASAPI](wasapi.md)-透過通訊裝置轉譯和捕獲音訊串流。</span><span class="sxs-lookup"><span data-stu-id="7017a-122">[WASAPI](wasapi.md)—to render and capture audio streams through the communication device.</span></span> <span data-ttu-id="7017a-123">作業系統會將通訊裝置上開啟的串流視為 *通訊串流*。</span><span class="sxs-lookup"><span data-stu-id="7017a-123">The operating system considers the stream opened on a communication device to be a *communication stream*.</span></span>

<span data-ttu-id="7017a-124">通訊應用程式會列舉裝置，並為通訊串流提供資料流程管理 (轉譯或捕捉) 串流的方式，與使用核心音訊 Api 來管理非通訊串流的方式相同。</span><span class="sxs-lookup"><span data-stu-id="7017a-124">The communication application enumerates devices and provides stream management for a communication stream (rendering or capture) stream in the same manner as it would manage a non-communication stream by using the Core Audio APIs.</span></span>

<span data-ttu-id="7017a-125">您可以在通訊應用程式中整合的其中一項功能是 *回避* 或 *串流衰減*。</span><span class="sxs-lookup"><span data-stu-id="7017a-125">One of the features that you can integrate in your communication application is *ducking* or *stream attenuation*.</span></span> <span data-ttu-id="7017a-126">此行為定義在開啟通訊串流時，其他音效必須發生什麼事，例如在通訊裝置上收到電話時。</span><span class="sxs-lookup"><span data-stu-id="7017a-126">This behavior defines what must happen to other sounds when a communication stream is opened, such as when a phone call is received on the communication device.</span></span> <span data-ttu-id="7017a-127">視使用者的選擇而定，系統可能會將非通訊資料流程的音訊音量靜音或降低。</span><span class="sxs-lookup"><span data-stu-id="7017a-127">The system might mute or lower the audio volume of the non-communication stream depending on the user's choice.</span></span> <span data-ttu-id="7017a-128">當開啟或關閉用於轉譯或捕獲資料流程的通訊資料流程時，音訊系統會產生回避事件。</span><span class="sxs-lookup"><span data-stu-id="7017a-128">The audio system generates ducking events when a communication stream is opened or closed for rendering or capturing streams.</span></span> <span data-ttu-id="7017a-129">根據預設，作業系統會提供預設的回避體驗。</span><span class="sxs-lookup"><span data-stu-id="7017a-129">By default, the operating system provides a default ducking experience.</span></span> <span data-ttu-id="7017a-130">媒體應用程式可以取代預設行為，並處理這些事件本身，以提供自訂的回避體驗。</span><span class="sxs-lookup"><span data-stu-id="7017a-130">A media application can replace the default behavior and handle these events itself to provide a customized ducking experience.</span></span>

<span data-ttu-id="7017a-131">下列各節說明如何使用核心音訊 Api 來提供自訂回避體驗。</span><span class="sxs-lookup"><span data-stu-id="7017a-131">The following sections describe how to use Core Audio APIs to provide a custom ducking experience.</span></span>

-   [<span data-ttu-id="7017a-132">預設回避體驗</span><span class="sxs-lookup"><span data-stu-id="7017a-132">Default Ducking Experience</span></span>](stream-attenuation.md)
-   [<span data-ttu-id="7017a-133">停用預設的回避體驗</span><span class="sxs-lookup"><span data-stu-id="7017a-133">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
-   [<span data-ttu-id="7017a-134">提供自訂回避行為</span><span class="sxs-lookup"><span data-stu-id="7017a-134">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
-   [<span data-ttu-id="7017a-135">回避通知的執行考慮</span><span class="sxs-lookup"><span data-stu-id="7017a-135">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
-   [<span data-ttu-id="7017a-136">取得回避事件</span><span class="sxs-lookup"><span data-stu-id="7017a-136">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a><span data-ttu-id="7017a-137">取得通訊裝置端點的參考</span><span class="sxs-lookup"><span data-stu-id="7017a-137">Getting a Reference to the Communication Device Endpoint</span></span>

<span data-ttu-id="7017a-138">若要使用通訊裝置，直接 WASAPI 用戶端必須使用裝置枚舉器來列舉裝置。</span><span class="sxs-lookup"><span data-stu-id="7017a-138">To use the communication device, a direct WASAPI client must enumerate the devices by using the device enumerator.</span></span> <span data-ttu-id="7017a-139">藉由呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)，取得預設通訊裝置端點的參考。</span><span class="sxs-lookup"><span data-stu-id="7017a-139">Get a reference to the endpoint of the default communication device by calling [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="7017a-140">在此呼叫中，應用程式必須在 *Role* 參數中指定 **eCommunications** ，以將裝置列舉限制為通訊裝置。</span><span class="sxs-lookup"><span data-stu-id="7017a-140">In this call, the application must specify **eCommunications** in the *Role* parameter to restrict the device enumeration to communication devices.</span></span> <span data-ttu-id="7017a-141">取得裝置的裝置端點參考之後，您可以藉由呼叫 [**IMMDevice：： activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)來啟動端點範圍的服務。</span><span class="sxs-lookup"><span data-stu-id="7017a-141">After you get a reference to the device endpoint for the device, you can activate the services that are scoped for the endpoint by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="7017a-142">例如，您可以傳遞 **iid \_ IAudioClient** 服務識別碼來啟用音訊用戶端物件，並使用它進行串流管理、使用 **iid \_ IAudioEndpointVolume** 識別碼來存取通訊裝置端點的磁片區控制項，或使用 **iid \_ IAudioSessionManager** 識別碼來啟用會話管理員，讓您能夠與端點的原則引擎進行互動。</span><span class="sxs-lookup"><span data-stu-id="7017a-142">For example, you can pass the **IID\_IAudioClient** service identifier to activate an audio client object and use it for stream management, the **IID\_IAudioEndpointVolume** identifier to get access to the volume controls of the communication device endpoint, or the **IID\_IAudioSessionManager** identifier to activate the session manager that enables you to interact with the policy engine of the endpoint.</span></span> <span data-ttu-id="7017a-143">如需資料流程作業的詳細資訊，請參閱 [資料流程管理](stream-management.md)。</span><span class="sxs-lookup"><span data-stu-id="7017a-143">For information about stream operations, see [Stream Management](stream-management.md).</span></span>

<span data-ttu-id="7017a-144">您也可以使用 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 參考，存取裝置端點的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="7017a-144">By using the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) reference, you can also access the property store for the device endpoint.</span></span> <span data-ttu-id="7017a-145">這些屬性值（例如裝置易記名稱和製造商名稱）會由 OEM 填入，並可讓應用程式判斷通訊裝置的特性。</span><span class="sxs-lookup"><span data-stu-id="7017a-145">These property values, such as device friendly name and manufacturer name, are populated by the OEM and enable an application to determine the characteristics of a communication device.</span></span> <span data-ttu-id="7017a-146">如需詳細資訊，請參閱 [裝置屬性](device-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="7017a-146">For more information, see [Device Properties](device-properties.md).</span></span>

<span data-ttu-id="7017a-147">下列範例程式碼會取得預設通訊裝置端點的參考，以呈現音訊串流。</span><span class="sxs-lookup"><span data-stu-id="7017a-147">The following example code gets a reference to the endpoint of the default communication device for rendering an audio stream.</span></span>


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a><span data-ttu-id="7017a-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="7017a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7017a-149">串流管理</span><span class="sxs-lookup"><span data-stu-id="7017a-149">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



