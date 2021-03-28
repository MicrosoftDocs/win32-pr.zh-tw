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
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973933"
---
# <a name="add---ps"></a><span data-ttu-id="e0a8e-104">新增-ps</span><span class="sxs-lookup"><span data-stu-id="e0a8e-104">add - ps</span></span>

<span data-ttu-id="e0a8e-105">新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="e0a8e-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a8e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0a8e-106">Syntax</span></span>



| <span data-ttu-id="e0a8e-107">新增 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="e0a8e-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="e0a8e-108">其中</span><span class="sxs-lookup"><span data-stu-id="e0a8e-108">where</span></span>

-   <span data-ttu-id="e0a8e-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e0a8e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e0a8e-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="e0a8e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="e0a8e-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="e0a8e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a8e-112">備註</span><span class="sxs-lookup"><span data-stu-id="e0a8e-112">Remarks</span></span>



| <span data-ttu-id="e0a8e-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e0a8e-113">Pixel shader versions</span></span> | <span data-ttu-id="e0a8e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e0a8e-114">1\_1</span></span> | <span data-ttu-id="e0a8e-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="e0a8e-115">1\_2</span></span> | <span data-ttu-id="e0a8e-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e0a8e-116">1\_3</span></span> | <span data-ttu-id="e0a8e-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="e0a8e-117">1\_4</span></span> | <span data-ttu-id="e0a8e-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0a8e-118">2\_0</span></span> | <span data-ttu-id="e0a8e-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-119">2\_x</span></span> | <span data-ttu-id="e0a8e-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e0a8e-120">2\_sw</span></span> | <span data-ttu-id="e0a8e-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0a8e-121">3\_0</span></span> | <span data-ttu-id="e0a8e-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e0a8e-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e0a8e-123">add</span><span class="sxs-lookup"><span data-stu-id="e0a8e-123">add</span></span>                   | <span data-ttu-id="e0a8e-124">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-124">x</span></span>    | <span data-ttu-id="e0a8e-125">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-125">x</span></span>    | <span data-ttu-id="e0a8e-126">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-126">x</span></span>    | <span data-ttu-id="e0a8e-127">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-127">x</span></span>    | <span data-ttu-id="e0a8e-128">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-128">x</span></span>    | <span data-ttu-id="e0a8e-129">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-129">x</span></span>    | <span data-ttu-id="e0a8e-130">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-130">x</span></span>     | <span data-ttu-id="e0a8e-131">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-131">x</span></span>    | <span data-ttu-id="e0a8e-132">x</span><span class="sxs-lookup"><span data-stu-id="e0a8e-132">x</span></span>     |



 

<span data-ttu-id="e0a8e-133">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="e0a8e-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="e0a8e-134">指示資訊</span><span class="sxs-lookup"><span data-stu-id="e0a8e-134">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e0a8e-135">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="e0a8e-135">Minimum operating system</span></span> | <span data-ttu-id="e0a8e-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e0a8e-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e0a8e-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0a8e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0a8e-138">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e0a8e-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




