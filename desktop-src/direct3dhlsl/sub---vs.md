---
title: sub-vs
description: 減去來源。 |sub-vs
ms.assetid: ccd7ca57-05a9-4ee8-8bda-c8c875476aaf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4bf15522798e1da5ec0bde5b729f241ff9dabde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945919"
---
# <a name="sub---vs"></a><span data-ttu-id="f11ae-104">sub-vs</span><span class="sxs-lookup"><span data-stu-id="f11ae-104">sub - vs</span></span>

<span data-ttu-id="f11ae-105">減去來源。</span><span class="sxs-lookup"><span data-stu-id="f11ae-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11ae-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f11ae-106">Syntax</span></span>



| <span data-ttu-id="f11ae-107">sub dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="f11ae-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="f11ae-108">其中</span><span class="sxs-lookup"><span data-stu-id="f11ae-108">where</span></span>

-   <span data-ttu-id="f11ae-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="f11ae-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f11ae-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="f11ae-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f11ae-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="f11ae-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f11ae-112">備註</span><span class="sxs-lookup"><span data-stu-id="f11ae-112">Remarks</span></span>



| <span data-ttu-id="f11ae-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="f11ae-113">Vertex shader versions</span></span> | <span data-ttu-id="f11ae-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f11ae-114">1\_1</span></span> | <span data-ttu-id="f11ae-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f11ae-115">2\_0</span></span> | <span data-ttu-id="f11ae-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f11ae-116">2\_x</span></span> | <span data-ttu-id="f11ae-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f11ae-117">2\_sw</span></span> | <span data-ttu-id="f11ae-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f11ae-118">3\_0</span></span> | <span data-ttu-id="f11ae-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="f11ae-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f11ae-120">sub</span><span class="sxs-lookup"><span data-stu-id="f11ae-120">sub</span></span>                    | <span data-ttu-id="f11ae-121">x</span><span class="sxs-lookup"><span data-stu-id="f11ae-121">x</span></span>    | <span data-ttu-id="f11ae-122">x</span><span class="sxs-lookup"><span data-stu-id="f11ae-122">x</span></span>    | <span data-ttu-id="f11ae-123">x</span><span class="sxs-lookup"><span data-stu-id="f11ae-123">x</span></span>    | <span data-ttu-id="f11ae-124">x</span><span class="sxs-lookup"><span data-stu-id="f11ae-124">x</span></span>     | <span data-ttu-id="f11ae-125">x</span><span class="sxs-lookup"><span data-stu-id="f11ae-125">x</span></span>    | <span data-ttu-id="f11ae-126">x</span><span class="sxs-lookup"><span data-stu-id="f11ae-126">x</span></span>     |



 

<span data-ttu-id="f11ae-127">此指示會執行此公式中顯示的減法。</span><span class="sxs-lookup"><span data-stu-id="f11ae-127">This instruction performs the subtraction shown in this formula.</span></span>


```
dest.x = src0.x - src1.x
dest.y = src0.y - src1.y
dest.z = src0.z - src1.z
dest.w = src0.w - src1.w
```



## <a name="related-topics"></a><span data-ttu-id="f11ae-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f11ae-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11ae-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="f11ae-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




