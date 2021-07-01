---
title: 'dcl- (sm2、sm3-ps asm) '
description: 宣告圖元著色器輸入暫存器。
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130097"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="a32a7-103">dcl- (sm2、sm3-ps asm) </span><span class="sxs-lookup"><span data-stu-id="a32a7-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="a32a7-104">宣告圖元著色器輸入暫存器。</span><span class="sxs-lookup"><span data-stu-id="a32a7-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32a7-105">Syntax</span></span>

<span data-ttu-id="a32a7-106">dcl \[ \_ pp \] 目標 \[ . 遮罩\]</span><span class="sxs-lookup"><span data-stu-id="a32a7-106">dcl\[\_pp\] dest\[.mask\]</span></span>



 

<span data-ttu-id="a32a7-107">其中：</span><span class="sxs-lookup"><span data-stu-id="a32a7-107">Where:</span></span>

-   <span data-ttu-id="a32a7-108">\[\_pp \] 是選擇性的局部有效位數。</span><span class="sxs-lookup"><span data-stu-id="a32a7-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="a32a7-109">請參閱 [部分有效位數](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)。</span><span class="sxs-lookup"><span data-stu-id="a32a7-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="a32a7-110">dest 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="a32a7-110">dest is a destination register.</span></span> <span data-ttu-id="a32a7-111">它必須是 [輸入色彩](dx9-graphics-reference-asm-ps-registers-input-color.md) 暫存器 (vn) 或 [紋理座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) 。</span><span class="sxs-lookup"><span data-stu-id="a32a7-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="a32a7-112">\[mask \] 是選擇性的寫入遮罩，可控制可寫入目的地登錄的哪些元件。</span><span class="sxs-lookup"><span data-stu-id="a32a7-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="a32a7-113">請參閱 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)。</span><span class="sxs-lookup"><span data-stu-id="a32a7-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a32a7-114">備註</span><span class="sxs-lookup"><span data-stu-id="a32a7-114">Remarks</span></span>



| <span data-ttu-id="a32a7-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="a32a7-115">Pixel shader versions</span></span> | <span data-ttu-id="a32a7-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="a32a7-116">1\_1</span></span> | <span data-ttu-id="a32a7-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="a32a7-117">1\_2</span></span> | <span data-ttu-id="a32a7-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a32a7-118">1\_3</span></span> | <span data-ttu-id="a32a7-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="a32a7-119">1\_4</span></span> | <span data-ttu-id="a32a7-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a32a7-120">2\_0</span></span> | <span data-ttu-id="a32a7-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a32a7-121">2\_x</span></span> | <span data-ttu-id="a32a7-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a32a7-122">2\_sw</span></span> | <span data-ttu-id="a32a7-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a32a7-123">3\_0</span></span> | <span data-ttu-id="a32a7-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a32a7-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a32a7-125">dcl</span><span class="sxs-lookup"><span data-stu-id="a32a7-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="a32a7-126">x</span><span class="sxs-lookup"><span data-stu-id="a32a7-126">x</span></span>    | <span data-ttu-id="a32a7-127">x</span><span class="sxs-lookup"><span data-stu-id="a32a7-127">x</span></span>    | <span data-ttu-id="a32a7-128">x</span><span class="sxs-lookup"><span data-stu-id="a32a7-128">x</span></span>     | <span data-ttu-id="a32a7-129">x</span><span class="sxs-lookup"><span data-stu-id="a32a7-129">x</span></span>    | <span data-ttu-id="a32a7-130">x</span><span class="sxs-lookup"><span data-stu-id="a32a7-130">x</span></span>     |



 

<span data-ttu-id="a32a7-131">所有的 dcl 指令都必須出現在第一個可執行指令之前。</span><span class="sxs-lookup"><span data-stu-id="a32a7-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a32a7-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="a32a7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a32a7-133">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="a32a7-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




