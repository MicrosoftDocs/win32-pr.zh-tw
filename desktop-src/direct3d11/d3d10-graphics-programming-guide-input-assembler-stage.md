---
title: 輸入組合階段
description: Direct3D 10 和更新版本的 API 會將管線的功能區域與階段分開。管線中的第一個階段是輸入組合語言 (IA) 階段。
ms.assetid: 71141a5e-2d79-4b02-8370-c0cbc8618908
keywords:
- " (Direct3D 10) 的輸入組合語言階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121d98ca66bbe42f6eaa3023150203ce0538445b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383361"
---
# <a name="input-assembler-stage"></a><span data-ttu-id="8d8d9-104">輸入組合階段</span><span class="sxs-lookup"><span data-stu-id="8d8d9-104">Input-Assembler Stage</span></span>

<span data-ttu-id="8d8d9-105">Direct3D 10 和更新版本的 API 會將管線的功能區域與階段分開。管線中的第一個階段是輸入組合語言 (IA) 階段。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-105">The Direct3D 10 and higher API separates functional areas of the pipeline into stages; the first stage in the pipeline is the input-assembler (IA) stage.</span></span>

<span data-ttu-id="8d8d9-106">輸入組合語言階段的目的是要從使用者填入的緩衝區中讀取基本資料 (點、線條及/或三角形) ，然後將資料組合成其他管線階段將使用的基本專案。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-106">The purpose of the input-assembler stage is to read primitive data (points, lines and/or triangles) from user-filled buffers and assemble the data into primitives that will be used by the other pipeline stages.</span></span> <span data-ttu-id="8d8d9-107">IA 階段可以將頂組合到數個不同的[基本類型](d3d10-graphics-programming-guide-primitive-topologies.md) (例如行清單、三角形連環或相鄰基本類型)。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-107">The IA stage can assemble vertices into several different [primitive types](d3d10-graphics-programming-guide-primitive-topologies.md) (such as line lists, triangle strips, or primitives with adjacency).</span></span> <span data-ttu-id="8d8d9-108">新的基本類型 (例如具有連續的行清單，或已新增相鄰) 的三角形清單，以支援幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-108">New primitive types (such as a line list with adjacency or a triangle list with adjacency) have been added to support the geometry shader.</span></span>

<span data-ttu-id="8d8d9-109">應用程式只能在在幾何著色器中看到相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-109">Adjacency information is visible to an application only in a geometry shader.</span></span> <span data-ttu-id="8d8d9-110">如果幾何著色器已叫用包括相鄰關係的三角形，輸入資料將在每個三角形包含 3 個頂點，而每個三角形有 3 個相鄰資料頂點。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-110">If a geometry shader were invoked with a triangle including adjacency, for instance, the input data would contain 3 vertices for each triangle and 3 vertices for adjacency data per triangle.</span></span>

<span data-ttu-id="8d8d9-111">當要求輸入組合語言階段輸出相鄰資料時，輸入資料必須包含連續的資料。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-111">When the input-assembler stage is requested to output adjacency data, the input data must include adjacency data.</span></span> <span data-ttu-id="8d8d9-112">這可能需要提供假頂點 (形成變質三角形)，或可能在其中一個頂點屬性標明頂點是否存在。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-112">This may require providing a dummy vertex (forming a degenerate triangle), or perhaps by flagging in one of the vertex attributes whether the vertex exists or not.</span></span> <span data-ttu-id="8d8d9-113">這也需由幾何著色器偵測和處理，雖然在點陣化階段將會揀選變質幾何。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-113">This would also need to be detected and handled by a geometry shader, although culling of degenerate geometry will happen in the rasterizer stage.</span></span>

