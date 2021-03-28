---
title: texldl-ps
description: 使用特定取樣器來取樣材質。 要取樣的特定 mipmap 詳細資料層級必須指定為紋理座標的第四個元件。 |texldl-ps
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973941"
---
# <a name="texldl---ps"></a><span data-ttu-id="2c2e1-105">texldl-ps</span><span class="sxs-lookup"><span data-stu-id="2c2e1-105">texldl - ps</span></span>

<span data-ttu-id="2c2e1-106">使用特定取樣器來取樣材質。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="2c2e1-107">要取樣的特定 mipmap 詳細資料層級必須指定為紋理座標的第四個元件。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c2e1-108">Syntax</span></span>



| <span data-ttu-id="2c2e1-109">texldl dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="2c2e1-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="2c2e1-110">其中：</span><span class="sxs-lookup"><span data-stu-id="2c2e1-110">Where:</span></span>

-   <span data-ttu-id="2c2e1-111">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-111">dst is a destination register.</span></span>
-   <span data-ttu-id="2c2e1-112">src0 是一種來源暫存器，可提供紋理範例的材質座標。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="2c2e1-113">請參閱 [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-113">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="2c2e1-114">src1 會識別來源取樣器 (s \#) ，其中 \# 指定要取樣的材質取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-114">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="2c2e1-115">取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) 列舉所定義的材質和控制項狀態相關聯 (例如 D3DSAMP \_ MINFILTER) 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-115">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c2e1-116">備註</span><span class="sxs-lookup"><span data-stu-id="2c2e1-116">Remarks</span></span>



| <span data-ttu-id="2c2e1-117">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="2c2e1-117">Pixel shader versions</span></span> | <span data-ttu-id="2c2e1-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="2c2e1-118">1\_1</span></span> | <span data-ttu-id="2c2e1-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="2c2e1-119">1\_2</span></span> | <span data-ttu-id="2c2e1-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2c2e1-120">1\_3</span></span> | <span data-ttu-id="2c2e1-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="2c2e1-121">1\_4</span></span> | <span data-ttu-id="2c2e1-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c2e1-122">2\_0</span></span> | <span data-ttu-id="2c2e1-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2c2e1-123">2\_x</span></span> | <span data-ttu-id="2c2e1-124">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2c2e1-124">2\_sw</span></span> | <span data-ttu-id="2c2e1-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2c2e1-125">3\_0</span></span> | <span data-ttu-id="2c2e1-126">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="2c2e1-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2c2e1-127">texldl</span><span class="sxs-lookup"><span data-stu-id="2c2e1-127">texldl</span></span>                |      |      |      |      |      |      |       | <span data-ttu-id="2c2e1-128">x</span><span class="sxs-lookup"><span data-stu-id="2c2e1-128">x</span></span>    | <span data-ttu-id="2c2e1-129">x</span><span class="sxs-lookup"><span data-stu-id="2c2e1-129">x</span></span>     |



 

