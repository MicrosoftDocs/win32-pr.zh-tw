---
title: '相對定址 (HLSL 與參考) '
description: 針對頂點著色器，\\ 語法只能用在某些著色器模型中可以相對定址的暫存器類型。
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406691"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="fc21e-103">相對定址 (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="fc21e-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="fc21e-104">此 \[ \] 語法只能用在某些著色器模型中可以相對定址的暫存器類型。</span><span class="sxs-lookup"><span data-stu-id="fc21e-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="fc21e-105">支援的語法格式如下所示 \[ \] ：</span><span class="sxs-lookup"><span data-stu-id="fc21e-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="fc21e-106">其中：</span><span class="sxs-lookup"><span data-stu-id="fc21e-106">Where:</span></span>

-   <span data-ttu-id="fc21e-107">"R" 代表任何可以相對定址的註冊類型。</span><span class="sxs-lookup"><span data-stu-id="fc21e-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="fc21e-108">"A" 代表任何可用來做為索引的暫存器，以相對於其他暫存器的位址。</span><span class="sxs-lookup"><span data-stu-id="fc21e-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="fc21e-109">n0-ni、m0-mj 和 k 為整數 >= 0。</span><span class="sxs-lookup"><span data-stu-id="fc21e-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="fc21e-110">\[\]語法</span><span class="sxs-lookup"><span data-stu-id="fc21e-110">\[ \] syntax</span></span>                              | <span data-ttu-id="fc21e-111">有效索引</span><span class="sxs-lookup"><span data-stu-id="fc21e-111">Effective index</span></span>                       | <span data-ttu-id="fc21e-112">範例</span><span class="sxs-lookup"><span data-stu-id="fc21e-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="fc21e-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="fc21e-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fc21e-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="fc21e-115">c. \[ x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="fc21e-116">R \[ k \] ( = Rk ) </span><span class="sxs-lookup"><span data-stu-id="fc21e-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="fc21e-117">k</span><span class="sxs-lookup"><span data-stu-id="fc21e-117">k</span></span>                                     | <span data-ttu-id="fc21e-118">c \[ 10 \] ( = c10 ) </span><span class="sxs-lookup"><span data-stu-id="fc21e-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="fc21e-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-119">R\[ A \]</span></span>                                  | <span data-ttu-id="fc21e-120">A</span><span class="sxs-lookup"><span data-stu-id="fc21e-120">A</span></span>                                     | <span data-ttu-id="fc21e-121">c. \[ y \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="fc21e-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="fc21e-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fc21e-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="fc21e-124">c8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="fc21e-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="fc21e-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fc21e-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="fc21e-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="fc21e-128">Rk \[\]</span><span class="sxs-lookup"><span data-stu-id="fc21e-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="fc21e-129">A + k</span><span class="sxs-lookup"><span data-stu-id="fc21e-129">A + k</span></span>                                 | <span data-ttu-id="fc21e-130">c12 \[ aL \] ，c0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="fc21e-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="fc21e-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="fc21e-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="fc21e-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="fc21e-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="fc21e-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="fc21e-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="fc21e-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="fc21e-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="fc21e-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="fc21e-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="fc21e-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="fc21e-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="fc21e-140">這些暫存器適用于下列版本：</span><span class="sxs-lookup"><span data-stu-id="fc21e-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="fc21e-141">註冊類型</span><span class="sxs-lookup"><span data-stu-id="fc21e-141">Register type</span></span> | <span data-ttu-id="fc21e-142">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="fc21e-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="fc21e-143">a0</span><span class="sxs-lookup"><span data-stu-id="fc21e-143">a0</span></span>            | <span data-ttu-id="fc21e-144">全部</span><span class="sxs-lookup"><span data-stu-id="fc21e-144">All</span></span>                    |
| <span data-ttu-id="fc21e-145">鋁</span><span class="sxs-lookup"><span data-stu-id="fc21e-145">aL</span></span>            | <span data-ttu-id="fc21e-146">vs \_ 2 \_ 0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="fc21e-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="fc21e-147">cn</span><span class="sxs-lookup"><span data-stu-id="fc21e-147">cn</span></span>            | <span data-ttu-id="fc21e-148">vs \_ 1 \_ 1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="fc21e-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="fc21e-149">on</span><span class="sxs-lookup"><span data-stu-id="fc21e-149">on</span></span>            | <span data-ttu-id="fc21e-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fc21e-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="fc21e-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc21e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc21e-152">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="fc21e-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




