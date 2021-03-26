---
title: '載入 (DirectX HLSL 材質物件) '
description: 讀取材質資料，而不進行任何篩選或取樣。
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104108380"
---
# <a name="load-directx-hlsl-texture-object"></a><span data-ttu-id="e0339-103">載入 (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="e0339-103">Load (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="e0339-104">讀取材質資料，而不進行任何篩選或取樣。</span><span class="sxs-lookup"><span data-stu-id="e0339-104">Reads texel data without any filtering or sampling.</span></span>



<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0339-105">ret 物件。 Load (</span><span class="sxs-lookup"><span data-stu-id="e0339-105">ret Object.Load(</span></span><dl> <span data-ttu-id="e0339-106">typeX 位置，</span><span class="sxs-lookup"><span data-stu-id="e0339-106">typeX Location,</span></span><br />
<span data-ttu-id="e0339-107">[typeX SampleIndex, ]</span><span class="sxs-lookup"><span data-stu-id="e0339-107">[typeX SampleIndex, ]</span></span><br />
<span data-ttu-id="e0339-108">[typeX Offset]</span><span class="sxs-lookup"><span data-stu-id="e0339-108">[typeX Offset ]</span></span><br />
</dl><span data-ttu-id="e0339-109">);</span><span class="sxs-lookup"><span data-stu-id="e0339-109">);</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e0339-110">typeX 表示有四種可能的類型： **int**、 **int2**、 **int3** 或 **int4**。</span><span class="sxs-lookup"><span data-stu-id="e0339-110">typeX denotes that there are four possible types: **int**, **int2**, **int3** or **int4**.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="e0339-111">參數</span><span class="sxs-lookup"><span data-stu-id="e0339-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0339-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*</span><span class="sxs-lookup"><span data-stu-id="e0339-112"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="e0339-113">[材質物件](dx-graphics-hlsl-to-type.md)類型 (除了 TextureCube 或 TextureCubeArray) 之外。</span><span class="sxs-lookup"><span data-stu-id="e0339-113">A [texture-object](dx-graphics-hlsl-to-type.md) type (except TextureCube or TextureCubeArray).</span></span>

</dd> <dt>

<span data-ttu-id="e0339-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*位置*</span><span class="sxs-lookup"><span data-stu-id="e0339-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="e0339-115">\[在 \] 材質座標中，最後一個元件會指定 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="e0339-115">\[in\] The texture coordinates; the last component specifies the mipmap level.</span></span> <span data-ttu-id="e0339-116">這個方法會使用以0為基礎的座標系統，而不是 0.0-1.0 的 UV 系統。</span><span class="sxs-lookup"><span data-stu-id="e0339-116">This method uses a 0-based coordinate system and not a 0.0-1.0 UV system.</span></span> <span data-ttu-id="e0339-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e0339-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e0339-118">物件類型</span><span class="sxs-lookup"><span data-stu-id="e0339-118">Object Type</span></span>                                  | <span data-ttu-id="e0339-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="e0339-119">Parameter Type</span></span> |
|----------------------------------------------|----------------|
| <span data-ttu-id="e0339-120">Buffer</span><span class="sxs-lookup"><span data-stu-id="e0339-120">Buffer</span></span>                                       | <span data-ttu-id="e0339-121">int</span><span class="sxs-lookup"><span data-stu-id="e0339-121">int</span></span>            |
| <span data-ttu-id="e0339-122">Texture1D, Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="e0339-122">Texture1D, Texture2DMS</span></span>                       | <span data-ttu-id="e0339-123">int2</span><span class="sxs-lookup"><span data-stu-id="e0339-123">int2</span></span>           |
| <span data-ttu-id="e0339-124">Texture1DArray、材質2D、Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e0339-124">Texture1DArray, Texture 2D, Texture2DMSArray</span></span> | <span data-ttu-id="e0339-125">int3</span><span class="sxs-lookup"><span data-stu-id="e0339-125">int3</span></span>           |
| <span data-ttu-id="e0339-126">Texture2DArray, Texture3D</span><span class="sxs-lookup"><span data-stu-id="e0339-126">Texture2DArray, Texture3D</span></span>                    | <span data-ttu-id="e0339-127">int4</span><span class="sxs-lookup"><span data-stu-id="e0339-127">int4</span></span>           |



 

