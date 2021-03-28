---
title: '裝置 (Direct3D 11 圖形) '
description: 本節說明 Direct3D 11 裝置和裝置內容物件。
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dda010b3801952e90514fac6307556f8f6fbaff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104991062"
---
# <a name="devices-direct3d-11-graphics"></a><span data-ttu-id="12eef-103">裝置 (Direct3D 11 圖形) </span><span class="sxs-lookup"><span data-stu-id="12eef-103">Devices (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="12eef-104">Direct3D 裝置會配置和終結物件、呈現基本專案，以及與圖形驅動程式和硬體通訊。</span><span class="sxs-lookup"><span data-stu-id="12eef-104">A Direct3D device allocates and destroys objects, renders primitives, and communicates with a graphics driver and the hardware.</span></span> <span data-ttu-id="12eef-105">在 Direct3D 11 中，裝置會分割成裝置物件來建立資源，以及執行轉譯的裝置內容物件。</span><span class="sxs-lookup"><span data-stu-id="12eef-105">In Direct3D 11, a device is separated into a device object for creating resources and a device-context object, which performs rendering.</span></span> <span data-ttu-id="12eef-106">本節說明 Direct3D 11 裝置和裝置內容物件。</span><span class="sxs-lookup"><span data-stu-id="12eef-106">This section describes Direct3D 11 device and device-context objects.</span></span>

<span data-ttu-id="12eef-107">從一個裝置建立的物件不能直接與其他裝置搭配使用。</span><span class="sxs-lookup"><span data-stu-id="12eef-107">Objects created from one device cannot be used directly with other devices.</span></span> <span data-ttu-id="12eef-108">使用共用資源，在多個裝置之間共用資料，其條件約束是共用物件只能由建立它的裝置使用。</span><span class="sxs-lookup"><span data-stu-id="12eef-108">Use a shared resource to share data between multiple devices, with the constraint that a shared object can be used only by the device that created it.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="12eef-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="12eef-109">In this section</span></span>



