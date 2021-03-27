---
title: 'dcl_resource (sm4-asm) '
description: 'dcl \_ 資源 (sm4-asm) '
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679180"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="c932e-103">dcl \_ 資源 (sm4-asm) </span><span class="sxs-lookup"><span data-stu-id="c932e-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="c932e-104">宣告非多重取樣的著色器輸入資源。</span><span class="sxs-lookup"><span data-stu-id="c932e-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="c932e-105">dcl \_ 資源 *tN*、 *resourceType*、 *returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="c932e-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="c932e-106">宣告多重取樣著色器輸入資源。</span><span class="sxs-lookup"><span data-stu-id="c932e-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="c932e-107">dcl \_ 資源 *tN*、 *resourceType \[ 大小 \] NN*、 *returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="c932e-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="c932e-108">項目</span><span class="sxs-lookup"><span data-stu-id="c932e-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="c932e-109">描述</span><span class="sxs-lookup"><span data-stu-id="c932e-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c932e-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="c932e-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="c932e-111">\[在材質暫存器中 \] ，其中 *N* 是表示註冊編號的整數。</span><span class="sxs-lookup"><span data-stu-id="c932e-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="c932e-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span><span class="sxs-lookup"><span data-stu-id="c932e-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="c932e-113">\[在 \] [ [材質物件](dx-graphics-hlsl-to-type.md) ] 頁面中所列的任何物件類型中。</span><span class="sxs-lookup"><span data-stu-id="c932e-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="c932e-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ 大小 \] NN*</span><span class="sxs-lookup"><span data-stu-id="c932e-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="c932e-115">\[在 \] Texture2D 或 Texture2DArray 物件類型中 (查看 [材質物件](dx-graphics-hlsl-to-type.md) 頁面) ; *size* 是選擇性的整數，表示陣列中的元素數目; *NN* 是表示 multisamples 數目的整數。</span><span class="sxs-lookup"><span data-stu-id="c932e-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="c932e-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="c932e-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="c932e-117">\[在 \] 每個元件的傳回型別中，這是下列其中一項： UNORM、SNORM、聖、UINT 或 FLOAT。</span><span class="sxs-lookup"><span data-stu-id="c932e-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="c932e-118">如果所有元件的類型都相同，則傳回型別的數目可以是 1 () ，但最多可以有四個。</span><span class="sxs-lookup"><span data-stu-id="c932e-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="c932e-119">使用 [load](dx-graphics-hlsl-to-load.md)在 HLSL 中存取資源;您也可以使用任何 HLSL [材質物件](dx-graphics-hlsl-to-type.md) 範例方法來存取非多重取樣材質。</span><span class="sxs-lookup"><span data-stu-id="c932e-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="c932e-120">如果資源系結至著色器階段，則會根據傳回類型來驗證資源格式。</span><span class="sxs-lookup"><span data-stu-id="c932e-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="c932e-121">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="c932e-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c932e-122">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="c932e-122">Vertex Shader</span></span> | <span data-ttu-id="c932e-123">幾何著色器</span><span class="sxs-lookup"><span data-stu-id="c932e-123">Geometry Shader</span></span> | <span data-ttu-id="c932e-124">像素著色器</span><span class="sxs-lookup"><span data-stu-id="c932e-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c932e-125">x</span><span class="sxs-lookup"><span data-stu-id="c932e-125">x</span></span>             | <span data-ttu-id="c932e-126">x</span><span class="sxs-lookup"><span data-stu-id="c932e-126">x</span></span>               | <span data-ttu-id="c932e-127">x</span><span class="sxs-lookup"><span data-stu-id="c932e-127">x</span></span>            |



 

<span data-ttu-id="c932e-128">包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。</span><span class="sxs-lookup"><span data-stu-id="c932e-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c932e-129">範例</span><span class="sxs-lookup"><span data-stu-id="c932e-129">Example</span></span>

<span data-ttu-id="c932e-130">範例如下。</span><span class="sxs-lookup"><span data-stu-id="c932e-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c932e-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c932e-131">Minimum Shader Model</span></span>

<span data-ttu-id="c932e-132">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="c932e-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c932e-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c932e-133">Shader Model</span></span>                                              | <span data-ttu-id="c932e-134">支援</span><span class="sxs-lookup"><span data-stu-id="c932e-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c932e-135">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c932e-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c932e-136">是</span><span class="sxs-lookup"><span data-stu-id="c932e-136">yes</span></span>       |
| [<span data-ttu-id="c932e-137">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="c932e-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c932e-138">是</span><span class="sxs-lookup"><span data-stu-id="c932e-138">yes</span></span>       |
| [<span data-ttu-id="c932e-139">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="c932e-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c932e-140">是</span><span class="sxs-lookup"><span data-stu-id="c932e-140">yes</span></span>       |
| [<span data-ttu-id="c932e-141">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c932e-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c932e-142">不可以</span><span class="sxs-lookup"><span data-stu-id="c932e-142">no</span></span>        |
| [<span data-ttu-id="c932e-143">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c932e-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c932e-144">不可以</span><span class="sxs-lookup"><span data-stu-id="c932e-144">no</span></span>        |
| [<span data-ttu-id="c932e-145">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c932e-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c932e-146">不可以</span><span class="sxs-lookup"><span data-stu-id="c932e-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c932e-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="c932e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c932e-148">著色器模型4元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="c932e-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





