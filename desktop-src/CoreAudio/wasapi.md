---
description: 關於 WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: 關於 WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936330"
---
# <a name="about-wasapi"></a><span data-ttu-id="33be0-103">關於 WASAPI</span><span class="sxs-lookup"><span data-stu-id="33be0-103">About WASAPI</span></span>

<span data-ttu-id="33be0-104">Windows 音訊會話 API (WASAPI) 可讓用戶端應用程式管理應用程式和 [音訊端點裝置](audio-endpoint-devices.md)之間的音訊資料流程程。</span><span class="sxs-lookup"><span data-stu-id="33be0-104">The Windows Audio Session API (WASAPI) enables client applications to manage the flow of audio data between the application and an [audio endpoint device](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="33be0-105">標頭檔 Audioclient .h 和 Audiopolicy 定義 WASAPI 介面。</span><span class="sxs-lookup"><span data-stu-id="33be0-105">Header files Audioclient.h and Audiopolicy.h define the WASAPI interfaces.</span></span>

<span data-ttu-id="33be0-106">每個音訊串流都是 [音訊會話](audio-sessions.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="33be0-106">Every audio stream is a member of an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="33be0-107">透過會話抽象，WASAPI 用戶端可以將音訊串流識別為相關音訊串流群組的成員。</span><span class="sxs-lookup"><span data-stu-id="33be0-107">Through the session abstraction, a WASAPI client can identify an audio stream as a member of a group of related audio streams.</span></span> <span data-ttu-id="33be0-108">系統可以將會話中的所有資料流程當作單一單位來管理。</span><span class="sxs-lookup"><span data-stu-id="33be0-108">The system can manage all of the streams in the session as a single unit.</span></span>

<span data-ttu-id="33be0-109">音訊引擎是 [使用者模式的音訊元件](user-mode-audio-components.md) ，應用程式可透過此元件共用音訊端點裝置的存取權。</span><span class="sxs-lookup"><span data-stu-id="33be0-109">The audio engine is the [user-mode audio component](user-mode-audio-components.md) through which applications share access to an audio endpoint device.</span></span> <span data-ttu-id="33be0-110">音訊引擎會在端點緩衝區和端點裝置之間傳輸音訊資料。</span><span class="sxs-lookup"><span data-stu-id="33be0-110">The audio engine transports audio data between an endpoint buffer and an endpoint device.</span></span> <span data-ttu-id="33be0-111">若要透過呈現端點裝置播放音訊串流，應用程式會定期將音訊資料寫入轉譯端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="33be0-111">To play an audio stream through a rendering endpoint device, an application periodically writes audio data to a rendering endpoint buffer.</span></span> <span data-ttu-id="33be0-112">音訊引擎混合不同應用程式的資料流程。</span><span class="sxs-lookup"><span data-stu-id="33be0-112">The audio engine mixes the streams from the various applications.</span></span> <span data-ttu-id="33be0-113">若要從「捕獲端點」裝置錄製音訊串流，應用程式會定期從「捕獲端點」緩衝區讀取音訊資料。</span><span class="sxs-lookup"><span data-stu-id="33be0-113">To record an audio stream from a capture endpoint device, an application periodically reads audio data from a capture endpoint buffer.</span></span>

<span data-ttu-id="33be0-114">WASAPI 包含數個介面。</span><span class="sxs-lookup"><span data-stu-id="33be0-114">WASAPI consists of several interfaces.</span></span> <span data-ttu-id="33be0-115">其中第一個是 [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) 介面。</span><span class="sxs-lookup"><span data-stu-id="33be0-115">The first of these is the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface.</span></span> <span data-ttu-id="33be0-116">若要存取 WASAPI 介面，用戶端會先呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法，並將參數 *Iid* 設定為 **REFIID** iid IAudioClient，以取得音訊端點裝置之 **IAudioClient** 介面的參考 \_ 。</span><span class="sxs-lookup"><span data-stu-id="33be0-116">To access the WASAPI interfaces, a client first obtains a reference to the **IAudioClient** interface of an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to **REFIID** IID\_IAudioClient.</span></span> <span data-ttu-id="33be0-117">用戶端會呼叫 [**IAudioClient：： initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 方法，以初始化端點裝置上的資料流程。</span><span class="sxs-lookup"><span data-stu-id="33be0-117">The client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to initialize a stream on an endpoint device.</span></span> <span data-ttu-id="33be0-118">在初始化資料流程之後，用戶端可以藉由呼叫 [**IAudioClient：： GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) 方法，取得其他 WASAPI 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="33be0-118">After initializing a stream, the client can obtain references to the other WASAPI interfaces by calling the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span>

<span data-ttu-id="33be0-119">\_ \_ \_ 如果用戶端應用程式使用的音訊端點裝置變得無效，WASAPI 中的許多方法會傳回錯誤碼 AUDCLNT E 裝置失效。</span><span class="sxs-lookup"><span data-stu-id="33be0-119">Many of the methods in WASAPI return error code AUDCLNT\_E\_DEVICE\_INVALIDATED if the audio endpoint device that a client application is using becomes invalid.</span></span> <span data-ttu-id="33be0-120">通常，應用程式可以從這個錯誤中復原。</span><span class="sxs-lookup"><span data-stu-id="33be0-120">Frequently, the application can recover from this error.</span></span> <span data-ttu-id="33be0-121">如需詳細資訊，請參閱 [從 Invalid-Device 錯誤中復原](recovering-from-an-invalid-device-error.md)。</span><span class="sxs-lookup"><span data-stu-id="33be0-121">For more information, see [Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md).</span></span>

<span data-ttu-id="33be0-122">WASAPI 會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="33be0-122">WASAPI implements the following interfaces.</span></span>



| <span data-ttu-id="33be0-123">介面</span><span class="sxs-lookup"><span data-stu-id="33be0-123">Interface</span></span>                                            | <span data-ttu-id="33be0-124">描述</span><span class="sxs-lookup"><span data-stu-id="33be0-124">Description</span></span>                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33be0-125">**IAudioCaptureClient**</span><span class="sxs-lookup"><span data-stu-id="33be0-125">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | <span data-ttu-id="33be0-126">可讓用戶端從 capture 端點緩衝區讀取輸入資料。</span><span class="sxs-lookup"><span data-stu-id="33be0-126">Enables a client to read input data from a capture endpoint buffer.</span></span>                                                                                             |
| [<span data-ttu-id="33be0-127">**IAudioClient**</span><span class="sxs-lookup"><span data-stu-id="33be0-127">**IAudioClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | <span data-ttu-id="33be0-128">可讓用戶端在音訊應用程式與音訊引擎或音訊端點裝置的硬體緩衝區之間，建立及初始化音訊串流。</span><span class="sxs-lookup"><span data-stu-id="33be0-128">Enables a client to create and initialize an audio stream between an audio application and the audio engine or the hardware buffer of an audio endpoint device.</span></span> |
| [<span data-ttu-id="33be0-129">**IAudioClock**</span><span class="sxs-lookup"><span data-stu-id="33be0-129">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | <span data-ttu-id="33be0-130">讓用戶端監視資料流程的資料速率，以及資料流程中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="33be0-130">Enables a client to monitor a stream's data rate and the current position in the stream.</span></span>                                                                        |
| [<span data-ttu-id="33be0-131">**IAudioRenderClient**</span><span class="sxs-lookup"><span data-stu-id="33be0-131">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | <span data-ttu-id="33be0-132">讓用戶端將輸出資料寫入轉譯端點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="33be0-132">Enables a client to write output data to a rendering endpoint buffer.</span></span>                                                                                           |
| [<span data-ttu-id="33be0-133">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="33be0-133">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | <span data-ttu-id="33be0-134">可讓用戶端設定音訊會話的控制參數，以及監視會話中的事件。</span><span class="sxs-lookup"><span data-stu-id="33be0-134">Enables a client to configure the control parameters for an audio session and to monitor events in the session.</span></span>                                                 |
| [<span data-ttu-id="33be0-135">**IAudioSessionManager**</span><span class="sxs-lookup"><span data-stu-id="33be0-135">**IAudioSessionManager**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | <span data-ttu-id="33be0-136">讓用戶端能夠存取跨進程和進程專屬音訊會話的會話控制項和磁片區控制項。</span><span class="sxs-lookup"><span data-stu-id="33be0-136">Enables a client to access the session controls and volume controls for both cross-process and process-specific audio sessions.</span></span>                                 |
| [<span data-ttu-id="33be0-137">**IAudioStreamVolume**</span><span class="sxs-lookup"><span data-stu-id="33be0-137">**IAudioStreamVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | <span data-ttu-id="33be0-138">可讓用戶端控制及監視音訊串流中所有通道的音量層級。</span><span class="sxs-lookup"><span data-stu-id="33be0-138">Enables a client to control and monitor the volume levels for all of the channels in an audio stream.</span></span>                                                           |
| [<span data-ttu-id="33be0-139">**IChannelAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="33be0-139">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | <span data-ttu-id="33be0-140">可讓用戶端控制串流所屬音訊會話中所有通道的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="33be0-140">Enables a client to control the volume levels for all of the channels in the audio session that the stream belongs to.</span></span>                                          |
| [<span data-ttu-id="33be0-141">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="33be0-141">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | <span data-ttu-id="33be0-142">可讓用戶端控制音訊會話的主要磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="33be0-142">Enables a client to control the master volume level of an audio session.</span></span>                                                                                        |



 

<span data-ttu-id="33be0-143">需要會話相關事件通知的 WASAPI 用戶端應該執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="33be0-143">WASAPI clients that require notification of session-related events should implement the following interface.</span></span>



| <span data-ttu-id="33be0-144">介面</span><span class="sxs-lookup"><span data-stu-id="33be0-144">Interface</span></span>                                          | <span data-ttu-id="33be0-145">描述</span><span class="sxs-lookup"><span data-stu-id="33be0-145">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33be0-146">**IAudioSessionEvents**</span><span class="sxs-lookup"><span data-stu-id="33be0-146">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | <span data-ttu-id="33be0-147">提供會話相關事件的通知，例如磁片區層級、顯示名稱和會話狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="33be0-147">Provides notifications of session-related events such as changes in the volume level, display name, and session state.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="33be0-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="33be0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33be0-149">串流管理</span><span class="sxs-lookup"><span data-stu-id="33be0-149">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="33be0-150">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="33be0-150">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



