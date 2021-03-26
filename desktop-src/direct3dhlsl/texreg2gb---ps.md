---
title: texreg2gb-ps
description: 將來源註冊的綠色和藍色色彩元件解讀為材質位址資料，以在對應至目的地暫存器編號的階段取樣材質。
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971717"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="599b4-103">texreg2gb-ps</span><span class="sxs-lookup"><span data-stu-id="599b4-103">texreg2gb - ps</span></span>

<span data-ttu-id="599b4-104">將來源註冊的綠色和藍色色彩元件解讀為材質位址資料，以在對應至目的地暫存器編號的階段取樣材質。</span><span class="sxs-lookup"><span data-stu-id="599b4-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="599b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="599b4-105">Syntax</span></span>



| <span data-ttu-id="599b4-106">texreg2gb dst、src</span><span class="sxs-lookup"><span data-stu-id="599b4-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="599b4-107">其中</span><span class="sxs-lookup"><span data-stu-id="599b4-107">where</span></span>

-   <span data-ttu-id="599b4-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="599b4-108">dst is the destination register.</span></span>
-   <span data-ttu-id="599b4-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="599b4-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="599b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="599b4-110">Remarks</span></span>



| <span data-ttu-id="599b4-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="599b4-111">Pixel shader versions</span></span> | <span data-ttu-id="599b4-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="599b4-112">1\_1</span></span> | <span data-ttu-id="599b4-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="599b4-113">1\_2</span></span> | <span data-ttu-id="599b4-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="599b4-114">1\_3</span></span> | <span data-ttu-id="599b4-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="599b4-115">1\_4</span></span> | <span data-ttu-id="599b4-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="599b4-116">2\_0</span></span> | <span data-ttu-id="599b4-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="599b4-117">2\_x</span></span> | <span data-ttu-id="599b4-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="599b4-118">2\_sw</span></span> | <span data-ttu-id="599b4-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="599b4-119">3\_0</span></span> | <span data-ttu-id="599b4-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="599b4-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="599b4-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="599b4-121">texreg2gb</span></span>             |      | <span data-ttu-id="599b4-122">x</span><span class="sxs-lookup"><span data-stu-id="599b4-122">x</span></span>    | <span data-ttu-id="599b4-123">x</span><span class="sxs-lookup"><span data-stu-id="599b4-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="599b4-124">此指示適用于色彩空間重新對應作業。</span><span class="sxs-lookup"><span data-stu-id="599b4-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="599b4-125">以下是指示的順序範例。</span><span class="sxs-lookup"><span data-stu-id="599b4-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="599b4-126">tex t (n) </span><span class="sxs-lookup"><span data-stu-id="599b4-126">tex t(n)</span></span>  
<span data-ttu-id="599b4-127">texreg2gb t (m) ，t (n) ，其中 m > n</span><span class="sxs-lookup"><span data-stu-id="599b4-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="599b4-128">第一個指令會將材質色彩載入 (RGBA) </span><span class="sxs-lookup"><span data-stu-id="599b4-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="599b4-129">進入 register tn</span><span class="sxs-lookup"><span data-stu-id="599b4-129">// into register tn</span></span>  
<span data-ttu-id="599b4-130">tex tn</span><span class="sxs-lookup"><span data-stu-id="599b4-130">tex tn</span></span>  
<span data-ttu-id="599b4-131">第二個指令會重新對應色彩</span><span class="sxs-lookup"><span data-stu-id="599b4-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="599b4-132">t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 t (n) <sub>GB</sub> 作為座標</span><span class="sxs-lookup"><span data-stu-id="599b4-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="599b4-133">\_bx2 不能用於 [texreg2ar ps](texreg2ar---ps.md) 或 texreg2gb 指令的 src 暫存器。</span><span class="sxs-lookup"><span data-stu-id="599b4-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="599b4-134">針對此指示，來源登錄必須使用未簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="599b4-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="599b4-135">在來源註冊中使用已簽署或混合的資料將會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="599b4-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="599b4-136">如需詳細資訊，請參閱 [D3DFORMAT](/windows/desktop/direct3d9/d3dformat)。</span><span class="sxs-lookup"><span data-stu-id="599b4-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="599b4-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="599b4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="599b4-138">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="599b4-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 