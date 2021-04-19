---
description: 彈性頂點格式常數（或 FVF 代碼）是用來描述在單一資料流程中交錯的頂點內容，此資料流程會由固定函式管線處理。
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4bfc1dcabdb6991b49af967bb596fd4c1e3bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970734"
---
# <a name="d3dfvf"></a><span data-ttu-id="8ee5c-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="8ee5c-103">D3DFVF</span></span>

<span data-ttu-id="8ee5c-104">彈性頂點格式常數（或 FVF 代碼）是用來描述在單一資料流程中交錯的頂點內容，此資料流程會由固定函式管線處理。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="8ee5c-105">頂點資料旗標</span><span class="sxs-lookup"><span data-stu-id="8ee5c-105">Vertex Data Flags</span></span>

<span data-ttu-id="8ee5c-106">下列旗標描述頂點格式。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="8ee5c-107">如需有關頂點格式的詳細資訊，請參閱 [ (Direct3D 9) 的固定函式 FVF 碼 ](fixed-function-fvf-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee5c-108">\#定義</span><span class="sxs-lookup"><span data-stu-id="8ee5c-108">\#define</span></span>                            | <span data-ttu-id="8ee5c-109">Description</span><span class="sxs-lookup"><span data-stu-id="8ee5c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="8ee5c-110">資料順序和類型</span><span class="sxs-lookup"><span data-stu-id="8ee5c-110">Data order and type</span></span>                                                                                       |
| <span data-ttu-id="8ee5c-111">D3DFVF \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="8ee5c-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="8ee5c-112">頂點格式包含擴散色彩元件。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="8ee5c-113">依 ARGB 順序的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-113">DWORD in ARGB order.</span></span> <span data-ttu-id="8ee5c-114">請參閱 [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="8ee5c-115">D3DFVF \_ 正常</span><span class="sxs-lookup"><span data-stu-id="8ee5c-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="8ee5c-116">頂點格式包含頂點一般向量。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="8ee5c-117">此旗標不可與 D3DFVF XYZRHW 旗標一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="8ee5c-118">float、float、float</span><span class="sxs-lookup"><span data-stu-id="8ee5c-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="8ee5c-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="8ee5c-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="8ee5c-120">以點大小指定的頂點格式。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-120">Vertex format specified in point size.</span></span> <span data-ttu-id="8ee5c-121">這種大小是以相機空間單位來表示，而這些頂點未轉換和亮，而裝置空間單位適用于已轉換和亮頂點。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="8ee5c-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8ee5c-122">float</span></span>                                                                                                     |
| <span data-ttu-id="8ee5c-123">D3DFVF \_ 反光</span><span class="sxs-lookup"><span data-stu-id="8ee5c-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="8ee5c-124">頂點格式包含反射色彩元件。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="8ee5c-125">依 ARGB 順序的 DWORD。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-125">DWORD in ARGB order.</span></span> <span data-ttu-id="8ee5c-126">請參閱 [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="8ee5c-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="8ee5c-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="8ee5c-128">頂點格式包含未轉換頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="8ee5c-129">此旗標不可與 D3DFVF XYZRHW 旗標一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="8ee5c-130">浮點數、浮點數、浮點數。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="8ee5c-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="8ee5c-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="8ee5c-132">頂點格式包含已轉換頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="8ee5c-133">此旗標不可與 D3DFVF \_ XYZ 或 D3DFVF \_ NORMAL 旗標一起使用。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="8ee5c-134">浮點數、浮點數、浮點數、浮點數。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="8ee5c-135">D3DFVF \_ XYZB1 到 D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="8ee5c-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="8ee5c-136">頂點格式包含位置資料，以及對應的加權數目 (Beta) 值，用於 multimatrix 頂點混合作業。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="8ee5c-137">目前，Direct3D 最多可以 blend 三個加權值和四個混合矩陣。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="8ee5c-138">如需使用混色矩陣的詳細資訊，請參閱 [ (Direct3D 9) 的索引頂點混色 ](indexed-vertex-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="8ee5c-139">1、2或3浮點數。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="8ee5c-140">使用 D3DFVF \_ LASTBETA \_ UBYTE4 時，會將最後一個混合權數視為 DWORD。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="8ee5c-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="8ee5c-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="8ee5c-142">頂點格式包含已轉換和裁剪的 (x、y、z、w) 資料。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="8ee5c-143">ProcessVertices 不會叫用 clipper，而是以裁剪座標輸出資料。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="8ee5c-144">這個常數是針對所設計，而且只能與可程式化的頂點管線搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="8ee5c-145">float、float、float、float</span><span class="sxs-lookup"><span data-stu-id="8ee5c-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="8ee5c-146">材質旗標</span><span class="sxs-lookup"><span data-stu-id="8ee5c-146">Texture Flags</span></span>

<span data-ttu-id="8ee5c-147">下列旗標描述固定函式管線所使用的材質旗標。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee5c-148">\#定義</span><span class="sxs-lookup"><span data-stu-id="8ee5c-148">\#define</span></span>                          | <span data-ttu-id="8ee5c-149">Description</span><span class="sxs-lookup"><span data-stu-id="8ee5c-149">Description</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8ee5c-150">D3DFVF \_ TEX0-D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="8ee5c-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="8ee5c-151">這個頂點的材質座標集數目。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="8ee5c-152">這些旗標的實際值不是連續的。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="8ee5c-153">D3DFVF \_ TEXCOORDSIZEN (coordIndex) </span><span class="sxs-lookup"><span data-stu-id="8ee5c-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="8ee5c-154">定義材質座標資料集。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="8ee5c-155">n 表示紋理座標的維度。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="8ee5c-156">coordIndex 表示紋理座標索引編號。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="8ee5c-157">請參閱 [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 和 [材質座標和材質階段](texture-coordinates.md)。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="8ee5c-158">遮罩旗標</span><span class="sxs-lookup"><span data-stu-id="8ee5c-158">Mask Flags</span></span>

<span data-ttu-id="8ee5c-159">下列旗標描述固定函式管線所使用的遮罩旗標。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="8ee5c-160">\#定義</span><span class="sxs-lookup"><span data-stu-id="8ee5c-160">\#define</span></span>                             | <span data-ttu-id="8ee5c-161">Description</span><span class="sxs-lookup"><span data-stu-id="8ee5c-161">Description</span></span>                                           |
| <span data-ttu-id="8ee5c-162">D3DFVF \_ 位置 \_ 遮罩</span><span class="sxs-lookup"><span data-stu-id="8ee5c-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="8ee5c-163">位置位的遮罩。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="8ee5c-164">D3DFVF \_ RESERVED0、D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="8ee5c-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="8ee5c-165">遮罩 FVF 中保留位的值。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="8ee5c-166">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-166">Do not use.</span></span> |
| <span data-ttu-id="8ee5c-167">D3DFVF \_ TEXCOUNT \_ MASK</span><span class="sxs-lookup"><span data-stu-id="8ee5c-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="8ee5c-168">材質旗標位的遮罩值。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="8ee5c-169">其他旗標</span><span class="sxs-lookup"><span data-stu-id="8ee5c-169">Miscellaneous Flags</span></span>

<span data-ttu-id="8ee5c-170">下列旗標描述固定函式管線所使用的各種旗標。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ee5c-171">#定義</span><span class="sxs-lookup"><span data-stu-id="8ee5c-171">#define</span></span></td>
<td><span data-ttu-id="8ee5c-172">Description</span><span class="sxs-lookup"><span data-stu-id="8ee5c-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee5c-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="8ee5c-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="8ee5c-174">頂點位置資料中的最後一個搶鮮版（Beta）欄位將會是 D3DCOLOR 類型。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="8ee5c-175">搶鮮版（Beta）欄位中的資料會搭配矩陣調色板的外觀使用，以指定矩陣索引。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee5c-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="8ee5c-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="8ee5c-177">頂點位置資料中的最後一個搶鮮版（Beta）欄位將會是 UBYTE4 類型。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="8ee5c-178">搶鮮版（Beta）欄位中的資料會搭配矩陣調色板的外觀使用，以指定矩陣索引。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="8ee5c-179">假設 FVF 宣告為： D3DFVF_XYZB5 |D3DFVF_LASTBETA_UBYTE4。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="8ee5c-180">權數和 MatrixIndices 包含在 Beta [5] 中，D3DFVF_LASTBETA_UBYTE4 表示要將 Beta [5] 中的最後一個 DWORD 解讀為類型 UBYTE4。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee5c-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="8ee5c-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="8ee5c-182">用來將識別頂點材質座標數目的整數值移位的位數。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="8ee5c-183">您可以使用此值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-183">This value might be used as shown below.</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a><span data-ttu-id="8ee5c-184">範例</span><span class="sxs-lookup"><span data-stu-id="8ee5c-184">Examples</span></span>

<span data-ttu-id="8ee5c-185">下列範例顯示其他常見的旗標組合。</span><span class="sxs-lookup"><span data-stu-id="8ee5c-185">The following examples show other common flag combinations.</span></span>


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a><span data-ttu-id="8ee5c-186">常數資訊</span><span class="sxs-lookup"><span data-stu-id="8ee5c-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="8ee5c-187">標頭</span><span class="sxs-lookup"><span data-stu-id="8ee5c-187">Header</span></span>                   | <span data-ttu-id="8ee5c-188">d3d9types。h</span><span class="sxs-lookup"><span data-stu-id="8ee5c-188">d3d9types.h</span></span> |
| <span data-ttu-id="8ee5c-189">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="8ee5c-189">Minimum operating system</span></span> | <span data-ttu-id="8ee5c-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8ee5c-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="8ee5c-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ee5c-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ee5c-192">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="8ee5c-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="8ee5c-193">修正 (Direct3D 9) 的函式 FVF 碼 </span><span class="sxs-lookup"><span data-stu-id="8ee5c-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="8ee5c-194"> (Direct3D 9) 的幾何混合 </span><span class="sxs-lookup"><span data-stu-id="8ee5c-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



