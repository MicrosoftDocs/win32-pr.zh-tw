---
title: abs-ps
description: 計算絕對值。 |abs-ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f4f22261a114333ed77d67d7c0ac2738d3522054
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343324"
---
# <a name="abs---ps"></a><span data-ttu-id="e3054-104">abs-ps</span><span class="sxs-lookup"><span data-stu-id="e3054-104">abs - ps</span></span>

<span data-ttu-id="e3054-105">計算絕對值。</span><span class="sxs-lookup"><span data-stu-id="e3054-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3054-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3054-106">Syntax</span></span>

<span data-ttu-id="e3054-107">**abs dst、src**</span><span class="sxs-lookup"><span data-stu-id="e3054-107">**abs dst, src**</span></span>

<span data-ttu-id="e3054-108">其中</span><span class="sxs-lookup"><span data-stu-id="e3054-108">where</span></span>

-   <span data-ttu-id="e3054-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e3054-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e3054-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="e3054-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3054-111">備註</span><span class="sxs-lookup"><span data-stu-id="e3054-111">Remarks</span></span>



| <span data-ttu-id="e3054-112">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="e3054-112">Pixel shader versions</span></span> | <span data-ttu-id="e3054-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="e3054-113">1\_1</span></span> | <span data-ttu-id="e3054-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="e3054-114">1\_2</span></span> | <span data-ttu-id="e3054-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e3054-115">1\_3</span></span> | <span data-ttu-id="e3054-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="e3054-116">1\_4</span></span> | <span data-ttu-id="e3054-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3054-117">2\_0</span></span> | <span data-ttu-id="e3054-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3054-118">2\_x</span></span> | <span data-ttu-id="e3054-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3054-119">2\_sw</span></span> | <span data-ttu-id="e3054-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3054-120">3\_0</span></span> | <span data-ttu-id="e3054-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3054-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e3054-122">abs</span><span class="sxs-lookup"><span data-stu-id="e3054-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="e3054-123">x</span><span class="sxs-lookup"><span data-stu-id="e3054-123">x</span></span>    | <span data-ttu-id="e3054-124">x</span><span class="sxs-lookup"><span data-stu-id="e3054-124">x</span></span>    | <span data-ttu-id="e3054-125">x</span><span class="sxs-lookup"><span data-stu-id="e3054-125">x</span></span>     | <span data-ttu-id="e3054-126">x</span><span class="sxs-lookup"><span data-stu-id="e3054-126">x</span></span>    | <span data-ttu-id="e3054-127">x</span><span class="sxs-lookup"><span data-stu-id="e3054-127">x</span></span>     |



 

<span data-ttu-id="e3054-128">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="e3054-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="e3054-129">指示資訊</span><span class="sxs-lookup"><span data-stu-id="e3054-129">Instruction Information</span></span>



| <span data-ttu-id="e3054-130">需求</span><span class="sxs-lookup"><span data-stu-id="e3054-130">Requirement</span></span>                         | <span data-ttu-id="e3054-131">值</span><span class="sxs-lookup"><span data-stu-id="e3054-131">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="e3054-132">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="e3054-132">Minimum operating system</span></span> | <span data-ttu-id="e3054-133">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e3054-133">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e3054-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3054-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3054-135">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="e3054-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




