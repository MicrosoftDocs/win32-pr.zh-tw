---
title: '相對定址 (HLSL 與參考) '
description: '\\ 語法只能用在某些著色器模型中可以相對定址的暫存器類型。'
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313785"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="9eee5-103">相對定址 (HLSL 與參考) </span><span class="sxs-lookup"><span data-stu-id="9eee5-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="9eee5-104">此 \[ \] 語法只能用在某些著色器模型中可以相對定址的暫存器類型。</span><span class="sxs-lookup"><span data-stu-id="9eee5-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="9eee5-105">支援的語法格式如下所示 \[ \] ：</span><span class="sxs-lookup"><span data-stu-id="9eee5-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="9eee5-106">其中：</span><span class="sxs-lookup"><span data-stu-id="9eee5-106">Where:</span></span>

-   <span data-ttu-id="9eee5-107">"R" 代表任何可以相對定址的註冊類型。</span><span class="sxs-lookup"><span data-stu-id="9eee5-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="9eee5-108">"A" 代表任何可用來做為索引的暫存器，以相對於其他暫存器的位址。</span><span class="sxs-lookup"><span data-stu-id="9eee5-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="9eee5-109">n0-ni、m0-mj 和 k 為整數 >= 0。</span><span class="sxs-lookup"><span data-stu-id="9eee5-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="9eee5-110">\[\]語法</span><span class="sxs-lookup"><span data-stu-id="9eee5-110">\[ \] syntax</span></span>                              | <span data-ttu-id="9eee5-111">有效索引</span><span class="sxs-lookup"><span data-stu-id="9eee5-111">Effective index</span></span>                       | <span data-ttu-id="9eee5-112">範例</span><span class="sxs-lookup"><span data-stu-id="9eee5-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="9eee5-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="9eee5-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="9eee5-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="9eee5-115">c. \[ x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="9eee5-116">R \[ k \] ( = Rk ) </span><span class="sxs-lookup"><span data-stu-id="9eee5-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="9eee5-117">k</span><span class="sxs-lookup"><span data-stu-id="9eee5-117">k</span></span>                                     | <span data-ttu-id="9eee5-118">c \[ 10 \] ( = c10 ) </span><span class="sxs-lookup"><span data-stu-id="9eee5-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="9eee5-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-119">R\[ A \]</span></span>                                  | <span data-ttu-id="9eee5-120">A</span><span class="sxs-lookup"><span data-stu-id="9eee5-120">A</span></span>                                     | <span data-ttu-id="9eee5-121">c. \[ y \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="9eee5-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="9eee5-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="9eee5-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="9eee5-124">c8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="9eee5-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="9eee5-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="9eee5-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="9eee5-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="9eee5-128">Rk \[\]</span><span class="sxs-lookup"><span data-stu-id="9eee5-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="9eee5-129">A + k</span><span class="sxs-lookup"><span data-stu-id="9eee5-129">A + k</span></span>                                 | <span data-ttu-id="9eee5-130">c12 \[ aL \] ，c0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="9eee5-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="9eee5-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="9eee5-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="9eee5-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="9eee5-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="9eee5-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="9eee5-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="9eee5-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="9eee5-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="9eee5-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="9eee5-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="9eee5-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="9eee5-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="9eee5-140">這些暫存器適用于下列版本：</span><span class="sxs-lookup"><span data-stu-id="9eee5-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="9eee5-141">註冊類型</span><span class="sxs-lookup"><span data-stu-id="9eee5-141">Register type</span></span> | <span data-ttu-id="9eee5-142">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="9eee5-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="9eee5-143">a0</span><span class="sxs-lookup"><span data-stu-id="9eee5-143">a0</span></span>            | <span data-ttu-id="9eee5-144">全部</span><span class="sxs-lookup"><span data-stu-id="9eee5-144">All</span></span>                    |
| <span data-ttu-id="9eee5-145">鋁</span><span class="sxs-lookup"><span data-stu-id="9eee5-145">aL</span></span>            | <span data-ttu-id="9eee5-146">vs \_ 2 \_ 0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="9eee5-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="9eee5-147">cn</span><span class="sxs-lookup"><span data-stu-id="9eee5-147">cn</span></span>            | <span data-ttu-id="9eee5-148">vs \_ 1 \_ 1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="9eee5-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="9eee5-149">on</span><span class="sxs-lookup"><span data-stu-id="9eee5-149">on</span></span>            | <span data-ttu-id="9eee5-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9eee5-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="9eee5-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eee5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eee5-152">頂點著色器暫存器</span><span class="sxs-lookup"><span data-stu-id="9eee5-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




