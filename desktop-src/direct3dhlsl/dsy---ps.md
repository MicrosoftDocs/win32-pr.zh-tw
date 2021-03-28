---
title: dsy-ps
description: 計算轉譯目標的 y 方向變化率。
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373747"
---
# <a name="dsy---ps"></a><span data-ttu-id="4b986-103">dsy-ps</span><span class="sxs-lookup"><span data-stu-id="4b986-103">dsy - ps</span></span>

<span data-ttu-id="4b986-104">計算轉譯目標的 y 方向變化率。</span><span class="sxs-lookup"><span data-stu-id="4b986-104">Compute the rate of change in the render target's y-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b986-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b986-105">Syntax</span></span>



| <span data-ttu-id="4b986-106">dsy dst、src</span><span class="sxs-lookup"><span data-stu-id="4b986-106">dsy dst, src</span></span> |
|--------------|



 

<span data-ttu-id="4b986-107">其中：</span><span class="sxs-lookup"><span data-stu-id="4b986-107">Where:</span></span>

-   <span data-ttu-id="4b986-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="4b986-108">dst is a destination register.</span></span>
-   <span data-ttu-id="4b986-109">src 是輸入來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="4b986-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b986-110">備註</span><span class="sxs-lookup"><span data-stu-id="4b986-110">Remarks</span></span>



| <span data-ttu-id="4b986-111">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="4b986-111">Pixel shader versions</span></span> | <span data-ttu-id="4b986-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="4b986-112">1\_1</span></span> | <span data-ttu-id="4b986-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="4b986-113">1\_2</span></span> | <span data-ttu-id="4b986-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4b986-114">1\_3</span></span> | <span data-ttu-id="4b986-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="4b986-115">1\_4</span></span> | <span data-ttu-id="4b986-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b986-116">2\_0</span></span> | <span data-ttu-id="4b986-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4b986-117">2\_x</span></span> | <span data-ttu-id="4b986-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b986-118">2\_sw</span></span> | <span data-ttu-id="4b986-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b986-119">3\_0</span></span> | <span data-ttu-id="4b986-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b986-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4b986-121">dsy</span><span class="sxs-lookup"><span data-stu-id="4b986-121">dsy</span></span>                   |      |      |      |      |      | <span data-ttu-id="4b986-122">x</span><span class="sxs-lookup"><span data-stu-id="4b986-122">x</span></span>    | <span data-ttu-id="4b986-123">x</span><span class="sxs-lookup"><span data-stu-id="4b986-123">x</span></span>     | <span data-ttu-id="4b986-124">x</span><span class="sxs-lookup"><span data-stu-id="4b986-124">x</span></span>    | <span data-ttu-id="4b986-125">x</span><span class="sxs-lookup"><span data-stu-id="4b986-125">x</span></span>     |



 

<span data-ttu-id="4b986-126">從來源暫存器計算的變更速率是相鄰圖元 (s 中相同暫存器內容的近似值，) 以目前的圖元來執行鎖定步驟中的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="4b986-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="4b986-127">[Dsx](dsx---ps.md)和 dsy 指示會藉由查看每個元件的來源暫存器 (的目前內容，) 在鎖定步驟中執行的區域區域內的各種圖元來計算結果。</span><span class="sxs-lookup"><span data-stu-id="4b986-127">The [dsx](dsx---ps.md) And dsy instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="4b986-128">用來計算漸層的確切公式會因硬體而異，但應該與硬體執行相同作業的方式，如同紋理取樣的詳細資料計算程式一部分。</span><span class="sxs-lookup"><span data-stu-id="4b986-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b986-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b986-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b986-130">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="4b986-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="4b986-131">texldd-ps</span><span class="sxs-lookup"><span data-stu-id="4b986-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




