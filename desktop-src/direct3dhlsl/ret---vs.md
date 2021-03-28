---
title: ret-vs
description: 從副程式或 main 函數返回。
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313652"
---
# <a name="ret---vs"></a><span data-ttu-id="6fee4-103">ret-vs</span><span class="sxs-lookup"><span data-stu-id="6fee4-103">ret - vs</span></span>

<span data-ttu-id="6fee4-104">從副程式或 main 函數返回。</span><span class="sxs-lookup"><span data-stu-id="6fee4-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fee4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fee4-105">Syntax</span></span>



| <span data-ttu-id="6fee4-106">Ret</span><span class="sxs-lookup"><span data-stu-id="6fee4-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="6fee4-107">備註</span><span class="sxs-lookup"><span data-stu-id="6fee4-107">Remarks</span></span>



| <span data-ttu-id="6fee4-108">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="6fee4-108">Vertex shader versions</span></span> | <span data-ttu-id="6fee4-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fee4-109">1\_1</span></span> | <span data-ttu-id="6fee4-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fee4-110">2\_0</span></span> | <span data-ttu-id="6fee4-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fee4-111">2\_x</span></span> | <span data-ttu-id="6fee4-112">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6fee4-112">2\_sw</span></span> | <span data-ttu-id="6fee4-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fee4-113">3\_0</span></span> | <span data-ttu-id="6fee4-114">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6fee4-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="6fee4-115">Ret</span><span class="sxs-lookup"><span data-stu-id="6fee4-115">ret</span></span>                    |      | <span data-ttu-id="6fee4-116">x</span><span class="sxs-lookup"><span data-stu-id="6fee4-116">x</span></span>    | <span data-ttu-id="6fee4-117">x</span><span class="sxs-lookup"><span data-stu-id="6fee4-117">x</span></span>    | <span data-ttu-id="6fee4-118">x</span><span class="sxs-lookup"><span data-stu-id="6fee4-118">x</span></span>     | <span data-ttu-id="6fee4-119">x</span><span class="sxs-lookup"><span data-stu-id="6fee4-119">x</span></span>    | <span data-ttu-id="6fee4-120">x</span><span class="sxs-lookup"><span data-stu-id="6fee4-120">x</span></span>     |



 

<span data-ttu-id="6fee4-121">此指令會從傳回位址堆疊取得指示的位址，並繼續執行。</span><span class="sxs-lookup"><span data-stu-id="6fee4-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="6fee4-122">在 main 函式的情況下，此指令會停止著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="6fee4-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="6fee4-123">Ret 指令會使用一個頂點著色器指令位置。</span><span class="sxs-lookup"><span data-stu-id="6fee4-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="6fee4-124">如果著色器未包含任何副程式，則在 main 程式結尾使用 ret 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6fee4-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="6fee4-125">Main 程式或任何副程式中不允許有多個 return 語句，第一個 return 語句會被視為 main 程式或副程式的結尾。</span><span class="sxs-lookup"><span data-stu-id="6fee4-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fee4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fee4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fee4-127">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="6fee4-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




