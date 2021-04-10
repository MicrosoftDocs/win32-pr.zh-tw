---
description: EndpointVolume API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: EndpointVolume API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688952"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="4671d-103">EndpointVolume API</span><span class="sxs-lookup"><span data-stu-id="4671d-103">EndpointVolume API</span></span>

<span data-ttu-id="4671d-104">EndpointVolume API 可讓特製化用戶端控制及監視 [音訊端點裝置](audio-endpoint-devices.md)的音量層級。</span><span class="sxs-lookup"><span data-stu-id="4671d-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="4671d-105">用戶端會取得 EndpointVolume API 中的介面參考，方法是取得音訊端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面，然後呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法。</span><span class="sxs-lookup"><span data-stu-id="4671d-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="4671d-106">標頭檔 Endpointvolume 會定義 EndpointVolume API 中的介面。</span><span class="sxs-lookup"><span data-stu-id="4671d-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="4671d-107">使用 [MMDEVICE API](mmdevice-api.md) 和 [WASAPI](wasapi.md) 的音訊應用程式通常會使用 [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) 介面來控制每個會話的音量層級。</span><span class="sxs-lookup"><span data-stu-id="4671d-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="4671d-108">只有兩種類型的音訊應用程式需要使用 EndpointVolume API。</span><span class="sxs-lookup"><span data-stu-id="4671d-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="4671d-109">這些應用程式類型包括：</span><span class="sxs-lookup"><span data-stu-id="4671d-109">These application types are:</span></span>

-   <span data-ttu-id="4671d-110">管理音訊端點裝置之主要磁片區層級的應用程式，類似于 Windows 大量控制程式，Sndvol.exe。</span><span class="sxs-lookup"><span data-stu-id="4671d-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="4671d-111">專業音訊 ( 「pro 音訊」 ) 需要以獨佔模式存取音訊端點裝置的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4671d-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="4671d-112">不當使用 EndpointVolume API 可能會干擾 Windows 音訊原則，並中斷使用者的系統磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="4671d-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="4671d-113">如果音訊端點裝置實行硬體磁片區和靜音控制，EndpointVolume API 會使用這些控制項來管理裝置磁片區。</span><span class="sxs-lookup"><span data-stu-id="4671d-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="4671d-114">否則，EndpointVolume API 會以透明的方式在用戶端上執行軟體中的控制項。</span><span class="sxs-lookup"><span data-stu-id="4671d-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="4671d-115">如果裝置具有硬體磁片區和靜音控制，透過 EndpointVolume API 對裝置磁片區和靜音設定所做的變更，會影響共用模式和獨佔模式中的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="4671d-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="4671d-116">如果裝置缺少硬體磁片區和靜音控制，透過 EndpointVolume API 對軟體磁片區和靜音控制所做的變更，會影響在共用模式中的磁片區層級，但不會影響獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="4671d-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="4671d-117">在獨佔模式中，用戶端和裝置會直接交換音訊資料，略過軟體控制項。</span><span class="sxs-lookup"><span data-stu-id="4671d-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="4671d-118">對於必須管理硬體磁片區和靜音控制的應用程式，EndpointVolume API 透過 [DEVICETOPOLOGY api](devicetopology-api.md)提供兩個可能的優點。</span><span class="sxs-lookup"><span data-stu-id="4671d-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="4671d-119">首先，有一些音訊介面卡裝置缺少硬體磁片區控制項。</span><span class="sxs-lookup"><span data-stu-id="4671d-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="4671d-120">如果裝置缺少硬體磁片區控制項，EndpointVolume API 中的 [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) 介面會自動在該裝置的串流上執行軟體磁片區控制。</span><span class="sxs-lookup"><span data-stu-id="4671d-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="4671d-121">針對 EndpointVolume API 的用戶端，不論裝置是否已在硬體中或由 EndpointVolume API 介面在軟體中執行磁片區控制，結果都會相同。</span><span class="sxs-lookup"><span data-stu-id="4671d-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="4671d-122">其次，即使介面卡裝置確實執行硬體磁片區控制項，使用 DeviceTopology API 來執行拓撲遍歷演算法的應用程式可能會找不到所要尋找的控制項。</span><span class="sxs-lookup"><span data-stu-id="4671d-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="4671d-123">一般而言，這類應用程式是設計來跨越特定裝置或一組相關裝置的硬體拓朴。</span><span class="sxs-lookup"><span data-stu-id="4671d-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="4671d-124">如果應用程式嘗試跨越尚未特別設計或測試的裝置拓撲，就會發生失敗的風險。</span><span class="sxs-lookup"><span data-stu-id="4671d-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="4671d-125">只有必須存取磁片區和靜音控制項以外之硬體功能的特殊應用程式，才需要使用 DeviceTopology API。</span><span class="sxs-lookup"><span data-stu-id="4671d-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="4671d-126">針對只需要控制獨佔模式資料流程之磁片區層級的應用程式，EndpointVolume API 較容易使用，而且可以可靠地使用更廣泛的音訊硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="4671d-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="4671d-127">如需在 EndpointVolume API 中使用介面的程式碼範例，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="4671d-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="4671d-128">端點磁片區控制項</span><span class="sxs-lookup"><span data-stu-id="4671d-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="4671d-129">尖峰計量</span><span class="sxs-lookup"><span data-stu-id="4671d-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="4671d-130">若要查看使用 EndpointVolume API 的範例，請參閱 Windows SDK 中的 [EndpointVolume](endpointvolume.md) 。</span><span class="sxs-lookup"><span data-stu-id="4671d-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="4671d-131">EndpointVolume API 會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="4671d-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="4671d-132">介面</span><span class="sxs-lookup"><span data-stu-id="4671d-132">Interface</span></span>                                                | <span data-ttu-id="4671d-133">描述</span><span class="sxs-lookup"><span data-stu-id="4671d-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4671d-134">**IAudioEndpointVolume**</span><span class="sxs-lookup"><span data-stu-id="4671d-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="4671d-135">代表音訊串流上或音訊端點裝置的音量控制項。</span><span class="sxs-lookup"><span data-stu-id="4671d-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="4671d-136">**IAudioMeterInformation**</span><span class="sxs-lookup"><span data-stu-id="4671d-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="4671d-137">表示音訊串流上或音訊端點裝置的尖峰計量。</span><span class="sxs-lookup"><span data-stu-id="4671d-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="4671d-138">此外，EndpointVolume API 的用戶端必須在音訊端點裝置上執行磁片區和靜音變更的通知，才能執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="4671d-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="4671d-139">介面</span><span class="sxs-lookup"><span data-stu-id="4671d-139">Interface</span></span>                                                            | <span data-ttu-id="4671d-140">描述</span><span class="sxs-lookup"><span data-stu-id="4671d-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4671d-141">**IAudioEndpointVolumeCallback**</span><span class="sxs-lookup"><span data-stu-id="4671d-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="4671d-142">當音訊端點裝置的音量層級或靜音狀態變更時，會提供通知。</span><span class="sxs-lookup"><span data-stu-id="4671d-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4671d-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="4671d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4671d-144">音量控制項</span><span class="sxs-lookup"><span data-stu-id="4671d-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="4671d-145">**IMMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="4671d-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="4671d-146">**IMMDevice：： Activate**</span><span class="sxs-lookup"><span data-stu-id="4671d-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="4671d-147">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="4671d-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="4671d-148">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="4671d-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



