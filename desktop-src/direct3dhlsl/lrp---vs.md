---
title: lrp-vs
description: 在第二個和第三個來源暫存器之間，以第一個來源登錄中指定的比例，以線性方式插補 |lrp-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992007"
---
# <a name="lrp---vs"></a><span data-ttu-id="9f34b-104">lrp-vs</span><span class="sxs-lookup"><span data-stu-id="9f34b-104">lrp - vs</span></span>

<span data-ttu-id="9f34b-105">在第二個和第三個來源暫存器之間，以第一個來源登錄中指定的比例，以線性方式插補</span><span class="sxs-lookup"><span data-stu-id="9f34b-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f34b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f34b-106">Syntax</span></span>



| <span data-ttu-id="9f34b-107">lrp dst、src0、src1、src2 收取</span><span class="sxs-lookup"><span data-stu-id="9f34b-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="9f34b-108">其中</span><span class="sxs-lookup"><span data-stu-id="9f34b-108">where</span></span>

-   <span data-ttu-id="9f34b-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="9f34b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="9f34b-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="9f34b-110">src0 is a source register.</span></span>
-   <span data-ttu-id="9f34b-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="9f34b-111">src1 is a source register.</span></span>
-   <span data-ttu-id="9f34b-112">src2 收取是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="9f34b-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f34b-113">備註</span><span class="sxs-lookup"><span data-stu-id="9f34b-113">Remarks</span></span>



| <span data-ttu-id="9f34b-114">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="9f34b-114">Vertex shader versions</span></span> | <span data-ttu-id="9f34b-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9f34b-115">1\_1</span></span> | <span data-ttu-id="9f34b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f34b-116">2\_0</span></span> | <span data-ttu-id="9f34b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9f34b-117">2\_x</span></span> | <span data-ttu-id="9f34b-118">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9f34b-118">2\_sw</span></span> | <span data-ttu-id="9f34b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f34b-119">3\_0</span></span> | <span data-ttu-id="9f34b-120">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="9f34b-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9f34b-121">Lrp</span><span class="sxs-lookup"><span data-stu-id="9f34b-121">lrp</span></span>                    |      | <span data-ttu-id="9f34b-122">x</span><span class="sxs-lookup"><span data-stu-id="9f34b-122">x</span></span>    | <span data-ttu-id="9f34b-123">x</span><span class="sxs-lookup"><span data-stu-id="9f34b-123">x</span></span>    | <span data-ttu-id="9f34b-124">x</span><span class="sxs-lookup"><span data-stu-id="9f34b-124">x</span></span>     | <span data-ttu-id="9f34b-125">x</span><span class="sxs-lookup"><span data-stu-id="9f34b-125">x</span></span>    | <span data-ttu-id="9f34b-126">x</span><span class="sxs-lookup"><span data-stu-id="9f34b-126">x</span></span>     |



 

<span data-ttu-id="9f34b-127">此指示會根據下列公式來執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="9f34b-127">This instruction performs the linear interpolation based on the following formula.</span></span>


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="9f34b-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f34b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f34b-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="9f34b-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




