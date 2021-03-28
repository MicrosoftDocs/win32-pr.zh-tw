---
title: 目的地註冊遮罩
description: 遮罩會指定將會以指示的結果更新目的地登錄的哪些元件。 材質暫存器有一組規則，而 noNtexture 暫存器有另一組規則。
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372401"
---
# <a name="destination-register-masking"></a><span data-ttu-id="62ade-104">目的地註冊遮罩</span><span class="sxs-lookup"><span data-stu-id="62ade-104">Destination Register Masking</span></span>

<span data-ttu-id="62ade-105">遮罩會指定將會以指示的結果更新目的地登錄的哪些元件。</span><span class="sxs-lookup"><span data-stu-id="62ade-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="62ade-106">材質暫存器有一組規則，而 noNtexture 暫存器有另一組規則。</span><span class="sxs-lookup"><span data-stu-id="62ade-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="62ade-107">dx9 \_ 圖形 \_ 參考 \_ asm 與登錄修飾詞 \_ \_ \_ \_ 遮罩-本節包含將遮罩套用至目的地暫存器的規則。</span><span class="sxs-lookup"><span data-stu-id="62ade-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="62ade-108">材質暫存器 \_ \_ 遮罩-材質暫存器有一些獨特的規則。</span><span class="sxs-lookup"><span data-stu-id="62ade-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="62ade-109">目的地註冊遮罩</span><span class="sxs-lookup"><span data-stu-id="62ade-109">Destination Register Masking</span></span>

<span data-ttu-id="62ade-110">如下表所示，遮罩 (其中是其中一個有效的頂點著色器 [頂點著色器](dx9-graphics-reference-asm-vs-registers.md) ，) 可以套用至向量資料的個別元件。</span><span class="sxs-lookup"><span data-stu-id="62ade-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="62ade-111">元件修飾詞</span><span class="sxs-lookup"><span data-stu-id="62ade-111">Component modifier</span></span> | <span data-ttu-id="62ade-112">Description</span><span class="sxs-lookup"><span data-stu-id="62ade-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="62ade-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="62ade-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="62ade-114">目的地遮罩</span><span class="sxs-lookup"><span data-stu-id="62ade-114">Destination mask</span></span> |



 

-   <span data-ttu-id="62ade-115">一般來說，指定目的地登錄寫入遮罩是很好的編碼樣式。</span><span class="sxs-lookup"><span data-stu-id="62ade-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="62ade-116">它讓程式碼更容易讀取和維護。</span><span class="sxs-lookup"><span data-stu-id="62ade-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="62ade-117">您可以指定任何元件組合 (包括 [無]) ，只要 x 在 y 之前、y 在 z 之前、y 到 z 之前，z 就會在 w 之前。</span><span class="sxs-lookup"><span data-stu-id="62ade-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="62ade-118">選擇和 oFog 輸出暫存器必須只使用一個遮罩。</span><span class="sxs-lookup"><span data-stu-id="62ade-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="62ade-119">某些指示需要目的地登錄才能使用單一寫入遮罩： exp、expp、log、logp、pow、rcp 和 rsq。</span><span class="sxs-lookup"><span data-stu-id="62ade-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="62ade-120">在1.0 版中，frc 指令必須有下列其中一個遮罩組合：. x 或. y 或 xy。</span><span class="sxs-lookup"><span data-stu-id="62ade-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="62ade-121">2.0 版沒有遮罩限制。</span><span class="sxs-lookup"><span data-stu-id="62ade-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="62ade-122">sincos 需要下列其中一個遮罩組合：. x 或. y 或 xyz。</span><span class="sxs-lookup"><span data-stu-id="62ade-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="62ade-123">m3x2 需要 xy 寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="62ade-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="62ade-124">m3x3 和 m4x3 需要 xyz 寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="62ade-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="62ade-125">m3x4 和 m4x4 需要 .xyz 寫入遮罩或預設寫入遮罩 (xyzw) 。</span><span class="sxs-lookup"><span data-stu-id="62ade-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="62ade-126">材質暫存器遮罩</span><span class="sxs-lookup"><span data-stu-id="62ade-126">Texture Register Masks</span></span>

<span data-ttu-id="62ade-127">在紋理座標暫存器上使用修飾詞的驗證規則，比其他暫存器的驗證規則更緊密。</span><span class="sxs-lookup"><span data-stu-id="62ade-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="62ade-128">如果寫入 oTn，所有先前的暫存器 (oTn-1 ~ oT0) 也必須撰寫。</span><span class="sxs-lookup"><span data-stu-id="62ade-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="62ade-129">任何 oT 註冊的「合併」寫入遮罩 \# 必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="62ade-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="62ade-130">.x</span><span class="sxs-lookup"><span data-stu-id="62ade-130">.x</span></span>
    -   <span data-ttu-id="62ade-131">xy</span><span class="sxs-lookup"><span data-stu-id="62ade-131">.xy</span></span>
    -   <span data-ttu-id="62ade-132">.xyz</span><span class="sxs-lookup"><span data-stu-id="62ade-132">.xyz</span></span>
    -   <span data-ttu-id="62ade-133">xyzw (，這相當於不使用任何元件修飾詞) </span><span class="sxs-lookup"><span data-stu-id="62ade-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="62ade-134">例如，頂點著色器可以個別的指示輸出至材質暫存器。</span><span class="sxs-lookup"><span data-stu-id="62ade-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="62ade-135">或者，您可以結合指令。</span><span class="sxs-lookup"><span data-stu-id="62ade-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="62ade-136">這些限制僅適用于材質座標暫存器。</span><span class="sxs-lookup"><span data-stu-id="62ade-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62ade-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="62ade-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62ade-138">頂點著色器暫存器修飾詞</span><span class="sxs-lookup"><span data-stu-id="62ade-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




