---
title: vs_1_1
description: 深入瞭解 vs_1_1，這是一個可程式化的頂點著色器，由一組在頂點資料上操作的指令所組成。
ms.assetid: 54ad41d7-aaa4-4cf4-8834-47f10cd5425c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 78ea10e751fd7fe902b1631376e9eb2023d31c12
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011061"
---
# <a name="vs_1_1"></a><span data-ttu-id="b750c-103">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b750c-103">vs\_1\_1</span></span>

<span data-ttu-id="b750c-104">可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。</span><span class="sxs-lookup"><span data-stu-id="b750c-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="b750c-105">註冊將資料傳入和傳出 ALU。</span><span class="sxs-lookup"><span data-stu-id="b750c-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="b750c-106">您可以套用其他控制項來修改指令、結果，或寫出哪些資料。</span><span class="sxs-lookup"><span data-stu-id="b750c-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="b750c-107">[指示-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md) 包含可用指令的清單。</span><span class="sxs-lookup"><span data-stu-id="b750c-107">[Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="b750c-108">暫存器[-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)會列出頂點著色器 ALU 所使用的不同類型的暫存器。</span><span class="sxs-lookup"><span data-stu-id="b750c-108">[Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="b750c-109">[頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。</span><span class="sxs-lookup"><span data-stu-id="b750c-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="b750c-110">[頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。</span><span class="sxs-lookup"><span data-stu-id="b750c-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="b750c-111">[[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制讀取、複製或寫入哪些註冊元件。</span><span class="sxs-lookup"><span data-stu-id="b750c-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied or written.</span></span>
-   <span data-ttu-id="b750c-112">[目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。</span><span class="sxs-lookup"><span data-stu-id="b750c-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b750c-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b750c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b750c-114">頂點著色器</span><span class="sxs-lookup"><span data-stu-id="b750c-114">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




