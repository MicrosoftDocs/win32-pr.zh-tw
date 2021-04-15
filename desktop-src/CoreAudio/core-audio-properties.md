---
description: 此核心音訊 SDK 的程式設計參考包含下列屬性。
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: 核心音訊屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510384"
---
# <a name="core-audio-properties"></a><span data-ttu-id="298bb-103">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="298bb-103">Core Audio Properties</span></span>

<span data-ttu-id="298bb-104">此核心音訊 SDK 的程式設計參考包含下列屬性。</span><span class="sxs-lookup"><span data-stu-id="298bb-104">This programming reference for the Core Audio SDK includes the following properties.</span></span>

## <a name="audio-endpoint-properties"></a><span data-ttu-id="298bb-105">音訊端點屬性</span><span class="sxs-lookup"><span data-stu-id="298bb-105">Audio Endpoint Properties</span></span>

<span data-ttu-id="298bb-106">Core Audio SDK 包含數個 [音訊端點裝置](audio-endpoint-devices.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="298bb-106">Core Audio SDK includes several properties of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="298bb-107">如需詳細資訊，請參閱 [音訊端點屬性](audio-endpoint-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="298bb-107">For more information, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span>

<span data-ttu-id="298bb-108">以下是在 Windows Vista 和更新版本的 Mmdeviceapi 中定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="298bb-108">The following properties are defined in Mmdeviceapi.h in Windows Vista and later.</span></span>



| <span data-ttu-id="298bb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="298bb-109">Property</span></span>                                                                                                            | <span data-ttu-id="298bb-110">描述</span><span class="sxs-lookup"><span data-stu-id="298bb-110">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="298bb-111">**PKEY \_ AudioEndpoint \_ 關聯**</span><span class="sxs-lookup"><span data-stu-id="298bb-111">**PKEY\_AudioEndpoint\_Association**</span></span>](pkey-audioendpoint-association.md)                                          | <span data-ttu-id="298bb-112">將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="298bb-112">Associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span>                                                                                |
| [<span data-ttu-id="298bb-113">**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**</span><span class="sxs-lookup"><span data-stu-id="298bb-113">**PKEY\_AudioEndpoint\_ControlPanelPageProvider**</span></span>](pkey-audioendpoint-controlpanelpageprovider.md)                | <span data-ttu-id="298bb-114">為音訊端點裝置的裝置屬性延伸模組指定已註冊提供者的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="298bb-114">Specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span>                                              |
| [<span data-ttu-id="298bb-115">**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**</span><span class="sxs-lookup"><span data-stu-id="298bb-115">**PKEY\_AudioEndpoint\_Disable\_SysFx**</span></span>](pkey-audioendpoint-disable-sysfx.md)                                     | <span data-ttu-id="298bb-116">指出是否已在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。</span><span class="sxs-lookup"><span data-stu-id="298bb-116">Indicates whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="298bb-117">**PKEY \_ AudioEndpoint \_ FormFactor**</span><span class="sxs-lookup"><span data-stu-id="298bb-117">**PKEY\_AudioEndpoint\_FormFactor**</span></span>](pkey-audioendpoint-formfactor.md)                                            | <span data-ttu-id="298bb-118">指出音訊端點裝置的實體屬性。</span><span class="sxs-lookup"><span data-stu-id="298bb-118">Indicates the physical attributes of the audio endpoint device.</span></span>                                                                                               |
| [<span data-ttu-id="298bb-119">**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**</span><span class="sxs-lookup"><span data-stu-id="298bb-119">**PKEY\_AudioEndpoint\_FullRangeSpeakers**</span></span>](pkey-audioendpoint-fullrangespeakers.md)                              | <span data-ttu-id="298bb-120">指定連線到音訊端點裝置的全範圍喇叭的通道設定遮罩。</span><span class="sxs-lookup"><span data-stu-id="298bb-120">Specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span>                                         |
| [<span data-ttu-id="298bb-121">**PKEY \_ AudioEndpoint \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="298bb-121">**PKEY\_AudioEndpoint\_GUID**</span></span>](pkey-audioendpoint-guid.md)                                                        | <span data-ttu-id="298bb-122">提供對應于音訊端點裝置的 DirectSound 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="298bb-122">Supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span>                                                                     |
| [<span data-ttu-id="298bb-123">**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**</span><span class="sxs-lookup"><span data-stu-id="298bb-123">**PKEY\_AudioEndpoint\_PhysicalSpeakers**</span></span>](pkey-audioendpoint-physicalspeakers.md)                                | <span data-ttu-id="298bb-124">定義音訊端點裝置的實體喇叭設定。</span><span class="sxs-lookup"><span data-stu-id="298bb-124">Defines the physical speaker configuration for the audio endpoint device.</span></span>                                                                                     |
| [<span data-ttu-id="298bb-125">**PKEY \_ AudioEngine \_ DeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="298bb-125">**PKEY\_AudioEngine\_DeviceFormat**</span></span>](pkey-audioengine-deviceformat.md)                                            | <span data-ttu-id="298bb-126">指定裝置格式，也就是音訊引擎針對流入或流出音訊端點裝置的共用模式資料流程所使用的格式。</span><span class="sxs-lookup"><span data-stu-id="298bb-126">Specifies the device format, which is the format that the audio engine uses for the shared-mode stream that flows to or from the audio endpoint device.</span></span>       |
| [<span data-ttu-id="298bb-127">**PKEY \_ AudioEngine \_ OEMFormat**</span><span class="sxs-lookup"><span data-stu-id="298bb-127">**PKEY\_AudioEngine\_OEMFormat**</span></span>](pkey-audioengine-oemformat.md)<br/>                                       | <span data-ttu-id="298bb-128">指定用於轉譯或捕捉資料流程之裝置的預設格式。</span><span class="sxs-lookup"><span data-stu-id="298bb-128">Specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="298bb-129">在 .inf 檔案中，OEM 會填入這些值。</span><span class="sxs-lookup"><span data-stu-id="298bb-129">The values are populated by the OEM in an .inf file.</span></span> <br/> |
| [<span data-ttu-id="298bb-130">**PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="298bb-130">**PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode**</span></span>](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | <span data-ttu-id="298bb-131">指出端點是否支援事件驅動模式。</span><span class="sxs-lookup"><span data-stu-id="298bb-131">Indicates whether the endpoint supports the event-driven mode.</span></span> <span data-ttu-id="298bb-132">在 .inf 檔案中，OEM 會填入這些值。</span><span class="sxs-lookup"><span data-stu-id="298bb-132">The values are populated by the OEM in an .inf file.</span></span><br/>                                |
| [<span data-ttu-id="298bb-133">**PKEY \_ AudioEndpoint \_ JackSubType**</span><span class="sxs-lookup"><span data-stu-id="298bb-133">**PKEY\_AudioEndpoint\_JackSubType**</span></span>](pkey-audioendpoint-jacksubtype.md)<br/>                               | <span data-ttu-id="298bb-134">包含音訊端點裝置的輸出類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="298bb-134">Contains an output category GUID for an audio endpoint device.</span></span> <br/>                                                                                    |



 

## <a name="device-properties"></a><span data-ttu-id="298bb-135">裝置內容</span><span class="sxs-lookup"><span data-stu-id="298bb-135">Device Properties</span></span>

<span data-ttu-id="298bb-136">Core Audio SDK 包含數個 [音訊端點裝置](audio-endpoint-devices.md)的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="298bb-136">Core Audio SDK includes several device properties of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="298bb-137">如需詳細資訊，請參閱 [裝置屬性](device-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="298bb-137">For more information, see [Device Properties](device-properties.md).</span></span>

<span data-ttu-id="298bb-138">下列屬性是在 \_ Windows Vista 和更新版本的 Functiondiscoverykeys devpkey 中定義。</span><span class="sxs-lookup"><span data-stu-id="298bb-138">The following properties are defined in Functiondiscoverykeys\_devpkey.h in Windows Vista and later.</span></span>



| <span data-ttu-id="298bb-139">屬性</span><span class="sxs-lookup"><span data-stu-id="298bb-139">Property</span></span>                                                                         | <span data-ttu-id="298bb-140">描述</span><span class="sxs-lookup"><span data-stu-id="298bb-140">Description</span></span>                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="298bb-141">**PKEY \_ DeviceInterface \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="298bb-141">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="298bb-142">端點裝置所連接之音訊介面卡的易記名稱 (例如「XYZ 音訊介面卡」 ) 。</span><span class="sxs-lookup"><span data-stu-id="298bb-142">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>                                                                               |
| [<span data-ttu-id="298bb-143">**PKEY \_ 裝置 \_ DeviceDesc**</span><span class="sxs-lookup"><span data-stu-id="298bb-143">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="298bb-144">端點裝置的裝置描述 (例如「喇叭」 ) 。</span><span class="sxs-lookup"><span data-stu-id="298bb-144">The device description of the endpoint device (for example, "Speakers").</span></span>                                                                                                                          |
| [<span data-ttu-id="298bb-145">**PKEY \_ 裝置 \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="298bb-145">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="298bb-146">端點裝置的易記名稱 (例如「喇叭 (XYZ 音訊介面卡) 」 ) 。</span><span class="sxs-lookup"><span data-stu-id="298bb-146">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>                                                                                                           |
| <span data-ttu-id="298bb-147">**PKEY \_ 裝置 \_ ContainerId**</span><span class="sxs-lookup"><span data-stu-id="298bb-147">**PKEY\_Device\_ContainerId**</span></span>                                                    | <span data-ttu-id="298bb-148">儲存執行音訊端點之 PnP 裝置的容器識別碼。</span><span class="sxs-lookup"><span data-stu-id="298bb-148">Stores the container identifier of the PnP device that implements the audio endpoint.</span></span> <span data-ttu-id="298bb-149">如需此屬性的詳細資訊，請參閱 Windows WDK 檔中的「裝置屬性參考」。</span><span class="sxs-lookup"><span data-stu-id="298bb-149">For more information about this property, see "Device Property Reference" in the Windows WDK documentation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="298bb-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="298bb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="298bb-151">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="298bb-151">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




