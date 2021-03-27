---
title: '材質座標註冊 (HLSL PS 參考) '
description: 包含材質座標的圖元著色器輸入暫存器。
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104971628"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="53811-103">材質座標註冊 (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="53811-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="53811-104">包含材質座標的圖元著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="53811-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="53811-105">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="53811-105">Pixel shader versions</span></span>       | <span data-ttu-id="53811-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="53811-106">1\_1</span></span> | <span data-ttu-id="53811-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="53811-107">1\_2</span></span> | <span data-ttu-id="53811-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="53811-108">1\_3</span></span> | <span data-ttu-id="53811-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="53811-109">1\_4</span></span> | <span data-ttu-id="53811-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53811-110">2\_0</span></span> | <span data-ttu-id="53811-111">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="53811-111">2\_sw</span></span> | <span data-ttu-id="53811-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53811-112">2\_x</span></span> | <span data-ttu-id="53811-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53811-113">3\_0</span></span> | <span data-ttu-id="53811-114">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="53811-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="53811-115">材質座標註冊</span><span class="sxs-lookup"><span data-stu-id="53811-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="53811-116">x</span><span class="sxs-lookup"><span data-stu-id="53811-116">x</span></span>    | <span data-ttu-id="53811-117">x</span><span class="sxs-lookup"><span data-stu-id="53811-117">x</span></span>     | <span data-ttu-id="53811-118">x</span><span class="sxs-lookup"><span data-stu-id="53811-118">x</span></span>    | <span data-ttu-id="53811-119">x</span><span class="sxs-lookup"><span data-stu-id="53811-119">x</span></span>    | <span data-ttu-id="53811-120">x</span><span class="sxs-lookup"><span data-stu-id="53811-120">x</span></span>     |



 

<span data-ttu-id="53811-121">材質座標註冊包含材質座標資料。</span><span class="sxs-lookup"><span data-stu-id="53811-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="53811-122">使用紋理座標暫存器之前，必須先使用圖元著色器宣告來宣告。</span><span class="sxs-lookup"><span data-stu-id="53811-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="53811-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="53811-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="53811-124">此外，以下是材質座標註冊的一些其他屬性。</span><span class="sxs-lookup"><span data-stu-id="53811-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="53811-125">有八個圖元著色器紋理座標暫存器（t0 至 t7）。</span><span class="sxs-lookup"><span data-stu-id="53811-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="53811-126">這些是唯讀的暫存器。</span><span class="sxs-lookup"><span data-stu-id="53811-126">These are read-only registers.</span></span>
-   <span data-ttu-id="53811-127">它們包含從輸入頂點反覆運算的四個元件 RGBA 值。</span><span class="sxs-lookup"><span data-stu-id="53811-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="53811-128">它們包含從頂點資料中插入的高精確度、高動態範圍資料值。</span><span class="sxs-lookup"><span data-stu-id="53811-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="53811-129">系統會以觀點正確的插補來產生值。</span><span class="sxs-lookup"><span data-stu-id="53811-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="53811-130">資料是浮點精確度，並經過簽署。</span><span class="sxs-lookup"><span data-stu-id="53811-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="53811-131">單一指令中最多隻有一個。</span><span class="sxs-lookup"><span data-stu-id="53811-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="53811-132">著色器內的多個紋理座標暫存器讀取必須使用相同的 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)。</span><span class="sxs-lookup"><span data-stu-id="53811-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="53811-133">選擇性的局部有效位數修飾詞 \[ \_ pp \] 適用于相依讀取。</span><span class="sxs-lookup"><span data-stu-id="53811-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="53811-134">這是因為部分有效位數會影響涉及紋理座標註冊的算數運算。</span><span class="sxs-lookup"><span data-stu-id="53811-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="53811-135">它不會影響材質位址指示的精確度，因為它不會影響材質座標反覆運算器。</span><span class="sxs-lookup"><span data-stu-id="53811-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53811-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="53811-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53811-137">寄存 器</span><span class="sxs-lookup"><span data-stu-id="53811-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




