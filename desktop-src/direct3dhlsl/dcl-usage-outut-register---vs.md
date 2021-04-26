---
title: 'dcl_usage output (sm1、sm2、sm3 與 asm) '
description: 各種類型的輸出暫存器已折迭為十二個輸出暫存器 (兩個用於色彩、八個用於材質、一個用於位置，另一個用於霧和點大小) 。
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999165"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="6fada-103">dcl \_ 使用方式輸出 (sm1、sm2、sm3-vs asm) </span><span class="sxs-lookup"><span data-stu-id="6fada-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="6fada-104">各種類型的輸出暫存器已折迭為十二個輸出暫存器 (兩個用於色彩、八個用於材質、一個用於位置，另一個用於霧和點大小) 。</span><span class="sxs-lookup"><span data-stu-id="6fada-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="6fada-105">這些可用於使用者想要插入圖元著色器的任何內容：材質座標、色彩、霧化等等。</span><span class="sxs-lookup"><span data-stu-id="6fada-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="6fada-106">輸出暫存器需要包含語義的宣告。</span><span class="sxs-lookup"><span data-stu-id="6fada-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="6fada-107">例如，藉由宣告具有位置或點大小語義的輸出暫存器，就會取代舊的位置和點大小暫存器。</span><span class="sxs-lookup"><span data-stu-id="6fada-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="6fada-108">在十二個輸出暫存器中，任何十個 (不一定 o0 至 o9) 有四個元件 (xyzw) ，另一個則必須宣告為 position (，而且也必須同時包含四個元件) ，也可以選擇性地將這四個元件全部包含在純量點大小。</span><span class="sxs-lookup"><span data-stu-id="6fada-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fada-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fada-109">Syntax</span></span>

<span data-ttu-id="6fada-110">宣告輸出暫存器的語法類似于輸入暫存器的宣告：</span><span class="sxs-lookup"><span data-stu-id="6fada-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="6fada-111">dcl \_ 語義 o \[ . 寫入 \_ 遮罩\]</span><span class="sxs-lookup"><span data-stu-id="6fada-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="6fada-112">其中：</span><span class="sxs-lookup"><span data-stu-id="6fada-112">Where:</span></span>

-   <span data-ttu-id="6fada-113">dcl \_ 語義可以使用與輸入宣告相同的一組語義。</span><span class="sxs-lookup"><span data-stu-id="6fada-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="6fada-114">語義名稱來自 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (，而且會與索引配對，例如 position3) 。</span><span class="sxs-lookup"><span data-stu-id="6fada-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="6fada-115">不使用 positiont0 語義時，一律必須有一個輸出暫存器，才能處理頂點。</span><span class="sxs-lookup"><span data-stu-id="6fada-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="6fada-116">Positiont0 語義和 pointsize0 語義是唯一的意義，只是允許從頂點到圖元著色器的連結。</span><span class="sxs-lookup"><span data-stu-id="6fada-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="6fada-117">若為具有流量控制的著色器，則會假設已宣告最糟的案例輸出。</span><span class="sxs-lookup"><span data-stu-id="6fada-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="6fada-118">如果著色器實際上未輸出它所宣告的內容，則不會 (預設值，因為流量控制) 。</span><span class="sxs-lookup"><span data-stu-id="6fada-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="6fada-119">o 是輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="6fada-119">o is an output register.</span></span> <span data-ttu-id="6fada-120">請 [參閱 \_ 輸出](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)暫存器。</span><span class="sxs-lookup"><span data-stu-id="6fada-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="6fada-121">寫入 \_ 遮罩表示可以多次宣告的相同輸出暫存器 (因此，每次都有唯一的寫入遮罩可將不同的語義套用至個別的元件) 。</span><span class="sxs-lookup"><span data-stu-id="6fada-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="6fada-122">不過，在宣告中不能多次使用相同的語義。</span><span class="sxs-lookup"><span data-stu-id="6fada-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="6fada-123">這表示向量必須是四個或更少的元件，且不能跨四個元件的暫存器界限 (個別的暫存器) 。</span><span class="sxs-lookup"><span data-stu-id="6fada-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="6fada-124">使用點大小語義時，它應該有完整的寫入遮罩，因為它會被視為純量。</span><span class="sxs-lookup"><span data-stu-id="6fada-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="6fada-125">使用位置語義時，它應該要有完整的寫入遮罩，因為必須寫入全部四個元件。</span><span class="sxs-lookup"><span data-stu-id="6fada-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fada-126">備註</span><span class="sxs-lookup"><span data-stu-id="6fada-126">Remarks</span></span>



| <span data-ttu-id="6fada-127">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="6fada-127">Vertex shader versions</span></span> | <span data-ttu-id="6fada-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fada-128">3\_0</span></span> | <span data-ttu-id="6fada-129">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6fada-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="6fada-130">dcl \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="6fada-130">dcl\_usage</span></span>             | <span data-ttu-id="6fada-131">x</span><span class="sxs-lookup"><span data-stu-id="6fada-131">x</span></span>    | <span data-ttu-id="6fada-132">x</span><span class="sxs-lookup"><span data-stu-id="6fada-132">x</span></span>     |



 

<span data-ttu-id="6fada-133">所有的 [dcl \_ 使用](dcl-usage-input-register---vs.md) 方式指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="6fada-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="6fada-134">宣告範例</span><span class="sxs-lookup"><span data-stu-id="6fada-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="6fada-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fada-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fada-136">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="6fada-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
