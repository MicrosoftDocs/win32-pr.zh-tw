---
description: Direct3D 9 支援點、線條、三角形和方格基本專案。
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: " (Direct3D 9 的 Higher-Order 基本) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67767dd955fa5c0c5c21315d7c1c510de422870c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687459"
---
# <a name="higher-order-primitives-direct3d-9"></a><span data-ttu-id="5e946-103"> (Direct3D 9 的 Higher-Order 基本) </span><span class="sxs-lookup"><span data-stu-id="5e946-103">Higher-Order Primitives (Direct3D 9)</span></span>

<span data-ttu-id="5e946-104">Direct3D 9 支援點、線條、三角形和方格基本專案。</span><span class="sxs-lookup"><span data-stu-id="5e946-104">Direct3D 9 supports points, lines, triangles, and grid primitives.</span></span> <span data-ttu-id="5e946-105">這些已擴充，可支援高序位的插補超過線性。</span><span class="sxs-lookup"><span data-stu-id="5e946-105">These have been extended to support higher-order interpolation beyond linear.</span></span> <span data-ttu-id="5e946-106">雖然三角形和線條具有空間範圍，但是現在它們都是使用線性插補來呈現。</span><span class="sxs-lookup"><span data-stu-id="5e946-106">While triangles and lines have spatial extent, until now they were both rendered using linear interpolation.</span></span> <span data-ttu-id="5e946-107">在 Direct3D 9 中，Direct3D 支援使用較高的順序（最多 quintic 的插補）來轉譯這些基本類型。</span><span class="sxs-lookup"><span data-stu-id="5e946-107">In Direct3D 9, Direct3D supports rendering of these primitive types using higher order, up to quintic, interpolation.</span></span> <span data-ttu-id="5e946-108">此外，現在支援新的四基本類型。</span><span class="sxs-lookup"><span data-stu-id="5e946-108">Furthermore, a new quad primitive type is now supported.</span></span> <span data-ttu-id="5e946-109">這個新類型也可以使用較高順序的插補來呈現。</span><span class="sxs-lookup"><span data-stu-id="5e946-109">This new type can also be rendered with higher-order interpolation.</span></span> <span data-ttu-id="5e946-110">這項功能主要是由動畫和字元轉譯的需求所驅動。</span><span class="sxs-lookup"><span data-stu-id="5e946-110">This feature is primarily driven by requirements for animation and rendering of characters.</span></span> <span data-ttu-id="5e946-111">也可用於其他表面，例如地形或水。</span><span class="sxs-lookup"><span data-stu-id="5e946-111">It can also be used for other surfaces such as terrain or water.</span></span>

<span data-ttu-id="5e946-112">當您以清單、帶狀、風扇或索引網格形式傳送至 API 時，較高順序的基本專案支援高序位的插補。</span><span class="sxs-lookup"><span data-stu-id="5e946-112">Higher-order primitives support higher-order interpolation when transmitted to the API as lists, strips, fans, or indexed meshes.</span></span> <span data-ttu-id="5e946-113">您可以使用在頂點本身編碼的額外資訊來達成這個目的。</span><span class="sxs-lookup"><span data-stu-id="5e946-113">This is achieved by using additional information encoded in the vertices themselves.</span></span> <span data-ttu-id="5e946-114">例如，一般向量可以用來定義頂點的正切平面，以啟用三次插補。</span><span class="sxs-lookup"><span data-stu-id="5e946-114">For example, normal vectors can be used to define tangent planes at the vertices to enable cubic interpolation.</span></span> <span data-ttu-id="5e946-115">大部分的實作為以鑲嵌為平面三角形的方式支援高階插補。</span><span class="sxs-lookup"><span data-stu-id="5e946-115">Most implementations support higher-order interpolation by tessellation into planar triangles.</span></span> <span data-ttu-id="5e946-116">鑲嵌式步驟會以邏輯方式在頂點著色器階段之前套用。</span><span class="sxs-lookup"><span data-stu-id="5e946-116">The tessellation step is applied logically before the vertex shader stage.</span></span> <span data-ttu-id="5e946-117">因為頂點著色器 API 不會在其輸入資料上強加語義，所以會提供特殊機制來識別代表位置的頂點資料流程元件，並選擇性地識別一般向量。</span><span class="sxs-lookup"><span data-stu-id="5e946-117">Because the vertex shader API does not impose semantics on its input data, a special mechanism is provided to identify the vertex stream component that represents the position, and optionally the normal vector.</span></span> <span data-ttu-id="5e946-118">所有其他元件則會據以插補。</span><span class="sxs-lookup"><span data-stu-id="5e946-118">All other components are interpolated accordingly.</span></span>

