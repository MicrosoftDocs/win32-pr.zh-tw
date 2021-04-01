---
title: nrm-vs
description: 標準化3D 向量。 |nrm-vs
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196000"
---
# <a name="nrm---vs"></a><span data-ttu-id="361ec-104">nrm-vs</span><span class="sxs-lookup"><span data-stu-id="361ec-104">nrm - vs</span></span>

<span data-ttu-id="361ec-105">標準化3D 向量。</span><span class="sxs-lookup"><span data-stu-id="361ec-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="361ec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="361ec-106">Syntax</span></span>



| <span data-ttu-id="361ec-107">nrm dst、src</span><span class="sxs-lookup"><span data-stu-id="361ec-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="361ec-108">其中</span><span class="sxs-lookup"><span data-stu-id="361ec-108">where</span></span>

-   <span data-ttu-id="361ec-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="361ec-109">dst is the destination register.</span></span>
-   <span data-ttu-id="361ec-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="361ec-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="361ec-111">備註</span><span class="sxs-lookup"><span data-stu-id="361ec-111">Remarks</span></span>



| <span data-ttu-id="361ec-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="361ec-112">Vertex shader versions</span></span> | <span data-ttu-id="361ec-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="361ec-113">1\_1</span></span> | <span data-ttu-id="361ec-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="361ec-114">2\_0</span></span> | <span data-ttu-id="361ec-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="361ec-115">2\_x</span></span> | <span data-ttu-id="361ec-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="361ec-116">2\_sw</span></span> | <span data-ttu-id="361ec-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="361ec-117">3\_0</span></span> | <span data-ttu-id="361ec-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="361ec-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="361ec-119">nrm</span><span class="sxs-lookup"><span data-stu-id="361ec-119">nrm</span></span>                    |      | <span data-ttu-id="361ec-120">x</span><span class="sxs-lookup"><span data-stu-id="361ec-120">x</span></span>    | <span data-ttu-id="361ec-121">x</span><span class="sxs-lookup"><span data-stu-id="361ec-121">x</span></span>    | <span data-ttu-id="361ec-122">x</span><span class="sxs-lookup"><span data-stu-id="361ec-122">x</span></span>     | <span data-ttu-id="361ec-123">x</span><span class="sxs-lookup"><span data-stu-id="361ec-123">x</span></span>    | <span data-ttu-id="361ec-124">x</span><span class="sxs-lookup"><span data-stu-id="361ec-124">x</span></span>     |



 

<span data-ttu-id="361ec-125">此指示在概念上的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="361ec-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="361ec-126">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z) <sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="361ec-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="361ec-127">目的地和 src 暫存器不可以相同。</span><span class="sxs-lookup"><span data-stu-id="361ec-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="361ec-128">目的地暫存器必須是臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="361ec-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="361ec-129">此指示會根據下列公式來執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="361ec-129">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="361ec-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="361ec-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="361ec-131">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="361ec-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




