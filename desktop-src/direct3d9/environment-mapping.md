---
description: 環境對應是一種在不使用光線追蹤的情況下，模擬高度反射表面的技巧。
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: " (Direct3D 9) 的環境對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687652"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="9df42-103"> (Direct3D 9) 的環境對應</span><span class="sxs-lookup"><span data-stu-id="9df42-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="9df42-104">環境對應是一種在不使用光線追蹤的情況下，模擬高度反射表面的技巧。</span><span class="sxs-lookup"><span data-stu-id="9df42-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="9df42-105">在實務上，環境對應會套用特殊材質圖，其中包含物件周圍之場景的影像。</span><span class="sxs-lookup"><span data-stu-id="9df42-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="9df42-106">結果近似于反射表面的外觀，夠近一點可欺騙，而不會產生任何與光線追蹤相關的複雜計算。</span><span class="sxs-lookup"><span data-stu-id="9df42-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="9df42-107">下圖示范稱為球形環境對應的環境對應類型。</span><span class="sxs-lookup"><span data-stu-id="9df42-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="9df42-108">如需詳細資訊，請參閱 [球形環境對應](spherical-environment-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="9df42-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![已套用材質的茶壺圖例，反映了周圍的周圍](images/spheremapped-teapot.png)

<span data-ttu-id="9df42-110">此影像中的茶壺會反映其周圍的情況;這實際上是套用至物件的材質。</span><span class="sxs-lookup"><span data-stu-id="9df42-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="9df42-111">由於環境對應會使用材質，並結合了特別計算的材質座標，因此可以即時執行。</span><span class="sxs-lookup"><span data-stu-id="9df42-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="9df42-112">本節提供有關使用 Direct3D 來執行兩個常見的環境對應類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="9df42-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="9df42-113">在整個圖形產業中使用的環境對應有許多種，但下列主題以兩個最常見的表單為目標：三個最常見的表單：三種環境對應和球面環境對應。</span><span class="sxs-lookup"><span data-stu-id="9df42-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="9df42-114">三次環境對應</span><span class="sxs-lookup"><span data-stu-id="9df42-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="9df42-115">球形環境對應</span><span class="sxs-lookup"><span data-stu-id="9df42-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="9df42-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9df42-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9df42-117">圖元管線</span><span class="sxs-lookup"><span data-stu-id="9df42-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



