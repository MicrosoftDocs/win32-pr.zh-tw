---
title: '相對定址 (HLSL PS 參考) '
description: 若是圖元著色器，\ \ 語法只能用在某些著色器模型中可以相對定址的暫存器類型。
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405481"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="c9120-103">相對定址 (HLSL PS 參考) </span><span class="sxs-lookup"><span data-stu-id="c9120-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="c9120-104">此 \[ \] 語法只能用在某些著色器模型中可以相對定址的暫存器類型。</span><span class="sxs-lookup"><span data-stu-id="c9120-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="c9120-105">支援的語法格式如下所示 \[ \] ：</span><span class="sxs-lookup"><span data-stu-id="c9120-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="c9120-106">其中：</span><span class="sxs-lookup"><span data-stu-id="c9120-106">Where:</span></span>

-   <span data-ttu-id="c9120-107">"R" 代表任何可以相對定址的註冊類型。</span><span class="sxs-lookup"><span data-stu-id="c9120-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="c9120-108">"A" 代表任何可用來做為索引的暫存器，以相對於其他暫存器的位址。</span><span class="sxs-lookup"><span data-stu-id="c9120-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="c9120-109">n0-ni、m0-mj 和 k 為整數 >= 0。</span><span class="sxs-lookup"><span data-stu-id="c9120-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="c9120-110">\[\]語法</span><span class="sxs-lookup"><span data-stu-id="c9120-110">\[ \] syntax</span></span>                              | <span data-ttu-id="c9120-111">有效索引</span><span class="sxs-lookup"><span data-stu-id="c9120-111">Effective index</span></span>                       | <span data-ttu-id="c9120-112">範例</span><span class="sxs-lookup"><span data-stu-id="c9120-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="c9120-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c9120-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="c9120-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c9120-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="c9120-115">c. \[ x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="c9120-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="c9120-116">R \[ k \] ( = Rk ) </span><span class="sxs-lookup"><span data-stu-id="c9120-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="c9120-117">k</span><span class="sxs-lookup"><span data-stu-id="c9120-117">k</span></span>                                     | <span data-ttu-id="c9120-118">c \[ 10 \] ( = c10 ) </span><span class="sxs-lookup"><span data-stu-id="c9120-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="c9120-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="c9120-119">R\[ A \]</span></span>                                  | <span data-ttu-id="c9120-120">A</span><span class="sxs-lookup"><span data-stu-id="c9120-120">A</span></span>                                     | <span data-ttu-id="c9120-121">c. \[ y \]</span><span class="sxs-lookup"><span data-stu-id="c9120-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="c9120-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c9120-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="c9120-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c9120-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="c9120-124">c8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="c9120-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="c9120-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c9120-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="c9120-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c9120-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="c9120-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="c9120-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="c9120-128">Rk \[\]</span><span class="sxs-lookup"><span data-stu-id="c9120-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="c9120-129">A + k</span><span class="sxs-lookup"><span data-stu-id="c9120-129">A + k</span></span>                                 | <span data-ttu-id="c9120-130">c12 \[ aL \] ，c0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="c9120-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="c9120-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="c9120-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="c9120-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="c9120-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="c9120-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="c9120-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="c9120-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="c9120-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="c9120-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="c9120-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="c9120-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="c9120-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="c9120-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="c9120-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="c9120-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="c9120-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="c9120-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="c9120-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="c9120-140">這些暫存器適用于下列版本：</span><span class="sxs-lookup"><span data-stu-id="c9120-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="c9120-141">註冊類型</span><span class="sxs-lookup"><span data-stu-id="c9120-141">Register type</span></span>                                                                                   | <span data-ttu-id="c9120-142">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="c9120-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="c9120-143">[迴圈計數器](dx9-graphics-reference-asm-ps-registers-loop-counter.md)：輸入暫存器上的 aL</span><span class="sxs-lookup"><span data-stu-id="c9120-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="c9120-144">ps \_ 3 \_ 0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c9120-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="c9120-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9120-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9120-146">寄存 器</span><span class="sxs-lookup"><span data-stu-id="c9120-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




