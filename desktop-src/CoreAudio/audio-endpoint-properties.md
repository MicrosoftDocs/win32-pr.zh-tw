---
description: 音訊端點屬性
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: 音訊端點屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187743"
---
# <a name="audio-endpoint-properties"></a><span data-ttu-id="e6ca1-103">音訊端點屬性</span><span class="sxs-lookup"><span data-stu-id="e6ca1-103">Audio Endpoint Properties</span></span>

<span data-ttu-id="e6ca1-104">標頭檔 Mmdeviceapi 會在 Windows Vista 和更新版本中定義 [音訊端點裝置](audio-endpoint-devices.md) 的數個屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-104">Header file Mmdeviceapi.h defines several properties of [audio endpoint devices](audio-endpoint-devices.md) in Windows Vista and later.</span></span> <span data-ttu-id="e6ca1-105">Windows 音訊服務會設定這些屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-105">The Windows audio service sets the values of these properties.</span></span> <span data-ttu-id="e6ca1-106">用戶端可以讀取這些屬性，但是不應該設定它們。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-106">Clients can read these properties, but should not set them.</span></span> <span data-ttu-id="e6ca1-107">屬性值會儲存為 **PROPVARIANT** 結構。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-107">Property values are stored as **PROPVARIANT** structures.</span></span>