<span data-ttu-id="e0339-128">例如，若要存取2D 材質，請提供前兩個元件的 UV 座標和第三個元件的 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="e0339-128">For example, to access a 2D texture, supply UV coordinates for the first two components and a mipmap level for the third component.</span></span>

> [!Note]  
> <span data-ttu-id="e0339-129">當某個 *位置* 中的一個或多個座標超過材質的 u、v 或 w mipmap 層級維度時， **載入** 會在所有元件中傳回零。</span><span class="sxs-lookup"><span data-stu-id="e0339-129">When one or more of the coordinates in *Location* exceed the u, v, or w mipmap level dimensions of the texture, **Load** returns zero in all components.</span></span> <span data-ttu-id="e0339-130">Direct3D 保證可針對任何超出範圍存取的資源傳回零。</span><span class="sxs-lookup"><span data-stu-id="e0339-130">Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

 

</dd> <dt>

<span data-ttu-id="e0339-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span><span class="sxs-lookup"><span data-stu-id="e0339-131"><span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*</span></span>
</dt> <dd>

<span data-ttu-id="e0339-132">\[在 \] 選擇性的取樣索引中。</span><span class="sxs-lookup"><span data-stu-id="e0339-132">\[in\] An optional sampling index.</span></span>



| <span data-ttu-id="e0339-133">材質類型</span><span class="sxs-lookup"><span data-stu-id="e0339-133">Texture Type</span></span>                                                                                                   | <span data-ttu-id="e0339-134">參數類型</span><span class="sxs-lookup"><span data-stu-id="e0339-134">Parameter Type</span></span> |
|----------------------------------------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="e0339-135">Texture1D、Texture1DArray、Texture2D、Texture2DArray、Texture3D、Texture2DArray、TextureCube、TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e0339-135">Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e0339-136">不支援</span><span class="sxs-lookup"><span data-stu-id="e0339-136">not supported</span></span>  |
| <span data-ttu-id="e0339-137">Texture2DMS，Texture2DMSArray ¹</span><span class="sxs-lookup"><span data-stu-id="e0339-137">Texture2DMS, Texture2DMSArray¹</span></span>                                                                                 | <span data-ttu-id="e0339-138">int</span><span class="sxs-lookup"><span data-stu-id="e0339-138">int</span></span>            |



 

> [!Note]  
> <span data-ttu-id="e0339-139">*SampleIndex* 僅適用于多範例紋理。</span><span class="sxs-lookup"><span data-stu-id="e0339-139">*SampleIndex* is only available for multi-sample textures.</span></span>

 

</dd> <dt>

<span data-ttu-id="e0339-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*抵消*</span><span class="sxs-lookup"><span data-stu-id="e0339-140"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="e0339-141">\[在 \] 取樣之前套用至材質座標的選擇性位移。</span><span class="sxs-lookup"><span data-stu-id="e0339-141">\[in\] An optional offset applied to the texture coordinates before sampling.</span></span> <span data-ttu-id="e0339-142">位移類型相依于材質物件類型，而且必須是靜態。</span><span class="sxs-lookup"><span data-stu-id="e0339-142">The offset type is dependent on the texture-object type, and needs to be static.</span></span>



