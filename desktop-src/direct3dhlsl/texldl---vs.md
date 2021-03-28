---
title: texldl-vs
description: 使用特定取樣器來取樣材質。 要取樣的特定 mipmap 詳細資料層級必須指定為紋理座標的第四個元件。 |texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035264"
---
# <a name="texldl---vs"></a><span data-ttu-id="9fea4-105">texldl-vs</span><span class="sxs-lookup"><span data-stu-id="9fea4-105">texldl - vs</span></span>

<span data-ttu-id="9fea4-106">使用特定取樣器來取樣材質。</span><span class="sxs-lookup"><span data-stu-id="9fea4-106">Sample a texture with a particular sampler.</span></span> <span data-ttu-id="9fea4-107">要取樣的特定 mipmap 詳細資料層級必須指定為紋理座標的第四個元件。</span><span class="sxs-lookup"><span data-stu-id="9fea4-107">The particular mipmap level-of-detail being sampled has to be specified as the fourth component of the texture coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fea4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fea4-108">Syntax</span></span>



| <span data-ttu-id="9fea4-109">texldl dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="9fea4-109">texldl dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="9fea4-110">其中：</span><span class="sxs-lookup"><span data-stu-id="9fea4-110">Where:</span></span>

-   <span data-ttu-id="9fea4-111">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="9fea4-111">dst is a destination register.</span></span>
-   <span data-ttu-id="9fea4-112">src0 是一種來源暫存器，可提供紋理範例的材質座標。</span><span class="sxs-lookup"><span data-stu-id="9fea4-112">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="9fea4-113">src1 會識別來源取樣器 (s \#) ，其中 \# 指定要取樣的材質取樣器數目。</span><span class="sxs-lookup"><span data-stu-id="9fea4-113">src1 identifies the source sampler register (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="9fea4-114">取樣器已將材質與 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) 列舉所定義的材質和控制項狀態相關聯 (例如 D3DSAMP \_ MINFILTER) 。</span><span class="sxs-lookup"><span data-stu-id="9fea4-114">The sampler has associated with it a texture and a control state defined by the [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) enumeration (for example, D3DSAMP\_MINFILTER).</span></span>

## <a name="remarks"></a><span data-ttu-id="9fea4-115">備註</span><span class="sxs-lookup"><span data-stu-id="9fea4-115">Remarks</span></span>



| <span data-ttu-id="9fea4-116">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="9fea4-116">Vertex shader versions</span></span> | <span data-ttu-id="9fea4-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="9fea4-117">1\_1</span></span> | <span data-ttu-id="9fea4-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9fea4-118">2\_0</span></span> | <span data-ttu-id="9fea4-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9fea4-119">2\_x</span></span> | <span data-ttu-id="9fea4-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9fea4-120">2\_sw</span></span> | <span data-ttu-id="9fea4-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9fea4-121">3\_0</span></span> | <span data-ttu-id="9fea4-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9fea4-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9fea4-123">texldl</span><span class="sxs-lookup"><span data-stu-id="9fea4-123">texldl</span></span>                 |      |      |      |       | <span data-ttu-id="9fea4-124">x</span><span class="sxs-lookup"><span data-stu-id="9fea4-124">x</span></span>    | <span data-ttu-id="9fea4-125">x</span><span class="sxs-lookup"><span data-stu-id="9fea4-125">x</span></span>     |



 

<span data-ttu-id="9fea4-126">texldl 會在 src1 所參考的取樣器階段上查閱材質集。</span><span class="sxs-lookup"><span data-stu-id="9fea4-126">texldl looks up the texture set at the sampler stage referenced by src1.</span></span> <span data-ttu-id="9fea4-127">詳細資料層級是從 src0 中選取的。</span><span class="sxs-lookup"><span data-stu-id="9fea4-127">The level-of-detail is selected from src0.w.</span></span> <span data-ttu-id="9fea4-128">這個值可以是負數，在這種情況下，選取的詳細資料層級是「第零個一」 (最大的地圖) 與 MAGFILTER。</span><span class="sxs-lookup"><span data-stu-id="9fea4-128">This value can be negative, in which case the level-of-detail selected is the "zeroth one" (biggest map) with the MAGFILTER.</span></span> <span data-ttu-id="9fea4-129">因為 src0 是浮點值，所以如果 MIPFILTER 是兩個 mip 層級之間的線性) ，則會使用小數值來插入 (。</span><span class="sxs-lookup"><span data-stu-id="9fea4-129">Because src0.w is a floating point value, the fractional value is used to interpolate (if MIPFILTER is LINEAR) between two mip levels.</span></span> <span data-ttu-id="9fea4-130">取樣器狀態會接受 MIPMAPLODBIAS 和 MAXMIPLEVEL。</span><span class="sxs-lookup"><span data-stu-id="9fea4-130">Sampler states MIPMAPLODBIAS and MAXMIPLEVEL are honored.</span></span> <span data-ttu-id="9fea4-131">如需取樣器狀態的詳細資訊，請參閱 [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype)。</span><span class="sxs-lookup"><span data-stu-id="9fea4-131">For more information about sampler states, see [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="9fea4-132">如果著色器程式範例來自沒有紋理集的取樣器，則會在目的地暫存器中取得0001。</span><span class="sxs-lookup"><span data-stu-id="9fea4-132">If a shader program samples from a sampler that does not have a texture set, 0001 is obtained in the destination register.</span></span>

<span data-ttu-id="9fea4-133">這是參考裝置演算法的近似值。</span><span class="sxs-lookup"><span data-stu-id="9fea4-133">This is an approximation to the reference device algorithm.</span></span>


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
   LOD = MAX( MAXMIPLEVEL, LOD);
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



<span data-ttu-id="9fea4-134">限制：</span><span class="sxs-lookup"><span data-stu-id="9fea4-134">Restrictions:</span></span>

-   <span data-ttu-id="9fea4-135">材質座標不應以紋理大小進行縮放。</span><span class="sxs-lookup"><span data-stu-id="9fea4-135">The texture coordinates should not be scaled by texture size.</span></span>
-   <span data-ttu-id="9fea4-136">dst 必須是 [暫時性的註冊](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \#) 。</span><span class="sxs-lookup"><span data-stu-id="9fea4-136">dst must be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="9fea4-137">dst 可以接受寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="9fea4-137">dst can accept a write mask.</span></span> <span data-ttu-id="9fea4-138">請參閱 [目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md)。</span><span class="sxs-lookup"><span data-stu-id="9fea4-138">See [Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).</span></span>
-   <span data-ttu-id="9fea4-139">遺漏元件的預設值為0或1，並取決於材質格式。</span><span class="sxs-lookup"><span data-stu-id="9fea4-139">Defaults for missing components are either 0 or 1, and depend on the texture format.</span></span>
-   <span data-ttu-id="9fea4-140">src1 必須是 [ (Direct3D 9 asm-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md) (s) 的取樣器 \# 。</span><span class="sxs-lookup"><span data-stu-id="9fea4-140">src1 must be a [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#).</span></span> <span data-ttu-id="9fea4-141">src1 可能不會使用否定修飾詞。</span><span class="sxs-lookup"><span data-stu-id="9fea4-141">src1 may not use a negate modifier.</span></span> <span data-ttu-id="9fea4-142">src1 可能會使用 swizzle，這會在採用寫入遮罩之前的取樣之後套用。</span><span class="sxs-lookup"><span data-stu-id="9fea4-142">src1 may use swizzle, which is applied after sampling before the write mask is honored.</span></span> <span data-ttu-id="9fea4-143">在著色器開頭，必須使用 [ \_ samplerType (sm3-vs asm) ](dcl-samplertype---vs.md)) ，將取樣器宣告 (。</span><span class="sxs-lookup"><span data-stu-id="9fea4-143">The sampler must have been declared (using [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)) at the beginning of the shader.</span></span>
-   <span data-ttu-id="9fea4-144">執行材質範例所需的座標數目取決於取樣器的宣告方式。</span><span class="sxs-lookup"><span data-stu-id="9fea4-144">The number of coordinates required to perform the texture sample depends on how the sampler was declared.</span></span> <span data-ttu-id="9fea4-145">如果它宣告為 cube，則需要三個元件的材質座標 ( rgb) 。</span><span class="sxs-lookup"><span data-stu-id="9fea4-145">If it was declared as a cube, a three-component texture coordinate is required (.rgb).</span></span> <span data-ttu-id="9fea4-146">驗證會強制為 texldl 提供的座標，足以滿足針對取樣器宣告的材質維度。</span><span class="sxs-lookup"><span data-stu-id="9fea4-146">Validation enforces that coordinates provided to texldl Are sufficient for the texture dimension declared for the sampler.</span></span> <span data-ttu-id="9fea4-147">但是，不保證應用程式會透過 API) 實際設定材質 (，其維度等於針對取樣器宣告的維度。</span><span class="sxs-lookup"><span data-stu-id="9fea4-147">However, it is not guaranteed that the application actually set a texture (through the API) with dimensions equal to the dimension declared for the sampler.</span></span> <span data-ttu-id="9fea4-148">在這種情況下，執行時間會嘗試偵測不相符的 (可能只有) 的 debug。</span><span class="sxs-lookup"><span data-stu-id="9fea4-148">In such a case, the runtime will attempt to detect mismatches (possibly in debug only).</span></span> <span data-ttu-id="9fea4-149">您可以使用小於紋理座標中所呈現之維度的材質進行取樣，而且會假設忽略額外的材質座標元件。</span><span class="sxs-lookup"><span data-stu-id="9fea4-149">Sampling a texture with fewer dimensions than are present in the texture coordinate will be allowed, and will be assumed to ignore the extra texture coordinate components.</span></span> <span data-ttu-id="9fea4-150">相反地，不允許對具有超過材質座標之維度的材質進行取樣。</span><span class="sxs-lookup"><span data-stu-id="9fea4-150">Conversely, sampling a texture with more dimensions than are present in the texture coordinate is not allowed.</span></span>
-   <span data-ttu-id="9fea4-151">如果 src0 (材質座標) 是 (r) 的 [臨時](dx9-graphics-reference-asm-vs-registers-temporary.md) 暫存器 \# ，則必須先撰寫上述 (所述的查閱) 元件。</span><span class="sxs-lookup"><span data-stu-id="9fea4-151">If the src0 (texture coordinate) is a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#), the components required for the lookup (described above) must have been previously written.</span></span>
-   <span data-ttu-id="9fea4-152">取樣不帶正負號的 RGB 材質將會產生介於0.0 到1.0 之間的 float 值。</span><span class="sxs-lookup"><span data-stu-id="9fea4-152">Sampling unsigned RGB textures will result in float values between 0.0 and 1.0.</span></span>
-   <span data-ttu-id="9fea4-153">取樣帶正負號的材質會導致介於-1.0 到1.0 之間的浮點值。</span><span class="sxs-lookup"><span data-stu-id="9fea4-153">Sampling signed textures will result in float values between -1.0 to 1.0.</span></span>
-   <span data-ttu-id="9fea4-154">取樣浮點數材質時，Float16 表示資料將在 MAX Float16 內的範圍內 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9fea4-154">When sampling floating point textures, Float16 means that the data will range within MAX\_FLOAT16.</span></span> <span data-ttu-id="9fea4-155">Float32 表示將會使用管線的最大範圍。</span><span class="sxs-lookup"><span data-stu-id="9fea4-155">Float32 means the maximum range of the pipeline will be used.</span></span> <span data-ttu-id="9fea4-156">在任一範圍之外取樣都未定義。</span><span class="sxs-lookup"><span data-stu-id="9fea4-156">Sampling outside of either range is undefined.</span></span>
-   <span data-ttu-id="9fea4-157">沒有相依的讀取限制。</span><span class="sxs-lookup"><span data-stu-id="9fea4-157">There is no dependent read limit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fea4-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fea4-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fea4-159">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="9fea4-159">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
