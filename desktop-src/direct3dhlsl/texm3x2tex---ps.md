---
title: texm3x2tex-ps
description: 執行3x2 矩陣相乘的最後一個資料列，並使用結果來執行材質查閱。 texm3x2tex 必須搭配 texm3x2pad ps 指令使用。
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990770"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="6addb-104">texm3x2tex-ps</span><span class="sxs-lookup"><span data-stu-id="6addb-104">texm3x2tex - ps</span></span>

<span data-ttu-id="6addb-105">執行3x2 矩陣相乘的最後一個資料列，並使用結果來執行材質查閱。</span><span class="sxs-lookup"><span data-stu-id="6addb-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="6addb-106">texm3x2tex 必須搭配 [texm3x2pad ps](texm3x2pad---ps.md) 指令使用。</span><span class="sxs-lookup"><span data-stu-id="6addb-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6addb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6addb-107">Syntax</span></span>



| <span data-ttu-id="6addb-108">texm3x2tex dst、src</span><span class="sxs-lookup"><span data-stu-id="6addb-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="6addb-109">其中</span><span class="sxs-lookup"><span data-stu-id="6addb-109">where</span></span>

-   <span data-ttu-id="6addb-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="6addb-110">dst is the destination register.</span></span>
-   <span data-ttu-id="6addb-111">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="6addb-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6addb-112">備註</span><span class="sxs-lookup"><span data-stu-id="6addb-112">Remarks</span></span>



| <span data-ttu-id="6addb-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="6addb-113">Pixel shader versions</span></span> | <span data-ttu-id="6addb-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="6addb-114">1\_1</span></span> | <span data-ttu-id="6addb-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="6addb-115">1\_2</span></span> | <span data-ttu-id="6addb-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6addb-116">1\_3</span></span> | <span data-ttu-id="6addb-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="6addb-117">1\_4</span></span> | <span data-ttu-id="6addb-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6addb-118">2\_0</span></span> | <span data-ttu-id="6addb-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6addb-119">2\_x</span></span> | <span data-ttu-id="6addb-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6addb-120">2\_sw</span></span> | <span data-ttu-id="6addb-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6addb-121">3\_0</span></span> | <span data-ttu-id="6addb-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6addb-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6addb-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="6addb-123">texm3x2tex</span></span>            | <span data-ttu-id="6addb-124">x</span><span class="sxs-lookup"><span data-stu-id="6addb-124">x</span></span>    | <span data-ttu-id="6addb-125">x</span><span class="sxs-lookup"><span data-stu-id="6addb-125">x</span></span>    | <span data-ttu-id="6addb-126">x</span><span class="sxs-lookup"><span data-stu-id="6addb-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="6addb-127">指令會用來做為兩個表示3x2 矩陣乘法運算的指示之一。</span><span class="sxs-lookup"><span data-stu-id="6addb-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="6addb-128">此指令必須搭配 [texm3x2pad ps](texm3x2pad---ps.md) 指令使用。</span><span class="sxs-lookup"><span data-stu-id="6addb-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="6addb-129">當您使用這兩個指示時，材質暫存器必須使用下列順序。</span><span class="sxs-lookup"><span data-stu-id="6addb-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="6addb-130">以下是如何完成3x2 乘法的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6addb-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="6addb-131">Texm3x2pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="6addb-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="6addb-132">u<sup>'</sup> = t (n) <sub>RGB</sub> \* TextureCoordinates (階段 m) <sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="6addb-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="6addb-133">Texm3x2tex 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="6addb-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="6addb-134">v<sup>'</sup> = t (n) <sub>RGB</sub> \* TextureCoordinates (階段 m + 1) <sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="6addb-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="6addb-135">Texm3x2tex 指令會使用 (u<sup>'</sup>，v<sup>'</sup>) ，在階段 (m + 1) 的材質取樣，並將結果儲存在 t (m + 1) 中。</span><span class="sxs-lookup"><span data-stu-id="6addb-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="6addb-136">t (m + 1) <sub>RGB</sub> = TextureSample (階段 m + 1) <sub>RGB</sub> 使用 (u<sup>'</sup>，v<sup>'</sup> ) 作為座標</span><span class="sxs-lookup"><span data-stu-id="6addb-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="6addb-137">範例</span><span class="sxs-lookup"><span data-stu-id="6addb-137">Examples</span></span>

<span data-ttu-id="6addb-138">以下是已識別材質地圖和材質階段的範例著色器。</span><span class="sxs-lookup"><span data-stu-id="6addb-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="6addb-139">此範例需要下列紋理階段中的材質。</span><span class="sxs-lookup"><span data-stu-id="6addb-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="6addb-140">階段0採用的地圖具有 (x、y、z) 更動資料。</span><span class="sxs-lookup"><span data-stu-id="6addb-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="6addb-141">階段1保存材質座標。</span><span class="sxs-lookup"><span data-stu-id="6addb-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="6addb-142">紋理階段中不需要材質。</span><span class="sxs-lookup"><span data-stu-id="6addb-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="6addb-143">階段2同時保有紋理座標，以及該材質階段的2D 材質集。</span><span class="sxs-lookup"><span data-stu-id="6addb-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6addb-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="6addb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6addb-145">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="6addb-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