| <span data-ttu-id="12eef-110">主題</span><span class="sxs-lookup"><span data-stu-id="12eef-110">Topic</span></span>                                                                                                                                                         | <span data-ttu-id="12eef-111">描述</span><span class="sxs-lookup"><span data-stu-id="12eef-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12eef-112">Direct3D 11 中的裝置簡介</span><span class="sxs-lookup"><span data-stu-id="12eef-112">Introduction to a Device in Direct3D 11</span></span>](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | <span data-ttu-id="12eef-113">Direct3D 11 物件模型會將資源建立和轉譯功能區分為裝置和一或多個內容。這項分隔是設計來協助多執行緒處理。</span><span class="sxs-lookup"><span data-stu-id="12eef-113">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span><br/>                                                  |
| [<span data-ttu-id="12eef-114">軟體層</span><span class="sxs-lookup"><span data-stu-id="12eef-114">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | <span data-ttu-id="12eef-115">Direct3D 11 執行時間是使用圖層來建立，從核心的基本功能開始，並在外部層建立選擇性和開發人員協助工具。</span><span class="sxs-lookup"><span data-stu-id="12eef-115">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="12eef-116">本節說明每個圖層的功能。</span><span class="sxs-lookup"><span data-stu-id="12eef-116">This section describes the functionality of each layer.</span></span><br/> |
| [<span data-ttu-id="12eef-117">建立變形和參考裝置的限制</span><span class="sxs-lookup"><span data-stu-id="12eef-117">Limitations Creating WARP and Reference Devices</span></span>](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | <span data-ttu-id="12eef-118">在 Direct3D 10.1 和 Direct3D 11.0 中建立變形和參考裝置有一些限制。</span><span class="sxs-lookup"><span data-stu-id="12eef-118">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="12eef-119">本主題討論這些限制。</span><span class="sxs-lookup"><span data-stu-id="12eef-119">This topic discusses those limitations.</span></span><br/>                                                                                              |
| [<span data-ttu-id="12eef-120">舊版硬體上的 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="12eef-120">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | <span data-ttu-id="12eef-121">本節討論如何設計 Direct3D 11，以支援新的和現有的硬體，從 DirectX 9 到 DirectX 11。</span><span class="sxs-lookup"><span data-stu-id="12eef-121">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="12eef-122">使用 Direct3D 11 功能資料來補充 Direct3D 功能等級</span><span class="sxs-lookup"><span data-stu-id="12eef-122">Using Direct3D 11 feature data to supplement Direct3D feature levels</span></span>](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | <span data-ttu-id="12eef-123">瞭解如何檢查裝置支援的選用功能，包括最新的 Windows 版本中新增的功能。</span><span class="sxs-lookup"><span data-stu-id="12eef-123">Find out how to check device support for optional features, including features that were added in recent versions of Windows.</span></span><br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a><span data-ttu-id="12eef-124">裝置的 how to 主題</span><span class="sxs-lookup"><span data-stu-id="12eef-124">How to topics about devices</span></span>



| <span data-ttu-id="12eef-125">主題</span><span class="sxs-lookup"><span data-stu-id="12eef-125">Topic</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="12eef-126">描述</span><span class="sxs-lookup"><span data-stu-id="12eef-126">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="12eef-127"><span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[如何：建立參考裝置](overviews-direct3d-11-devices-create-ref.md)</span><span class="sxs-lookup"><span data-stu-id="12eef-127"><span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[How To: Create a Reference Device](overviews-direct3d-11-devices-create-ref.md)</span></span><br/>                                                 | <span data-ttu-id="12eef-128">說明如何建立參照裝置。</span><span class="sxs-lookup"><span data-stu-id="12eef-128">Describes how to create a reference device.</span></span><br/>                            |
| <span data-ttu-id="12eef-129"><span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[如何：建立變形裝置](overviews-direct3d-11-devices-create-warp.md)</span><span class="sxs-lookup"><span data-stu-id="12eef-129"><span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[How To: Create a WARP Device](overviews-direct3d-11-devices-create-warp.md)</span></span><br/>                                                                    | <span data-ttu-id="12eef-130">說明如何建立變形裝置。</span><span class="sxs-lookup"><span data-stu-id="12eef-130">Describes how to create a WARP device.</span></span><br/>                                 |
| <span data-ttu-id="12eef-131"><span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[如何：建立交換鏈](overviews-direct3d-11-devices-create-swap-chain.md)</span><span class="sxs-lookup"><span data-stu-id="12eef-131"><span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[How To: Create a Swap Chain](overviews-direct3d-11-devices-create-swap-chain.md)</span></span><br/>                                                                  | <span data-ttu-id="12eef-132">說明如何建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="12eef-132">Describes how to create a swap chain.</span></span><br/>                                  |
| <span data-ttu-id="12eef-133"><span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[如何：列舉介面卡](overviews-direct3d-11-devices-enum.md)</span><span class="sxs-lookup"><span data-stu-id="12eef-133"><span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md)</span></span><br/>                                                                                   | <span data-ttu-id="12eef-134">說明如何列舉實體顯示配接器。</span><span class="sxs-lookup"><span data-stu-id="12eef-134">Describes how to enumerate the physical display adapters.</span></span><br/>              |
| <span data-ttu-id="12eef-135"><span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[如何：取得介面卡顯示模式](overviews-direct3d-11-devices-get-adapter-info.md)</span><span class="sxs-lookup"><span data-stu-id="12eef-135"><span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[How To: Get Adapter Display Modes](overviews-direct3d-11-devices-get-adapter-info.md)</span></span><br/>                                           | <span data-ttu-id="12eef-136">說明如何取得介面卡支援的顯示功能。</span><span class="sxs-lookup"><span data-stu-id="12eef-136">Describes how to get the supported display capabilities of an adapter.</span></span><br/> |
| <span data-ttu-id="12eef-137"><span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[如何：建立裝置和立即內容](overviews-direct3d-11-devices-initialize.md)</span><span class="sxs-lookup"><span data-stu-id="12eef-137"><span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[How To: Create a Device and Immediate Context](overviews-direct3d-11-devices-initialize.md)</span></span><br/> | <span data-ttu-id="12eef-138">說明如何初始化裝置。</span><span class="sxs-lookup"><span data-stu-id="12eef-138">Describes how to initialize a device.</span></span><br/>                                  |



 

## <a name="related-topics"></a><span data-ttu-id="12eef-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="12eef-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12eef-140">Direct3D 11 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="12eef-140">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