<span data-ttu-id="5e946-119">本節介紹高階的基本專案，並討論如何在應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="5e946-119">This section introduces higher-order primitives and discusses how they can be used in your applications.</span></span> <span data-ttu-id="5e946-120">資訊分成下列主題。</span><span class="sxs-lookup"><span data-stu-id="5e946-120">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="5e946-121">透過解析度增強功能改善品質</span><span class="sxs-lookup"><span data-stu-id="5e946-121">Improved Quality through Resolution Enhancement</span></span>](#improved-quality-through-resolution-enhancement)
-   [<span data-ttu-id="5e946-122">Spline-Based 工具的直接對應</span><span class="sxs-lookup"><span data-stu-id="5e946-122">Direct Mapping from Spline-Based Tools</span></span>](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a><span data-ttu-id="5e946-123">透過解析度增強功能改善品質</span><span class="sxs-lookup"><span data-stu-id="5e946-123">Improved Quality through Resolution Enhancement</span></span>

<span data-ttu-id="5e946-124">目前的基本專案不適合用來表示平滑表面。</span><span class="sxs-lookup"><span data-stu-id="5e946-124">Current primitives are not ideal for representing smooth surfaces.</span></span> <span data-ttu-id="5e946-125">較高順序的插補方法（例如立方 polynomials）允許更精確的計算呈現曲線形狀。</span><span class="sxs-lookup"><span data-stu-id="5e946-125">Higher-order interpolation methods, such as cubic polynomials, allow more accurate calculations in rendering curved shapes.</span></span> <span data-ttu-id="5e946-126">藉由減少或消除在側面剪影邊緣或反射表面光源上可見的 facet 構件，可提供更高的真實性。</span><span class="sxs-lookup"><span data-stu-id="5e946-126">This provides increased realism by reducing or eliminating faceting artifacts visible on silhouette edges or on specular surface lighting.</span></span> <span data-ttu-id="5e946-127">此外，在晶片上進行鑲嵌時，鑲嵌三角形不會影響匯流排頻寬。</span><span class="sxs-lookup"><span data-stu-id="5e946-127">Furthermore, when tessellation occurs on the chip, the tessellated triangles do not impact the bus bandwidth.</span></span> <span data-ttu-id="5e946-128">在許多情況下，少量鑲嵌可提供映射品質的改進，並對效能造成最小的影響。</span><span class="sxs-lookup"><span data-stu-id="5e946-128">In many cases, a small amount of tessellation can provide improvements in image quality with minimal performance impact.</span></span>

<span data-ttu-id="5e946-129">Direct3D 9 提供簡單的方法，讓您將解析度增強功能套用至現有的多邊形導向工具和藝術管線所建立的內容。</span><span class="sxs-lookup"><span data-stu-id="5e946-129">Direct3D 9 provides a simple way to apply resolution enhancement to content created by existing polygon-oriented tools and art pipelines.</span></span> <span data-ttu-id="5e946-130">應用程式只需要提供所需的鑲嵌層級，並使用包含一般向量的標準三角形語法來傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="5e946-130">The application need only provide a desired level of tessellation, and transmit the data using standard triangle syntax that includes normal vectors.</span></span>

## <a name="direct-mapping-from-spline-based-tools"></a><span data-ttu-id="5e946-131">Spline-Based 工具的直接對應</span><span class="sxs-lookup"><span data-stu-id="5e946-131">Direct Mapping from Spline-Based Tools</span></span>

<span data-ttu-id="5e946-132">許多目前的撰寫工具都支援較高順序的基本專案，以啟用比一般提供的平面三角形網格更強大的模型作業。</span><span class="sxs-lookup"><span data-stu-id="5e946-132">Many current authoring tools support higher-order primitives to enable more powerful modeling operations than are commonly provided for with planar triangle meshes.</span></span> <span data-ttu-id="5e946-133">當有效率地使用時，可讓產生的修補程式數目合理，這類工具可以產生可直接由 API 轉譯的內容。</span><span class="sxs-lookup"><span data-stu-id="5e946-133">When used efficiently, so that the number of patches generated is reasonable, such tools can produce content that can be rendered directly by the API.</span></span> <span data-ttu-id="5e946-134">為了滿足這項需求，已加入新的進入點，可將傳入的頂點資料流程視為控制點的2D 陣列，並 tessellates 為所需的解析度。</span><span class="sxs-lookup"><span data-stu-id="5e946-134">To meet this requirement, a new entry point has been added that interprets the incoming vertex data stream as a 2D array of control points and tessellates it to the desired resolution.</span></span>

-   [<span data-ttu-id="5e946-135">使用 Higher-Order 基本 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="5e946-135">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)

## <a name="related-topics"></a><span data-ttu-id="5e946-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e946-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e946-137">頂點管線</span><span class="sxs-lookup"><span data-stu-id="5e946-137">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



