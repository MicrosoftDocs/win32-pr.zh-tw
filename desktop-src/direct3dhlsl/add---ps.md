---
title: 新增-ps
description: 新增兩個向量。 |新增-ps
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130087"
---
# <a name="add---ps"></a><span data-ttu-id="9ff55-104">新增-ps</span><span class="sxs-lookup"><span data-stu-id="9ff55-104">add - ps</span></span>

<span data-ttu-id="9ff55-105">新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="9ff55-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff55-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ff55-106">Syntax</span></span>



| <span data-ttu-id="9ff55-107">新增 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="9ff55-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="9ff55-108">其中</span><span class="sxs-lookup"><span data-stu-id="9ff55-108">where</span></span>

-   <span data-ttu-id="9ff55-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="9ff55-109">dst is the destination register.</span></span>
-   <span data-ttu-id="9ff55-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="9ff55-110">src0 is a source register.</span></span>
-   <span data-ttu-id="9ff55-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="9ff55-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff55-112">備註</span><span class="sxs-lookup"><span data-stu-id="9ff55-112">Remarks</span></span>



| <span data-ttu-id="9ff55-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="9ff55-113">Pixel shader versions</span></span> | <span data-ttu-id="9ff55-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="9ff55-114">1\_1</span></span> | <span data-ttu-id="9ff55-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="9ff55-115">1\_2</span></span> | <span data-ttu-id="9ff55-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9ff55-116">1\_3</span></span> | <span data-ttu-id="9ff55-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="9ff55-117">1\_4</span></span> | <span data-ttu-id="9ff55-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ff55-118">2\_0</span></span> | <span data-ttu-id="9ff55-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9ff55-119">2\_x</span></span> | <span data-ttu-id="9ff55-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9ff55-120">2\_sw</span></span> | <span data-ttu-id="9ff55-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9ff55-121">3\_0</span></span> | <span data-ttu-id="9ff55-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9ff55-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9ff55-123">add</span><span class="sxs-lookup"><span data-stu-id="9ff55-123">add</span></span>                   | <span data-ttu-id="9ff55-124">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-124">x</span></span>    | <span data-ttu-id="9ff55-125">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-125">x</span></span>    | <span data-ttu-id="9ff55-126">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-126">x</span></span>    | <span data-ttu-id="9ff55-127">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-127">x</span></span>    | <span data-ttu-id="9ff55-128">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-128">x</span></span>    | <span data-ttu-id="9ff55-129">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-129">x</span></span>    | <span data-ttu-id="9ff55-130">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-130">x</span></span>     | <span data-ttu-id="9ff55-131">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-131">x</span></span>    | <span data-ttu-id="9ff55-132">x</span><span class="sxs-lookup"><span data-stu-id="9ff55-132">x</span></span>     |



 

<span data-ttu-id="9ff55-133">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="9ff55-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="9ff55-134">指示資訊</span><span class="sxs-lookup"><span data-stu-id="9ff55-134">Instruction Information</span></span>



|   <span data-ttu-id="9ff55-135">需求</span><span class="sxs-lookup"><span data-stu-id="9ff55-135">Requirement</span></span>                       | <span data-ttu-id="9ff55-136">值</span><span class="sxs-lookup"><span data-stu-id="9ff55-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="9ff55-137">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="9ff55-137">Minimum operating system</span></span> | <span data-ttu-id="9ff55-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9ff55-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9ff55-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ff55-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ff55-140">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="9ff55-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




