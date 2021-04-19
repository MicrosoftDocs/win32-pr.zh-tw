---
description: 早期電腦產生的 3D 影像，雖然普遍對當代而言算先進，但通常會有具光澤的塑膠感。
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: " (Direct3D 9) 的基本紋理概念"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972570"
---
# <a name="basic-texturing-concepts-direct3d-9"></a><span data-ttu-id="a32b3-103"> (Direct3D 9) 的基本紋理概念</span><span class="sxs-lookup"><span data-stu-id="a32b3-103">Basic Texturing Concepts (Direct3D 9)</span></span>

<span data-ttu-id="a32b3-104">早期電腦產生的 3D 影像，雖然普遍對當代而言算先進，但通常會有具光澤的塑膠感。</span><span class="sxs-lookup"><span data-stu-id="a32b3-104">Early computer-generated 3D images, although generally advanced for their time, tended to have a shiny plastic look.</span></span> <span data-ttu-id="a32b3-105">其缺乏可讓 3D 物件看起來逼真且複雜的標記類型，例如磨損、裂縫，指紋及指尖。</span><span class="sxs-lookup"><span data-stu-id="a32b3-105">They lacked the types of markings-such as scuffs, cracks, fingerprints, and smudges-that give 3D objects realistic visual complexity.</span></span> <span data-ttu-id="a32b3-106">在最近幾年，紋理在開發人員之間獲得了更熱門的功能，以增強電腦產生的3D 影像的真實性。</span><span class="sxs-lookup"><span data-stu-id="a32b3-106">In recent years, textures have gained popularity among developers as a tool for enhancing the realism of computer-generated 3D images.</span></span>

<span data-ttu-id="a32b3-107">在日常的使用中，文字紋理是指物件的平滑或粗糙度。</span><span class="sxs-lookup"><span data-stu-id="a32b3-107">In its everyday use, the word texture refers to an object's smoothness or roughness.</span></span> <span data-ttu-id="a32b3-108">不過，在電腦圖形中，紋理是像素色彩的點陣圖，讓物件具有紋理的外觀。</span><span class="sxs-lookup"><span data-stu-id="a32b3-108">In computer graphics, however, a texture is a bitmap of pixel colors that give an object the appearance of texture.</span></span>

<span data-ttu-id="a32b3-109">因為 Direct3D 紋理為點陣圖，所以任何點陣圖都可套用至 Direct3D 原始物件。</span><span class="sxs-lookup"><span data-stu-id="a32b3-109">Because Direct3D textures are bitmaps, any bitmap can be applied to a Direct3D primitive.</span></span> <span data-ttu-id="a32b3-110">例如，應用程式可以建立並操控似乎具備木紋圖樣的物件。</span><span class="sxs-lookup"><span data-stu-id="a32b3-110">For instance, applications can create and manipulate objects that appear to have a wood grain pattern in them.</span></span> <span data-ttu-id="a32b3-111">草地、泥土和岩石可套用至形成山丘的一組 3D 原始物件。</span><span class="sxs-lookup"><span data-stu-id="a32b3-111">Grass, dirt, and rocks can be applied to a set of 3D primitives that form a hill.</span></span> <span data-ttu-id="a32b3-112">結果為逼真的山坡。</span><span class="sxs-lookup"><span data-stu-id="a32b3-112">The result is a realistic-looking hillside.</span></span> <span data-ttu-id="a32b3-113">您也可以添加紋理來建立效果，例如路旁的路標、懸崖的岩石層，或地板大理石的外觀。</span><span class="sxs-lookup"><span data-stu-id="a32b3-113">You can also use texturing to create effects such as signs along a roadside, rock strata in a cliff, or the appearance of marble on a floor.</span></span>

<span data-ttu-id="a32b3-114">此外，Direct3D 支援更進階的添加紋理技術，例如紋理混合 (選擇性搭配透明度) 及光線對應。</span><span class="sxs-lookup"><span data-stu-id="a32b3-114">In addition, Direct3D supports more advanced texturing techniques such as texture blending-with or without transparency-and light mapping.</span></span> <span data-ttu-id="a32b3-115">如需詳細資訊，請參閱使用 [) 的材質混合 (direct3d 9 ](texture-blending.md) 和 [紋理的燈光對應 (Direct3D 9) ](light-mapping-with-textures.md)。</span><span class="sxs-lookup"><span data-stu-id="a32b3-115">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md) and [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

<span data-ttu-id="a32b3-116">如果您的應用程式建立硬體抽象層 (HAL) 裝置或軟體裝置，其可以使用 8、16、24、32、64 或 128 位元紋理。</span><span class="sxs-lookup"><span data-stu-id="a32b3-116">If your application creates a hardware abstraction layer (HAL) device or a software device, it can use 8, 16, 24, 32, 64, or 128-bit textures.</span></span>

<span data-ttu-id="a32b3-117">下列主題包含其他資訊。</span><span class="sxs-lookup"><span data-stu-id="a32b3-117">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="a32b3-118"> (Direct3D 9) 的材質定址模式 </span><span class="sxs-lookup"><span data-stu-id="a32b3-118">Texture Addressing Modes (Direct3D 9)</span></span>](texture-addressing-modes.md)
-   [<span data-ttu-id="a32b3-119"> (Direct3D 9) 的材質中途區域 </span><span class="sxs-lookup"><span data-stu-id="a32b3-119">Texture Dirty Regions (Direct3D 9)</span></span>](texture-dirty-regions.md)
-   [<span data-ttu-id="a32b3-120"> (Direct3D 9) 的材質調色板 </span><span class="sxs-lookup"><span data-stu-id="a32b3-120">Texture Palettes (Direct3D 9)</span></span>](texture-palettes.md)

## <a name="related-topics"></a><span data-ttu-id="a32b3-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="a32b3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a32b3-122">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="a32b3-122">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 



