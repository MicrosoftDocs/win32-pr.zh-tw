---
title: texreg2ar-ps
description: 將來源註冊的 Alpha 和紅色元件以材質位址資料的形式轉譯 (u，v) ，以在對應至目的地暫存器編號的階段取樣紋理。 結果會儲存在目的地註冊中。
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463313"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="6e21c-104">texreg2ar-ps</span><span class="sxs-lookup"><span data-stu-id="6e21c-104">texreg2ar - ps</span></span>

<span data-ttu-id="6e21c-105">將來源註冊的 Alpha 和紅色元件以材質位址資料的形式轉譯 (u，v) ，以在對應至目的地暫存器編號的階段取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="6e21c-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="6e21c-106">結果會儲存在目的地註冊中。</span><span class="sxs-lookup"><span data-stu-id="6e21c-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e21c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e21c-107">Syntax</span></span>



| <span data-ttu-id="6e21c-108">texreg2ar dst、src</span><span class="sxs-lookup"><span data-stu-id="6e21c-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="6e21c-109">其中</span><span class="sxs-lookup"><span data-stu-id="6e21c-109">where</span></span>

-   <span data-ttu-id="6e21c-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="6e21c-110">dst is the destination register.</span></span>
-   <span data-ttu-id="6e21c-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="6e21c-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e21c-112">備註</span><span class="sxs-lookup"><span data-stu-id="6e21c-112">Remarks</span></span>



| <span data-ttu-id="6e21c-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="6e21c-113">Pixel shader versions</span></span> | <span data-ttu-id="6e21c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="6e21c-114">1\_1</span></span> | <span data-ttu-id="6e21c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="6e21c-115">1\_2</span></span> | <span data-ttu-id="6e21c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6e21c-116">1\_3</span></span> | <span data-ttu-id="6e21c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="6e21c-117">1\_4</span></span> | <span data-ttu-id="6e21c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6e21c-118">2\_0</span></span> | <span data-ttu-id="6e21c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6e21c-119">2\_x</span></span> | <span data-ttu-id="6e21c-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6e21c-120">2\_sw</span></span> | <span data-ttu-id="6e21c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6e21c-121">3\_0</span></span> | <span data-ttu-id="6e21c-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6e21c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6e21c-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="6e21c-123">texreg2ar</span></span>             | <span data-ttu-id="6e21c-124">x</span><span class="sxs-lookup"><span data-stu-id="6e21c-124">x</span></span>    | <span data-ttu-id="6e21c-125">x</span><span class="sxs-lookup"><span data-stu-id="6e21c-125">x</span></span>    | <span data-ttu-id="6e21c-126">x</span><span class="sxs-lookup"><span data-stu-id="6e21c-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="6e21c-127">此指示適用于色彩空間重新對應作業。</span><span class="sxs-lookup"><span data-stu-id="6e21c-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="6e21c-128">以下是指示所遵循的順序範例：</span><span class="sxs-lookup"><span data-stu-id="6e21c-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="6e21c-129">tex t (n) </span><span class="sxs-lookup"><span data-stu-id="6e21c-129">tex t(n)</span></span>  
<span data-ttu-id="6e21c-130">texreg2ar t (m) ，t (n) ，其中 m > n</span><span class="sxs-lookup"><span data-stu-id="6e21c-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="6e21c-131">第一個指令會將材質色彩載入 (RGBA) </span><span class="sxs-lookup"><span data-stu-id="6e21c-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="6e21c-132">進入 register tn</span><span class="sxs-lookup"><span data-stu-id="6e21c-132">// into register tn</span></span>  
<span data-ttu-id="6e21c-133">tex tn</span><span class="sxs-lookup"><span data-stu-id="6e21c-133">tex tn</span></span>  
<span data-ttu-id="6e21c-134">第二個指令會重新對應色彩</span><span class="sxs-lookup"><span data-stu-id="6e21c-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="6e21c-135">t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 t (n) <sub>AR</sub> 作為座標</span><span class="sxs-lookup"><span data-stu-id="6e21c-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="6e21c-136">\_bx2 不能用在 src register for texreg2ar 或 [texreg2gb-ps](texreg2gb---ps.md) 指令。</span><span class="sxs-lookup"><span data-stu-id="6e21c-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="6e21c-137">針對此指示，來源登錄必須使用未簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="6e21c-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="6e21c-138">在來源註冊中使用已簽署或混合的資料將會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="6e21c-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="6e21c-139">如需詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。</span><span class="sxs-lookup"><span data-stu-id="6e21c-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e21c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e21c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e21c-141">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="6e21c-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 