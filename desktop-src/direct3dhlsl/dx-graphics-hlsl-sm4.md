---
title: 著色器模型4
description: 著色器模型4是著色器模型3中功能的超集合，不同之處在于著色器模型4不支援著色器模型1中的功能。
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374266"
---
# <a name="shader-model-4"></a><span data-ttu-id="15a4b-103">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="15a4b-103">Shader Model 4</span></span>

<span data-ttu-id="15a4b-104">著色器模型4是 [著色器模型 3](dx-graphics-hlsl-sm3.md)中功能的超集合，不同之處在于著色器模型4不支援著色器模型1中的功能。</span><span class="sxs-lookup"><span data-stu-id="15a4b-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="15a4b-105">它是使用通用著色器核心所設計，可提供一組通用的功能給所有可程式化的著色器，這些著色器只能使用 HLSL 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="15a4b-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15a4b-106">功能</span><span class="sxs-lookup"><span data-stu-id="15a4b-106">Feature</span></span></th>
<th><span data-ttu-id="15a4b-107">功能</span><span class="sxs-lookup"><span data-stu-id="15a4b-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15a4b-108">指令集</span><span class="sxs-lookup"><span data-stu-id="15a4b-108">Instruction Set</span></span></td>
<td><span data-ttu-id="15a4b-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL 函式</strong></a></span><span class="sxs-lookup"><span data-stu-id="15a4b-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15a4b-110">註冊集</span><span class="sxs-lookup"><span data-stu-id="15a4b-110">Register Set</span></span></td>
<td><span data-ttu-id="15a4b-111">您可以使用 HLSL 語義（例如元件封裝），透過常數和材質緩衝區中的成員來存取暫存器集。</span><span class="sxs-lookup"><span data-stu-id="15a4b-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="15a4b-112">圖元著色器暫存器 (請參閱暫存器 <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">-ps_4_0</a> 和暫存器 <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">-ps_4_1</a>) </span><span class="sxs-lookup"><span data-stu-id="15a4b-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="15a4b-113">頂點著色器暫存器 (請參閱暫存器 <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">-vs_4_0</a> 和暫存器 <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">-vs_4_1</a>) </span><span class="sxs-lookup"><span data-stu-id="15a4b-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="15a4b-114">幾何著色器暫存器 (查看暫存器 <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">-gs_4_0</a> 和暫存器 <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">-gs_4_1</a>) </span><span class="sxs-lookup"><span data-stu-id="15a4b-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15a4b-115">頂點著色器最大值</span><span class="sxs-lookup"><span data-stu-id="15a4b-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="15a4b-116">沒有限制</span><span class="sxs-lookup"><span data-stu-id="15a4b-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15a4b-117">圖元著色器最大值</span><span class="sxs-lookup"><span data-stu-id="15a4b-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="15a4b-118">沒有限制</span><span class="sxs-lookup"><span data-stu-id="15a4b-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15a4b-119">新增著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="15a4b-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="15a4b-120">gs_4_0、ps_4_0、vs_4_0、gs_4_1 *、ps_4_1*、gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="15a4b-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15a4b-121">已新增新的 Effect-Framework 設定檔</span><span class="sxs-lookup"><span data-stu-id="15a4b-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="15a4b-122">fx_4_0，fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="15a4b-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15a4b-123">\*\_ \_ \_ \_ \_ \_ \_ \_ 在 Direct3D 10.1 或更高版本上，支援 gs 4 1、ps 4 1、vs 4 1 和 fx 4 1。</span><span class="sxs-lookup"><span data-stu-id="15a4b-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="15a4b-124">著色器模型4支援新的管線階段（幾何著色器階段），可用來建立或修改現有的幾何。</span><span class="sxs-lookup"><span data-stu-id="15a4b-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="15a4b-125">它也包含兩個新的物件類型：資料流程輸出物件的設計目的是要從幾何階段串流資料，以及實作為紋理取樣函數的樣板化紋理物件。</span><span class="sxs-lookup"><span data-stu-id="15a4b-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="15a4b-126">一般著色器核心</span><span class="sxs-lookup"><span data-stu-id="15a4b-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="15a4b-127">常數</span><span class="sxs-lookup"><span data-stu-id="15a4b-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="15a4b-128">Geometry-著色器物件</span><span class="sxs-lookup"><span data-stu-id="15a4b-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="15a4b-129">資料流程輸出物件</span><span class="sxs-lookup"><span data-stu-id="15a4b-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="15a4b-130">材質物件</span><span class="sxs-lookup"><span data-stu-id="15a4b-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="15a4b-131">著色器模型4支援封裝規則，這些規則會規定資料儲存時如何排列緊密的資料。</span><span class="sxs-lookup"><span data-stu-id="15a4b-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="15a4b-132">[常數變數的封裝規則](dx-graphics-hlsl-packing-rules.md)中描述這些規則</span><span class="sxs-lookup"><span data-stu-id="15a4b-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="15a4b-133">[著色器模型4元件](dx-graphics-hlsl-sm4-asm.md)一節描述著色器模型4和著色器模型4.1 支援的元件指示。</span><span class="sxs-lookup"><span data-stu-id="15a4b-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15a4b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="15a4b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15a4b-135">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="15a4b-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




