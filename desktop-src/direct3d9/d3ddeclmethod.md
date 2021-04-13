---
description: 定義頂點宣告方法，這是鑲嵌 (所執行的預先定義作業，或是在鑲嵌) 期間，頂點資料上的任何程式性幾何常式。
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: 'D3DDECLMETHOD 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322731"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="930a1-103">D3DDECLMETHOD 列舉</span><span class="sxs-lookup"><span data-stu-id="930a1-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="930a1-104">定義頂點宣告方法，這是鑲嵌 (所執行的預先定義作業，或是在鑲嵌) 期間，頂點資料上的任何程式性幾何常式。</span><span class="sxs-lookup"><span data-stu-id="930a1-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="930a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="930a1-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="930a1-106">常數</span><span class="sxs-lookup"><span data-stu-id="930a1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="930a1-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="930a1-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-108">預設值。</span><span class="sxs-lookup"><span data-stu-id="930a1-108">Default value.</span></span> <span data-ttu-id="930a1-109">鑲嵌會) 依原樣複製 (曲線資料的頂點資料，而不會有其他計算。</span><span class="sxs-lookup"><span data-stu-id="930a1-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="930a1-110">使用鑲嵌時，會插入這個元素。</span><span class="sxs-lookup"><span data-stu-id="930a1-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="930a1-111">否則，會將頂點資料複製到輸入暫存器中。</span><span class="sxs-lookup"><span data-stu-id="930a1-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="930a1-112">輸入和輸出類型可以是任何值，但一律是相同的類型。</span><span class="sxs-lookup"><span data-stu-id="930a1-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="930a1-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**</span><span class="sxs-lookup"><span data-stu-id="930a1-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-114">以 U 方向計算矩形或三角形 patch 上某個點的正切函數。</span><span class="sxs-lookup"><span data-stu-id="930a1-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="930a1-115">輸入類型可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="930a1-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="930a1-116">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="930a1-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="930a1-117">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="930a1-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="930a1-118">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="930a1-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="930a1-119">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="930a1-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="930a1-120">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="930a1-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="930a1-121">輸出類型一律為 D3DDECLTYPE \_ FLOAT3。</span><span class="sxs-lookup"><span data-stu-id="930a1-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="930a1-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**</span><span class="sxs-lookup"><span data-stu-id="930a1-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-123">以 V 方向計算矩形或三角形 patch 上某個點的正切函數。</span><span class="sxs-lookup"><span data-stu-id="930a1-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="930a1-124">輸入類型可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="930a1-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="930a1-125">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="930a1-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="930a1-126">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="930a1-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="930a1-127">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="930a1-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="930a1-128">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="930a1-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="930a1-129">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="930a1-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="930a1-130">輸出類型一律為 D3DDECLTYPE \_ FLOAT3。</span><span class="sxs-lookup"><span data-stu-id="930a1-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="930a1-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**</span><span class="sxs-lookup"><span data-stu-id="930a1-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-132">藉由採用兩個正切的交叉乘積，計算矩形或三角形 patch 上某個點的法線。</span><span class="sxs-lookup"><span data-stu-id="930a1-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="930a1-133">輸入類型可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="930a1-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="930a1-134">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="930a1-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="930a1-135">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="930a1-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="930a1-136">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="930a1-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="930a1-137">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="930a1-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="930a1-138">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="930a1-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="930a1-139">輸出類型一律為 D3DDECLTYPE \_ FLOAT3。</span><span class="sxs-lookup"><span data-stu-id="930a1-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="930a1-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**</span><span class="sxs-lookup"><span data-stu-id="930a1-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-141">將 U、V 值複製到矩形或三角形 patch 上的某個點。</span><span class="sxs-lookup"><span data-stu-id="930a1-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="930a1-142">這會導致2D 浮點數。</span><span class="sxs-lookup"><span data-stu-id="930a1-142">This results in a 2D float.</span></span> <span data-ttu-id="930a1-143">輸入類型必須設定為 D3DDECLTYPE \_ 未使用。</span><span class="sxs-lookup"><span data-stu-id="930a1-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="930a1-144">輸出資料類型一律為 D3DDECLTYPE \_ FLOAT2。</span><span class="sxs-lookup"><span data-stu-id="930a1-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="930a1-145">輸入資料流程和位移也是未使用的 (但必須設定為 0) 。</span><span class="sxs-lookup"><span data-stu-id="930a1-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="930a1-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD \_ 查閱**</span><span class="sxs-lookup"><span data-stu-id="930a1-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-147">查閱置換圖。</span><span class="sxs-lookup"><span data-stu-id="930a1-147">Look up a displacement map.</span></span> <span data-ttu-id="930a1-148">輸入類型可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="930a1-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="930a1-149">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="930a1-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="930a1-150">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="930a1-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="930a1-151">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="930a1-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="930a1-152">紋理對應查閱只會使用. x 和. y 元件。</span><span class="sxs-lookup"><span data-stu-id="930a1-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="930a1-153">輸出類型一律為 D3DDECLTYPE \_ FLOAT1。</span><span class="sxs-lookup"><span data-stu-id="930a1-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="930a1-154">裝置必須支援置換對應。</span><span class="sxs-lookup"><span data-stu-id="930a1-154">The device must support displacement mapping.</span></span> <span data-ttu-id="930a1-155">如需置換對應的詳細資訊，請參閱 [ (Direct3D 9) 的置換對應 ](displacement-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="930a1-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="930a1-156">如果啟用了 N 個修補程式，則只有 N 個修補程式資料的可程式化管線才支援這個常數。</span><span class="sxs-lookup"><span data-stu-id="930a1-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="930a1-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**</span><span class="sxs-lookup"><span data-stu-id="930a1-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="930a1-158">查閱 presampled 置換地圖。</span><span class="sxs-lookup"><span data-stu-id="930a1-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="930a1-159">輸入類型必須設定為 D3DDECLTYPE \_ 未使用; 資料流程索引和資料流程位移必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="930a1-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="930a1-160">這項作業的輸出類型一律為 D3DDECLTYPE \_ FLOAT1。</span><span class="sxs-lookup"><span data-stu-id="930a1-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="930a1-161">裝置必須支援置換對應。</span><span class="sxs-lookup"><span data-stu-id="930a1-161">The device must support displacement mapping.</span></span> <span data-ttu-id="930a1-162">如需置換對應的詳細資訊，請參閱 [ (Direct3D 9) 的置換對應 ](displacement-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="930a1-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="930a1-163">如果啟用了 N 個修補程式，則只有 N 個修補程式資料的可程式化管線才支援這個常數。</span><span class="sxs-lookup"><span data-stu-id="930a1-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="930a1-164">這個方法只能搭配 D3DDECLUSAGE \_ 範例使用。</span><span class="sxs-lookup"><span data-stu-id="930a1-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="930a1-165">備註</span><span class="sxs-lookup"><span data-stu-id="930a1-165">Remarks</span></span>

