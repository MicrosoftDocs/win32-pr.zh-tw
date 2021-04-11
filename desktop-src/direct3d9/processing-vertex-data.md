---
description: IDirect3DDevice9 介面支援在軟體和硬體中處理頂點。
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: 處理 (Direct3D 9) 的頂點資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846591"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="1962b-103">處理 (Direct3D 9) 的頂點資料</span><span class="sxs-lookup"><span data-stu-id="1962b-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="1962b-104">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面支援在軟體和硬體中處理頂點。</span><span class="sxs-lookup"><span data-stu-id="1962b-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="1962b-105">一般情況下，軟體和硬體頂點處理的裝置功能並不相同。</span><span class="sxs-lookup"><span data-stu-id="1962b-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="1962b-106">硬體功能是可變的，取決於顯示器介面卡和驅動程式，而軟體功能則是固定的。</span><span class="sxs-lookup"><span data-stu-id="1962b-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="1962b-107">下列旗標可控制硬體抽象層的頂點處理行為 (HAL) 和參考裝置。</span><span class="sxs-lookup"><span data-stu-id="1962b-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="1962b-108">D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="1962b-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="1962b-109">D3DCREATE \_ 硬體 \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="1962b-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="1962b-110">D3DCREATE \_ 混合 \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="1962b-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="1962b-111">呼叫 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)時，請指定其中一個頂點處理行為旗標。</span><span class="sxs-lookup"><span data-stu-id="1962b-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="1962b-112">混合模式旗標可讓裝置執行軟體和硬體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="1962b-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="1962b-113">裝置一次只能設定一個頂點處理旗標。</span><span class="sxs-lookup"><span data-stu-id="1962b-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="1962b-114">請注意， \_ \_ (D3DCREATE PUREDEVICE) 建立純裝置時，必須設定 D3DCREATE 硬體 VERTEXPROCESSING 旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1962b-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="1962b-115">為了避免單一裝置上的雙重頂點處理功能，在執行時間只會查詢硬體頂點處理功能。</span><span class="sxs-lookup"><span data-stu-id="1962b-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="1962b-116">軟體頂點處理功能是固定的，而且無法在執行時間查詢。</span><span class="sxs-lookup"><span data-stu-id="1962b-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="1962b-117">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構的 VertexProcessingCaps 成員會決定裝置的硬體頂點處理功能。</span><span class="sxs-lookup"><span data-stu-id="1962b-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="1962b-118">針對軟體頂點處理，支援下列功能。</span><span class="sxs-lookup"><span data-stu-id="1962b-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="1962b-119">D3DVTXPCAPS 的 D3DVTXPCAPS \_ DIRECTIONALLIGHTS 成員[](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="1962b-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="1962b-120">D3DVTXPCAPS 的 D3DVTXPCAPS \_ LOCALVIEWER 成員[](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="1962b-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="1962b-121">D3DVTXPCAPS 的 D3DVTXPCAPS \_ MATERIALSOURCE7 成員[](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="1962b-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="1962b-122">D3DVTXPCAPS 的 D3DVTXPCAPS \_ POSITIONALLIGHTS 成員[](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="1962b-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="1962b-123">D3DVTXPCAPS 的 D3DVTXPCAPS \_ TEXGEN 成員[](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="1962b-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="1962b-124">D3DVTXPCAPS 的 D3DVTXPCAPS \_ 補間成員[](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="1962b-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="1962b-125">此外，下表列出針對軟體頂點處理模式之裝置的 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構成員所設定的值。</span><span class="sxs-lookup"><span data-stu-id="1962b-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="1962b-126">成員</span><span class="sxs-lookup"><span data-stu-id="1962b-126">Member</span></span>                 | <span data-ttu-id="1962b-127">軟體頂點處理功能</span><span class="sxs-lookup"><span data-stu-id="1962b-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="1962b-128">MaxActiveLights</span><span class="sxs-lookup"><span data-stu-id="1962b-128">MaxActiveLights</span></span>        | <span data-ttu-id="1962b-129">無限制</span><span class="sxs-lookup"><span data-stu-id="1962b-129">Unlimited</span></span>                               |
| <span data-ttu-id="1962b-130">MaxUserClipPlanes</span><span class="sxs-lookup"><span data-stu-id="1962b-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="1962b-131">6</span><span class="sxs-lookup"><span data-stu-id="1962b-131">6</span></span>                                       |
| <span data-ttu-id="1962b-132">MaxVertexBlendMatrices</span><span class="sxs-lookup"><span data-stu-id="1962b-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="1962b-133">4</span><span class="sxs-lookup"><span data-stu-id="1962b-133">4</span></span>                                       |
| <span data-ttu-id="1962b-134">MaxStreams</span><span class="sxs-lookup"><span data-stu-id="1962b-134">MaxStreams</span></span>             | <span data-ttu-id="1962b-135">16</span><span class="sxs-lookup"><span data-stu-id="1962b-135">16</span></span>                                      |
| <span data-ttu-id="1962b-136">MaxVertexIndex</span><span class="sxs-lookup"><span data-stu-id="1962b-136">MaxVertexIndex</span></span>         | <span data-ttu-id="1962b-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1962b-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="1962b-138">一般而言，任何已系結至頂點的應用程式都應該使用 HAL 裝置。</span><span class="sxs-lookup"><span data-stu-id="1962b-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="1962b-139">軟體頂點處理提供一組保證的頂點處理功能，包括不限數目的燈光和可程式化頂點著色器的完整支援。</span><span class="sxs-lookup"><span data-stu-id="1962b-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="1962b-140">使用 HAL 裝置時，您隨時可以在軟體和硬體頂點處理之間切換 (這是唯一支援硬體和軟體頂點處理) 的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="1962b-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="1962b-141">唯一的需求是必須在系統記憶體中配置用於軟體頂點處理的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1962b-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1962b-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="1962b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1962b-143">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="1962b-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
