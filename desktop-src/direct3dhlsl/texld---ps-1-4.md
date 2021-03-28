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
ms.openlocfilehash: 23827dffc396a40be134be4db3996d2e9f498288
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990795"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="676bd-104">texld-ps \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="676bd-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="676bd-105">使用來源登錄的內容作為材質座標，以色彩資料 (RGBA) 取樣來載入目的地暫存器。</span><span class="sxs-lookup"><span data-stu-id="676bd-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="676bd-106">取樣材質是與目的地暫存器編號相關聯的材質。</span><span class="sxs-lookup"><span data-stu-id="676bd-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="676bd-107">texld dst、src</span><span class="sxs-lookup"><span data-stu-id="676bd-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="676bd-108">暫存器</span><span class="sxs-lookup"><span data-stu-id="676bd-108">Registers</span></span>



| <span data-ttu-id="676bd-109">引數</span><span class="sxs-lookup"><span data-stu-id="676bd-109">Argument</span></span> | <span data-ttu-id="676bd-110">描述</span><span class="sxs-lookup"><span data-stu-id="676bd-110">Description</span></span>          | <span data-ttu-id="676bd-111">暫存器</span><span class="sxs-lookup"><span data-stu-id="676bd-111">Registers</span></span> |     |     |     | <span data-ttu-id="676bd-112">版本</span><span class="sxs-lookup"><span data-stu-id="676bd-112">Version</span></span>      |
|----------|----------------------|-----------|-----|-----|-----|--------------|
|          |                      | <span data-ttu-id="676bd-113">vn</span><span class="sxs-lookup"><span data-stu-id="676bd-113">vₙ</span></span>        | <span data-ttu-id="676bd-114">快遞 之 家</span><span class="sxs-lookup"><span data-stu-id="676bd-114">cₙ</span></span>  | <span data-ttu-id="676bd-115">Tn</span><span class="sxs-lookup"><span data-stu-id="676bd-115">tₙ</span></span>  | <span data-ttu-id="676bd-116">Rn</span><span class="sxs-lookup"><span data-stu-id="676bd-116">rₙ</span></span>  |              |
| <span data-ttu-id="676bd-117">Dst</span><span class="sxs-lookup"><span data-stu-id="676bd-117">dst</span></span>      | <span data-ttu-id="676bd-118">目的地註冊</span><span class="sxs-lookup"><span data-stu-id="676bd-118">Destination register</span></span> |           |     |     | <span data-ttu-id="676bd-119">x</span><span class="sxs-lookup"><span data-stu-id="676bd-119">x</span></span>   | <span data-ttu-id="676bd-120">1\_4</span><span class="sxs-lookup"><span data-stu-id="676bd-120">1\_4</span></span>         |
| <span data-ttu-id="676bd-121">src</span><span class="sxs-lookup"><span data-stu-id="676bd-121">src</span></span>      | <span data-ttu-id="676bd-122">來源註冊</span><span class="sxs-lookup"><span data-stu-id="676bd-122">Source register</span></span>      |           |     | <span data-ttu-id="676bd-123">x</span><span class="sxs-lookup"><span data-stu-id="676bd-123">x</span></span>   |     | <span data-ttu-id="676bd-124">1 \_ 4 階段1</span><span class="sxs-lookup"><span data-stu-id="676bd-124">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="676bd-125">x</span><span class="sxs-lookup"><span data-stu-id="676bd-125">x</span></span>   | <span data-ttu-id="676bd-126">x</span><span class="sxs-lookup"><span data-stu-id="676bd-126">x</span></span>   | <span data-ttu-id="676bd-127">1 \_ 4 階段</span><span class="sxs-lookup"><span data-stu-id="676bd-127">1\_4 phase</span></span>   |



 

