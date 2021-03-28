---
title: 軟體著色器
description: 軟體著色器的實作為允許在沒有基礎硬體支援的情況下開發著色器。 它們支援完整的功能集。 因為它們是在軟體中執行，所以不會產生最佳效能。
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022120"
---
# <a name="software-shaders"></a><span data-ttu-id="3df48-105">軟體著色器</span><span class="sxs-lookup"><span data-stu-id="3df48-105">Software Shaders</span></span>

<span data-ttu-id="3df48-106">軟體著色器的實作為允許在沒有基礎硬體支援的情況下開發著色器。</span><span class="sxs-lookup"><span data-stu-id="3df48-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="3df48-107">它們支援完整的功能集。</span><span class="sxs-lookup"><span data-stu-id="3df48-107">They support the full feature set.</span></span> <span data-ttu-id="3df48-108">因為它們是在軟體中執行，所以不會產生最佳效能。</span><span class="sxs-lookup"><span data-stu-id="3df48-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="3df48-109">版本</span><span class="sxs-lookup"><span data-stu-id="3df48-109">Version</span></span>   | <span data-ttu-id="3df48-110">功能集</span><span class="sxs-lookup"><span data-stu-id="3df48-110">Feature Set</span></span>                  | <span data-ttu-id="3df48-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3df48-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="3df48-112">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3df48-112">vs\_2\_sw</span></span> | <span data-ttu-id="3df48-113">Vs \_ 2 x 的所有功能 \_</span><span class="sxs-lookup"><span data-stu-id="3df48-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="3df48-114">只有軟體頂點處理和參考裝置才支援。</span><span class="sxs-lookup"><span data-stu-id="3df48-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="3df48-115">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3df48-115">vs\_3\_sw</span></span> | <span data-ttu-id="3df48-116">Vs \_ 3 0 的所有功能 \_</span><span class="sxs-lookup"><span data-stu-id="3df48-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="3df48-117">只有軟體頂點處理和參考裝置才支援。</span><span class="sxs-lookup"><span data-stu-id="3df48-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="3df48-118">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3df48-118">ps\_2\_sw</span></span> | <span data-ttu-id="3df48-119">Ps \_ 2 x 的所有功能 \_</span><span class="sxs-lookup"><span data-stu-id="3df48-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="3df48-120">只有參考設備支援。</span><span class="sxs-lookup"><span data-stu-id="3df48-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="3df48-121">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="3df48-121">ps\_3\_sw</span></span> | <span data-ttu-id="3df48-122">Ps \_ 3 0 的所有功能 \_</span><span class="sxs-lookup"><span data-stu-id="3df48-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="3df48-123">只有參考設備支援。</span><span class="sxs-lookup"><span data-stu-id="3df48-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="3df48-124">某些驗證會針對軟體著色器放寬。</span><span class="sxs-lookup"><span data-stu-id="3df48-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="3df48-125">這適用于偵錯工具和原型設計用途。</span><span class="sxs-lookup"><span data-stu-id="3df48-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="3df48-126">下列驗證會放寬： (所有其他驗證保持不變) </span><span class="sxs-lookup"><span data-stu-id="3df48-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="3df48-127">驗證類型</span><span class="sxs-lookup"><span data-stu-id="3df48-127">Validation type</span></span>                                 | <span data-ttu-id="3df48-128">放鬆</span><span class="sxs-lookup"><span data-stu-id="3df48-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df48-129">指令計數：</span><span class="sxs-lookup"><span data-stu-id="3df48-129">Instruction Counts:</span></span>                             | <span data-ttu-id="3df48-130">這對 vs \_ 2 \_ sw、vs \_ 3 \_ sw 和 ps \_ 2 \_ sw、ps \_ 3 \_ sw 而言是寬鬆的。</span><span class="sxs-lookup"><span data-stu-id="3df48-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="3df48-131">允許無限制的指示。</span><span class="sxs-lookup"><span data-stu-id="3df48-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="3df48-132">浮點數常數計數：</span><span class="sxs-lookup"><span data-stu-id="3df48-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="3df48-133">這對 vs \_ 2 \_ sw、vs \_ 3 \_ sw 和 ps \_ 2 \_ sw、ps \_ 3 \_ sw 而言是寬鬆的。</span><span class="sxs-lookup"><span data-stu-id="3df48-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="3df48-134">最多允許8192個常數。</span><span class="sxs-lookup"><span data-stu-id="3df48-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="3df48-135">整數常數計數：</span><span class="sxs-lookup"><span data-stu-id="3df48-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="3df48-136">這對 vs \_ 2 \_ sw、vs \_ 3 \_ sw 和 ps \_ 2 \_ sw、ps \_ 3 \_ sw 而言是寬鬆的。</span><span class="sxs-lookup"><span data-stu-id="3df48-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="3df48-137">最多允許2048個常數。</span><span class="sxs-lookup"><span data-stu-id="3df48-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="3df48-138">布林值常數計數：</span><span class="sxs-lookup"><span data-stu-id="3df48-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="3df48-139">這對 vs \_ 2 \_ sw、vs \_ 3 \_ sw 和 ps \_ 2 \_ sw、ps \_ 3 \_ sw 而言是寬鬆的。</span><span class="sxs-lookup"><span data-stu-id="3df48-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="3df48-140">最多允許2048個常數。</span><span class="sxs-lookup"><span data-stu-id="3df48-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="3df48-141">相依-讀取深度：</span><span class="sxs-lookup"><span data-stu-id="3df48-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="3df48-142">這對於 ps 2 sw 而言是寬鬆的 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="3df48-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="3df48-143">如同在 vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 中，允許無限制的相依讀取。</span><span class="sxs-lookup"><span data-stu-id="3df48-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="3df48-144">流程式控制制指令和標籤的數目：</span><span class="sxs-lookup"><span data-stu-id="3df48-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="3df48-145">Vs 2 軟體會放寬這項功能 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="3df48-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="3df48-146">允許無限制的流程式控制制指示，以及最高2048的標籤。</span><span class="sxs-lookup"><span data-stu-id="3df48-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="3df48-147">迴圈計數/開始/步驟：</span><span class="sxs-lookup"><span data-stu-id="3df48-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="3df48-148">這些會針對 vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw 和 ps \_ 3 sw 放寬 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3df48-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="3df48-149">Rep 和迴圈指示的反復專案開始和反覆運算步驟大小為32位帶正負號的 intergers。</span><span class="sxs-lookup"><span data-stu-id="3df48-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="3df48-150">反覆運算計數的最大值可以是 \_ INT/64。</span><span class="sxs-lookup"><span data-stu-id="3df48-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="3df48-151">讀取埠限制：</span><span class="sxs-lookup"><span data-stu-id="3df48-151">Read-port limits:</span></span>                               | <span data-ttu-id="3df48-152">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw 和 ps \_ 3 \_ sw 沒有讀取埠的限制。</span><span class="sxs-lookup"><span data-stu-id="3df48-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="3df48-153">Interpolators 數目：</span><span class="sxs-lookup"><span data-stu-id="3df48-153">Number of interpolators:</span></span>                        | <span data-ttu-id="3df48-154">Vs 3 sw 中有16個暫存器 [-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \#) \_ \_ ，而10個 [ps \_ 3 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \#) 適用于 ps \_ 3 \_ sw。</span><span class="sxs-lookup"><span data-stu-id="3df48-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="3df48-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="3df48-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3df48-156">Asm 著色器參考</span><span class="sxs-lookup"><span data-stu-id="3df48-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




