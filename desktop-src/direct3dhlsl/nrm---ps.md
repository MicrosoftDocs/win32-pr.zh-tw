---
title: nrm-ps
description: 標準化3D 向量。 |nrm-ps
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322120"
---
# <a name="nrm---ps"></a><span data-ttu-id="99026-104">nrm-ps</span><span class="sxs-lookup"><span data-stu-id="99026-104">nrm - ps</span></span>

<span data-ttu-id="99026-105">標準化3D 向量。</span><span class="sxs-lookup"><span data-stu-id="99026-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="99026-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="99026-106">Syntax</span></span>



| <span data-ttu-id="99026-107">nrm dst、src</span><span class="sxs-lookup"><span data-stu-id="99026-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="99026-108">其中</span><span class="sxs-lookup"><span data-stu-id="99026-108">where</span></span>

-   <span data-ttu-id="99026-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="99026-109">dst is the destination register.</span></span>
-   <span data-ttu-id="99026-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="99026-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="99026-111">備註</span><span class="sxs-lookup"><span data-stu-id="99026-111">Remarks</span></span>



| <span data-ttu-id="99026-112">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="99026-112">Pixel shader versions</span></span> | <span data-ttu-id="99026-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="99026-113">1\_1</span></span> | <span data-ttu-id="99026-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="99026-114">1\_2</span></span> | <span data-ttu-id="99026-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="99026-115">1\_3</span></span> | <span data-ttu-id="99026-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="99026-116">1\_4</span></span> | <span data-ttu-id="99026-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99026-117">2\_0</span></span> | <span data-ttu-id="99026-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="99026-118">2\_x</span></span> | <span data-ttu-id="99026-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="99026-119">2\_sw</span></span> | <span data-ttu-id="99026-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99026-120">3\_0</span></span> | <span data-ttu-id="99026-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="99026-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="99026-122">nrm</span><span class="sxs-lookup"><span data-stu-id="99026-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="99026-123">x</span><span class="sxs-lookup"><span data-stu-id="99026-123">x</span></span>    | <span data-ttu-id="99026-124">x</span><span class="sxs-lookup"><span data-stu-id="99026-124">x</span></span>    | <span data-ttu-id="99026-125">x</span><span class="sxs-lookup"><span data-stu-id="99026-125">x</span></span>     | <span data-ttu-id="99026-126">x</span><span class="sxs-lookup"><span data-stu-id="99026-126">x</span></span>    | <span data-ttu-id="99026-127">x</span><span class="sxs-lookup"><span data-stu-id="99026-127">x</span></span>     |



 

<span data-ttu-id="99026-128">此指示在概念上的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="99026-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="99026-129">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z) <sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="99026-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="99026-130">目的地和 src 暫存器不可以相同。</span><span class="sxs-lookup"><span data-stu-id="99026-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="99026-131">目的地暫存器必須是臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="99026-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="99026-132">此指示會根據下列公式來執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="99026-132">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="99026-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="99026-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99026-134">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="99026-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




