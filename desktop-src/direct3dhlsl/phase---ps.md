---
title: 階段-ps
description: 階段指令會標示第1階段和第2階段之間的轉換。 如果沒有任何階段指令，則整個著色器的執行方式就如同第2階段著色器。
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022847"
---
# <a name="phase---ps"></a><span data-ttu-id="07d9b-104">階段-ps</span><span class="sxs-lookup"><span data-stu-id="07d9b-104">phase - ps</span></span>

<span data-ttu-id="07d9b-105">階段指令會標示第1階段和第2階段之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="07d9b-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="07d9b-106">如果沒有任何階段指令，則整個著色器的執行方式就如同第2階段著色器。</span><span class="sxs-lookup"><span data-stu-id="07d9b-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="07d9b-107">此指令僅適用于第1版 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07d9b-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="07d9b-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="07d9b-109">備註</span><span class="sxs-lookup"><span data-stu-id="07d9b-109">Remarks</span></span>



| <span data-ttu-id="07d9b-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="07d9b-110">Pixel shader versions</span></span> | <span data-ttu-id="07d9b-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="07d9b-111">1\_1</span></span> | <span data-ttu-id="07d9b-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="07d9b-112">1\_2</span></span> | <span data-ttu-id="07d9b-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="07d9b-113">1\_3</span></span> | <span data-ttu-id="07d9b-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="07d9b-114">1\_4</span></span> | <span data-ttu-id="07d9b-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07d9b-115">2\_0</span></span> | <span data-ttu-id="07d9b-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="07d9b-116">2\_x</span></span> | <span data-ttu-id="07d9b-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="07d9b-117">2\_sw</span></span> | <span data-ttu-id="07d9b-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07d9b-118">3\_0</span></span> | <span data-ttu-id="07d9b-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="07d9b-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="07d9b-120">階段</span><span class="sxs-lookup"><span data-stu-id="07d9b-120">phase</span></span>                 |      |      |      | <span data-ttu-id="07d9b-121">x</span><span class="sxs-lookup"><span data-stu-id="07d9b-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="07d9b-122">階段指令之前發生的著色器指示是階段1指示。</span><span class="sxs-lookup"><span data-stu-id="07d9b-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="07d9b-123">所有其他指示都是階段2指示。</span><span class="sxs-lookup"><span data-stu-id="07d9b-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="07d9b-124">有兩個指示的階段，每個著色器的指令數目上限就會增加。</span><span class="sxs-lookup"><span data-stu-id="07d9b-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="07d9b-125">階段轉換的副作用是， [暫存](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) 暫存器的 Alpha 元件不會跨轉換保存。</span><span class="sxs-lookup"><span data-stu-id="07d9b-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="07d9b-126">換句話說，Alpha 元件必須在階段指令之後重新初始化。</span><span class="sxs-lookup"><span data-stu-id="07d9b-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="07d9b-127">範例</span><span class="sxs-lookup"><span data-stu-id="07d9b-127">Example</span></span>

<span data-ttu-id="07d9b-128">此範例示範如何將指令群組為著色器內的第1階段或第2階段指令。</span><span class="sxs-lookup"><span data-stu-id="07d9b-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="07d9b-129">階段指令通常也稱為階段標記，因為它會標示第1階段和第2個指令之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="07d9b-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="07d9b-130">在第1版的 \_ 圖元著色器中，如果階段標記不存在，就會以第2階段執行著色器。</span><span class="sxs-lookup"><span data-stu-id="07d9b-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="07d9b-131">這點很重要，因為階段1和2的指示之間有差異，並註冊可用性。</span><span class="sxs-lookup"><span data-stu-id="07d9b-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="07d9b-132">所有參考部分都會注明差異。</span><span class="sxs-lookup"><span data-stu-id="07d9b-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="07d9b-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="07d9b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d9b-134">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="07d9b-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




