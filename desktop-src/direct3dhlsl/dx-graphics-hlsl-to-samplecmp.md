---
title: 'SampleCmp (DirectX HLSL 材質物件) '
description: 針對材質進行紋理取樣，並將單一元件與指定的比較值進行比較。
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "104991050"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a><span data-ttu-id="04e9d-103">SampleCmp (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="04e9d-103">SampleCmp (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="04e9d-104">針對材質進行紋理取樣，並將單一元件與指定的比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="04e9d-104">Samples a texture and compares a single component against the specified comparison value.</span></span>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04e9d-105">float 物件. SampleCmp (</span><span class="sxs-lookup"><span data-stu-id="04e9d-105">float Object.SampleCmp(</span></span> <dl> <span data-ttu-id="04e9d-106">SamplerComparisonState S、</span><span class="sxs-lookup"><span data-stu-id="04e9d-106">SamplerComparisonState S,</span></span><br />
<span data-ttu-id="04e9d-107">float 位置、</span><span class="sxs-lookup"><span data-stu-id="04e9d-107">float Location,</span></span><br />
<span data-ttu-id="04e9d-108">float CompareValue、</span><span class="sxs-lookup"><span data-stu-id="04e9d-108">float CompareValue,</span></span><br />
<span data-ttu-id="04e9d-109">[int Offset]</span><span class="sxs-lookup"><span data-stu-id="04e9d-109">[int Offset]</span></span><br />
</dl><span data-ttu-id="04e9d-110">);</span><span class="sxs-lookup"><span data-stu-id="04e9d-110">);</span></span></td>
</tr>
</tbody>
</table>
 

<span data-ttu-id="04e9d-111">比較是材質中儲存的第一個元件與方法中所傳遞的比較值之間的單一元件比較。</span><span class="sxs-lookup"><span data-stu-id="04e9d-111">The comparison is a single-component comparison between the first component stored in the texture, and the comparison value passed into the method.</span></span>

<span data-ttu-id="04e9d-112">這個方法只能從圖元著色器叫用;頂點或幾何著色器不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="04e9d-112">This method can be invoked only from a pixel shader; it isn't supported in a vertex or geometry shader.</span></span>

## <a name="parameters"></a><span data-ttu-id="04e9d-113">參數</span><span class="sxs-lookup"><span data-stu-id="04e9d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e9d-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*物件*</span><span class="sxs-lookup"><span data-stu-id="04e9d-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span>
</dt> <dd>

<span data-ttu-id="04e9d-115">任何 [材質物件](dx-graphics-hlsl-to-type.md) 類型 (除了 Texture2DMS、Texture2DMSArray 或 Texture3D) 之外。</span><span class="sxs-lookup"><span data-stu-id="04e9d-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type (except Texture2DMS, Texture2DMSArray, or Texture3D).</span></span>

</dd> <dt>

<span data-ttu-id="04e9d-116"><span id="S"></span><span id="s"></span>*！*</span><span class="sxs-lookup"><span data-stu-id="04e9d-116"><span id="S"></span><span id="s"></span>*S*</span></span>
</dt> <dd>

<span data-ttu-id="04e9d-117">\[在 \] 取樣器的比較狀態中，也就是取樣器狀態加上比較狀態 (比較函數和比較篩選) 。</span><span class="sxs-lookup"><span data-stu-id="04e9d-117">\[in\] A sampler-comparison state, which is the sampler state plus a comparison state (a comparison function and a comparison filter).</span></span> <span data-ttu-id="04e9d-118">如需詳細資訊和範例，請參閱 [取樣器類型](dx-graphics-hlsl-sampler.md) 。</span><span class="sxs-lookup"><span data-stu-id="04e9d-118">See the [sampler type](dx-graphics-hlsl-sampler.md) for details and an example.</span></span>

</dd> <dt>

<span data-ttu-id="04e9d-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*位置*</span><span class="sxs-lookup"><span data-stu-id="04e9d-119"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Location*</span></span>
</dt> <dd>

<span data-ttu-id="04e9d-120">\[在 \] 紋理座標中。</span><span class="sxs-lookup"><span data-stu-id="04e9d-120">\[in\] The texture coordinates.</span></span> <span data-ttu-id="04e9d-121">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="04e9d-121">The argument type is dependent on the texture-object type.</span></span>

