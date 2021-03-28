---
title: '述詞 Register (HLSL 與參考) '
description: 此頂點著色器輸出暫存器包含每個通道的布林值。
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104022870"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="9eda9-103">述詞 Register (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="9eda9-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="9eda9-104">此頂點著色器輸出暫存器包含每個通道的布林值。</span><span class="sxs-lookup"><span data-stu-id="9eda9-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="9eda9-105">下列版本支援述詞註冊。</span><span class="sxs-lookup"><span data-stu-id="9eda9-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="9eda9-106">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="9eda9-106">Vertex shader versions</span></span> | <span data-ttu-id="9eda9-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="9eda9-107">1\_1</span></span> | <span data-ttu-id="9eda9-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9eda9-108">2\_0</span></span> | <span data-ttu-id="9eda9-109">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9eda9-109">2\_sw</span></span> | <span data-ttu-id="9eda9-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9eda9-110">2\_x</span></span> | <span data-ttu-id="9eda9-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9eda9-111">3\_0</span></span> | <span data-ttu-id="9eda9-112">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9eda9-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="9eda9-113">述詞註冊</span><span class="sxs-lookup"><span data-stu-id="9eda9-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="9eda9-114">x</span><span class="sxs-lookup"><span data-stu-id="9eda9-114">x</span></span>    | <span data-ttu-id="9eda9-115">x</span><span class="sxs-lookup"><span data-stu-id="9eda9-115">x</span></span>    | <span data-ttu-id="9eda9-116">x</span><span class="sxs-lookup"><span data-stu-id="9eda9-116">x</span></span>     |



 

<span data-ttu-id="9eda9-117">以下是註冊屬性。</span><span class="sxs-lookup"><span data-stu-id="9eda9-117">Here are the register properties.</span></span>



| <span data-ttu-id="9eda9-118">註冊類型</span><span class="sxs-lookup"><span data-stu-id="9eda9-118">Register type</span></span> | <span data-ttu-id="9eda9-119">Count</span><span class="sxs-lookup"><span data-stu-id="9eda9-119">Count</span></span> | <span data-ttu-id="9eda9-120">R/W</span><span class="sxs-lookup"><span data-stu-id="9eda9-120">R/W</span></span> | <span data-ttu-id="9eda9-121">\# 讀取埠</span><span class="sxs-lookup"><span data-stu-id="9eda9-121">\# Read ports</span></span> | <span data-ttu-id="9eda9-122">\# 讀取/inst</span><span class="sxs-lookup"><span data-stu-id="9eda9-122">\# Reads/inst</span></span> | <span data-ttu-id="9eda9-123">維度</span><span class="sxs-lookup"><span data-stu-id="9eda9-123">Dimension</span></span> | <span data-ttu-id="9eda9-124">RelAddr</span><span class="sxs-lookup"><span data-stu-id="9eda9-124">RelAddr</span></span> | <span data-ttu-id="9eda9-125">Defaults</span><span class="sxs-lookup"><span data-stu-id="9eda9-125">Defaults</span></span> | <span data-ttu-id="9eda9-126">需要 DCL</span><span class="sxs-lookup"><span data-stu-id="9eda9-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="9eda9-127">述詞 (p) </span><span class="sxs-lookup"><span data-stu-id="9eda9-127">Predicate(p)</span></span>  | <span data-ttu-id="9eda9-128">1</span><span class="sxs-lookup"><span data-stu-id="9eda9-128">1</span></span>     | <span data-ttu-id="9eda9-129">R/W</span><span class="sxs-lookup"><span data-stu-id="9eda9-129">R/W</span></span> | <span data-ttu-id="9eda9-130">1</span><span class="sxs-lookup"><span data-stu-id="9eda9-130">1</span></span>             | <span data-ttu-id="9eda9-131">1</span><span class="sxs-lookup"><span data-stu-id="9eda9-131">1</span></span>             | <span data-ttu-id="9eda9-132">4</span><span class="sxs-lookup"><span data-stu-id="9eda9-132">4</span></span>         | <span data-ttu-id="9eda9-133">N/A</span><span class="sxs-lookup"><span data-stu-id="9eda9-133">N/A</span></span>     | <span data-ttu-id="9eda9-134">無</span><span class="sxs-lookup"><span data-stu-id="9eda9-134">None</span></span>     | <span data-ttu-id="9eda9-135">N</span><span class="sxs-lookup"><span data-stu-id="9eda9-135">N</span></span>            |



 

<span data-ttu-id="9eda9-136">您可以使用 [setp \_ 複合-vs](setp-comp---vs.md)來修改述詞註冊。此暫存器沒有預設值，因此應用程式必須在使用之前先設定註冊。</span><span class="sxs-lookup"><span data-stu-id="9eda9-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eda9-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eda9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eda9-138">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="9eda9-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




