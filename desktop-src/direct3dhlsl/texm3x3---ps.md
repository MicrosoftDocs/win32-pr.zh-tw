---
title: texm3x3-ps
description: 當與兩個 texm3x3pad ps 指令搭配使用時，會執行3x3 矩陣乘法。
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971549"
---
# <a name="texm3x3---ps"></a><span data-ttu-id="04848-103">texm3x3-ps</span><span class="sxs-lookup"><span data-stu-id="04848-103">texm3x3 - ps</span></span>

<span data-ttu-id="04848-104">當與兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令搭配使用時，會執行3x3 矩陣乘法。</span><span class="sxs-lookup"><span data-stu-id="04848-104">Performs a 3x3 matrix multiply when used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="04848-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04848-105">Syntax</span></span>



| <span data-ttu-id="04848-106">texm3x3 dst、src</span><span class="sxs-lookup"><span data-stu-id="04848-106">texm3x3 dst, src</span></span> |
|------------------|



 

<span data-ttu-id="04848-107">其中</span><span class="sxs-lookup"><span data-stu-id="04848-107">where</span></span>

-   <span data-ttu-id="04848-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="04848-108">dst is the destination register.</span></span>
-   <span data-ttu-id="04848-109">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="04848-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="04848-110">備註</span><span class="sxs-lookup"><span data-stu-id="04848-110">Remarks</span></span>



| <span data-ttu-id="04848-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="04848-111">Pixel shader versions</span></span> | <span data-ttu-id="04848-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="04848-112">1\_1</span></span> | <span data-ttu-id="04848-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="04848-113">1\_2</span></span> | <span data-ttu-id="04848-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="04848-114">1\_3</span></span> | <span data-ttu-id="04848-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="04848-115">1\_4</span></span> | <span data-ttu-id="04848-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04848-116">2\_0</span></span> | <span data-ttu-id="04848-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="04848-117">2\_x</span></span> | <span data-ttu-id="04848-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="04848-118">2\_sw</span></span> | <span data-ttu-id="04848-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04848-119">3\_0</span></span> | <span data-ttu-id="04848-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="04848-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="04848-121">texm3x3</span><span class="sxs-lookup"><span data-stu-id="04848-121">texm3x3</span></span>               |      | <span data-ttu-id="04848-122">x</span><span class="sxs-lookup"><span data-stu-id="04848-122">x</span></span>    | <span data-ttu-id="04848-123">x</span><span class="sxs-lookup"><span data-stu-id="04848-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="04848-124">此指示與 [texm3x3tex ps](texm3x3tex---ps.md) 指令相同，不需要材質查閱。</span><span class="sxs-lookup"><span data-stu-id="04848-124">This instruction is the same as the [texm3x3tex - ps](texm3x3tex---ps.md) instruction, without the texture lookup.</span></span>

<span data-ttu-id="04848-125">此指令會當做三個指示的最後三個指示使用，表示3x3 矩陣乘法運算。</span><span class="sxs-lookup"><span data-stu-id="04848-125">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation.</span></span> <span data-ttu-id="04848-126">3x3 矩陣是由第三個材質階段的材質座標，以及兩個先前的材質階段所組成。</span><span class="sxs-lookup"><span data-stu-id="04848-126">The 3x3 matrix is comprised of the texture coordinates of the third texture stage, and by the two preceding texture stages.</span></span> <span data-ttu-id="04848-127">任何指派給三個材質階段的材質都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="04848-127">Any texture assigned to any of the three texture stages is ignored.</span></span>

<span data-ttu-id="04848-128">此指令必須搭配兩個 texm3x3pad 指令使用。</span><span class="sxs-lookup"><span data-stu-id="04848-128">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="04848-129">材質暫存器必須遵循下列順序。</span><span class="sxs-lookup"><span data-stu-id="04848-129">Texture registers must follow the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



<span data-ttu-id="04848-130">以下是有關3x3 乘法如何完成的更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="04848-130">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="04848-131">第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="04848-131">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="04848-132">u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="04848-132">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="04848-133">第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="04848-133">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="04848-134">v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="04848-134">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="04848-135">Texm3x3tex 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。</span><span class="sxs-lookup"><span data-stu-id="04848-135">The texm3x3tex instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="04848-136">w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="04848-136">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="04848-137">將矩陣相乘的結果放在目的地暫存器中。</span><span class="sxs-lookup"><span data-stu-id="04848-137">Place the result of the matrix multiply in the destination register.</span></span>

<span data-ttu-id="04848-138">t (m + 2) <sub>RGBA</sub> = (u<sup>'</sup> 、v<sup>'</sup> 、w<sup>'</sup> 、1) </span><span class="sxs-lookup"><span data-stu-id="04848-138">t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)</span></span>

## <a name="related-topics"></a><span data-ttu-id="04848-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="04848-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04848-140">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="04848-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