<span data-ttu-id="2c2e1-130">texldl 會在 src1 所參考的取樣器階段上查閱材質集。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-130">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="2c2e1-131">詳細資料層級是從 src0 中選取的。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-131">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="2c2e1-132">這個值可以是負數，在這種情況下，選取的詳細資料層級就是第零個與 MAGFILTER)  (最大的地圖。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-132">This value can be negative in which case the level-of-detail selected is the zeroth one (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="2c2e1-133">由於 src0 是浮點值，因此如果 MIPFILTER 是兩個 mip 層級之間的線性) ，則會使用小數值來插入 (。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-133">Since src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="2c2e1-134">取樣器狀態會接受 MIPMAPLODBIAS 和 MAXMIPLEVEL。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-134">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="2c2e1-135">如需取樣器狀態的詳細資訊，請參閱 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-135">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="2c2e1-136">如果著色器程式是從沒有紋理集的取樣器取樣，則會在目的地暫存器中取得0001。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-136">If a shader program samples from a sampler that does not have a texture set, then 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="2c2e1-137">以下是參考裝置所遵循的粗略演算法：</span><span class="sxs-lookup"><span data-stu-id="2c2e1-137">The following is a rough algorithm that the reference device follows:</span></span>


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="2c2e1-138">限制：</span><span class="sxs-lookup"><span data-stu-id="2c2e1-138">Restrictions:</span></span>

-   <span data-ttu-id="2c2e1-139">材質座標不應以紋理大小進行縮放。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-139">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="2c2e1-140">dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-140">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="2c2e1-141">dst 可以接受 writemask。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-141">dst can accept a writemask.</span></span> <span data-ttu-id="2c2e1-142">請參閱 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-142">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="2c2e1-143">遺漏元件的預設值為0或1，並取決於材質格式。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-143">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="2c2e1-144">src1 必須是 [ (Direct3D 9 asm-ps) ](dx9-graphics-reference-asm-ps-registers-sampler.md) (s) 的取樣器 \# 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-144">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="2c2e1-145">src1 可能不會使用否定修飾詞 (請參閱 [目的地登錄寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-145">src1 may not use a negate modifier (see [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)).</span></span> <span data-ttu-id="2c2e1-146">src1 可能會使用 swizzle (請參閱 [來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)) ，這會在取樣之後套用，但在寫入遮罩 (上，請參閱) 接受的目的地登錄寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-146">src1 may use swizzle (see [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), which is applied after sampling, but before the write mask (see Destination Register Write Mask) is honored.</span></span> <span data-ttu-id="2c2e1-147">您必須使用 [ \_ samplerType (sm2、sm3-ps asm) ](dcl-samplertype---ps.md)) 在著色器的開頭 (宣告取樣器。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-147">The sampler must have been declared (using [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="2c2e1-148">執行材質範例所需的座標數目取決於取樣器的宣告方式。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-148">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="2c2e1-149">如果它宣告為 cube，則需要三個元件的材質座標 ( rgb) 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-149">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="2c2e1-150">驗證會強制為 tex ldl 提供的座標，足以滿足針對取樣器宣告的 \_ 材質維度。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-150">Validation enforces that coordinates provided to tex\_ldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="2c2e1-151">但是，不保證應用程式實際上會透過 API) 來設定材質 (，其維度等於針對取樣器宣告的維度。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-151">However, it is not guaranteed that the application actually sets a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="2c2e1-152">在這種情況下，執行時間會嘗試偵測不相符的 (可能只有) 的 debug。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-152">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="2c2e1-153">系統會允許和紋理座標中具有較少維度的材質進行取樣，並假設忽略額外的材質座標元件。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-153">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed and assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="2c2e1-154">相反地，針對材質座標中有多個維度的材質進行取樣，是不合法的。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-154">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is illegal.</span></span>
-   <span data-ttu-id="2c2e1-155">如果 src0 (材質座標) 是 [暫時性](dx9-graphics-reference-asm-ps-registers-temporary.md)暫存器，則必須先撰寫查閱 (所需的元件) 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-155">If the src0 (texture coordinate) is [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="2c2e1-156">取樣不帶正負號的 RGB 材質將會產生介於0.0 到1.0 之間的 float 值。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-156">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="2c2e1-157">取樣帶正負號的材質會導致介於-1.0 到1.0 之間的浮點值。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-157">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="2c2e1-158">取樣浮點數材質時，Float16 表示資料將在 MAX Float16 內的範圍內 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-158">When sampling floating-point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="2c2e1-159">Float32 表示將會使用管線的最大範圍。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-159">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="2c2e1-160">在任一範圍之外取樣都未定義。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-160">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="2c2e1-161">沒有相依的讀取限制。</span><span class="sxs-lookup"><span data-stu-id="2c2e1-161">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c2e1-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c2e1-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c2e1-163">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="2c2e1-163">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
