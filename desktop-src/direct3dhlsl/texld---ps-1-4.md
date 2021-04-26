---
title: texld-ps_1_4
description: 使用來源登錄的內容作為材質座標，以色彩資料 (RGBA) 取樣來載入目的地暫存器。 取樣材質是與目的地暫存器編號相關聯的材質。
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996865"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="c97ad-104">texld-ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="c97ad-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="c97ad-105">使用來源登錄的內容作為材質座標，以色彩資料 (RGBA) 取樣來載入目的地暫存器。</span><span class="sxs-lookup"><span data-stu-id="c97ad-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="c97ad-106">取樣材質是與目的地暫存器編號相關聯的材質。</span><span class="sxs-lookup"><span data-stu-id="c97ad-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="c97ad-107">texld dst、src</span><span class="sxs-lookup"><span data-stu-id="c97ad-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="c97ad-108">暫存器</span><span class="sxs-lookup"><span data-stu-id="c97ad-108">Registers</span></span>



|          |                      | <span data-ttu-id="c97ad-109">vn</span><span class="sxs-lookup"><span data-stu-id="c97ad-109">vₙ</span></span>        | <span data-ttu-id="c97ad-110">快遞 之 家</span><span class="sxs-lookup"><span data-stu-id="c97ad-110">cₙ</span></span>  | <span data-ttu-id="c97ad-111">Tn</span><span class="sxs-lookup"><span data-stu-id="c97ad-111">tₙ</span></span>  | <span data-ttu-id="c97ad-112">Rn</span><span class="sxs-lookup"><span data-stu-id="c97ad-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="c97ad-113">Dst</span><span class="sxs-lookup"><span data-stu-id="c97ad-113">dst</span></span>      | <span data-ttu-id="c97ad-114">目的地註冊</span><span class="sxs-lookup"><span data-stu-id="c97ad-114">Destination register</span></span> |           |     |     | <span data-ttu-id="c97ad-115">x</span><span class="sxs-lookup"><span data-stu-id="c97ad-115">x</span></span>   | <span data-ttu-id="c97ad-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="c97ad-116">1\_4</span></span>         |
| <span data-ttu-id="c97ad-117">src</span><span class="sxs-lookup"><span data-stu-id="c97ad-117">src</span></span>      | <span data-ttu-id="c97ad-118">來源註冊</span><span class="sxs-lookup"><span data-stu-id="c97ad-118">Source register</span></span>      |           |     | <span data-ttu-id="c97ad-119">x</span><span class="sxs-lookup"><span data-stu-id="c97ad-119">x</span></span>   |     | <span data-ttu-id="c97ad-120">1 \_ 4 階段1</span><span class="sxs-lookup"><span data-stu-id="c97ad-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="c97ad-121">x</span><span class="sxs-lookup"><span data-stu-id="c97ad-121">x</span></span>   | <span data-ttu-id="c97ad-122">x</span><span class="sxs-lookup"><span data-stu-id="c97ad-122">x</span></span>   | <span data-ttu-id="c97ad-123">1 \_ 4 階段</span><span class="sxs-lookup"><span data-stu-id="c97ad-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="c97ad-124">使用 r (n) 作為來源暫存器時， (XYZ) 的前三個元件必須已在著色器的上一個階段中初始化。</span><span class="sxs-lookup"><span data-stu-id="c97ad-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="c97ad-125">若要深入瞭解註冊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="c97ad-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c97ad-126">備註</span><span class="sxs-lookup"><span data-stu-id="c97ad-126">Remarks</span></span>

<span data-ttu-id="c97ad-127">此指令會在與目的地暫存器編號相關聯的材質階段中，填入材質的範例。</span><span class="sxs-lookup"><span data-stu-id="c97ad-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="c97ad-128">紋理會使用來自來源暫存器的材質座標資料進行取樣。</span><span class="sxs-lookup"><span data-stu-id="c97ad-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="c97ad-129">Texld 和 texcrd 指示的語法會公開支援使用材質暫存器修飾詞來分割。</span><span class="sxs-lookup"><span data-stu-id="c97ad-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="c97ad-130">針對圖元著色器1.4 版， \_ 一律會忽略 D3DTTFF 投射的材質轉換旗標。</span><span class="sxs-lookup"><span data-stu-id="c97ad-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="c97ad-131">使用 texld 的規則：</span><span class="sxs-lookup"><span data-stu-id="c97ad-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="c97ad-132">相同的 xyw 修飾詞必須套用至每次讀取個別 t (n) 在 texcrd 或 texld 指令中進行註冊。</span><span class="sxs-lookup"><span data-stu-id="c97ad-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="c97ad-133">如果 xyw 是在 t (n) 登錄讀取，則可以使用 xyw dw 的相同 t (n) 註冊的其他讀取來混用。 \_</span><span class="sxs-lookup"><span data-stu-id="c97ad-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="c97ad-134">\_Dz 來源修飾詞只適用于 r (n) 來源登錄 (因此僅限第2階段) 的 texld。</span><span class="sxs-lookup"><span data-stu-id="c97ad-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="c97ad-135">\_每個著色器的使用次數不可超過兩次。</span><span class="sxs-lookup"><span data-stu-id="c97ad-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="c97ad-136">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c97ad-136">Pixel shader versions</span></span> | <span data-ttu-id="c97ad-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="c97ad-137">1\_1</span></span> | <span data-ttu-id="c97ad-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="c97ad-138">1\_2</span></span> | <span data-ttu-id="c97ad-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c97ad-139">1\_3</span></span> | <span data-ttu-id="c97ad-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="c97ad-140">1\_4</span></span> | <span data-ttu-id="c97ad-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c97ad-141">2\_0</span></span> | <span data-ttu-id="c97ad-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c97ad-142">2\_x</span></span> | <span data-ttu-id="c97ad-143">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c97ad-143">2\_sw</span></span> | <span data-ttu-id="c97ad-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c97ad-144">3\_0</span></span> | <span data-ttu-id="c97ad-145">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c97ad-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c97ad-146">texld</span><span class="sxs-lookup"><span data-stu-id="c97ad-146">texld</span></span>                 |      |      |      | <span data-ttu-id="c97ad-147">x</span><span class="sxs-lookup"><span data-stu-id="c97ad-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="c97ad-148">範例</span><span class="sxs-lookup"><span data-stu-id="c97ad-148">Examples</span></span>

<span data-ttu-id="c97ad-149">Texld 指令可讓您控制要使用來源材質座標資料的元件。</span><span class="sxs-lookup"><span data-stu-id="c97ad-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="c97ad-150">Texld 的一組完整的允許語法如下所示，並包含所有有效的來源登錄修飾詞、選取器和寫入遮罩組合。</span><span class="sxs-lookup"><span data-stu-id="c97ad-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="c97ad-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="c97ad-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c97ad-152">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c97ad-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




