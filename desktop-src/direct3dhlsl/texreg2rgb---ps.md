---
title: texreg2rgb-ps
description: 將來源暫存器的紅色、綠色和藍色 (RGB) 色彩元件，轉譯為紋理位址資料，以便在對應至目的地暫存器編號的階段取樣材質。 結果會儲存在目的地註冊中。
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507720"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="cc354-104">texreg2rgb-ps</span><span class="sxs-lookup"><span data-stu-id="cc354-104">texreg2rgb - ps</span></span>

<span data-ttu-id="cc354-105">將來源暫存器的紅色、綠色和藍色 (RGB) 色彩元件，轉譯為紋理位址資料，以便在對應至目的地暫存器編號的階段取樣材質。</span><span class="sxs-lookup"><span data-stu-id="cc354-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="cc354-106">結果會儲存在目的地註冊中。</span><span class="sxs-lookup"><span data-stu-id="cc354-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc354-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc354-107">Syntax</span></span>



| <span data-ttu-id="cc354-108">texreg2rgb dst、src</span><span class="sxs-lookup"><span data-stu-id="cc354-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="cc354-109">其中</span><span class="sxs-lookup"><span data-stu-id="cc354-109">where</span></span>

-   <span data-ttu-id="cc354-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="cc354-110">dst is the destination register.</span></span>
-   <span data-ttu-id="cc354-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="cc354-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc354-112">備註</span><span class="sxs-lookup"><span data-stu-id="cc354-112">Remarks</span></span>



| <span data-ttu-id="cc354-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="cc354-113">Pixel shader versions</span></span> | <span data-ttu-id="cc354-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc354-114">1\_1</span></span> | <span data-ttu-id="cc354-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="cc354-115">1\_2</span></span> | <span data-ttu-id="cc354-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cc354-116">1\_3</span></span> | <span data-ttu-id="cc354-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="cc354-117">1\_4</span></span> | <span data-ttu-id="cc354-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc354-118">2\_0</span></span> | <span data-ttu-id="cc354-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc354-119">2\_x</span></span> | <span data-ttu-id="cc354-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cc354-120">2\_sw</span></span> | <span data-ttu-id="cc354-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc354-121">3\_0</span></span> | <span data-ttu-id="cc354-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cc354-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cc354-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="cc354-123">texreg2rgb</span></span>            |      | <span data-ttu-id="cc354-124">x</span><span class="sxs-lookup"><span data-stu-id="cc354-124">x</span></span>    | <span data-ttu-id="cc354-125">x</span><span class="sxs-lookup"><span data-stu-id="cc354-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="cc354-126">此指示適用于色彩空間重新對應作業。</span><span class="sxs-lookup"><span data-stu-id="cc354-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="cc354-127">它支援二維 (2D) 和三維 (3D) 座標。</span><span class="sxs-lookup"><span data-stu-id="cc354-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="cc354-128">它的使用方式就像是 [texreg2ar-ps](texreg2ar---ps.md) 或 [texreg2gb-ps](texreg2gb---ps.md) ，可重新對應2d 資料。</span><span class="sxs-lookup"><span data-stu-id="cc354-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="cc354-129">不過，此指示也支援3D 資料，因此可用於 cube 地圖和3D 音量材質。</span><span class="sxs-lookup"><span data-stu-id="cc354-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="cc354-130">以下是指示的順序範例。</span><span class="sxs-lookup"><span data-stu-id="cc354-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="cc354-131">以下是如何完成重新對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cc354-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="cc354-132">第一個指令會將材質色彩 (RGBA) 載入至 register tn</span><span class="sxs-lookup"><span data-stu-id="cc354-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="cc354-133">tex tn</span><span class="sxs-lookup"><span data-stu-id="cc354-133">tex tn</span></span>  
<span data-ttu-id="cc354-134">第二個指令會重新對應色彩</span><span class="sxs-lookup"><span data-stu-id="cc354-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="cc354-135">t (m) <sub>rgba</sub> = TextureSample (階段 m) <sub>RGBA</sub> 使用 t (n) <sub>RGB</sub> 作為座標</span><span class="sxs-lookup"><span data-stu-id="cc354-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="cc354-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc354-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc354-137">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="cc354-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




