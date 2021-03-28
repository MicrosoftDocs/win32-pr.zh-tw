---
title: dp4-ps
description: 計算來源註冊的四個元件點乘積。 |dp4-ps
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035268"
---
# <a name="dp4---ps"></a><span data-ttu-id="06e1a-104">dp4-ps</span><span class="sxs-lookup"><span data-stu-id="06e1a-104">dp4 - ps</span></span>

<span data-ttu-id="06e1a-105">計算來源註冊的四個元件點乘積。</span><span class="sxs-lookup"><span data-stu-id="06e1a-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e1a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e1a-106">Syntax</span></span>



| <span data-ttu-id="06e1a-107">dp4 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="06e1a-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="06e1a-108">其中</span><span class="sxs-lookup"><span data-stu-id="06e1a-108">where</span></span>

-   <span data-ttu-id="06e1a-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="06e1a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="06e1a-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="06e1a-110">src0 is a source register.</span></span>
-   <span data-ttu-id="06e1a-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="06e1a-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="06e1a-112">備註</span><span class="sxs-lookup"><span data-stu-id="06e1a-112">Remarks</span></span>



| <span data-ttu-id="06e1a-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="06e1a-113">Pixel shader versions</span></span> | <span data-ttu-id="06e1a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="06e1a-114">1\_1</span></span> | <span data-ttu-id="06e1a-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="06e1a-115">1\_2</span></span> | <span data-ttu-id="06e1a-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="06e1a-116">1\_3</span></span> | <span data-ttu-id="06e1a-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="06e1a-117">1\_4</span></span> | <span data-ttu-id="06e1a-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="06e1a-118">2\_0</span></span> | <span data-ttu-id="06e1a-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="06e1a-119">2\_x</span></span> | <span data-ttu-id="06e1a-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="06e1a-120">2\_sw</span></span> | <span data-ttu-id="06e1a-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="06e1a-121">3\_0</span></span> | <span data-ttu-id="06e1a-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="06e1a-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="06e1a-123">dp4</span><span class="sxs-lookup"><span data-stu-id="06e1a-123">dp4</span></span>                   |      | <span data-ttu-id="06e1a-124">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-124">x</span></span>    | <span data-ttu-id="06e1a-125">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-125">x</span></span>    | <span data-ttu-id="06e1a-126">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-126">x</span></span>    | <span data-ttu-id="06e1a-127">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-127">x</span></span>    | <span data-ttu-id="06e1a-128">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-128">x</span></span>    | <span data-ttu-id="06e1a-129">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-129">x</span></span>     | <span data-ttu-id="06e1a-130">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-130">x</span></span>    | <span data-ttu-id="06e1a-131">x</span><span class="sxs-lookup"><span data-stu-id="06e1a-131">x</span></span>     |



 

<span data-ttu-id="06e1a-132">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="06e1a-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="06e1a-133">Ps \_ 1 \_ 2 和 ps \_ 1 3 的限制 \_ ：</span><span class="sxs-lookup"><span data-stu-id="06e1a-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="06e1a-134">每個著色器最多可以使用四個 dp4 指令。</span><span class="sxs-lookup"><span data-stu-id="06e1a-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="06e1a-135">每個 dp4 指令都會計算為兩個算術指令。</span><span class="sxs-lookup"><span data-stu-id="06e1a-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="06e1a-136">1 \_ X 版本的限制：</span><span class="sxs-lookup"><span data-stu-id="06e1a-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="06e1a-137">因為 dp4 是在向量和 Alpha 管線中執行，所以無法共同發出此指令。</span><span class="sxs-lookup"><span data-stu-id="06e1a-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06e1a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="06e1a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e1a-139">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="06e1a-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




