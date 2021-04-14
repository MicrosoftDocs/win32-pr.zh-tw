---
title: texcrd-ps
description: 將材質座標資料從來源材質座標反覆運算器註冊複製為目的地暫存器中的色彩資料。
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990923"
---
# <a name="texcrd---ps"></a><span data-ttu-id="554b4-103">texcrd-ps</span><span class="sxs-lookup"><span data-stu-id="554b4-103">texcrd - ps</span></span>

<span data-ttu-id="554b4-104">將材質座標資料從來源材質座標反覆運算器註冊複製為目的地暫存器中的色彩資料。</span><span class="sxs-lookup"><span data-stu-id="554b4-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="554b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="554b4-105">Syntax</span></span>



| <span data-ttu-id="554b4-106">texcrd dst、src</span><span class="sxs-lookup"><span data-stu-id="554b4-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="554b4-107">其中</span><span class="sxs-lookup"><span data-stu-id="554b4-107">where</span></span>

-   <span data-ttu-id="554b4-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="554b4-108">dst is the destination register.</span></span>
-   <span data-ttu-id="554b4-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="554b4-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="554b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="554b4-110">Remarks</span></span>



| <span data-ttu-id="554b4-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="554b4-111">Pixel shader versions</span></span> | <span data-ttu-id="554b4-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="554b4-112">1\_1</span></span> | <span data-ttu-id="554b4-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="554b4-113">1\_2</span></span> | <span data-ttu-id="554b4-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="554b4-114">1\_3</span></span> | <span data-ttu-id="554b4-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="554b4-115">1\_4</span></span> | <span data-ttu-id="554b4-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="554b4-116">2\_0</span></span> | <span data-ttu-id="554b4-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="554b4-117">2\_x</span></span> | <span data-ttu-id="554b4-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="554b4-118">2\_sw</span></span> | <span data-ttu-id="554b4-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="554b4-119">3\_0</span></span> | <span data-ttu-id="554b4-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="554b4-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="554b4-121">texcrd</span><span class="sxs-lookup"><span data-stu-id="554b4-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="554b4-122">x</span><span class="sxs-lookup"><span data-stu-id="554b4-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="554b4-123">此指令會將座標資料解讀為色彩資料 (RGBA) 。</span><span class="sxs-lookup"><span data-stu-id="554b4-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="554b4-124">此指令未取樣任何紋理。</span><span class="sxs-lookup"><span data-stu-id="554b4-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="554b4-125">只有在此材質階段設定的材質座標是相關的。</span><span class="sxs-lookup"><span data-stu-id="554b4-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="554b4-126">使用 texcrd 時，請記住下列有關如何將資料從來源暫存器複製到目的地登錄的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="554b4-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="554b4-127">來源材質座標暫存器 (t \#) 將資料存放在 D3DCAPS9 範圍內 \[ 。MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat \] ，而目的地登錄 (r \#) 只能將資料存放在 (可能較小) 範圍 \[ D3DCAPS9。PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue \] 。</span><span class="sxs-lookup"><span data-stu-id="554b4-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="554b4-128">請注意，對於圖元著色器第1版 \_ ，D3DCAPS9。PixelShader1xMaxValue 必須至少為8。</span><span class="sxs-lookup"><span data-stu-id="554b4-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="554b4-129">Texcrd 指令在固定來源資料超出目的地登錄範圍的過程中，可能會在不同的硬體上有不同的行為。</span><span class="sxs-lookup"><span data-stu-id="554b4-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="554b4-130">市場上第1個圖元著色器第 1 \_ 4 個硬體，將會針對超出範圍的值執行特殊的夾具。</span><span class="sxs-lookup"><span data-stu-id="554b4-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="554b4-131">此夾具的設計目的是要產生可符合目的地暫存器的數位，但也可以保留超出範圍資料的材質定址行為 (查看 [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) 如果資料後續用於紋理取樣。</span><span class="sxs-lookup"><span data-stu-id="554b4-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="554b4-132">不過，不同製造商的新硬體可能不會顯示這種行為，而且可能只會切割資料以符合目的地暫存器範圍。</span><span class="sxs-lookup"><span data-stu-id="554b4-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="554b4-133">因此，使用圖元著色器第1版 texcrd 時，最安全的動作 \_ 就是將材質座標資料僅提供給已在8到8範圍內的圖元著色器， \[ \] 如此您就不會依賴硬體個的方式。</span><span class="sxs-lookup"><span data-stu-id="554b4-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="554b4-134">不同于 texcoord \_ ，texcrd 不會在0和1之間進行值的夾具。</span><span class="sxs-lookup"><span data-stu-id="554b4-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="554b4-135">使用 texcrd 的規則：</span><span class="sxs-lookup"><span data-stu-id="554b4-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="554b4-136">在 texcrd 或 texld 指令中，每次讀取個別 t (n) 註冊時，都必須套用相同的 xyz 或 xyw 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="554b4-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="554b4-137">在所有情況下，texcrd 的第四個通道結果都是未設定/未定義。</span><span class="sxs-lookup"><span data-stu-id="554b4-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="554b4-138">Xyw dw 案例的第三個通道未設定/未定義 \_ 。</span><span class="sxs-lookup"><span data-stu-id="554b4-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="554b4-139">範例</span><span class="sxs-lookup"><span data-stu-id="554b4-139">Examples</span></span>

<span data-ttu-id="554b4-140">以下顯示一組完整的 texcrd 語法，其中會將所有有效的來源修飾詞/選取器和目的地寫入遮罩組合納入考慮。</span><span class="sxs-lookup"><span data-stu-id="554b4-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="554b4-141">請注意，您可以交換使用 rgba 和. xyzw 標記法。</span><span class="sxs-lookup"><span data-stu-id="554b4-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="554b4-142">將材質座標反覆運算器註冊的前三個通道（t (n) ）複製到 r (m) 。</span><span class="sxs-lookup"><span data-stu-id="554b4-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="554b4-143">R (m) 的第四個通道未初始化。</span><span class="sxs-lookup"><span data-stu-id="554b4-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="554b4-144">將 t (n) 的第一個、第二個和第四個元件放置於 r (m) 的前三個通道中。</span><span class="sxs-lookup"><span data-stu-id="554b4-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="554b4-145">R (m) 的第四個通道未初始化。</span><span class="sxs-lookup"><span data-stu-id="554b4-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="554b4-146">以下是使用 dw 修飾詞的 projective 除法範例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="554b4-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="554b4-147">此範例會將 x/w 和 y/w 從 t (n) 複製到 r (m) 的前兩個通道中。</span><span class="sxs-lookup"><span data-stu-id="554b4-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="554b4-148">R (m) 的第三個和第四個通道未初始化。</span><span class="sxs-lookup"><span data-stu-id="554b4-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="554b4-149">先前寫入 r (m) 的第三個通道的任何資料將會遺失。</span><span class="sxs-lookup"><span data-stu-id="554b4-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="554b4-150">R (m) 的第四個通道中的資料會因為階段標記而遺失。</span><span class="sxs-lookup"><span data-stu-id="554b4-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="554b4-151">若為第1版 \_ ，則 \_ 會忽略 D3DTTFF 投射旗標。</span><span class="sxs-lookup"><span data-stu-id="554b4-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="554b4-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="554b4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="554b4-153">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="554b4-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 