<span data-ttu-id="930a1-166">鑲嵌會查看方法，以判斷在鑲嵌期間要從頂點資料計算的資料。</span><span class="sxs-lookup"><span data-stu-id="930a1-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="930a1-167">網格資料應使用預設值。</span><span class="sxs-lookup"><span data-stu-id="930a1-167">Mesh data should use the default value.</span></span> <span data-ttu-id="930a1-168">修補程式可以使用任何其他已實的類型。</span><span class="sxs-lookup"><span data-stu-id="930a1-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="930a1-169">頂點資料是使用 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來宣告。</span><span class="sxs-lookup"><span data-stu-id="930a1-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="930a1-170">陣列中的每個元素都包含一個頂點宣告方法。</span><span class="sxs-lookup"><span data-stu-id="930a1-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="930a1-171">除了使用 D3DDECLMETHOD \_ 預設值， \_ \_ 當啟用 N 個修補程式時，一般網格可以使用 D3DDECLMETHOD LOOKUP 和 D3DDECLMETHOD LOOKUPPRESAMPLED 方法。</span><span class="sxs-lookup"><span data-stu-id="930a1-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="930a1-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="930a1-172">Requirements</span></span>



| <span data-ttu-id="930a1-173">需求</span><span class="sxs-lookup"><span data-stu-id="930a1-173">Requirement</span></span> | <span data-ttu-id="930a1-174">值</span><span class="sxs-lookup"><span data-stu-id="930a1-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="930a1-175">標頭</span><span class="sxs-lookup"><span data-stu-id="930a1-175">Header</span></span><br/> | <dl> <span data-ttu-id="930a1-176"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="930a1-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930a1-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="930a1-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930a1-178">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="930a1-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




