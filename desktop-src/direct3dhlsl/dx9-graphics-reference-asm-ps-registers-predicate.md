---
title: '述詞 register (HLSL PS 參考) '
description: 這個圖元著色器輸出暫存器包含每個通道的布林值。
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679220"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="5a8c7-103">述詞 register (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="5a8c7-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="5a8c7-104">這個圖元著色器輸出暫存器包含每個通道的布林值。</span><span class="sxs-lookup"><span data-stu-id="5a8c7-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="5a8c7-105">下列版本支援述詞註冊：</span><span class="sxs-lookup"><span data-stu-id="5a8c7-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="5a8c7-106">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="5a8c7-106">Pixel shader versions</span></span> | <span data-ttu-id="5a8c7-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="5a8c7-107">1\_1</span></span> | <span data-ttu-id="5a8c7-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="5a8c7-108">1\_2</span></span> | <span data-ttu-id="5a8c7-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5a8c7-109">1\_3</span></span> | <span data-ttu-id="5a8c7-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="5a8c7-110">1\_4</span></span> | <span data-ttu-id="5a8c7-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a8c7-111">2\_0</span></span> | <span data-ttu-id="5a8c7-112">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5a8c7-112">2\_sw</span></span> | <span data-ttu-id="5a8c7-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a8c7-113">2\_x</span></span> | <span data-ttu-id="5a8c7-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a8c7-114">3\_0</span></span> | <span data-ttu-id="5a8c7-115">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="5a8c7-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="5a8c7-116">述詞註冊</span><span class="sxs-lookup"><span data-stu-id="5a8c7-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="5a8c7-117">x</span><span class="sxs-lookup"><span data-stu-id="5a8c7-117">x</span></span>    | <span data-ttu-id="5a8c7-118">x</span><span class="sxs-lookup"><span data-stu-id="5a8c7-118">x</span></span>    | <span data-ttu-id="5a8c7-119">x</span><span class="sxs-lookup"><span data-stu-id="5a8c7-119">x</span></span>     |



 

<span data-ttu-id="5a8c7-120">以下是註冊屬性。</span><span class="sxs-lookup"><span data-stu-id="5a8c7-120">Here are the register properties.</span></span>



| <span data-ttu-id="5a8c7-121">註冊類型</span><span class="sxs-lookup"><span data-stu-id="5a8c7-121">Register type</span></span> | <span data-ttu-id="5a8c7-122">Count</span><span class="sxs-lookup"><span data-stu-id="5a8c7-122">Count</span></span> | <span data-ttu-id="5a8c7-123">R/W</span><span class="sxs-lookup"><span data-stu-id="5a8c7-123">R/W</span></span> | <span data-ttu-id="5a8c7-124">\# 讀取埠</span><span class="sxs-lookup"><span data-stu-id="5a8c7-124">\# Read ports</span></span> | <span data-ttu-id="5a8c7-125">\# 讀取/inst</span><span class="sxs-lookup"><span data-stu-id="5a8c7-125">\# Reads/inst</span></span> | <span data-ttu-id="5a8c7-126">維度</span><span class="sxs-lookup"><span data-stu-id="5a8c7-126">Dimension</span></span> | <span data-ttu-id="5a8c7-127">RelAddr</span><span class="sxs-lookup"><span data-stu-id="5a8c7-127">RelAddr</span></span> | <span data-ttu-id="5a8c7-128">Defaults</span><span class="sxs-lookup"><span data-stu-id="5a8c7-128">Defaults</span></span> | <span data-ttu-id="5a8c7-129">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="5a8c7-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="5a8c7-130">述詞 (p) </span><span class="sxs-lookup"><span data-stu-id="5a8c7-130">Predicate(p)</span></span>  | <span data-ttu-id="5a8c7-131">1</span><span class="sxs-lookup"><span data-stu-id="5a8c7-131">1</span></span>     | <span data-ttu-id="5a8c7-132">R/W</span><span class="sxs-lookup"><span data-stu-id="5a8c7-132">R/W</span></span> | <span data-ttu-id="5a8c7-133">1</span><span class="sxs-lookup"><span data-stu-id="5a8c7-133">1</span></span>             | <span data-ttu-id="5a8c7-134">1</span><span class="sxs-lookup"><span data-stu-id="5a8c7-134">1</span></span>             | <span data-ttu-id="5a8c7-135">4</span><span class="sxs-lookup"><span data-stu-id="5a8c7-135">4</span></span>         | <span data-ttu-id="5a8c7-136">N/A</span><span class="sxs-lookup"><span data-stu-id="5a8c7-136">N/A</span></span>     | <span data-ttu-id="5a8c7-137">無</span><span class="sxs-lookup"><span data-stu-id="5a8c7-137">None</span></span>     | <span data-ttu-id="5a8c7-138">N</span><span class="sxs-lookup"><span data-stu-id="5a8c7-138">N</span></span>            |



 

<span data-ttu-id="5a8c7-139">您可以使用 [setp 的 \_ 複合-ps](setp-comp---ps.md)來修改述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="5a8c7-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="5a8c7-140">此註冊沒有預設值;應用程式必須先設定註冊才能使用。</span><span class="sxs-lookup"><span data-stu-id="5a8c7-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a8c7-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a8c7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8c7-142">寄存 器</span><span class="sxs-lookup"><span data-stu-id="5a8c7-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




