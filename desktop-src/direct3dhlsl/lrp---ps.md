---
title: lrp-ps
description: 在第二個和第三個來源暫存器之間，以第一個來源登錄中指定的比例，以線性方式插補 |lrp-ps
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035312"
---
# <a name="lrp---ps"></a><span data-ttu-id="4717e-104">lrp-ps</span><span class="sxs-lookup"><span data-stu-id="4717e-104">lrp - ps</span></span>

<span data-ttu-id="4717e-105">在第二個和第三個來源暫存器之間，以第一個來源登錄中指定的比例，以線性方式插補</span><span class="sxs-lookup"><span data-stu-id="4717e-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="4717e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4717e-106">Syntax</span></span>



| <span data-ttu-id="4717e-107">lrp dst、src0、src1、src2 收取</span><span class="sxs-lookup"><span data-stu-id="4717e-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="4717e-108">其中</span><span class="sxs-lookup"><span data-stu-id="4717e-108">where</span></span>

-   <span data-ttu-id="4717e-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="4717e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="4717e-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="4717e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="4717e-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="4717e-111">src1 is a source register.</span></span>
-   <span data-ttu-id="4717e-112">src2 收取是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="4717e-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="4717e-113">備註</span><span class="sxs-lookup"><span data-stu-id="4717e-113">Remarks</span></span>



| <span data-ttu-id="4717e-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="4717e-114">Pixel shader versions</span></span> | <span data-ttu-id="4717e-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="4717e-115">1\_1</span></span> | <span data-ttu-id="4717e-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="4717e-116">1\_2</span></span> | <span data-ttu-id="4717e-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4717e-117">1\_3</span></span> | <span data-ttu-id="4717e-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="4717e-118">1\_4</span></span> | <span data-ttu-id="4717e-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4717e-119">2\_0</span></span> | <span data-ttu-id="4717e-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4717e-120">2\_x</span></span> | <span data-ttu-id="4717e-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4717e-121">2\_sw</span></span> | <span data-ttu-id="4717e-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4717e-122">3\_0</span></span> | <span data-ttu-id="4717e-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4717e-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4717e-124">Lrp</span><span class="sxs-lookup"><span data-stu-id="4717e-124">lrp</span></span>                   | <span data-ttu-id="4717e-125">x</span><span class="sxs-lookup"><span data-stu-id="4717e-125">x</span></span>    | <span data-ttu-id="4717e-126">x</span><span class="sxs-lookup"><span data-stu-id="4717e-126">x</span></span>    | <span data-ttu-id="4717e-127">x</span><span class="sxs-lookup"><span data-stu-id="4717e-127">x</span></span>    | <span data-ttu-id="4717e-128">x</span><span class="sxs-lookup"><span data-stu-id="4717e-128">x</span></span>    | <span data-ttu-id="4717e-129">x</span><span class="sxs-lookup"><span data-stu-id="4717e-129">x</span></span>    | <span data-ttu-id="4717e-130">x</span><span class="sxs-lookup"><span data-stu-id="4717e-130">x</span></span>    | <span data-ttu-id="4717e-131">x</span><span class="sxs-lookup"><span data-stu-id="4717e-131">x</span></span>     | <span data-ttu-id="4717e-132">x</span><span class="sxs-lookup"><span data-stu-id="4717e-132">x</span></span>    | <span data-ttu-id="4717e-133">x</span><span class="sxs-lookup"><span data-stu-id="4717e-133">x</span></span>     |



 

<span data-ttu-id="4717e-134">此指示會根據下列公式來執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="4717e-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="4717e-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="4717e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4717e-136">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="4717e-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




