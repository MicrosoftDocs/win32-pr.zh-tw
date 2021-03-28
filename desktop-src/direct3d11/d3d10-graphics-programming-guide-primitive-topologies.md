---
title: 基本拓撲
description: Direct3D 10 和更新版本支援數個基本類型 (或以 D3D \_ 基本拓撲列舉類型表示的拓撲) \_ 。 這些類型會定義管線如何轉譯和呈現頂點。
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315217"
---
# <a name="primitive-topologies"></a><span data-ttu-id="2d1b0-104">基本拓撲</span><span class="sxs-lookup"><span data-stu-id="2d1b0-104">Primitive Topologies</span></span>

<span data-ttu-id="2d1b0-105">Direct3D 10 和更新版本支援數個基本類型 (或以 [**D3D \_ 基本 \_ 拓撲**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) 列舉類型表示的拓撲) 。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-105">Direct3D 10 and higher supports several primitive types (or topologies) that are represented by the [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) enumerated type.</span></span> <span data-ttu-id="2d1b0-106">這些類型會定義管線如何轉譯和呈現頂點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-106">These types define how vertices are interpreted and rendered by the pipeline.</span></span>

-   [<span data-ttu-id="2d1b0-107">基本基本類型</span><span class="sxs-lookup"><span data-stu-id="2d1b0-107">Basic Primitive Types</span></span>](#basic-primitive-types)
-   [<span data-ttu-id="2d1b0-108">基本相鄰</span><span class="sxs-lookup"><span data-stu-id="2d1b0-108">Primitive Adjacency</span></span>](#primitive-adjacency)
-   [<span data-ttu-id="2d1b0-109">纏繞方向和前置頂點位置</span><span class="sxs-lookup"><span data-stu-id="2d1b0-109">Winding Direction and Leading Vertex Positions</span></span>](#winding-direction-and-leading-vertex-positions)
-   [<span data-ttu-id="2d1b0-110">產生多個停車線</span><span class="sxs-lookup"><span data-stu-id="2d1b0-110">Generating Multiple Strips</span></span>](#generating-multiple-strips)
-   [<span data-ttu-id="2d1b0-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d1b0-111">Related topics</span></span>](#related-topics)

## <a name="basic-primitive-types"></a><span data-ttu-id="2d1b0-112">基本基本類型</span><span class="sxs-lookup"><span data-stu-id="2d1b0-112">Basic Primitive Types</span></span>

<span data-ttu-id="2d1b0-113">以下是支援的基本基本類型：</span><span class="sxs-lookup"><span data-stu-id="2d1b0-113">The following basic primitive types are supported:</span></span>

-   [<span data-ttu-id="2d1b0-114">點清單</span><span class="sxs-lookup"><span data-stu-id="2d1b0-114">Point List</span></span>](/windows/desktop/direct3d9/point-lists)
-   [<span data-ttu-id="2d1b0-115">行清單</span><span class="sxs-lookup"><span data-stu-id="2d1b0-115">Line List</span></span>](/windows/desktop/direct3d9/line-lists)
-   [<span data-ttu-id="2d1b0-116">行帶</span><span class="sxs-lookup"><span data-stu-id="2d1b0-116">Line Strip</span></span>](/windows/desktop/direct3d9/line-strips)
-   [<span data-ttu-id="2d1b0-117">三角形清單</span><span class="sxs-lookup"><span data-stu-id="2d1b0-117">Triangle List</span></span>](/windows/desktop/direct3d9/triangle-lists)
-   [<span data-ttu-id="2d1b0-118">邊帶</span><span class="sxs-lookup"><span data-stu-id="2d1b0-118">Triange Strip</span></span>](/windows/desktop/direct3d9/triangle-strips)

<span data-ttu-id="2d1b0-119">如需每個基本類型的視覺效果，請參閱本主題稍後的 [纏繞方向和前置頂點位置](#winding-direction-and-leading-vertex-positions)的圖表。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-119">For a visualization of each primitive type, see the diagram later in this topic in [Winding Direction and Leading Vertex Positions](#winding-direction-and-leading-vertex-positions).</span></span>

<span data-ttu-id="2d1b0-120">輸入組合語言階段會從頂點和索引緩衝區讀取資料、將資料組合成這些基本專案，然後將資料傳送至其餘的管線階段。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-120">The input-assembler stage reads data from vertex and index buffers, assembles the data into these primitives, and then sends the data to the remaining pipeline stages.</span></span> <span data-ttu-id="2d1b0-121"> (您可以使用 [**>id3d11devicecoNtext：： IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) 方法來指定輸入組合語言階段的基本類型。 ) </span><span class="sxs-lookup"><span data-stu-id="2d1b0-121">(You can use the [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) method to specify the primitive type for the input-assembler stage.)</span></span>

## <a name="primitive-adjacency"></a><span data-ttu-id="2d1b0-122">基本相鄰</span><span class="sxs-lookup"><span data-stu-id="2d1b0-122">Primitive Adjacency</span></span>

<span data-ttu-id="2d1b0-123">除了點清單) 之外，所有 Direct3D 10 和更高的基本型別 (都有兩個版本：一個具有連續的基本型別，以及一個不連續的基本類型。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-123">All Direct3D 10 and higher primitive types (except the point list) are available in two versions: one primitive type with adjacency and one primitive type without adjacency.</span></span> <span data-ttu-id="2d1b0-124">具有相鄰關係的基本類型包含一些周圍頂點，而不具相鄰關係的基本類型僅包含目標基本類型的頂點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-124">Primitives with adjacency contain some of the surrounding vertices, while primitives without adjacency contain only the vertices of the target primitive.</span></span> <span data-ttu-id="2d1b0-125">例如，「 **d3d \_ 基本 \_ 拓撲 \_ LINELIST** 值代表的行清單基本 () 具有對應的行清單原始物件，其中包含 **d3d \_ 基本 \_ 拓撲 \_ LINELIST \_** 調整值所代表的相鄰 (。 ) </span><span class="sxs-lookup"><span data-stu-id="2d1b0-125">For example, the line list primitive (represented by the **D3D\_PRIMITIVE\_TOPOLOGY\_LINELIST** value) has a corresponding line list primitive that includes adjacency (represented by the **D3D\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ** value.)</span></span>

<span data-ttu-id="2d1b0-126">相鄰基本類型旨在提供您更多幾何的相關資訊，並僅透過幾何著色器顯示。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-126">Adjacent primitives are intended to provide more information about your geometry and are only visible through a geometry shader.</span></span> <span data-ttu-id="2d1b0-127">相鄰關係適用於使用剪影偵測、陰影磁碟區立體化等的幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-127">Adjacency is useful for geometry shaders that use silhouette detection, shadow volume extrusion, and so on.</span></span>

<span data-ttu-id="2d1b0-128">例如，假設您想要繪圖具有相鄰關係的三角形清單。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-128">For example, suppose you want to draw a triangle list with adjacency.</span></span> <span data-ttu-id="2d1b0-129">包含 36 個頂點 (具有相鄰關係) 的三角形清單將產生 6 個已完成的基本類型。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-129">A triangle list that contains 36 vertices (with adjacency) will yield 6 completed primitives.</span></span> <span data-ttu-id="2d1b0-130">具相鄰關係的基本類型 (帶狀線除外) 包含的頂點數是不具相鄰關係的同等基本類型正好兩倍，其中每個額外的頂點是相鄰的頂點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-130">Primitives with adjacency (except line strips) contain exactly twice as many vertices as the equivalent primitive without adjacency, where each additional vertex is an adjacent vertex.</span></span>

## <a name="winding-direction-and-leading-vertex-positions"></a><span data-ttu-id="2d1b0-131">纏繞方向和前置頂點位置</span><span class="sxs-lookup"><span data-stu-id="2d1b0-131">Winding Direction and Leading Vertex Positions</span></span>

<span data-ttu-id="2d1b0-132">如下圖所示，前置頂點是基本類型中的第一個非相鄰頂點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-132">As shown in the following illustration, a leading vertex is the first non-adjacent vertex in a primitive.</span></span> <span data-ttu-id="2d1b0-133">基本類型可讓多個前置頂點經過定義，只要每個前置頂點是用於不同基本類型。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-133">A primitive type can have multiple leading vertices defined, as long as each one is used for a different primitive.</span></span> <span data-ttu-id="2d1b0-134">具相鄰關係三角形連環，前置頂點是 0、2、4、6 等。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-134">For a triangle strip with adjacency, the leading vertices are 0, 2, 4, 6, and so on.</span></span> <span data-ttu-id="2d1b0-135">具相鄰關係的帶狀線，前置頂點是 1、2、3 等。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-135">For a line strip with adjacency, the leading vertices are 1, 2, 3, and so on.</span></span> <span data-ttu-id="2d1b0-136">換句話說，相鄰基本類型沒有前置頂點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-136">An adjacent primitive, on the other hand, has no leading vertex.</span></span>

<span data-ttu-id="2d1b0-137">下圖顯示可產生輸入組合語言的所有基本類型的頂點排序。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-137">The following illustration shows the vertex ordering for all of the primitive types that the input assembler can produce.</span></span>

![基本類型頂點排序圖表](images/d3d10-primitive-topologies.png)

<span data-ttu-id="2d1b0-139">前述圖中的符號在下表中說明。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-139">The symbols in the preceding illustration are described in the following table.</span></span>



| <span data-ttu-id="2d1b0-140">符號</span><span class="sxs-lookup"><span data-stu-id="2d1b0-140">Symbol</span></span>                                                                                   | <span data-ttu-id="2d1b0-141">名稱</span><span class="sxs-lookup"><span data-stu-id="2d1b0-141">Name</span></span>              | <span data-ttu-id="2d1b0-142">描述</span><span class="sxs-lookup"><span data-stu-id="2d1b0-142">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![頂點符號](images/d3d10-primitive-topologies-vertex.png)                     | <span data-ttu-id="2d1b0-144">頂點</span><span class="sxs-lookup"><span data-stu-id="2d1b0-144">Vertex</span></span>            | <span data-ttu-id="2d1b0-145">3D 空間中的點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-145">A point in 3D space.</span></span>                                                                                                                                                                               |
| ![線圈方向的符號](images/d3d10-primitive-topologies-winding-direction.png) | <span data-ttu-id="2d1b0-147">線圈方向</span><span class="sxs-lookup"><span data-stu-id="2d1b0-147">Winding Direction</span></span> | <span data-ttu-id="2d1b0-148">組合基本類型時的頂點排序。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-148">The vertex order when assembling a primitive.</span></span> <span data-ttu-id="2d1b0-149">可以順時針或逆時針;藉由呼叫 [**ID3D11Device1：： CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)來指定此項。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-149">Can be clockwise or counterclockwise; specify this by calling [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1).</span></span> |
| ![前置頂點的符號](images/d3d10-primitive-topologies-leading-vertex.png)       | <span data-ttu-id="2d1b0-151">前置頂點</span><span class="sxs-lookup"><span data-stu-id="2d1b0-151">Leading Vertex</span></span>    | <span data-ttu-id="2d1b0-152">包含每個常數資料的基本類型中的第一非相鄰頂點。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-152">The first non-adjacent vertex in a primitive that contains per-constant data.</span></span>                                                                                                                      |



 

## <a name="generating-multiple-strips"></a><span data-ttu-id="2d1b0-153">產生多個停車線</span><span class="sxs-lookup"><span data-stu-id="2d1b0-153">Generating Multiple Strips</span></span>

<span data-ttu-id="2d1b0-154">您可以透過寬帶切割產生多條寬帶。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-154">You can generate multiple strips through strip cutting.</span></span> <span data-ttu-id="2d1b0-155">您可以明確呼叫 [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL 函式或將特殊索引值插入索引緩衝區，來執行寬帶切割。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-155">You can perform a strip cut by explicitly calling the [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL function, or by inserting a special index value into the index buffer.</span></span> <span data-ttu-id="2d1b0-156">這個值是 –1，32 位元索引是 0xffffffff 或 16 位元索引是 0xffff。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-156">This value is –1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices.</span></span> <span data-ttu-id="2d1b0-157">–1 的索引表示明確「剪下」或」重新啟動」目前的寬帶。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-157">An index of –1 indicates an explicit 'cut' or 'restart' of the current strip.</span></span> <span data-ttu-id="2d1b0-158">上一個索引完成上一個基本類型或寬帶，而下一個索引開始新的基本類型或寬帶。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-158">The previous index completes the previous primitive or strip and the next index starts a new primitive or strip.</span></span> <span data-ttu-id="2d1b0-159">如需產生多個停車線的詳細資訊，請參閱 [幾何著色器階段](/previous-versions//bb205146(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-159">For more info about generating multiple strips, see [Geometry-Shader Stage](/previous-versions//bb205146(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="2d1b0-160">您需要 [功能等級](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 或更高的硬體，因為並非所有10level9 硬體都能實行這項功能。</span><span class="sxs-lookup"><span data-stu-id="2d1b0-160">You need [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 or higher hardware because not all 10level9 hardware implements this functionality.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2d1b0-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d1b0-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d1b0-162">使用 Input-Assembler 階段開始使用</span><span class="sxs-lookup"><span data-stu-id="2d1b0-162">Getting Started with the Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[<span data-ttu-id="2d1b0-163"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="2d1b0-163">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 