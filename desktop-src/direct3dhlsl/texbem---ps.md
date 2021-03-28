---
title: texbem-ps
description: 套用假的凹凸環境對應轉換。 這是藉由使用 address 更動 data (du、dv) 和2D 凹凸環境矩陣來修改目的地暫存器的材質位址資料來完成。
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971720"
---
# <a name="texbem---ps"></a><span data-ttu-id="a1322-104">texbem-ps</span><span class="sxs-lookup"><span data-stu-id="a1322-104">texbem - ps</span></span>

<span data-ttu-id="a1322-105">套用假的凹凸環境對應轉換。</span><span class="sxs-lookup"><span data-stu-id="a1322-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="a1322-106">這是藉由使用 address 更動 data (du、dv) 和2D 凹凸環境矩陣來修改目的地暫存器的材質位址資料來完成。</span><span class="sxs-lookup"><span data-stu-id="a1322-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1322-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1322-107">Syntax</span></span>



| <span data-ttu-id="a1322-108">texbem dst、src</span><span class="sxs-lookup"><span data-stu-id="a1322-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="a1322-109">其中</span><span class="sxs-lookup"><span data-stu-id="a1322-109">where</span></span>

-   <span data-ttu-id="a1322-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="a1322-110">dst is the destination register.</span></span>
-   <span data-ttu-id="a1322-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="a1322-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1322-112">備註</span><span class="sxs-lookup"><span data-stu-id="a1322-112">Remarks</span></span>



| <span data-ttu-id="a1322-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="a1322-113">Pixel shader versions</span></span> | <span data-ttu-id="a1322-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a1322-114">1\_1</span></span> | <span data-ttu-id="a1322-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="a1322-115">1\_2</span></span> | <span data-ttu-id="a1322-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a1322-116">1\_3</span></span> | <span data-ttu-id="a1322-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="a1322-117">1\_4</span></span> | <span data-ttu-id="a1322-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1322-118">2\_0</span></span> | <span data-ttu-id="a1322-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a1322-119">2\_x</span></span> | <span data-ttu-id="a1322-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a1322-120">2\_sw</span></span> | <span data-ttu-id="a1322-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1322-121">3\_0</span></span> | <span data-ttu-id="a1322-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a1322-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a1322-123">texbem</span><span class="sxs-lookup"><span data-stu-id="a1322-123">texbem</span></span>                | <span data-ttu-id="a1322-124">x</span><span class="sxs-lookup"><span data-stu-id="a1322-124">x</span></span>    | <span data-ttu-id="a1322-125">x</span><span class="sxs-lookup"><span data-stu-id="a1322-125">x</span></span>    | <span data-ttu-id="a1322-126">x</span><span class="sxs-lookup"><span data-stu-id="a1322-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="a1322-127">Src 暫存器中的紅色和綠色色彩資料會解讀為更動資料 (du、dv) 。</span><span class="sxs-lookup"><span data-stu-id="a1322-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="a1322-128">此指令會使用2D 凹凸環境對應矩陣，轉換來源暫存器中的 red 和綠元件。</span><span class="sxs-lookup"><span data-stu-id="a1322-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="a1322-129">結果會新增至對應至目的地暫存器編號的材質座標集合，並用來取樣目前的材質階段。</span><span class="sxs-lookup"><span data-stu-id="a1322-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="a1322-130">這種作業一律會將 du 和 dv 解釋為帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="a1322-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="a1322-131">針對版本 1 \_ 0 和 1 \_ 1，輸入引數不允許 [來源登錄的已簽署調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) 輸入修飾詞 (\_ bx2) 。</span><span class="sxs-lookup"><span data-stu-id="a1322-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="a1322-132">當輸入紋理包含已簽署的格式資料時，此指令會產生已定義的結果。</span><span class="sxs-lookup"><span data-stu-id="a1322-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="a1322-133">只有當前兩個通道包含已簽署的資料時，混合格式資料才會運作。</span><span class="sxs-lookup"><span data-stu-id="a1322-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="a1322-134">如需有關介面格式的詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。</span><span class="sxs-lookup"><span data-stu-id="a1322-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="a1322-135">這可用於以位址更動為基礎的各種技術，包括假的每圖元環境對應和擴散光源 (的) 增加對應。</span><span class="sxs-lookup"><span data-stu-id="a1322-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="a1322-136">使用這個指令時，材質暫存器必須遵循下列順序。</span><span class="sxs-lookup"><span data-stu-id="a1322-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="a1322-137">在指令中完成的計算如下所示。</span><span class="sxs-lookup"><span data-stu-id="a1322-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="a1322-138">u ' = TextureCoordinates (階段 m) <sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (階段 m) \* t (n) <sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (階段 m) \* t (n) <sub>G</sub> v ' = TextureCoordinates (階段 m) <sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (階段 m) \* t (n) <sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (階段 \* <sub></sub> <sub></sub>) </span><span class="sxs-lookup"><span data-stu-id="a1322-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="a1322-139">使用 (u '，v ' ) 作為座標</span><span class="sxs-lookup"><span data-stu-id="a1322-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="a1322-140">無法稍後再讀取 texbem/ps 或 [texbeml ps](texbeml---ps.md) 指令讀取的資料，但另一個 texbem-ps 或 texbeml-ps 除外。</span><span class="sxs-lookup"><span data-stu-id="a1322-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="a1322-141">範例</span><span class="sxs-lookup"><span data-stu-id="a1322-141">Examples</span></span>

<span data-ttu-id="a1322-142">以下是已識別材質地圖和識別材質階段的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="a1322-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="a1322-143">texbem 需要下列材質階段中的材質。</span><span class="sxs-lookup"><span data-stu-id="a1322-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="a1322-144">階段0會指派具有 (du、dv) 更動資料的一種凹凸地圖。</span><span class="sxs-lookup"><span data-stu-id="a1322-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="a1322-145">階段1使用材質地圖與色彩資料。</span><span class="sxs-lookup"><span data-stu-id="a1322-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="a1322-146">此指令會在已取樣的材質階段上設定矩陣資料。</span><span class="sxs-lookup"><span data-stu-id="a1322-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="a1322-147">這不同于固定函式管線的功能，其中更動資料和矩陣會佔用相同的材質階段。</span><span class="sxs-lookup"><span data-stu-id="a1322-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1322-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1322-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1322-149">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="a1322-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 