<span data-ttu-id="e6ca1-108">讀取音訊輸入裝置屬性的建議方式是使用 Windows 中的 Api。 [**列舉**](/uwp/api/Windows.Devices.Enumeration) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-108">The recommended way of reading the properties of an audio input device is to use the APIs in the [**Windows.Devices.Enumeration**](/uwp/api/Windows.Devices.Enumeration) namespace.</span></span> <span data-ttu-id="e6ca1-109">Windows Store 應用程式和桌面應用程式支援這些 Api。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-109">These APIs are supported for Windows Store apps and desktop apps.</span></span> <span data-ttu-id="e6ca1-110">針對使用 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面讀取裝置屬性的現有桌面應用程式，請參閱 [裝置屬性](device-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-110">For existing desktop apps that read device properties using the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface, see [Device Properties](device-properties.md).</span></span> <span data-ttu-id="e6ca1-111">**IMMDevice** 不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-111">**IMMDevice** is not supported for Windows Store apps.</span></span>

<span data-ttu-id="e6ca1-112">如需示範如何存取音訊端點裝置屬性的程式碼範例，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="e6ca1-112">For code examples that show how to access the properties of an audio endpoint device, see the following topics:</span></span>

-   [<span data-ttu-id="e6ca1-113">裝置事件</span><span class="sxs-lookup"><span data-stu-id="e6ca1-113">Device Events</span></span>](device-events.md)
-   [<span data-ttu-id="e6ca1-114">DirectSound 應用程式的裝置角色</span><span class="sxs-lookup"><span data-stu-id="e6ca1-114">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)

<span data-ttu-id="e6ca1-115">如需 **PROPVARIANT** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-115">For information about **PROPVARIANT**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="e6ca1-116">下列是音訊端點裝置專用的屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-116">The following properties are specific to audio endpoint devices.</span></span>



| <span data-ttu-id="e6ca1-117">屬性</span><span class="sxs-lookup"><span data-stu-id="e6ca1-117">Property</span></span>                                                                                                            | <span data-ttu-id="e6ca1-118">描述</span><span class="sxs-lookup"><span data-stu-id="e6ca1-118">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6ca1-119">**PKEY \_ AudioEndpoint \_ 關聯**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-119">**PKEY\_AudioEndpoint\_Association**</span></span>](pkey-audioendpoint-association.md)                                          | <span data-ttu-id="e6ca1-120">將核心串流 (KS) 釘選類別與音訊端點裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-120">Associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span>                                                                                |
| [<span data-ttu-id="e6ca1-121">**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-121">**PKEY\_AudioEndpoint\_ControlPanelPageProvider**</span></span>](pkey-audioendpoint-controlpanelpageprovider.md)                | <span data-ttu-id="e6ca1-122">為音訊端點裝置的裝置屬性延伸模組指定已註冊提供者的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-122">Specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span>                                              |
| [<span data-ttu-id="e6ca1-123">**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-123">**PKEY\_AudioEndpoint\_Disable\_SysFx**</span></span>](pkey-audioendpoint-disable-sysfx.md)                                     | <span data-ttu-id="e6ca1-124">指出是否已在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-124">Indicates whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="e6ca1-125">**PKEY \_ AudioEndpoint \_ FormFactor**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-125">**PKEY\_AudioEndpoint\_FormFactor**</span></span>](pkey-audioendpoint-formfactor.md)                                            | <span data-ttu-id="e6ca1-126">指出音訊端點裝置的實體屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-126">Indicates the physical attributes of the audio endpoint device.</span></span>                                                                                               |
| [<span data-ttu-id="e6ca1-127">**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-127">**PKEY\_AudioEndpoint\_FullRangeSpeakers**</span></span>](pkey-audioendpoint-fullrangespeakers.md)                              | <span data-ttu-id="e6ca1-128">指定連線到音訊端點裝置的全範圍喇叭的通道設定遮罩。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-128">Specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span>                                         |
| [<span data-ttu-id="e6ca1-129">**PKEY \_ AudioEndpoint \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-129">**PKEY\_AudioEndpoint\_GUID**</span></span>](pkey-audioendpoint-guid.md)                                                        | <span data-ttu-id="e6ca1-130">提供對應于音訊端點裝置的 DirectSound 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-130">Supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span>                                                                     |
| [<span data-ttu-id="e6ca1-131">**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-131">**PKEY\_AudioEndpoint\_PhysicalSpeakers**</span></span>](pkey-audioendpoint-physicalspeakers.md)                                | <span data-ttu-id="e6ca1-132">定義音訊端點裝置的實體喇叭設定。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-132">Defines the physical speaker configuration for the audio endpoint device.</span></span>                                                                                     |
| [<span data-ttu-id="e6ca1-133">**PKEY \_ AudioEngine \_ DeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-133">**PKEY\_AudioEngine\_DeviceFormat**</span></span>](pkey-audioengine-deviceformat.md)                                            | <span data-ttu-id="e6ca1-134">指定裝置格式，也就是音訊引擎針對流入或流出音訊端點裝置的共用模式資料流程所使用的格式。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-134">Specifies the device format, which is the format that the audio engine uses for the shared-mode stream that flows to or from the audio endpoint device.</span></span>       |
| [<span data-ttu-id="e6ca1-135">**PKEY \_ AudioEngine \_ OEMFormat**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-135">**PKEY\_AudioEngine\_OEMFormat**</span></span>](pkey-audioengine-oemformat.md)<br/>                                       | <span data-ttu-id="e6ca1-136">指定用於轉譯或捕捉資料流程之裝置的預設格式。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-136">Specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="e6ca1-137">在 .inf 檔案中，OEM 會填入這些值。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-137">The values are populated by the OEM in an .inf file.</span></span> <br/> |
| [<span data-ttu-id="e6ca1-138">**PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-138">**PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode**</span></span>](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | <span data-ttu-id="e6ca1-139">指出端點是否支援事件驅動模式。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-139">Indicates whether the endpoint supports the event-driven mode.</span></span> <span data-ttu-id="e6ca1-140">在 .inf 檔案中，OEM 會填入這些值。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-140">The values are populated by the OEM in an .inf file.</span></span><br/>                                |



 

<span data-ttu-id="e6ca1-141">核心音訊 Api 支援不會專門用於音訊端點裝置的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-141">The core audio APIs support additional properties that do not apply exclusively to audio endpoint devices.</span></span> <span data-ttu-id="e6ca1-142">如需這些額外屬性的詳細資訊，請參閱 [裝置屬性](device-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="e6ca1-142">For more information about these additional properties, see [Device Properties](device-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6ca1-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6ca1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ca1-144">音訊端點裝置</span><span class="sxs-lookup"><span data-stu-id="e6ca1-144">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="e6ca1-145">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="e6ca1-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