| <span data-ttu-id="e0339-143">材質類型</span><span class="sxs-lookup"><span data-stu-id="e0339-143">Texture Type</span></span>                                             | <span data-ttu-id="e0339-144">參數類型</span><span class="sxs-lookup"><span data-stu-id="e0339-144">Parameter Type</span></span> |
|----------------------------------------------------------|----------------|
| <span data-ttu-id="e0339-145">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e0339-145">Texture1D, Texture1DArray</span></span>                                | <span data-ttu-id="e0339-146">int</span><span class="sxs-lookup"><span data-stu-id="e0339-146">int</span></span>            |
| <span data-ttu-id="e0339-147">Texture2D、Texture2DArray、Texture2DMS、Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e0339-147">Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray</span></span> | <span data-ttu-id="e0339-148">int2</span><span class="sxs-lookup"><span data-stu-id="e0339-148">int2</span></span>           |
| <span data-ttu-id="e0339-149">Texture3D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e0339-149">Texture3D, Texture2DArray</span></span>                                | <span data-ttu-id="e0339-150">int3</span><span class="sxs-lookup"><span data-stu-id="e0339-150">int3</span></span>           |



 

> [!Note]  
> <span data-ttu-id="e0339-151">如果您使用 *Offset* 搭配多範例紋理，您也必須指定 *SampleIndex*。</span><span class="sxs-lookup"><span data-stu-id="e0339-151">If you use *Offset* with multi-sample textures, you must also specify *SampleIndex*.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0339-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0339-152">Return Value</span></span>

<span data-ttu-id="e0339-153">傳回型別符合 *物件* 宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="e0339-153">The return type matches the type in the *Object* declaration.</span></span> <span data-ttu-id="e0339-154">例如，宣告為 "Texture2d myTexture;" 的 Texture2D 物件 <uint4> 具有 **uint4** 類型的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e0339-154">For example, a Texture2D object that was declared as "Texture2d<uint4> myTexture;" has a return value of type **uint4**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e0339-155">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e0339-155">Minimum Shader Model</span></span>

<span data-ttu-id="e0339-156">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e0339-156">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e0339-157">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0339-157">vs\_4\_0</span></span> | <span data-ttu-id="e0339-158">vs \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="e0339-158">vs\_4\_1¹</span></span> | <span data-ttu-id="e0339-159">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0339-159">ps\_4\_0</span></span> | <span data-ttu-id="e0339-160">ps \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="e0339-160">ps\_4\_1¹</span></span> | <span data-ttu-id="e0339-161">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0339-161">gs\_4\_0</span></span> | <span data-ttu-id="e0339-162">gs \_ 4 \_ 1 ¹</span><span class="sxs-lookup"><span data-stu-id="e0339-162">gs\_4\_1¹</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="e0339-163">x</span><span class="sxs-lookup"><span data-stu-id="e0339-163">x</span></span>        | <span data-ttu-id="e0339-164">x</span><span class="sxs-lookup"><span data-stu-id="e0339-164">x</span></span>         | <span data-ttu-id="e0339-165">x</span><span class="sxs-lookup"><span data-stu-id="e0339-165">x</span></span>        | <span data-ttu-id="e0339-166">x</span><span class="sxs-lookup"><span data-stu-id="e0339-166">x</span></span>         | <span data-ttu-id="e0339-167">x</span><span class="sxs-lookup"><span data-stu-id="e0339-167">x</span></span>        | <span data-ttu-id="e0339-168">x</span><span class="sxs-lookup"><span data-stu-id="e0339-168">x</span></span>         |



 

-   <span data-ttu-id="e0339-169">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="e0339-169">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="e0339-170">範例</span><span class="sxs-lookup"><span data-stu-id="e0339-170">Example</span></span>

<span data-ttu-id="e0339-171">這個部分程式碼範例是來自 [AdvancedParticles 範例](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)中的油漆檔案。</span><span class="sxs-lookup"><span data-stu-id="e0339-171">This partial code example is from the Paint.fx file in the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).</span></span>


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a><span data-ttu-id="e0339-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0339-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0339-173">材質物件</span><span class="sxs-lookup"><span data-stu-id="e0339-173">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




