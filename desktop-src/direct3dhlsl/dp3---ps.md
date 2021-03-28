---
title: dp3-ps
description: 計算來源註冊的三個元件點乘積。 |dp3-ps
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974076"
---
# <a name="dp3---ps"></a><span data-ttu-id="42ba9-104">dp3-ps</span><span class="sxs-lookup"><span data-stu-id="42ba9-104">dp3 - ps</span></span>

<span data-ttu-id="42ba9-105">計算來源註冊的三個元件點乘積。</span><span class="sxs-lookup"><span data-stu-id="42ba9-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ba9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="42ba9-106">Syntax</span></span>



| <span data-ttu-id="42ba9-107">dp3 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="42ba9-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="42ba9-108">其中</span><span class="sxs-lookup"><span data-stu-id="42ba9-108">where</span></span>

-   <span data-ttu-id="42ba9-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="42ba9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="42ba9-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="42ba9-110">src0 is a source register.</span></span>
-   <span data-ttu-id="42ba9-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="42ba9-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ba9-112">備註</span><span class="sxs-lookup"><span data-stu-id="42ba9-112">Remarks</span></span>



| <span data-ttu-id="42ba9-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="42ba9-113">Pixel shader versions</span></span> | <span data-ttu-id="42ba9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="42ba9-114">1\_1</span></span> | <span data-ttu-id="42ba9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="42ba9-115">1\_2</span></span> | <span data-ttu-id="42ba9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="42ba9-116">1\_3</span></span> | <span data-ttu-id="42ba9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="42ba9-117">1\_4</span></span> | <span data-ttu-id="42ba9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42ba9-118">2\_0</span></span> | <span data-ttu-id="42ba9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="42ba9-119">2\_x</span></span> | <span data-ttu-id="42ba9-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="42ba9-120">2\_sw</span></span> | <span data-ttu-id="42ba9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42ba9-121">3\_0</span></span> | <span data-ttu-id="42ba9-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="42ba9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="42ba9-123">dp3</span><span class="sxs-lookup"><span data-stu-id="42ba9-123">dp3</span></span>                   | <span data-ttu-id="42ba9-124">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-124">x</span></span>    | <span data-ttu-id="42ba9-125">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-125">x</span></span>    | <span data-ttu-id="42ba9-126">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-126">x</span></span>    | <span data-ttu-id="42ba9-127">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-127">x</span></span>    | <span data-ttu-id="42ba9-128">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-128">x</span></span>    | <span data-ttu-id="42ba9-129">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-129">x</span></span>    | <span data-ttu-id="42ba9-130">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-130">x</span></span>     | <span data-ttu-id="42ba9-131">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-131">x</span></span>    | <span data-ttu-id="42ba9-132">x</span><span class="sxs-lookup"><span data-stu-id="42ba9-132">x</span></span>     |



 

<span data-ttu-id="42ba9-133">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="42ba9-133">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



<span data-ttu-id="42ba9-134">此指令會在向量管線中執行，並一律寫出至色彩通道。</span><span class="sxs-lookup"><span data-stu-id="42ba9-134">This instruction runs in the vector pipeline, always writing out to the color channels.</span></span> <span data-ttu-id="42ba9-135">在第1版 \_ 中，此指令仍會使用向量管線，但可能會寫入至任何通道。</span><span class="sxs-lookup"><span data-stu-id="42ba9-135">For version 1\_4, this instruction still uses the vector pipeline but may write to any channel.</span></span>

<span data-ttu-id="42ba9-136">具有目的地 register 的指令 ( xyz) 寫入遮罩可與 dp3 共同發行，如下所示。</span><span class="sxs-lookup"><span data-stu-id="42ba9-136">An instruction with a destination register .rgb (.xyz) write mask may be co-issued with dp3 As shown below.</span></span>


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



<span data-ttu-id="42ba9-137">您可以使用「 [來源登錄」已簽署的調整](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) 輸入引數修飾詞 (\_ bx2) 套用至其輸入引數的 dp3 指令，如果它們尚未擴充至已簽署的動態範圍。</span><span class="sxs-lookup"><span data-stu-id="42ba9-137">The dp3 instruction can be modified using the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input argument modifier (\_bx2) applied to its input arguments if they are not already expanded to signed dynamic range.</span></span> <span data-ttu-id="42ba9-138">針對光源著色器， (sat) 的飽和指令修飾詞 \_ 通常會用來將負數值夾具至黑色，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="42ba9-138">For a lighting shader, the saturate instruction modifier (\_sat) is often used to clamp the negative values to black, as shown in the following example.</span></span>


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a><span data-ttu-id="42ba9-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="42ba9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42ba9-140">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="42ba9-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