| <span data-ttu-id="04e9d-122">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="04e9d-122">Texture-Object Type</span></span>          | <span data-ttu-id="04e9d-123">參數類型</span><span class="sxs-lookup"><span data-stu-id="04e9d-123">Parameter Type</span></span> |
|------------------------------|----------------|
| <span data-ttu-id="04e9d-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04e9d-124">Texture1D</span></span>                    | <span data-ttu-id="04e9d-125">FLOAT</span><span class="sxs-lookup"><span data-stu-id="04e9d-125">float</span></span>          |
| <span data-ttu-id="04e9d-126">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="04e9d-126">Texture1DArray, Texture2D</span></span>    | <span data-ttu-id="04e9d-127">float2</span><span class="sxs-lookup"><span data-stu-id="04e9d-127">float2</span></span>         |
| <span data-ttu-id="04e9d-128">Texture2DArray ¹，TextureCube</span><span class="sxs-lookup"><span data-stu-id="04e9d-128">Texture2DArray¹, TextureCube</span></span> | <span data-ttu-id="04e9d-129">float3</span><span class="sxs-lookup"><span data-stu-id="04e9d-129">float3</span></span>         |
| <span data-ttu-id="04e9d-130">TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="04e9d-130">TextureCubeArray¹</span></span>            | <span data-ttu-id="04e9d-131">float4</span><span class="sxs-lookup"><span data-stu-id="04e9d-131">float4</span></span>         |

</dd> <dt>

<span data-ttu-id="04e9d-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span><span class="sxs-lookup"><span data-stu-id="04e9d-132"><span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*</span></span>
</dt> <dd>

<span data-ttu-id="04e9d-133">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="04e9d-133">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="04e9d-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*抵消*</span><span class="sxs-lookup"><span data-stu-id="04e9d-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*</span></span>
</dt> <dd>

<span data-ttu-id="04e9d-135">\[在 \] 選擇性的材質座標位移中（可用於任何材質物件類型）; 位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="04e9d-135">\[in\] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="04e9d-136">材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="04e9d-136">The texture offsets need to be static.</span></span> <span data-ttu-id="04e9d-137">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="04e9d-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="04e9d-138">如需詳細資訊，請參閱套用 [材質座標位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="04e9d-138">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>

| <span data-ttu-id="04e9d-139">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="04e9d-139">Texture-Object Type</span></span>            | <span data-ttu-id="04e9d-140">參數類型</span><span class="sxs-lookup"><span data-stu-id="04e9d-140">Parameter Type</span></span> |
|--------------------------------|----------------|
| <span data-ttu-id="04e9d-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="04e9d-141">Texture1D, Texture1DArray</span></span>      | <span data-ttu-id="04e9d-142">int</span><span class="sxs-lookup"><span data-stu-id="04e9d-142">int</span></span>            |
| <span data-ttu-id="04e9d-143">Texture2D，Texture2DArray ¹</span><span class="sxs-lookup"><span data-stu-id="04e9d-143">Texture2D, Texture2DArray¹</span></span>     | <span data-ttu-id="04e9d-144">int2</span><span class="sxs-lookup"><span data-stu-id="04e9d-144">int2</span></span>           |
| <span data-ttu-id="04e9d-145">TextureCube，TextureCubeArray ¹</span><span class="sxs-lookup"><span data-stu-id="04e9d-145">TextureCube, TextureCubeArray¹</span></span> | <span data-ttu-id="04e9d-146">不支援</span><span class="sxs-lookup"><span data-stu-id="04e9d-146">Not supported</span></span>  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e9d-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="04e9d-147">Return Value</span></span>

