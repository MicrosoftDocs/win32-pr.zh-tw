---
title: crs-ps
description: 使用右手條規則來計算交叉乘積。 |crs-ps
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322003"
---
# <a name="crs---ps"></a><span data-ttu-id="d1b00-104">crs-ps</span><span class="sxs-lookup"><span data-stu-id="d1b00-104">crs - ps</span></span>

<span data-ttu-id="d1b00-105">使用右手條規則來計算交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="d1b00-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b00-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1b00-106">Syntax</span></span>



| <span data-ttu-id="d1b00-107">crs dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="d1b00-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="d1b00-108">其中</span><span class="sxs-lookup"><span data-stu-id="d1b00-108">where</span></span>

-   <span data-ttu-id="d1b00-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="d1b00-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d1b00-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="d1b00-110">src0 is a source register.</span></span>
-   <span data-ttu-id="d1b00-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="d1b00-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b00-112">備註</span><span class="sxs-lookup"><span data-stu-id="d1b00-112">Remarks</span></span>



| <span data-ttu-id="d1b00-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="d1b00-113">Pixel shader versions</span></span> | <span data-ttu-id="d1b00-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d1b00-114">1\_1</span></span> | <span data-ttu-id="d1b00-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="d1b00-115">1\_2</span></span> | <span data-ttu-id="d1b00-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d1b00-116">1\_3</span></span> | <span data-ttu-id="d1b00-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="d1b00-117">1\_4</span></span> | <span data-ttu-id="d1b00-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d1b00-118">2\_0</span></span> | <span data-ttu-id="d1b00-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d1b00-119">2\_x</span></span> | <span data-ttu-id="d1b00-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d1b00-120">2\_sw</span></span> | <span data-ttu-id="d1b00-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d1b00-121">3\_0</span></span> | <span data-ttu-id="d1b00-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d1b00-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d1b00-123">Crs</span><span class="sxs-lookup"><span data-stu-id="d1b00-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="d1b00-124">x</span><span class="sxs-lookup"><span data-stu-id="d1b00-124">x</span></span>    | <span data-ttu-id="d1b00-125">x</span><span class="sxs-lookup"><span data-stu-id="d1b00-125">x</span></span>    | <span data-ttu-id="d1b00-126">x</span><span class="sxs-lookup"><span data-stu-id="d1b00-126">x</span></span>     | <span data-ttu-id="d1b00-127">x</span><span class="sxs-lookup"><span data-stu-id="d1b00-127">x</span></span>    | <span data-ttu-id="d1b00-128">x</span><span class="sxs-lookup"><span data-stu-id="d1b00-128">x</span></span>     |



 

<span data-ttu-id="d1b00-129">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="d1b00-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="d1b00-130">使用的一些限制：</span><span class="sxs-lookup"><span data-stu-id="d1b00-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="d1b00-131">src0 不可以是與 dest 相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1b00-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="d1b00-132">src1 不可以是與 dest 相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1b00-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="d1b00-133">src0 不能有預設 swizzle ( xyzw) 以外的任何 swizzle。</span><span class="sxs-lookup"><span data-stu-id="d1b00-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="d1b00-134">src1 不能有預設 swizzle ( xyzw) 以外的任何 swizzle。</span><span class="sxs-lookup"><span data-stu-id="d1b00-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="d1b00-135">dest 必須剛好有下列其中一個 yz：.. \| z. z. z. z. z. \| z. \| \| \| \|</span><span class="sxs-lookup"><span data-stu-id="d1b00-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="d1b00-136">dest 必須是臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="d1b00-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="d1b00-137">目的地不得與 src0 或 src1 相同的註冊</span><span class="sxs-lookup"><span data-stu-id="d1b00-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1b00-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1b00-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1b00-139">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="d1b00-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




