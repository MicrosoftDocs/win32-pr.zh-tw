---
title: texdepth-ps
description: 計算要在此圖元的深度緩衝區比較測試中使用的深度值。
ms.assetid: f7128dbb-a5f3-4e95-b53b-7432439ae0c4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3eb5cd337108d08efee465c136adf1afb4921123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841640"
---
# <a name="texdepth---ps"></a><span data-ttu-id="e98e4-103">texdepth-ps</span><span class="sxs-lookup"><span data-stu-id="e98e4-103">texdepth - ps</span></span>

<span data-ttu-id="e98e4-104">計算要在此圖元的深度緩衝區比較測試中使用的深度值。</span><span class="sxs-lookup"><span data-stu-id="e98e4-104">Calculate depth values to be used in the depth buffer comparison test for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e98e4-105">Syntax</span></span>



| <span data-ttu-id="e98e4-106">texdepth dst</span><span class="sxs-lookup"><span data-stu-id="e98e4-106">texdepth dst</span></span> |
|--------------|



 

<span data-ttu-id="e98e4-107">其中</span><span class="sxs-lookup"><span data-stu-id="e98e4-107">where</span></span>

-   <span data-ttu-id="e98e4-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e98e4-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98e4-109">備註</span><span class="sxs-lookup"><span data-stu-id="e98e4-109">Remarks</span></span>



| <span data-ttu-id="e98e4-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e98e4-110">Pixel shader versions</span></span> | <span data-ttu-id="e98e4-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="e98e4-111">1\_1</span></span> | <span data-ttu-id="e98e4-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="e98e4-112">1\_2</span></span> | <span data-ttu-id="e98e4-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e98e4-113">1\_3</span></span> | <span data-ttu-id="e98e4-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="e98e4-114">1\_4</span></span> | <span data-ttu-id="e98e4-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e98e4-115">2\_0</span></span> | <span data-ttu-id="e98e4-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e98e4-116">2\_x</span></span> | <span data-ttu-id="e98e4-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e98e4-117">2\_sw</span></span> | <span data-ttu-id="e98e4-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e98e4-118">3\_0</span></span> | <span data-ttu-id="e98e4-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e98e4-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e98e4-120">texdepth</span><span class="sxs-lookup"><span data-stu-id="e98e4-120">texdepth</span></span>              |      |      |      | <span data-ttu-id="e98e4-121">x</span><span class="sxs-lookup"><span data-stu-id="e98e4-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="e98e4-122">此指令會在此圖元的深度緩衝區比較測試中使用 r5. r/r5. g。</span><span class="sxs-lookup"><span data-stu-id="e98e4-122">This instruction uses r5.r / r5.g in the depth buffer comparison test for this pixel.</span></span> <span data-ttu-id="e98e4-123">藍色和 Alpha 通道中的資料會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e98e4-123">The data in the blue and alpha channels is ignored.</span></span> <span data-ttu-id="e98e4-124">如果 r5 = 0，則是 r5. r/r5. g = 1.0 的結果。</span><span class="sxs-lookup"><span data-stu-id="e98e4-124">If r5.g = 0, the result of r5.r / r5.g = 1.0.</span></span>

<span data-ttu-id="e98e4-125">暫時登錄 r5 是此指令唯一可以使用的暫存器。</span><span class="sxs-lookup"><span data-stu-id="e98e4-125">Temporary register r5 is the only register that this instruction can use.</span></span>

<span data-ttu-id="e98e4-126">執行此指令之後，無法在著色器中使用暫時性登錄 r5。</span><span class="sxs-lookup"><span data-stu-id="e98e4-126">After executing this instruction, temporary register r5 is unavailable for additional use in the shader.</span></span>

<span data-ttu-id="e98e4-127">取樣時，使用此指令可排除較高解析度深度緩衝區的大部分優點。</span><span class="sxs-lookup"><span data-stu-id="e98e4-127">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="e98e4-128">因為圖元著色器每圖元執行一次，所以 [texm3x2depth-ps](texm3x2depth---ps.md) 或 texdepth 的單一深度值輸出將用於每個子圖元深度比較測試。</span><span class="sxs-lookup"><span data-stu-id="e98e4-128">Because the pixel shader runs once per pixel, the single depth value output by [texm3x2depth - ps](texm3x2depth---ps.md) or texdepth will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="examples"></a><span data-ttu-id="e98e4-129">範例</span><span class="sxs-lookup"><span data-stu-id="e98e4-129">Examples</span></span>

<span data-ttu-id="e98e4-130">以下是使用 texdepth 的範例。</span><span class="sxs-lookup"><span data-stu-id="e98e4-130">Here is an example using texdepth.</span></span>


```
ps_1_4              
texld  r0, t0        // Sample texture from texture stage 0 (dest 
                     //   register number) into r0
                     // Use texture coordinate data from t0
texcrd r1.rgb, t1    // Load a second set of texture coordinate data into r1
add    r5.rg, r0, r1 // Add the two sets of texture coordinate data
phase                // Phase marker, required when using texdepth instruction
texdepth  r5         // Calculate pixel depth as r5.r / r5.g
                     // Do other color calculations with shader output r0
```



## <a name="related-topics"></a><span data-ttu-id="e98e4-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="e98e4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e98e4-132">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e98e4-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




