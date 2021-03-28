---
title: 著色器模型5
description: 本章節包含 HLSL 著色器模型5的參考頁面。
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375708"
---
# <a name="shader-model-5"></a><span data-ttu-id="4da86-103">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4da86-103">Shader Model 5</span></span>

<span data-ttu-id="4da86-104">本章節包含 HLSL 著色器模型5的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4da86-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="4da86-105">著色器模型5是 [著色器模型 4](dx-graphics-hlsl-sm4.md)中功能的超集合。</span><span class="sxs-lookup"><span data-stu-id="4da86-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="4da86-106">它是使用通用著色器核心設計的，可為所有可程式化的著色器提供一組通用的功能，這些著色器只能使用 HLSL 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="4da86-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="4da86-107">功能</span><span class="sxs-lookup"><span data-stu-id="4da86-107">Feature</span></span>                   | <span data-ttu-id="4da86-108">功能</span><span class="sxs-lookup"><span data-stu-id="4da86-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da86-109">指令集</span><span class="sxs-lookup"><span data-stu-id="4da86-109">Instruction Set</span></span>           | [<span data-ttu-id="4da86-110">**HLSL 內建函式**</span><span class="sxs-lookup"><span data-stu-id="4da86-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="4da86-111">頂點著色器最大值</span><span class="sxs-lookup"><span data-stu-id="4da86-111">Vertex Shader Max</span></span>         | <span data-ttu-id="4da86-112">沒有限制</span><span class="sxs-lookup"><span data-stu-id="4da86-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="4da86-113">圖元著色器最大值</span><span class="sxs-lookup"><span data-stu-id="4da86-113">Pixel Shader Max</span></span>          | <span data-ttu-id="4da86-114">沒有限制</span><span class="sxs-lookup"><span data-stu-id="4da86-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="4da86-115">新增著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="4da86-115">New Shader Profiles Added</span></span> | <span data-ttu-id="4da86-116">cs \_ 4 \_ 0、gs \_ 4 \_ 0 \* 、ps \_ 4 \_ 0 \* 、vs \_ 4 \_ 0 \* 、cs \_ 4 \_ 1、gs \_ 4 \_ 1 \* 、ps \_ 4 \_ 1 \* 、vs \_ 4 \_ 1 \* 、cs \_ 5 \_ 0、ds \_ 5 \_ 0、gs \_ 5 \_ 0、hs \_ 5 \_ 0、ps \_ 5 \_ 0、vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4da86-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="4da86-117">\* -gs \_ 4 \_ 0、gs \_ 4 \_ 1、ps \_ 4 \_ 0、ps \_ 4 \_ 1、vs \_ 4 \_ 0 和 vs \_ 4 \_ 1 是在著色器模型4.0 中引進，但 directx 11 會將 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) 和位元組位址緩衝區的支援新增至在 DirectX 10 硬體上執行的著色器模型4。</span><span class="sxs-lookup"><span data-stu-id="4da86-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="4da86-118">著色器模型5引進了 [計算著色器](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) ，可提供高速的一般用途計算。</span><span class="sxs-lookup"><span data-stu-id="4da86-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="4da86-119">最完整的著色器模型5功能清單包含在 [Direct3D 11 功能](/windows/desktop/direct3d11/direct3d-11-features)清單中。</span><span class="sxs-lookup"><span data-stu-id="4da86-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="4da86-120">[著色器模型5元件](shader-model-5-assembly--directx-hlsl-.md)一節描述著色器模型5所支援的元件指示。</span><span class="sxs-lookup"><span data-stu-id="4da86-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4da86-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="4da86-121">In This Section</span></span>



| <span data-ttu-id="4da86-122">項目</span><span class="sxs-lookup"><span data-stu-id="4da86-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="4da86-123">描述</span><span class="sxs-lookup"><span data-stu-id="4da86-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4da86-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[著色器模型5屬性](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="4da86-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="4da86-125">著色器模型5屬性的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4da86-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="4da86-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[著色器模型5內建函式](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="4da86-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="4da86-127">著色器模型5內建函式的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4da86-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="4da86-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="4da86-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="4da86-129">著色器模型5物件和方法的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4da86-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="4da86-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[著色器模型5系統值](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="4da86-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="4da86-131">著色器模型5系統值的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="4da86-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="4da86-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="4da86-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da86-133">著色器模型與著色器設定檔</span><span class="sxs-lookup"><span data-stu-id="4da86-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

