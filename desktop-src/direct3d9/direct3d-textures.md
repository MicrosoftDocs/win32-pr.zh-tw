---
description: 紋理是在電腦產生 3D 影像中創造真實感的利器。 Direct3D 支援廣泛的紋理功能設定，提供開發人員輕鬆存取進階紋理技術。
ms.assetid: 48dcbc86-631e-4bc7-b809-b0e4a0a9ae8e
title: 'Direct3d 材質 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afebd7217b36ad5f740616e198963314a1d2aca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108468"
---
# <a name="direct3d-textures-direct3d-9"></a><span data-ttu-id="229e9-104">Direct3d 材質 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="229e9-104">Direct3D Textures (Direct3D 9)</span></span>

<span data-ttu-id="229e9-105">紋理是在電腦產生 3D 影像中創造真實感的利器。</span><span class="sxs-lookup"><span data-stu-id="229e9-105">Textures are a powerful tool in creating realism in computer-generated 3D images.</span></span> <span data-ttu-id="229e9-106">Direct3D 支援廣泛的紋理功能設定，提供開發人員輕鬆存取進階紋理技術。</span><span class="sxs-lookup"><span data-stu-id="229e9-106">Direct3D supports an extensive texturing feature set, providing developers with easy access to advanced texturing techniques.</span></span>

<span data-ttu-id="229e9-107">本節將協助您開始使用紋理。</span><span class="sxs-lookup"><span data-stu-id="229e9-107">This section will get you started using textures.</span></span>

-   [<span data-ttu-id="229e9-108"> (Direct3D 9) 的基本紋理概念 </span><span class="sxs-lookup"><span data-stu-id="229e9-108">Basic Texturing Concepts (Direct3D 9)</span></span>](basic-texturing-concepts.md)
-   [<span data-ttu-id="229e9-109"> (Direct3D 9) 的材質座標 </span><span class="sxs-lookup"><span data-stu-id="229e9-109">Texture Coordinates (Direct3D 9)</span></span>](texture-coordinates.md)
-   [<span data-ttu-id="229e9-110"> (Direct3D 9) 的材質篩選 </span><span class="sxs-lookup"><span data-stu-id="229e9-110">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
-   [<span data-ttu-id="229e9-111"> (Direct3D 9) 的材質資源 </span><span class="sxs-lookup"><span data-stu-id="229e9-111">Texture Resources (Direct3D 9)</span></span>](texture-resources.md)
-   [<span data-ttu-id="229e9-112"> (Direct3D 9) 的材質換行 </span><span class="sxs-lookup"><span data-stu-id="229e9-112">Texture Wrapping (Direct3D 9)</span></span>](texture-wrapping.md)
-   [<span data-ttu-id="229e9-113"> (Direct3D 9) 的材質混合 </span><span class="sxs-lookup"><span data-stu-id="229e9-113">Texture Blending (Direct3D 9)</span></span>](texture-blending.md)

<span data-ttu-id="229e9-114">這些主題將詳細說明其他紋理功能。</span><span class="sxs-lookup"><span data-stu-id="229e9-114">These topics will go into more detail about additional texturing functionality.</span></span>

-   [<span data-ttu-id="229e9-115">自動產生 Mipmap (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="229e9-115">Automatic Generation of Mipmaps (Direct3D 9)</span></span>](automatic-generation-of-mipmaps.md)
-   [<span data-ttu-id="229e9-116">自動材質管理 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="229e9-116">Automatic Texture Management (Direct3D 9)</span></span>](automatic-texture-management.md)
-   [<span data-ttu-id="229e9-117"> (Direct3D 9) 的壓縮材質資源 </span><span class="sxs-lookup"><span data-stu-id="229e9-117">Compressed Texture Resources (Direct3D 9)</span></span>](compressed-texture-resources.md)
-   [<span data-ttu-id="229e9-118"> (Direct3D 9) 進行紋理的硬體考慮 </span><span class="sxs-lookup"><span data-stu-id="229e9-118">Hardware Considerations for Texturing (Direct3D 9)</span></span>](hardware-considerations-for-texturing.md)
-   [<span data-ttu-id="229e9-119"> (Direct3D 9) 的音量材質資源 </span><span class="sxs-lookup"><span data-stu-id="229e9-119">Volume Texture Resources (Direct3D 9)</span></span>](volume-texture-resources.md)

<span data-ttu-id="229e9-120">若要改善效能，請考慮使用動態紋理。</span><span class="sxs-lookup"><span data-stu-id="229e9-120">For improved performance, consider using dynamic textures.</span></span> <span data-ttu-id="229e9-121">動態紋理可以在每個影格中鎖定、寫入，或是解鎖。</span><span class="sxs-lookup"><span data-stu-id="229e9-121">A dynamic texture can be locked, written to, and unlocked each frame.</span></span> <span data-ttu-id="229e9-122">請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="229e9-122">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="229e9-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="229e9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="229e9-124">快速入門</span><span class="sxs-lookup"><span data-stu-id="229e9-124">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



