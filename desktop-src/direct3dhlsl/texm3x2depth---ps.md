---
title: texm3x2depth-ps
description: 計算要用於此圖元深度測試的深度值。
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971565"
---
# <a name="texm3x2depth---ps"></a><span data-ttu-id="36745-103">texm3x2depth-ps</span><span class="sxs-lookup"><span data-stu-id="36745-103">texm3x2depth - ps</span></span>

<span data-ttu-id="36745-104">計算要用於此圖元深度測試的深度值。</span><span class="sxs-lookup"><span data-stu-id="36745-104">Calculate the depth value to be used in depth testing for this pixel.</span></span>

## <a name="syntax"></a><span data-ttu-id="36745-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36745-105">Syntax</span></span>



| <span data-ttu-id="36745-106">texm3x2depth dst、src</span><span class="sxs-lookup"><span data-stu-id="36745-106">texm3x2depth dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="36745-107">其中</span><span class="sxs-lookup"><span data-stu-id="36745-107">where</span></span>

-   <span data-ttu-id="36745-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="36745-108">dst is the destination register.</span></span>
-   <span data-ttu-id="36745-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="36745-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="36745-110">備註</span><span class="sxs-lookup"><span data-stu-id="36745-110">Remarks</span></span>



| <span data-ttu-id="36745-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="36745-111">Pixel shader versions</span></span> | <span data-ttu-id="36745-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="36745-112">1\_1</span></span> | <span data-ttu-id="36745-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="36745-113">1\_2</span></span> | <span data-ttu-id="36745-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="36745-114">1\_3</span></span> | <span data-ttu-id="36745-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="36745-115">1\_4</span></span> | <span data-ttu-id="36745-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="36745-116">2\_0</span></span> | <span data-ttu-id="36745-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="36745-117">2\_x</span></span> | <span data-ttu-id="36745-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="36745-118">2\_sw</span></span> | <span data-ttu-id="36745-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="36745-119">3\_0</span></span> | <span data-ttu-id="36745-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="36745-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="36745-121">texm3x2depth</span><span class="sxs-lookup"><span data-stu-id="36745-121">texm3x2depth</span></span>          |      |      | <span data-ttu-id="36745-122">x</span><span class="sxs-lookup"><span data-stu-id="36745-122">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="36745-123">此指令必須搭配 [texm3x2pad ps](texm3x2pad---ps.md) 指令使用。</span><span class="sxs-lookup"><span data-stu-id="36745-123">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="36745-124">當您使用這兩個指示時，材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="36745-124">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



<span data-ttu-id="36745-125">深度計算是在使用點乘積運算來尋找 z 和 w 之後完成。</span><span class="sxs-lookup"><span data-stu-id="36745-125">The depth calculation is done after using a dot product operation to find z and w.</span></span> <span data-ttu-id="36745-126">以下是如何完成深度計算的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36745-126">Here is more detail about how the depth calculation is accomplished.</span></span>

<span data-ttu-id="36745-127">Texm3x2pad 指令會計算 z。</span><span class="sxs-lookup"><span data-stu-id="36745-127">The texm3x2pad instruction calculates z.</span></span>

<span data-ttu-id="36745-128">z = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="36745-128">z = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="36745-129">Texm3x2depth 指令會計算 w。</span><span class="sxs-lookup"><span data-stu-id="36745-129">The texm3x2depth instruction calculates w.</span></span>

<span data-ttu-id="36745-130">w = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="36745-130">w = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="36745-131">計算深度並將結果儲存在 t (m + 1) 。</span><span class="sxs-lookup"><span data-stu-id="36745-131">Calculate depth and store the result in t(m+1).</span></span>


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



<span data-ttu-id="36745-132">計算的深度會標記為要用於圖元的深度測試，並取代圖元的現有深度測試值。</span><span class="sxs-lookup"><span data-stu-id="36745-132">The calculated depth is tagged to be used in the depth test for the pixel, replacing the existing depth test value for the pixel.</span></span>

<span data-ttu-id="36745-133">請務必將 z/w 夾具在 (0-1) 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="36745-133">Be sure to clamp z/w to be in the range of (0-1).</span></span> <span data-ttu-id="36745-134">如果 z/w 超出此範圍，則儲存在深度緩衝區的結果將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="36745-134">If z/w is outside this range, the result stored in the depth buffer will be undefined.</span></span>

<span data-ttu-id="36745-135">執行 texm3x2depth 之後，請註冊 t (m + 1) 不再適用于著色器。</span><span class="sxs-lookup"><span data-stu-id="36745-135">After running texm3x2depth, register t(m+1) is no longer available for use in the shader.</span></span>

<span data-ttu-id="36745-136">取樣時，使用此指令可排除較高解析度深度緩衝區的大部分優點。</span><span class="sxs-lookup"><span data-stu-id="36745-136">When multisampling, using this instruction eliminates most of the benefit of the higher resolution depth buffer.</span></span> <span data-ttu-id="36745-137">因為圖元著色器每圖元執行一次，所以 texm3x2depth 或 [texdepth](texdepth---ps.md) 的單一深度值輸出將用於每個子圖元深度比較測試。</span><span class="sxs-lookup"><span data-stu-id="36745-137">Because the pixel shader runs once per pixel, the single depth value output by texm3x2depth or [texdepth - ps](texdepth---ps.md) will be used for each of the subpixel depth comparison tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36745-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="36745-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36745-139">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="36745-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




