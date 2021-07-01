---
title: bem-ps
description: 套用假的凹凸環境對應轉換。
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129927"
---
# <a name="bem---ps"></a><span data-ttu-id="dc716-103">bem-ps</span><span class="sxs-lookup"><span data-stu-id="dc716-103">bem - ps</span></span>

<span data-ttu-id="dc716-104">套用假的凹凸環境對應轉換。</span><span class="sxs-lookup"><span data-stu-id="dc716-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc716-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc716-105">Syntax</span></span>



| <span data-ttu-id="dc716-106">bem src0、src1 的 dst</span><span class="sxs-lookup"><span data-stu-id="dc716-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="dc716-107">其中</span><span class="sxs-lookup"><span data-stu-id="dc716-107">where</span></span>

-   <span data-ttu-id="dc716-108">dst. rg dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="dc716-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="dc716-109">必須使用紅色和綠色的元件書寫遮罩。</span><span class="sxs-lookup"><span data-stu-id="dc716-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="dc716-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="dc716-110">src0 is a source register.</span></span>
-   <span data-ttu-id="dc716-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="dc716-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc716-112">備註</span><span class="sxs-lookup"><span data-stu-id="dc716-112">Remarks</span></span>



| <span data-ttu-id="dc716-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="dc716-113">Pixel shader versions</span></span> | <span data-ttu-id="dc716-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="dc716-114">1\_1</span></span> | <span data-ttu-id="dc716-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="dc716-115">1\_2</span></span> | <span data-ttu-id="dc716-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dc716-116">1\_3</span></span> | <span data-ttu-id="dc716-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="dc716-117">1\_4</span></span> | <span data-ttu-id="dc716-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc716-118">2\_0</span></span> | <span data-ttu-id="dc716-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="dc716-119">2\_x</span></span> | <span data-ttu-id="dc716-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="dc716-120">2\_sw</span></span> | <span data-ttu-id="dc716-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc716-121">3\_0</span></span> | <span data-ttu-id="dc716-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="dc716-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="dc716-123">bem</span><span class="sxs-lookup"><span data-stu-id="dc716-123">bem</span></span>                   |      |      |      | <span data-ttu-id="dc716-124">x</span><span class="sxs-lookup"><span data-stu-id="dc716-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="dc716-125">此指令會執行下列計算。</span><span class="sxs-lookup"><span data-stu-id="dc716-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="dc716-126">使用 bem 的規則：</span><span class="sxs-lookup"><span data-stu-id="dc716-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="dc716-127">bem 必須出現在著色器的第一個階段， (也就是在階段標記) 之前。</span><span class="sxs-lookup"><span data-stu-id="dc716-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="dc716-128">bem 會使用兩個算術指示位置。</span><span class="sxs-lookup"><span data-stu-id="dc716-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="dc716-129">每個著色器只允許一個使用此指令。</span><span class="sxs-lookup"><span data-stu-id="dc716-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="dc716-130">目的地 writemask 必須是. rg/.xy。</span><span class="sxs-lookup"><span data-stu-id="dc716-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="dc716-131">無法共同發出此指令。</span><span class="sxs-lookup"><span data-stu-id="dc716-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="dc716-132">除了目的地寫入遮罩的限制之外，來源 src0、src1 和指令修飾詞上的修飾詞不受限制。</span><span class="sxs-lookup"><span data-stu-id="dc716-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="dc716-133">指示資訊</span><span class="sxs-lookup"><span data-stu-id="dc716-133">Instruction Information</span></span>



| <span data-ttu-id="dc716-134">需求</span><span class="sxs-lookup"><span data-stu-id="dc716-134">Requirement</span></span>                         | <span data-ttu-id="dc716-135">值</span><span class="sxs-lookup"><span data-stu-id="dc716-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="dc716-136">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="dc716-136">Minimum operating system</span></span> | <span data-ttu-id="dc716-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="dc716-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dc716-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc716-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc716-139">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="dc716-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




