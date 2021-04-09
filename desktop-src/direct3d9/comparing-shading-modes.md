---
description: 在平面陰影模式中，會顯示下列金字塔與相鄰臉部之間的尖邊緣。 不過，在 Gouraud 網底模式中，會在邊緣插入網底值，最後的外觀會是曲線表面。
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: 比較 (Direct3D 9) 的陰影模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111661"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="95949-104">比較 (Direct3D 9) 的陰影模式</span><span class="sxs-lookup"><span data-stu-id="95949-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="95949-105">在平面陰影模式中，會顯示下列金字塔與相鄰臉部之間的尖邊緣。</span><span class="sxs-lookup"><span data-stu-id="95949-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="95949-106">不過，在 Gouraud 網底模式中，會在邊緣插入網底值，最後的外觀會是曲線表面。</span><span class="sxs-lookup"><span data-stu-id="95949-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![金字塔的圖，其中包含指向臉部法線的尖邊和箭號](images/shade2.png)

<span data-ttu-id="95949-108">Gouraud 陰影燈的平面表面比一般陰影更真實。</span><span class="sxs-lookup"><span data-stu-id="95949-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="95949-109">一般陰影模式中的臉部是一致的色彩，但 Gouraud 陰影可讓光線更正確地落在表面上。</span><span class="sxs-lookup"><span data-stu-id="95949-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="95949-110">如果有鄰近的點來源，此效果特別明顯。</span><span class="sxs-lookup"><span data-stu-id="95949-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="95949-111">Gouraud 陰影會平滑化多邊形之間的尖邊（以平面陰影顯示）。</span><span class="sxs-lookup"><span data-stu-id="95949-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="95949-112">不過，它可能會導致符合的波段，也就是不會在相鄰多邊形間順暢地混合的色彩或淺色的區段。</span><span class="sxs-lookup"><span data-stu-id="95949-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="95949-113">您的應用程式可以藉由增加物件中的多邊形數目、增加螢幕解析度或增加應用程式的色彩深度，來減少符合區的外觀。</span><span class="sxs-lookup"><span data-stu-id="95949-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="95949-114">Gouraud 陰影可能會遺漏一些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="95949-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="95949-115">例如，在下圖中，焦點會完全包含在多邊形臉部內。</span><span class="sxs-lookup"><span data-stu-id="95949-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![多邊形臉部內的焦點圖例](images/gouraud.png)

<span data-ttu-id="95949-117">在此情況下，Gouraud 陰影會在頂點之間進行插補，這會完全遺漏焦點;臉部會轉譯成焦點不存在。</span><span class="sxs-lookup"><span data-stu-id="95949-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95949-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="95949-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95949-119">陰影</span><span class="sxs-lookup"><span data-stu-id="95949-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



