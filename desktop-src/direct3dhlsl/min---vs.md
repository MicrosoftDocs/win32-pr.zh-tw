---
title: 最小值-vs
description: 計算來源的最小值。 |最小值-vs
ms.assetid: cecfe98b-8efd-4fbf-a7b5-d228de724e71
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eda47b75398b8643f7010ff7468f72f4a7d8c199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974260"
---
# <a name="min---vs"></a><span data-ttu-id="16c5e-104">最小值-vs</span><span class="sxs-lookup"><span data-stu-id="16c5e-104">min - vs</span></span>

<span data-ttu-id="16c5e-105">計算來源的最小值。</span><span class="sxs-lookup"><span data-stu-id="16c5e-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c5e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16c5e-106">Syntax</span></span>



| <span data-ttu-id="16c5e-107">最小 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="16c5e-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="16c5e-108">其中</span><span class="sxs-lookup"><span data-stu-id="16c5e-108">where</span></span>

-   <span data-ttu-id="16c5e-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="16c5e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="16c5e-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="16c5e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="16c5e-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="16c5e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c5e-112">備註</span><span class="sxs-lookup"><span data-stu-id="16c5e-112">Remarks</span></span>



| <span data-ttu-id="16c5e-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="16c5e-113">Vertex shader versions</span></span> | <span data-ttu-id="16c5e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="16c5e-114">1\_1</span></span> | <span data-ttu-id="16c5e-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16c5e-115">2\_0</span></span> | <span data-ttu-id="16c5e-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16c5e-116">2\_x</span></span> | <span data-ttu-id="16c5e-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="16c5e-117">2\_sw</span></span> | <span data-ttu-id="16c5e-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16c5e-118">3\_0</span></span> | <span data-ttu-id="16c5e-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="16c5e-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="16c5e-120">分鐘</span><span class="sxs-lookup"><span data-stu-id="16c5e-120">min</span></span>                    | <span data-ttu-id="16c5e-121">x</span><span class="sxs-lookup"><span data-stu-id="16c5e-121">x</span></span>    | <span data-ttu-id="16c5e-122">x</span><span class="sxs-lookup"><span data-stu-id="16c5e-122">x</span></span>    | <span data-ttu-id="16c5e-123">x</span><span class="sxs-lookup"><span data-stu-id="16c5e-123">x</span></span>    | <span data-ttu-id="16c5e-124">x</span><span class="sxs-lookup"><span data-stu-id="16c5e-124">x</span></span>     | <span data-ttu-id="16c5e-125">x</span><span class="sxs-lookup"><span data-stu-id="16c5e-125">x</span></span>    | <span data-ttu-id="16c5e-126">x</span><span class="sxs-lookup"><span data-stu-id="16c5e-126">x</span></span>     |



 

<span data-ttu-id="16c5e-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="16c5e-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="16c5e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="16c5e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16c5e-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="16c5e-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




