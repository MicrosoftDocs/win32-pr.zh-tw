---
description: 在轉譯期間，管線會在每個矩形上插入頂點資料。
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: " (Direct3D 9) 的三角形插補"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972952"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="2db02-103"> (Direct3D 9) 的三角形插補</span><span class="sxs-lookup"><span data-stu-id="2db02-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="2db02-104">在轉譯期間，管線會在每個矩形上插入頂點資料。</span><span class="sxs-lookup"><span data-stu-id="2db02-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="2db02-105">頂點資料可以是各種不同的資料，而且可以包含 (但不限於) ：擴散色彩、反射色彩、擴散 Alpha (三角形不透明度) 、反射 Alpha 和霧化因數 (取自固定函式頂點管線的反射 Alpha，以及可程式化頂點管線) 的霧化暫存器。</span><span class="sxs-lookup"><span data-stu-id="2db02-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="2db02-106">頂點資料是由 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告所定義。</span><span class="sxs-lookup"><span data-stu-id="2db02-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="2db02-107">某些頂點資料的插補取決於目前的陰影模式，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="2db02-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="2db02-108">陰影模式</span><span class="sxs-lookup"><span data-stu-id="2db02-108">Shading mode</span></span> | <span data-ttu-id="2db02-109">Description</span><span class="sxs-lookup"><span data-stu-id="2db02-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db02-110">一般</span><span class="sxs-lookup"><span data-stu-id="2db02-110">Flat</span></span>         | <span data-ttu-id="2db02-111">在平面陰影模式下，只內插霧因數。</span><span class="sxs-lookup"><span data-stu-id="2db02-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="2db02-112">對於所有其他內插補值，三角形中第一個頂點的色彩會套用到整個面。</span><span class="sxs-lookup"><span data-stu-id="2db02-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="2db02-113">Gouraud</span><span class="sxs-lookup"><span data-stu-id="2db02-113">Gouraud</span></span>      | <span data-ttu-id="2db02-114">在所有三個頂點之間執行線性內插補點。</span><span class="sxs-lookup"><span data-stu-id="2db02-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="2db02-115">擴散色彩和反射色彩的處理方式不同，視色彩模型而定。</span><span class="sxs-lookup"><span data-stu-id="2db02-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="2db02-116">在 RGB 色彩模型，系統會在內插補點中使用紅色、綠色和藍色元件。</span><span class="sxs-lookup"><span data-stu-id="2db02-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="2db02-117">色彩的 Alpha 元件被視為不同的內插補值，因為裝置驅動程式可透過兩種不同方式實作透明度：使用紋理混合或使用點畫。</span><span class="sxs-lookup"><span data-stu-id="2db02-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="2db02-118">使用 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 ShadeCaps 成員，判斷目前設備磁碟機支援的插補形式。</span><span class="sxs-lookup"><span data-stu-id="2db02-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2db02-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="2db02-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db02-120">座標系統和幾何</span><span class="sxs-lookup"><span data-stu-id="2db02-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



