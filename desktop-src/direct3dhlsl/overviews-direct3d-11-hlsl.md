---
title: HLSL 著色器模型5
description: HLSL 著色器模型5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842428"
---
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="f3cfc-103">HLSL 著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f3cfc-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="f3cfc-104">本章節包含 High-Level 著色器語言的總覽內容，特別是在 Microsoft Direct3D 11 引進的著色器模型5中的新功能。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3cfc-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f3cfc-105">In This Section</span></span>



| <span data-ttu-id="f3cfc-106">項目</span><span class="sxs-lookup"><span data-stu-id="f3cfc-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="f3cfc-107">描述</span><span class="sxs-lookup"><span data-stu-id="f3cfc-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cfc-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[動態連結](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="f3cfc-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="f3cfc-109">動態連結可讓執行時間在繪製 (時間進行決策，而不是在編譯時間) ，以瞭解要執行的程式碼路徑。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="f3cfc-110">這樣可以減少著色器幾乎相同的輸入簽章所造成的著色器激增問題。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="f3cfc-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[幾何著色器功能](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="f3cfc-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="f3cfc-112">新的幾何著色器功能包括：實例，可在資料流程中的基本專案順序不重要時提高效能，以及多個點輸出資料流程，讓著色器可以在多個資料流程上輸出頂點。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="f3cfc-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[鑲嵌](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="f3cfc-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="f3cfc-114">Direct3D 11 執行時間支援三個新階段來執行鑲嵌式，這會將低細節的細分圖介面轉換成 GPU 上較高的基本專案。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="f3cfc-115">鑲嵌並排顯示高位表面 (或將其分裂) 成為適合轉譯的結構。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="f3cfc-116">三個鑲嵌階段為輪廓-著色器、鑲嵌和網域著色器階段。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="f3cfc-117">此外，參考章節還涵蓋了許多適用于著色器模型5的新 API 元素，包括： [屬性](d3d11-graphics-reference-sm5-attributes.md)、 [內建函式](d3d11-graphics-reference-sm5-intrinsics.md)、 [著色器模型5物件和方法](d3d11-graphics-reference-sm5-objects.md)，以及 [系統值](d3d11-graphics-reference-sm5-system-values.md)。</span><span class="sxs-lookup"><span data-stu-id="f3cfc-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3cfc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3cfc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3cfc-119">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f3cfc-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

