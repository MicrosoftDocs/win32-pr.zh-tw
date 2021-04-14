---
title: mul-ps
description: 將來源乘以目的地。 |mul-ps
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fefe89d4fdbe5f75965f2707a5ceb2c1673e1326
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992083"
---
# <a name="mul---ps"></a><span data-ttu-id="31db2-104">mul-ps</span><span class="sxs-lookup"><span data-stu-id="31db2-104">mul - ps</span></span>

<span data-ttu-id="31db2-105">將來源乘以目的地。</span><span class="sxs-lookup"><span data-stu-id="31db2-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="31db2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="31db2-106">Syntax</span></span>



| <span data-ttu-id="31db2-107">mul dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="31db2-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="31db2-108">其中</span><span class="sxs-lookup"><span data-stu-id="31db2-108">where</span></span>

-   <span data-ttu-id="31db2-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="31db2-109">dst is the destination register.</span></span>
-   <span data-ttu-id="31db2-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="31db2-110">src0 is a source register.</span></span>
-   <span data-ttu-id="31db2-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="31db2-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="31db2-112">備註</span><span class="sxs-lookup"><span data-stu-id="31db2-112">Remarks</span></span>



| <span data-ttu-id="31db2-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="31db2-113">Pixel shader versions</span></span> | <span data-ttu-id="31db2-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="31db2-114">1\_1</span></span> | <span data-ttu-id="31db2-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="31db2-115">1\_2</span></span> | <span data-ttu-id="31db2-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="31db2-116">1\_3</span></span> | <span data-ttu-id="31db2-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="31db2-117">1\_4</span></span> | <span data-ttu-id="31db2-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31db2-118">2\_0</span></span> | <span data-ttu-id="31db2-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31db2-119">2\_x</span></span> | <span data-ttu-id="31db2-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="31db2-120">2\_sw</span></span> | <span data-ttu-id="31db2-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31db2-121">3\_0</span></span> | <span data-ttu-id="31db2-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="31db2-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="31db2-123">mul</span><span class="sxs-lookup"><span data-stu-id="31db2-123">mul</span></span>                   | <span data-ttu-id="31db2-124">x</span><span class="sxs-lookup"><span data-stu-id="31db2-124">x</span></span>    | <span data-ttu-id="31db2-125">x</span><span class="sxs-lookup"><span data-stu-id="31db2-125">x</span></span>    | <span data-ttu-id="31db2-126">x</span><span class="sxs-lookup"><span data-stu-id="31db2-126">x</span></span>    | <span data-ttu-id="31db2-127">x</span><span class="sxs-lookup"><span data-stu-id="31db2-127">x</span></span>    | <span data-ttu-id="31db2-128">x</span><span class="sxs-lookup"><span data-stu-id="31db2-128">x</span></span>    | <span data-ttu-id="31db2-129">x</span><span class="sxs-lookup"><span data-stu-id="31db2-129">x</span></span>    | <span data-ttu-id="31db2-130">x</span><span class="sxs-lookup"><span data-stu-id="31db2-130">x</span></span>     | <span data-ttu-id="31db2-131">x</span><span class="sxs-lookup"><span data-stu-id="31db2-131">x</span></span>    | <span data-ttu-id="31db2-132">x</span><span class="sxs-lookup"><span data-stu-id="31db2-132">x</span></span>     |



 

<span data-ttu-id="31db2-133">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="31db2-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="31db2-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="31db2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31db2-135">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="31db2-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