<span data-ttu-id="04e9d-148">傳回範圍 0 ..1 中的浮點值。 \[ \]</span><span class="sxs-lookup"><span data-stu-id="04e9d-148">Returns a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="04e9d-149">針對每個根據篩選模式) 的取樣器設定取得 (的材質， **SampleCmp** 會根據材質值（如果比較成功，從著色器針對值 (1），執行 z 值 (第三個) 元件的比較。否則為 0) 。</span><span class="sxs-lookup"><span data-stu-id="04e9d-149">For each texel fetched (based on the sampler configuration of the filter mode), **SampleCmp** performs a comparison of the z value (3rd component of input) from the shader against the texel value (1 if the comparison passes; otherwise 0).</span></span> <span data-ttu-id="04e9d-150">然後， **SampleCmp** 會將每個材質的這0和1個結果混合成一般材質篩選 (不是平均) ，並將產生的 \[ 0 ..1 \] 值傳回給著色器。</span><span class="sxs-lookup"><span data-stu-id="04e9d-150">**SampleCmp** then blends these 0 and 1 results for each texel together as in normal texture filtering (not an average) and returns the resulting \[0..1\] value to the shader.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e9d-151">備註</span><span class="sxs-lookup"><span data-stu-id="04e9d-151">Remarks</span></span>

<span data-ttu-id="04e9d-152">比較篩選會提供基本的篩選作業，適用于百分比深度的篩選。</span><span class="sxs-lookup"><span data-stu-id="04e9d-152">Comparison filtering provides a basic filtering operation that is useful for percentage-closer-depth filtering.</span></span>

<span data-ttu-id="04e9d-153">在浮點資源上使用這個方法時 (而非經過簽署的正規化或不帶正負號標準化) 格式時，不會自動在0.0 和1.0 之間壓制比較值。</span><span class="sxs-lookup"><span data-stu-id="04e9d-153">When using this method on a floating-point resource (Instead of a signed-normalized or unsigned-normalized format), the comparison value is not automatically clamped between 0.0 and 1.0.</span></span> <span data-ttu-id="04e9d-154">因此，常見的遮蔽技術可能需要比較值的手動夾具。</span><span class="sxs-lookup"><span data-stu-id="04e9d-154">Therefore, a manual clamp of the comparison value may be necessary for common shadowing techniques.</span></span>

<span data-ttu-id="04e9d-155">只在整數 miplevel 使用位移;否則，您可能會根據硬體的執行或驅動程式設定取得不同的結果。</span><span class="sxs-lookup"><span data-stu-id="04e9d-155">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="04e9d-156">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="04e9d-156">Minimum Shader Model</span></span>

<span data-ttu-id="04e9d-157">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="04e9d-157">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="04e9d-158">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04e9d-158">vs\_4\_0</span></span> | <span data-ttu-id="04e9d-159">vs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="04e9d-159">vs\_4\_1²</span></span> | <span data-ttu-id="04e9d-160">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04e9d-160">ps\_4\_0</span></span> | <span data-ttu-id="04e9d-161">ps \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="04e9d-161">ps\_4\_1²</span></span> | <span data-ttu-id="04e9d-162">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04e9d-162">gs\_4\_0</span></span> | <span data-ttu-id="04e9d-163">gs \_ 4 \_ 1 ²</span><span class="sxs-lookup"><span data-stu-id="04e9d-163">gs\_4\_1²</span></span> |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="04e9d-164">x ¹</span><span class="sxs-lookup"><span data-stu-id="04e9d-164">x¹</span></span>       | <span data-ttu-id="04e9d-165">x</span><span class="sxs-lookup"><span data-stu-id="04e9d-165">x</span></span>         |          |           |

1.  <span data-ttu-id="04e9d-166">Texture2DArray 和 TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="04e9d-166">Texture2DArray and TextureCubeArray are available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="04e9d-167">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="04e9d-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

> [!NOTE]  
> <span data-ttu-id="04e9d-168"> \_ \_ \_ \_ \_ \_ \_ \_ 當您使用在[Direct3D 功能層級9中執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10))時所述的技術，也可以在 ps 4 0 層級 9 1 和 4 0 層級 9 3 中使用 SampleCmp。</span><span class="sxs-lookup"><span data-stu-id="04e9d-168">**SampleCmp** is also available in ps 4\_0\_level\_9\_1 and 4\_0\_level\_9\_3 when you use the techniques that are described in [Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04e9d-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="04e9d-169">Related topics</span></span>

[<span data-ttu-id="04e9d-170">材質物件</span><span class="sxs-lookup"><span data-stu-id="04e9d-170">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