<span data-ttu-id="8d8d9-114">在組合基本專案時，IA 的次要用途是附加 [系統產生的值](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ，以協助著色器更有效率。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-114">While assembling primitives, a secondary purpose of the IA is to attach [system-generated values](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) to help make shaders more efficient.</span></span> <span data-ttu-id="8d8d9-115">系統產生的值為也稱為語意的文字字串。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-115">System-generated values are text strings that are also called semantics.</span></span> <span data-ttu-id="8d8d9-116">所有三個著色器階段都是從常見的著色器核心來建立，而著色器核心會使用系統產生的值 (例如基本識別碼、實例識別碼或頂點識別碼) ，因此著色器階段可以減少只處理尚未處理的基本、實例或頂點。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-116">All three shader stages are constructed from a common shader core, and the shader core uses system-generated values (such as a primitive id, an instance id, or a vertex id) so that a shader stage can reduce processing to only those primitives, instances, or vertices that have not already been processed.</span></span>

<span data-ttu-id="8d8d9-117">如 [管線區塊圖](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)所示，在 IA 階段從記憶體讀取資料之後 (將資料組合成基本專案，並將系統產生的值附加) ，資料就會輸出到 [頂點著色器階段](/previous-versions//bb205146(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-117">As shown in the [pipeline-block diagram](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages), once the IA stage reads data from memory (assembles the data into primitives and attaches system-generated values), the data is output to the [vertex shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>


## <a name="in-this-section"></a><span data-ttu-id="8d8d9-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="8d8d9-118">In this section</span></span>



| <span data-ttu-id="8d8d9-119">主題</span><span class="sxs-lookup"><span data-stu-id="8d8d9-119">Topic</span></span>                                                                                                                                   | <span data-ttu-id="8d8d9-120">描述</span><span class="sxs-lookup"><span data-stu-id="8d8d9-120">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d8d9-121">使用 Input-Assembler 階段開始使用</span><span class="sxs-lookup"><span data-stu-id="8d8d9-121">Getting Started with the Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)<br/> | <span data-ttu-id="8d8d9-122">有幾個步驟需要初始化輸入組合語言 (IA) 階段。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-122">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="8d8d9-123">例如，您需要使用管線所需的頂點資料來建立緩衝區資源、告知 IA 階段，其中緩衝區是和它們所包含的資料類型，並指定要從資料組合的基本類型。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-123">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span><br/> |
| [<span data-ttu-id="8d8d9-124">基本拓撲</span><span class="sxs-lookup"><span data-stu-id="8d8d9-124">Primitive Topologies</span></span>](d3d10-graphics-programming-guide-primitive-topologies.md)<br/>                                            | <span data-ttu-id="8d8d9-125">Direct3D 10 和更新版本支援數個基本類型 (或以 [**D3D \_ 基本 \_ 拓撲**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) 列舉類型表示的拓撲) 。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-125">Direct3D 10 and higher supports several primitive types (or topologies) that are represented by the [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) enumerated type.</span></span> <span data-ttu-id="8d8d9-126">這些類型會定義管線如何轉譯和呈現頂點。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-126">These types define how vertices are interpreted and rendered by the pipeline.</span></span><br/>                                                          |
| [<span data-ttu-id="8d8d9-127">使用不含緩衝區的 Input-Assembler 階段</span><span class="sxs-lookup"><span data-stu-id="8d8d9-127">Using the Input-Assembler Stage without Buffers</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md)<br/>     | <span data-ttu-id="8d8d9-128">如果您的著色器不需要緩衝區，則不需要建立和系結緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-128">Creating and binding buffers is not necessary if your shaders don't require buffers.</span></span> <span data-ttu-id="8d8d9-129">本節包含繪製單一三角形的簡單頂點和圖元著色器範例。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-129">This section contains an example of simple vertex and pixel shaders that draw a single triangle.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="8d8d9-130">使用 System-Generated 值</span><span class="sxs-lookup"><span data-stu-id="8d8d9-130">Using System-Generated Values</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-using.md)<br/>                            | <span data-ttu-id="8d8d9-131">根據使用者提供的輸入 [語義](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) ，IA 階段會產生系統產生的值 (，) 以允許著色器作業中有某些效率。</span><span class="sxs-lookup"><span data-stu-id="8d8d9-131">System-generated values are generated by the IA stage (based on user-supplied input [semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) to allow certain efficiencies in shader operations.</span></span> <br/>                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="8d8d9-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d8d9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d8d9-133">圖形管線</span><span class="sxs-lookup"><span data-stu-id="8d8d9-133">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="8d8d9-134"> (Direct3D 10) 的管線階段 </span><span class="sxs-lookup"><span data-stu-id="8d8d9-134">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

