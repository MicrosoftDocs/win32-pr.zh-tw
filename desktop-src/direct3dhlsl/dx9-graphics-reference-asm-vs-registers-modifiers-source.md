---
title: 頂點著色器來源登錄修飾詞
description: 您可以套用來源修飾詞，以修改指令使用資料之前，從來源暫存器讀取的資料。
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372400"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="456f8-103">頂點著色器來源登錄修飾詞</span><span class="sxs-lookup"><span data-stu-id="456f8-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="456f8-104">您可以套用來源修飾詞，以修改指令使用資料之前，從來源暫存器讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="456f8-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="456f8-105">Negate</span><span class="sxs-lookup"><span data-stu-id="456f8-105">Negate</span></span>

<span data-ttu-id="456f8-106">否定來源暫存器的內容。</span><span class="sxs-lookup"><span data-stu-id="456f8-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="456f8-107">元件修飾詞</span><span class="sxs-lookup"><span data-stu-id="456f8-107">Component modifier</span></span> | <span data-ttu-id="456f8-108">Description</span><span class="sxs-lookup"><span data-stu-id="456f8-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="456f8-109">\- R</span><span class="sxs-lookup"><span data-stu-id="456f8-109">\- r</span></span>               | <span data-ttu-id="456f8-110">來源否定</span><span class="sxs-lookup"><span data-stu-id="456f8-110">Source negation</span></span> |



 

<span data-ttu-id="456f8-111">不能在這些指示的第二個來源登錄上使用否定修飾詞： [m3x2-vs](m3x2---vs.md)、 [m3x3-vs](m3x3---vs.md)、 [m3x4-vs](m3x4---vs.md)、 [m4x3-vs](m4x3---vs.md)、 [m4x4-vs](m4x4---vs.md)。</span><span class="sxs-lookup"><span data-stu-id="456f8-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="456f8-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="456f8-112">Vertex shader versions</span></span> | <span data-ttu-id="456f8-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="456f8-113">1\_1</span></span> | <span data-ttu-id="456f8-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="456f8-114">2\_0</span></span> | <span data-ttu-id="456f8-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="456f8-115">2\_x</span></span> | <span data-ttu-id="456f8-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="456f8-116">2\_sw</span></span> | <span data-ttu-id="456f8-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="456f8-117">3\_0</span></span> | <span data-ttu-id="456f8-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="456f8-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="456f8-119">x</span><span class="sxs-lookup"><span data-stu-id="456f8-119">x</span></span>    | <span data-ttu-id="456f8-120">x</span><span class="sxs-lookup"><span data-stu-id="456f8-120">x</span></span>    | <span data-ttu-id="456f8-121">x</span><span class="sxs-lookup"><span data-stu-id="456f8-121">x</span></span>    | <span data-ttu-id="456f8-122">x</span><span class="sxs-lookup"><span data-stu-id="456f8-122">x</span></span>     | <span data-ttu-id="456f8-123">x</span><span class="sxs-lookup"><span data-stu-id="456f8-123">x</span></span>    | <span data-ttu-id="456f8-124">x</span><span class="sxs-lookup"><span data-stu-id="456f8-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="456f8-125">絕對值</span><span class="sxs-lookup"><span data-stu-id="456f8-125">Absolute Value</span></span>

<span data-ttu-id="456f8-126">取得註冊的絕對值。</span><span class="sxs-lookup"><span data-stu-id="456f8-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="456f8-127">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="456f8-127">Vertex shader versions</span></span> | <span data-ttu-id="456f8-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="456f8-128">1\_1</span></span> | <span data-ttu-id="456f8-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="456f8-129">2\_0</span></span> | <span data-ttu-id="456f8-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="456f8-130">2\_x</span></span> | <span data-ttu-id="456f8-131">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="456f8-131">2\_sw</span></span> | <span data-ttu-id="456f8-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="456f8-132">3\_0</span></span> | <span data-ttu-id="456f8-133">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="456f8-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="456f8-134">abs</span><span class="sxs-lookup"><span data-stu-id="456f8-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="456f8-135">x</span><span class="sxs-lookup"><span data-stu-id="456f8-135">x</span></span>    | <span data-ttu-id="456f8-136">x</span><span class="sxs-lookup"><span data-stu-id="456f8-136">x</span></span>     |



 

<span data-ttu-id="456f8-137">如果任何第3版著色器從一或多個常數浮點數暫存器 (c \#) 讀取，下列其中一個條件必須為 true。</span><span class="sxs-lookup"><span data-stu-id="456f8-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="456f8-138">所有常數浮點數暫存器都必須使用 abs 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="456f8-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="456f8-139">沒有常數浮點數暫存器可以使用 abs 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="456f8-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="456f8-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="456f8-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="456f8-141">頂點著色器暫存器修飾詞</span><span class="sxs-lookup"><span data-stu-id="456f8-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