<span data-ttu-id="676bd-128">使用 r (n) 作為來源暫存器時， (XYZ) 的前三個元件必須已在著色器的上一個階段中初始化。</span><span class="sxs-lookup"><span data-stu-id="676bd-128">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="676bd-129">若要深入瞭解註冊，請參閱[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)。</span><span class="sxs-lookup"><span data-stu-id="676bd-129">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="676bd-130">備註</span><span class="sxs-lookup"><span data-stu-id="676bd-130">Remarks</span></span>

<span data-ttu-id="676bd-131">此指令會在與目的地暫存器編號相關聯的材質階段中，填入材質的範例。</span><span class="sxs-lookup"><span data-stu-id="676bd-131">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="676bd-132">紋理會使用來自來源暫存器的材質座標資料進行取樣。</span><span class="sxs-lookup"><span data-stu-id="676bd-132">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="676bd-133">Texld 和 texcrd 指示的語法會公開支援使用材質暫存器修飾詞來分割。</span><span class="sxs-lookup"><span data-stu-id="676bd-133">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="676bd-134">針對圖元著色器1.4 版， \_ 一律會忽略 D3DTTFF 投射的材質轉換旗標。</span><span class="sxs-lookup"><span data-stu-id="676bd-134">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="676bd-135">使用 texld 的規則：</span><span class="sxs-lookup"><span data-stu-id="676bd-135">Rules for using texld:</span></span>

1.  <span data-ttu-id="676bd-136">相同的 xyw 修飾詞必須套用至每次讀取個別 t (n) 在 texcrd 或 texld 指令中進行註冊。</span><span class="sxs-lookup"><span data-stu-id="676bd-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="676bd-137">如果 xyw 是在 t (n) 登錄讀取，則可以使用 xyw dw 的相同 t (n) 註冊的其他讀取來混用。 \_</span><span class="sxs-lookup"><span data-stu-id="676bd-137">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="676bd-138">\_Dz 來源修飾詞只適用于 r (n) 來源登錄 (因此僅限第2階段) 的 texld。</span><span class="sxs-lookup"><span data-stu-id="676bd-138">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="676bd-139">\_每個著色器的使用次數不可超過兩次。</span><span class="sxs-lookup"><span data-stu-id="676bd-139">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="676bd-140">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="676bd-140">Pixel shader versions</span></span> | <span data-ttu-id="676bd-141">1\_1</span><span class="sxs-lookup"><span data-stu-id="676bd-141">1\_1</span></span> | <span data-ttu-id="676bd-142">1\_2</span><span class="sxs-lookup"><span data-stu-id="676bd-142">1\_2</span></span> | <span data-ttu-id="676bd-143">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="676bd-143">1\_3</span></span> | <span data-ttu-id="676bd-144">1\_4</span><span class="sxs-lookup"><span data-stu-id="676bd-144">1\_4</span></span> | <span data-ttu-id="676bd-145">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="676bd-145">2\_0</span></span> | <span data-ttu-id="676bd-146">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="676bd-146">2\_x</span></span> | <span data-ttu-id="676bd-147">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="676bd-147">2\_sw</span></span> | <span data-ttu-id="676bd-148">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="676bd-148">3\_0</span></span> | <span data-ttu-id="676bd-149">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="676bd-149">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="676bd-150">texld</span><span class="sxs-lookup"><span data-stu-id="676bd-150">texld</span></span>                 |      |      |      | <span data-ttu-id="676bd-151">x</span><span class="sxs-lookup"><span data-stu-id="676bd-151">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="676bd-152">範例</span><span class="sxs-lookup"><span data-stu-id="676bd-152">Examples</span></span>

<span data-ttu-id="676bd-153">Texld 指令可讓您控制要使用來源材質座標資料的元件。</span><span class="sxs-lookup"><span data-stu-id="676bd-153">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="676bd-154">Texld 的一組完整的允許語法如下所示，並包含所有有效的來源登錄修飾詞、選取器和寫入遮罩組合。</span><span class="sxs-lookup"><span data-stu-id="676bd-154">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="676bd-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="676bd-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="676bd-156">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="676bd-156">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




