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
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373839"
---
# <a name="bem---ps"></a><span data-ttu-id="785b7-103">bem-ps</span><span class="sxs-lookup"><span data-stu-id="785b7-103">bem - ps</span></span>

<span data-ttu-id="785b7-104">套用假的凹凸環境對應轉換。</span><span class="sxs-lookup"><span data-stu-id="785b7-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="785b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="785b7-105">Syntax</span></span>



| <span data-ttu-id="785b7-106">bem src0、src1 的 dst</span><span class="sxs-lookup"><span data-stu-id="785b7-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="785b7-107">其中</span><span class="sxs-lookup"><span data-stu-id="785b7-107">where</span></span>

-   <span data-ttu-id="785b7-108">dst. rg dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="785b7-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="785b7-109">必須使用紅色和綠色的元件書寫遮罩。</span><span class="sxs-lookup"><span data-stu-id="785b7-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="785b7-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="785b7-110">src0 is a source register.</span></span>
-   <span data-ttu-id="785b7-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="785b7-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="785b7-112">備註</span><span class="sxs-lookup"><span data-stu-id="785b7-112">Remarks</span></span>



| <span data-ttu-id="785b7-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="785b7-113">Pixel shader versions</span></span> | <span data-ttu-id="785b7-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="785b7-114">1\_1</span></span> | <span data-ttu-id="785b7-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="785b7-115">1\_2</span></span> | <span data-ttu-id="785b7-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="785b7-116">1\_3</span></span> | <span data-ttu-id="785b7-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="785b7-117">1\_4</span></span> | <span data-ttu-id="785b7-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="785b7-118">2\_0</span></span> | <span data-ttu-id="785b7-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="785b7-119">2\_x</span></span> | <span data-ttu-id="785b7-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="785b7-120">2\_sw</span></span> | <span data-ttu-id="785b7-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="785b7-121">3\_0</span></span> | <span data-ttu-id="785b7-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="785b7-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="785b7-123">bem</span><span class="sxs-lookup"><span data-stu-id="785b7-123">bem</span></span>                   |      |      |      | <span data-ttu-id="785b7-124">x</span><span class="sxs-lookup"><span data-stu-id="785b7-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="785b7-125">此指令會執行下列計算。</span><span class="sxs-lookup"><span data-stu-id="785b7-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="785b7-126">使用 bem 的規則：</span><span class="sxs-lookup"><span data-stu-id="785b7-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="785b7-127">bem 必須出現在著色器的第一個階段， (也就是在階段標記) 之前。</span><span class="sxs-lookup"><span data-stu-id="785b7-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="785b7-128">bem 會使用兩個算術指示位置。</span><span class="sxs-lookup"><span data-stu-id="785b7-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="785b7-129">每個著色器只允許一個使用此指令。</span><span class="sxs-lookup"><span data-stu-id="785b7-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="785b7-130">目的地 writemask 必須是. rg/.xy。</span><span class="sxs-lookup"><span data-stu-id="785b7-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="785b7-131">無法共同發出此指令。</span><span class="sxs-lookup"><span data-stu-id="785b7-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="785b7-132">除了目的地寫入遮罩的限制之外，來源 src0、src1 和指令修飾詞上的修飾詞不受限制。</span><span class="sxs-lookup"><span data-stu-id="785b7-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="785b7-133">指示資訊</span><span class="sxs-lookup"><span data-stu-id="785b7-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="785b7-134">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="785b7-134">Minimum operating system</span></span> | <span data-ttu-id="785b7-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="785b7-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="785b7-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="785b7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="785b7-137">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="785b7-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




