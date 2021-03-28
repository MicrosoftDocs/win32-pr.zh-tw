---
title: texbeml-ps
description: 套用具有亮度校正的假凸塊環境對應轉換。 這是藉由使用位址更動資料 (du、dv) 、2D 凹凸環境矩陣和亮度來修改目的地註冊的材質位址資料來完成。
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933564"
---
# <a name="texbeml---ps"></a><span data-ttu-id="7eef4-104">texbeml-ps</span><span class="sxs-lookup"><span data-stu-id="7eef4-104">texbeml - ps</span></span>

<span data-ttu-id="7eef4-105">套用具有亮度校正的假凸塊環境對應轉換。</span><span class="sxs-lookup"><span data-stu-id="7eef4-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="7eef4-106">這是藉由使用位址更動資料 (du、dv) 、2D 凹凸環境矩陣和亮度來修改目的地註冊的材質位址資料來完成。</span><span class="sxs-lookup"><span data-stu-id="7eef4-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eef4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eef4-107">Syntax</span></span>



| <span data-ttu-id="7eef4-108">texbeml dst、src</span><span class="sxs-lookup"><span data-stu-id="7eef4-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="7eef4-109">其中</span><span class="sxs-lookup"><span data-stu-id="7eef4-109">where</span></span>

-   <span data-ttu-id="7eef4-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="7eef4-110">dst is the destination register.</span></span>
-   <span data-ttu-id="7eef4-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="7eef4-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eef4-112">備註</span><span class="sxs-lookup"><span data-stu-id="7eef4-112">Remarks</span></span>



| <span data-ttu-id="7eef4-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="7eef4-113">Pixel shader versions</span></span> | <span data-ttu-id="7eef4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="7eef4-114">1\_1</span></span> | <span data-ttu-id="7eef4-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="7eef4-115">1\_2</span></span> | <span data-ttu-id="7eef4-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7eef4-116">1\_3</span></span> | <span data-ttu-id="7eef4-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="7eef4-117">1\_4</span></span> | <span data-ttu-id="7eef4-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7eef4-118">2\_0</span></span> | <span data-ttu-id="7eef4-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7eef4-119">2\_x</span></span> | <span data-ttu-id="7eef4-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="7eef4-120">2\_sw</span></span> | <span data-ttu-id="7eef4-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7eef4-121">3\_0</span></span> | <span data-ttu-id="7eef4-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="7eef4-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7eef4-123">texbeml</span><span class="sxs-lookup"><span data-stu-id="7eef4-123">texbeml</span></span>               | <span data-ttu-id="7eef4-124">x</span><span class="sxs-lookup"><span data-stu-id="7eef4-124">x</span></span>    | <span data-ttu-id="7eef4-125">x</span><span class="sxs-lookup"><span data-stu-id="7eef4-125">x</span></span>    | <span data-ttu-id="7eef4-126">x</span><span class="sxs-lookup"><span data-stu-id="7eef4-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="7eef4-127">Src 暫存器中的紅色和綠色色彩資料會解讀為更動資料 (du、dv) 。</span><span class="sxs-lookup"><span data-stu-id="7eef4-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="7eef4-128">Src 暫存器中的藍色資料會被視為亮度資料。</span><span class="sxs-lookup"><span data-stu-id="7eef4-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="7eef4-129">此指令會使用2D 凹凸環境對應矩陣來轉換來源暫存器中的紅色和綠色元件。</span><span class="sxs-lookup"><span data-stu-id="7eef4-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="7eef4-130">結果會新增至對應至目的地暫存器編號的材質座標集合。</span><span class="sxs-lookup"><span data-stu-id="7eef4-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="7eef4-131">使用亮度值和偏差紋理階段值來套用亮度校正。</span><span class="sxs-lookup"><span data-stu-id="7eef4-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="7eef4-132">結果會用來取樣目前的材質階段。</span><span class="sxs-lookup"><span data-stu-id="7eef4-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="7eef4-133">這可用於根據地址更動的各種技術，例如假的每圖元環境對應。</span><span class="sxs-lookup"><span data-stu-id="7eef4-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="7eef4-134">這種作業一律會將 du 和 dv 解釋為帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="7eef4-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="7eef4-135">針對版本 1 \_ 0 和 1 \_ 1，輸入引數不允許 [來源登錄的已簽署調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) 輸入修飾詞 (\_ bx2) 。</span><span class="sxs-lookup"><span data-stu-id="7eef4-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="7eef4-136">當輸入紋理包含混合的格式資料時，此指令會產生已定義的結果。</span><span class="sxs-lookup"><span data-stu-id="7eef4-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="7eef4-137">如需有關介面格式的詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。</span><span class="sxs-lookup"><span data-stu-id="7eef4-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="7eef4-138">此範例顯示在指令中完成的計算。</span><span class="sxs-lookup"><span data-stu-id="7eef4-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="7eef4-139">u ' = TextureCoordinates (階段 m) <sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="7eef4-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="7eef4-140">D3DTSS \_ BUMPENVMAT00 (階段 m) \* t (n) <sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="7eef4-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="7eef4-141">D3DTSS \_ BUMPENVMAT10 (階段 m) \* t (n) <sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="7eef4-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="7eef4-142">v ' = TextureCoordinates (階段 m) <sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="7eef4-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="7eef4-143">D3DTSS \_ BUMPENVMAT01 (階段 m) \* t (n) <sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="7eef4-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="7eef4-144">D3DTSS \_ BUMPENVMAT11 (階段 m) \* t (n) <sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="7eef4-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="7eef4-145">t (m) <sub>RGBA</sub> = TextureSample (階段 m) 使用 (u '，v ' ) 作為座標</span><span class="sxs-lookup"><span data-stu-id="7eef4-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="7eef4-146">t (m) <sub>rgba</sub> = t (m) <sub>RGBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="7eef4-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="7eef4-147">\[ (t (n) <sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (階段 m) ) +</span><span class="sxs-lookup"><span data-stu-id="7eef4-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="7eef4-148">D3DTSS \_ BUMPENVLOFFSET (階段 m) \]</span><span class="sxs-lookup"><span data-stu-id="7eef4-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="7eef4-149">除了其他 texbem 或 texbeml 之外，無法稍後再讀取 [texbem](texbem---ps.md) 或 texbeml 指令讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="7eef4-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="7eef4-150">範例</span><span class="sxs-lookup"><span data-stu-id="7eef4-150">Examples</span></span>

<span data-ttu-id="7eef4-151">以下是已識別材質地圖和識別材質階段的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="7eef4-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="7eef4-152">此範例需要下列紋理階段中的材質。</span><span class="sxs-lookup"><span data-stu-id="7eef4-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="7eef4-153">階段0會指派具有 (du、dv) 更動資料的一種凹凸地圖。</span><span class="sxs-lookup"><span data-stu-id="7eef4-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="7eef4-154">第1階段會指派具有色彩資料的材質地圖。</span><span class="sxs-lookup"><span data-stu-id="7eef4-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="7eef4-155">texbeml 會在已取樣的材質階段上設定矩陣資料。</span><span class="sxs-lookup"><span data-stu-id="7eef4-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="7eef4-156">這不同于固定函式管線的功能，其中更動資料和矩陣會佔用相同的材質階段。</span><span class="sxs-lookup"><span data-stu-id="7eef4-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7eef4-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="7eef4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eef4-158">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="7eef4-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 