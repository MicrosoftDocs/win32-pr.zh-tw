---
title: vs_2_0
description: 可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971445"
---
# <a name="vs_2_0"></a><span data-ttu-id="8a7cc-105">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8a7cc-105">vs\_2\_0</span></span>

<span data-ttu-id="8a7cc-106">可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="8a7cc-107">註冊將資料傳入和傳出 ALU。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="8a7cc-108">您可以套用其他控制項來修改指令、結果，或寫出哪些資料。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="8a7cc-109">[指示-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="8a7cc-110">暫存器[-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md)會列出頂點著色器 ALU 所使用的不同類型的暫存器。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="8a7cc-111">[頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="8a7cc-112">[頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="8a7cc-113">[[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="8a7cc-114">[目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="8a7cc-115">指令計數</span><span class="sxs-lookup"><span data-stu-id="8a7cc-115">Instruction Count</span></span>

<span data-ttu-id="8a7cc-116">每個頂點著色器最多可以儲存256指令。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="8a7cc-117">執行的指令數目可能會更高 (因為迴圈/代表支援) ，且受 D3DCAPS9 限制。MaxVShaderInstructionsExecuted，至少應該是0xFFFF。</span><span class="sxs-lookup"><span data-stu-id="8a7cc-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a7cc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a7cc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a7cc-119">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="8a7cc-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




