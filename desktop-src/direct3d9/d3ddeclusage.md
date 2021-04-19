---
description: 識別頂點資料的用途。
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: 'D3DDECLUSAGE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992529"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="1e74d-103">D3DDECLUSAGE 列舉</span><span class="sxs-lookup"><span data-stu-id="1e74d-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="1e74d-104">識別頂點資料的用途。</span><span class="sxs-lookup"><span data-stu-id="1e74d-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e74d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e74d-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="1e74d-106">常數</span><span class="sxs-lookup"><span data-stu-id="1e74d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e74d-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="1e74d-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-108">將資料從 (-1、-1) 到 (1、1) 等位置。</span><span class="sxs-lookup"><span data-stu-id="1e74d-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="1e74d-109">使用 D3DDECLUSAGE \_ 位置搭配0的使用方式索引，以指定固定函式頂點處理和 n patch 鑲嵌的未轉換位置。</span><span class="sxs-lookup"><span data-stu-id="1e74d-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="1e74d-110">使用 D3DDECLUSAGE \_ 位置搭配1的使用方式索引，在固定的函式頂點著色器中指定頂點補間的未轉換位置。</span><span class="sxs-lookup"><span data-stu-id="1e74d-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="1e74d-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-112">混合權數資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-112">Blending weight data.</span></span> <span data-ttu-id="1e74d-113">使用 D3DDECLUSAGE \_ BLENDWEIGHT 搭配使用方式索引0，以指定用於索引和非索引頂點混合的 blend 加權。</span><span class="sxs-lookup"><span data-stu-id="1e74d-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**</span><span class="sxs-lookup"><span data-stu-id="1e74d-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-115">混合索引資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-115">Blending indices data.</span></span> <span data-ttu-id="1e74d-116">使用 D3DDECLUSAGE \_ BLENDINDICES 搭配使用索引0，以指定索引的調色板外觀的矩陣索引。</span><span class="sxs-lookup"><span data-stu-id="1e74d-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ 正常**</span><span class="sxs-lookup"><span data-stu-id="1e74d-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-118">頂點一般資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-118">Vertex normal data.</span></span> <span data-ttu-id="1e74d-119">使用 D3DDECLUSAGE \_ NORMAL 搭配0的使用方式索引，以指定固定函式頂點處理和 n patch 鑲嵌的頂點法線。</span><span class="sxs-lookup"><span data-stu-id="1e74d-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="1e74d-120">使用 D3DDECLUSAGE \_ NORMAL 搭配1的使用方式索引，為頂點補間的固定函數頂點處理指定頂點法線。</span><span class="sxs-lookup"><span data-stu-id="1e74d-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**</span><span class="sxs-lookup"><span data-stu-id="1e74d-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-122">點大小資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-122">Point size data.</span></span> <span data-ttu-id="1e74d-123">使用 D3DDECLUSAGE \_ PSIZE 搭配使用方式索引0，以指定轉譯器的安裝程式引擎所使用的點大小屬性，以針對點 sprite 功能將點展開至四個點。</span><span class="sxs-lookup"><span data-stu-id="1e74d-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**</span><span class="sxs-lookup"><span data-stu-id="1e74d-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-125">材質座標資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-125">Texture coordinate data.</span></span> <span data-ttu-id="1e74d-126">使用 D3DDECLUSAGE \_ TEXCOORD、n 可指定固定函式頂點處理中的材質座標，以及 ps 3 0 之前的圖元著色器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="1e74d-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="1e74d-127">這些可以用來傳遞使用者定義的資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ 正切函數**</span><span class="sxs-lookup"><span data-stu-id="1e74d-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-129">頂點正切資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BINORMAL**</span><span class="sxs-lookup"><span data-stu-id="1e74d-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-131">頂點 binormal 資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**</span><span class="sxs-lookup"><span data-stu-id="1e74d-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-133">單一正整數浮點值。</span><span class="sxs-lookup"><span data-stu-id="1e74d-133">Single positive floating point value.</span></span> <span data-ttu-id="1e74d-134">使用 D3DDECLUSAGE \_ TESSFACTOR 搭配使用方式索引0，以指定鑲嵌式單位中所使用的鑲嵌因數來控制鑲嵌率。</span><span class="sxs-lookup"><span data-stu-id="1e74d-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="1e74d-135">如需資料類型的詳細資訊，請參閱 D3DDECLTYPE \_ FLOAT1。</span><span class="sxs-lookup"><span data-stu-id="1e74d-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ POSITIONT**</span><span class="sxs-lookup"><span data-stu-id="1e74d-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-137">頂點資料包含已轉換的位置資料，範圍從 (0、0) 到 (的資料區寬度、視口高度) 。</span><span class="sxs-lookup"><span data-stu-id="1e74d-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="1e74d-138">使用 D3DDECLUSAGE \_ POSITIONT 搭配使用索引0，以指定轉換的位置。</span><span class="sxs-lookup"><span data-stu-id="1e74d-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="1e74d-139">當設定包含此的宣告時，管線不會執行頂點處理。</span><span class="sxs-lookup"><span data-stu-id="1e74d-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE \_ 色彩**</span><span class="sxs-lookup"><span data-stu-id="1e74d-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-141">頂點資料包含漫射或反射色彩。</span><span class="sxs-lookup"><span data-stu-id="1e74d-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="1e74d-142">使用 \_ 具有0之使用方式索引的 D3DDECLUSAGE 色彩，在固定函式頂點著色器和圖元著色器中指定在 ps \_ 3 0 之前的擴散色彩 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1e74d-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="1e74d-143">使用 D3DDECLUSAGE \_ 色彩搭配1的使用方式索引，以指定固定函式頂點著色器中的反射色彩，以及 ps 3 0 之前的圖元著色器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="1e74d-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ 霧化**</span><span class="sxs-lookup"><span data-stu-id="1e74d-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-145">頂點資料包含霧化資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-145">Vertex data contains fog data.</span></span> <span data-ttu-id="1e74d-146">使用 D3DDECLUSAGE \_ 霧化搭配0的使用方式索引，以指定圖元網底完成後使用的霧化 blend 值。</span><span class="sxs-lookup"><span data-stu-id="1e74d-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="1e74d-147">這適用于 ps 3 0 版之前的圖元著色器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="1e74d-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ 深度**</span><span class="sxs-lookup"><span data-stu-id="1e74d-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-149">頂點資料包含深度資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="1e74d-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="1e74d-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="1e74d-151">頂點資料包含取樣器資料。</span><span class="sxs-lookup"><span data-stu-id="1e74d-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="1e74d-152">使用 D3DDECLUSAGE \_ 範例搭配0的使用方式索引，以指定要查閱的置換值。</span><span class="sxs-lookup"><span data-stu-id="1e74d-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="1e74d-153">只能搭配 D3DDECLUSAGE \_ LOOKUPPRESAMPLED 或 D3DDECLUSAGE \_ LOOKUP 使用。</span><span class="sxs-lookup"><span data-stu-id="1e74d-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e74d-154">備註</span><span class="sxs-lookup"><span data-stu-id="1e74d-154">Remarks</span></span>

<span data-ttu-id="1e74d-155">頂點資料是使用 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來宣告。</span><span class="sxs-lookup"><span data-stu-id="1e74d-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="1e74d-156">陣列中的每個元素都包含使用類型。</span><span class="sxs-lookup"><span data-stu-id="1e74d-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="1e74d-157">如需有關頂點宣告的詳細資訊，請參閱 [ (Direct3D 9) 的頂點 ](vertex-declaration.md)宣告。</span><span class="sxs-lookup"><span data-stu-id="1e74d-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e74d-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e74d-158">Requirements</span></span>



| <span data-ttu-id="1e74d-159">需求</span><span class="sxs-lookup"><span data-stu-id="1e74d-159">Requirement</span></span> | <span data-ttu-id="1e74d-160">值</span><span class="sxs-lookup"><span data-stu-id="1e74d-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e74d-161">標頭</span><span class="sxs-lookup"><span data-stu-id="1e74d-161">Header</span></span><br/> | <dl> <span data-ttu-id="1e74d-162"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e74d-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e74d-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e74d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e74d-164">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="1e74d-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1e74d-165"> (Direct3D 9) 的頂點宣告 </span><span class="sxs-lookup"><span data-stu-id="1e74d-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




