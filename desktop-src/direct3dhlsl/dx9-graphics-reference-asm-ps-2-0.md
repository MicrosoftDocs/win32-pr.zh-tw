---
title: ps_2_0
description: 可程式化的圖元著色器是由一組操作圖元資料的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971325"
---
# <a name="ps_2_0"></a><span data-ttu-id="2f3d1-105">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f3d1-105">ps\_2\_0</span></span>

<span data-ttu-id="2f3d1-106">可程式化的圖元著色器是由一組操作圖元資料的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="2f3d1-107">註冊將資料傳入和傳出 ALU。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="2f3d1-108">您可以套用其他控制項來修改指令、結果，或寫出哪些資料。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="2f3d1-109">[ps \_ 2 \_ 0 指示](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="2f3d1-110">[ps \_ 2 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) 會列出頂點著色器 ALU 所使用的不同類型的暫存器。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="2f3d1-111">[](dx9-graphics-reference-asm-ps-registers-modifiers.md)修飾詞用來修改指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="2f3d1-112">[目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) 會決定要寫入的目的地登錄元件。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="2f3d1-113">[圖元著色器來源暫存器](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) 修飾詞在執行指令之前，會改變來源暫存器資料。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="2f3d1-114">[[來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="2f3d1-115">指令計數</span><span class="sxs-lookup"><span data-stu-id="2f3d1-115">Instruction Count</span></span>

<span data-ttu-id="2f3d1-116">著色器具有最大指令計數的限制。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="2f3d1-117">指令插槽總數： 96 (64 算術和32材質) 。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="2f3d1-118">取樣器計數</span><span class="sxs-lookup"><span data-stu-id="2f3d1-118">Sampler Count</span></span>

<span data-ttu-id="2f3d1-119">可用的紋理取樣器數目是16。</span><span class="sxs-lookup"><span data-stu-id="2f3d1-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f3d1-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f3d1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f3d1-121">圖元著色器</span><span class="sxs-lookup"><span data-stu-id="2f3d1-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




