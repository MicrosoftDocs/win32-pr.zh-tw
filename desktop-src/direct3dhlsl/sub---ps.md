---
title: 子 ps
description: 減去來源。 |子 ps
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696354"
---
# <a name="sub---ps"></a><span data-ttu-id="eab59-104">子 ps</span><span class="sxs-lookup"><span data-stu-id="eab59-104">sub - ps</span></span>

<span data-ttu-id="eab59-105">減去來源。</span><span class="sxs-lookup"><span data-stu-id="eab59-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab59-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eab59-106">Syntax</span></span>



| <span data-ttu-id="eab59-107">sub dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="eab59-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="eab59-108">其中</span><span class="sxs-lookup"><span data-stu-id="eab59-108">where</span></span>

-   <span data-ttu-id="eab59-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="eab59-109">dst is the destination register.</span></span>
-   <span data-ttu-id="eab59-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="eab59-110">src0 is a source register.</span></span>
-   <span data-ttu-id="eab59-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="eab59-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab59-112">備註</span><span class="sxs-lookup"><span data-stu-id="eab59-112">Remarks</span></span>



| <span data-ttu-id="eab59-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="eab59-113">Pixel shader versions</span></span> | <span data-ttu-id="eab59-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="eab59-114">1\_1</span></span> | <span data-ttu-id="eab59-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="eab59-115">1\_2</span></span> | <span data-ttu-id="eab59-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="eab59-116">1\_3</span></span> | <span data-ttu-id="eab59-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="eab59-117">1\_4</span></span> | <span data-ttu-id="eab59-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eab59-118">2\_0</span></span> | <span data-ttu-id="eab59-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="eab59-119">2\_x</span></span> | <span data-ttu-id="eab59-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="eab59-120">2\_sw</span></span> | <span data-ttu-id="eab59-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eab59-121">3\_0</span></span> | <span data-ttu-id="eab59-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="eab59-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="eab59-123">sub</span><span class="sxs-lookup"><span data-stu-id="eab59-123">sub</span></span>                   | <span data-ttu-id="eab59-124">x</span><span class="sxs-lookup"><span data-stu-id="eab59-124">x</span></span>    | <span data-ttu-id="eab59-125">x</span><span class="sxs-lookup"><span data-stu-id="eab59-125">x</span></span>    | <span data-ttu-id="eab59-126">x</span><span class="sxs-lookup"><span data-stu-id="eab59-126">x</span></span>    | <span data-ttu-id="eab59-127">x</span><span class="sxs-lookup"><span data-stu-id="eab59-127">x</span></span>    | <span data-ttu-id="eab59-128">x</span><span class="sxs-lookup"><span data-stu-id="eab59-128">x</span></span>    | <span data-ttu-id="eab59-129">x</span><span class="sxs-lookup"><span data-stu-id="eab59-129">x</span></span>    | <span data-ttu-id="eab59-130">x</span><span class="sxs-lookup"><span data-stu-id="eab59-130">x</span></span>     | <span data-ttu-id="eab59-131">x</span><span class="sxs-lookup"><span data-stu-id="eab59-131">x</span></span>    | <span data-ttu-id="eab59-132">x</span><span class="sxs-lookup"><span data-stu-id="eab59-132">x</span></span>     |



 

<span data-ttu-id="eab59-133">此指示會執行此公式中顯示的減法。</span><span class="sxs-lookup"><span data-stu-id="eab59-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="eab59-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="eab59-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eab59-135">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="eab59-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




