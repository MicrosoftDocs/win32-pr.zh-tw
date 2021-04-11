---
description: 凹凸對應是一種特殊形式的反射或擴散環境對應，可模擬精確鑲嵌物件的反映，而不需要極高的多邊形計數。
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: " (Direct3D 9) 的凹凸對應"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111273"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="0a378-103"> (Direct3D 9) 的凹凸對應</span><span class="sxs-lookup"><span data-stu-id="0a378-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="0a378-104">凹凸對應是一種特殊形式的反射或擴散環境對應，可模擬精確鑲嵌物件的反映，而不需要極高的多邊形計數。</span><span class="sxs-lookup"><span data-stu-id="0a378-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="0a378-105">Direct3D 所執行的自動調整對應可以精確描述為反射或擴散環境對應的每個圖元材質座標更動，因為您會在差異值方面提供有關放大圖分佈的資訊，而系統會將該值套用至下一個材質階段中環境對應的您和 v 材質座標。</span><span class="sxs-lookup"><span data-stu-id="0a378-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="0a378-106">Delta 值是以 [凹凸地圖介面] 的像素格式來編碼 (請參閱 [放大 [地圖像素格式](bump-map-pixel-formats.md) ]) 。</span><span class="sxs-lookup"><span data-stu-id="0a378-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="0a378-107">凹凸對應依賴于混合多重紋理。</span><span class="sxs-lookup"><span data-stu-id="0a378-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="0a378-108">這表示裝置必須至少支援兩個混合階段;一個用於凹凸地圖，另一個用於環境對應。</span><span class="sxs-lookup"><span data-stu-id="0a378-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="0a378-109">至少需要三個材質混合階段，才能套用額外的基底材質圖，也就是最常見的情況。</span><span class="sxs-lookup"><span data-stu-id="0a378-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="0a378-110">下圖顯示材質混合串聯中的基底材質、凹凸地圖和環境地圖之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="0a378-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![材質混色 cascade 的圖表](images/bumpmap-tcascade.png)

<span data-ttu-id="0a378-112">您必須適當地備妥紋理階段，才能啟用凹凸對應。</span><span class="sxs-lookup"><span data-stu-id="0a378-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="0a378-113">下列主題將介紹「進行」對應，並提供如何在應用程式中使用它的詳細資料：</span><span class="sxs-lookup"><span data-stu-id="0a378-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="0a378-114">凹凸地圖像素格式</span><span class="sxs-lookup"><span data-stu-id="0a378-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="0a378-115">凹凸對應公式</span><span class="sxs-lookup"><span data-stu-id="0a378-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="0a378-116">使用凹凸對應</span><span class="sxs-lookup"><span data-stu-id="0a378-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="0a378-117">Direct3D 原本就不支援高度對應;它們只是方便的格式，可用於儲存和視覺化分佈資料。</span><span class="sxs-lookup"><span data-stu-id="0a378-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="0a378-118">您的應用程式可以儲存任何格式的輪廓資訊，甚至產生程式性的放大地圖。</span><span class="sxs-lookup"><span data-stu-id="0a378-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a378-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a378-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a378-120">圖元管線</span><span class="sxs-lookup"><span data-stu-id="0a378-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



