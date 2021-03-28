---
title: crs-vs
description: 使用右手條規則來計算交叉乘積。 |crs-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322000"
---
# <a name="crs---vs"></a><span data-ttu-id="f1386-104">crs-vs</span><span class="sxs-lookup"><span data-stu-id="f1386-104">crs - vs</span></span>

<span data-ttu-id="f1386-105">使用右手條規則來計算交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="f1386-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1386-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1386-106">Syntax</span></span>



| <span data-ttu-id="f1386-107">crs dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="f1386-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="f1386-108">其中</span><span class="sxs-lookup"><span data-stu-id="f1386-108">where</span></span>

-   <span data-ttu-id="f1386-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="f1386-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f1386-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="f1386-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f1386-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="f1386-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1386-112">備註</span><span class="sxs-lookup"><span data-stu-id="f1386-112">Remarks</span></span>



| <span data-ttu-id="f1386-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="f1386-113">Vertex shader versions</span></span> | <span data-ttu-id="f1386-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f1386-114">1\_1</span></span> | <span data-ttu-id="f1386-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1386-115">2\_0</span></span> | <span data-ttu-id="f1386-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f1386-116">2\_x</span></span> | <span data-ttu-id="f1386-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f1386-117">2\_sw</span></span> | <span data-ttu-id="f1386-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1386-118">3\_0</span></span> | <span data-ttu-id="f1386-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f1386-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f1386-120">Crs</span><span class="sxs-lookup"><span data-stu-id="f1386-120">crs</span></span>                    |      | <span data-ttu-id="f1386-121">x</span><span class="sxs-lookup"><span data-stu-id="f1386-121">x</span></span>    | <span data-ttu-id="f1386-122">x</span><span class="sxs-lookup"><span data-stu-id="f1386-122">x</span></span>    | <span data-ttu-id="f1386-123">x</span><span class="sxs-lookup"><span data-stu-id="f1386-123">x</span></span>     | <span data-ttu-id="f1386-124">x</span><span class="sxs-lookup"><span data-stu-id="f1386-124">x</span></span>    | <span data-ttu-id="f1386-125">x</span><span class="sxs-lookup"><span data-stu-id="f1386-125">x</span></span>     |



 

<span data-ttu-id="f1386-126">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="f1386-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="f1386-127">使用的一些限制：</span><span class="sxs-lookup"><span data-stu-id="f1386-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="f1386-128">src0 不可以是與 dest 相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="f1386-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="f1386-129">src1 不可以是與 dest 相同的暫存器。</span><span class="sxs-lookup"><span data-stu-id="f1386-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="f1386-130">src0 不能有預設 swizzle ( xyzw) 以外的任何 swizzle。</span><span class="sxs-lookup"><span data-stu-id="f1386-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="f1386-131">src1 不能有預設 swizzle ( xyzw) 以外的任何 swizzle。</span><span class="sxs-lookup"><span data-stu-id="f1386-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="f1386-132">dest 必須剛好有下列其中一個 yz：.. \| z. z. z. z. z. \| z. \| \| \| \|</span><span class="sxs-lookup"><span data-stu-id="f1386-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="f1386-133">dest 必須是臨時暫存器。</span><span class="sxs-lookup"><span data-stu-id="f1386-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="f1386-134">目的地不得與 src0 或 src1 相同的註冊</span><span class="sxs-lookup"><span data-stu-id="f1386-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1386-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1386-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1386-136">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="f1386-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




