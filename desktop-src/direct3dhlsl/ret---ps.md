---
title: ret-ps
description: 從傳回位址堆疊取得指示的位址，並繼續執行。 在 main 函式的情況下，此指令會停止著色器的執行。
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971545"
---
# <a name="ret---ps"></a><span data-ttu-id="a69f9-104">ret-ps</span><span class="sxs-lookup"><span data-stu-id="a69f9-104">ret - ps</span></span>

<span data-ttu-id="a69f9-105">從傳回位址堆疊取得指示的位址，並繼續執行。</span><span class="sxs-lookup"><span data-stu-id="a69f9-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="a69f9-106">在 main 函式的情況下，此指令會停止著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="a69f9-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="a69f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a69f9-107">Syntax</span></span>



| <span data-ttu-id="a69f9-108">Ret</span><span class="sxs-lookup"><span data-stu-id="a69f9-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="a69f9-109">備註</span><span class="sxs-lookup"><span data-stu-id="a69f9-109">Remarks</span></span>



| <span data-ttu-id="a69f9-110">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="a69f9-110">Pixel shader versions</span></span> | <span data-ttu-id="a69f9-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="a69f9-111">1\_1</span></span> | <span data-ttu-id="a69f9-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="a69f9-112">1\_2</span></span> | <span data-ttu-id="a69f9-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a69f9-113">1\_3</span></span> | <span data-ttu-id="a69f9-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="a69f9-114">1\_4</span></span> | <span data-ttu-id="a69f9-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a69f9-115">2\_0</span></span> | <span data-ttu-id="a69f9-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a69f9-116">2\_x</span></span> | <span data-ttu-id="a69f9-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a69f9-117">2\_sw</span></span> | <span data-ttu-id="a69f9-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a69f9-118">3\_0</span></span> | <span data-ttu-id="a69f9-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="a69f9-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a69f9-120">Ret</span><span class="sxs-lookup"><span data-stu-id="a69f9-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="a69f9-121">x</span><span class="sxs-lookup"><span data-stu-id="a69f9-121">x</span></span>    | <span data-ttu-id="a69f9-122">x</span><span class="sxs-lookup"><span data-stu-id="a69f9-122">x</span></span>     | <span data-ttu-id="a69f9-123">x</span><span class="sxs-lookup"><span data-stu-id="a69f9-123">x</span></span>    | <span data-ttu-id="a69f9-124">x</span><span class="sxs-lookup"><span data-stu-id="a69f9-124">x</span></span>     |



 

<span data-ttu-id="a69f9-125">此指令會從傳回位址堆疊取得指示的位址，並繼續執行。</span><span class="sxs-lookup"><span data-stu-id="a69f9-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="a69f9-126">在 main 函式的情況下，此指令會停止著色器的執行。</span><span class="sxs-lookup"><span data-stu-id="a69f9-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="a69f9-127">Ret 指令會使用一個頂點著色器指令位置。</span><span class="sxs-lookup"><span data-stu-id="a69f9-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="a69f9-128">如果著色器未包含任何副程式，則在 main 程式結尾使用 ret 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a69f9-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="a69f9-129">Main 程式或任何副程式中不允許有多個 return 語句，第一個 return 語句會被視為 main 程式或副程式的結尾。</span><span class="sxs-lookup"><span data-stu-id="a69f9-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a69f9-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="a69f9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a69f9-131">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="a69f9-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




