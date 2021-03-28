---
title: 'dcl_semantics (sm3-ps asm) '
description: 宣告頂點著色器輸出和圖元著色器輸入之間的關聯。
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092916"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="c5481-103">dcl \_ 語義 (sm3-ps asm) </span><span class="sxs-lookup"><span data-stu-id="c5481-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="c5481-104">宣告頂點著色器輸出和圖元著色器輸入之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="c5481-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5481-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5481-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="c5481-106">\_ \[ \_ 距心 \] dst 的 dcl 語義 \[ 。寫入 \_ 遮罩\]</span><span class="sxs-lookup"><span data-stu-id="c5481-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="c5481-107">其中：</span><span class="sxs-lookup"><span data-stu-id="c5481-107">Where:</span></span>

-   <span data-ttu-id="c5481-108">\_語義：識別預期的資料使用方式，而且可以是 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (中沒有 D3DDECLUSAGE 前置詞) 的任何值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c5481-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="c5481-109">此外，您可以將整數索引附加至語義，以區分使用類似語義的參數。</span><span class="sxs-lookup"><span data-stu-id="c5481-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="c5481-110">\[\_[距心](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \]這是選擇性的指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="c5481-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="c5481-111">在宣告輸入暫存器 \_ 和紋理查閱指示的 dcl 使用指示上支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c5481-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="c5481-112">距心會附加沒有空格的位置。</span><span class="sxs-lookup"><span data-stu-id="c5481-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="c5481-113">dst：目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="c5481-113">dst: destination register.</span></span> <span data-ttu-id="c5481-114">請參閱 [ps \_ 3 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)。</span><span class="sxs-lookup"><span data-stu-id="c5481-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="c5481-115">寫入 \_ 遮罩：相同的輸出暫存器可以多次宣告，每次都有唯一的寫入遮罩 (如此一來，就可以將不同的語義套用至) 的個別元件。</span><span class="sxs-lookup"><span data-stu-id="c5481-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="c5481-116">不過，在宣告中不能多次使用相同的語義。</span><span class="sxs-lookup"><span data-stu-id="c5481-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="c5481-117">這表示向量必須是四個或更少的元件，而且無法跨四個元件的暫存器界限 (個別的輸出暫存器) 。</span><span class="sxs-lookup"><span data-stu-id="c5481-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="c5481-118">\_使用 psize 語義時，它應該有完整的寫入遮罩，因為它會被視為純量。</span><span class="sxs-lookup"><span data-stu-id="c5481-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="c5481-119">\_使用位置語義時，它應該有完整的寫入遮罩，因為必須寫入全部四個元件。</span><span class="sxs-lookup"><span data-stu-id="c5481-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5481-120">備註</span><span class="sxs-lookup"><span data-stu-id="c5481-120">Remarks</span></span>



| <span data-ttu-id="c5481-121">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c5481-121">Pixel shader versions</span></span> | <span data-ttu-id="c5481-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="c5481-122">1\_1</span></span> | <span data-ttu-id="c5481-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="c5481-123">1\_2</span></span> | <span data-ttu-id="c5481-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c5481-124">1\_3</span></span> | <span data-ttu-id="c5481-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="c5481-125">1\_4</span></span> | <span data-ttu-id="c5481-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5481-126">2\_0</span></span> | <span data-ttu-id="c5481-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c5481-127">2\_x</span></span> | <span data-ttu-id="c5481-128">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c5481-128">2\_sw</span></span> | <span data-ttu-id="c5481-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5481-129">3\_0</span></span> | <span data-ttu-id="c5481-130">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c5481-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c5481-131">dcl \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="c5481-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="c5481-132">x</span><span class="sxs-lookup"><span data-stu-id="c5481-132">x</span></span>    | <span data-ttu-id="c5481-133">x</span><span class="sxs-lookup"><span data-stu-id="c5481-133">x</span></span>     |



 

<span data-ttu-id="c5481-134">所有 \_ 的 dcl 使用方式指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="c5481-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="c5481-135">宣告範例</span><span class="sxs-lookup"><span data-stu-id="c5481-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="c5481-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5481-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5481-137">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c5481-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="c5481-138">[消除鋸齒範例](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="c5481-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 