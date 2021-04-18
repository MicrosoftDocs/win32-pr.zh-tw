---
title: 最大-ps
description: 計算來源的最大值。 |最大-ps
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974424"
---
# <a name="max---ps"></a><span data-ttu-id="6ec70-104">最大-ps</span><span class="sxs-lookup"><span data-stu-id="6ec70-104">max - ps</span></span>

<span data-ttu-id="6ec70-105">計算來源的最大值。</span><span class="sxs-lookup"><span data-stu-id="6ec70-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec70-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ec70-106">Syntax</span></span>



| <span data-ttu-id="6ec70-107">最大 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="6ec70-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="6ec70-108">其中</span><span class="sxs-lookup"><span data-stu-id="6ec70-108">where</span></span>

-   <span data-ttu-id="6ec70-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="6ec70-109">dst is the destination register.</span></span>
-   <span data-ttu-id="6ec70-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="6ec70-110">src0 is a source register.</span></span>
-   <span data-ttu-id="6ec70-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="6ec70-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec70-112">備註</span><span class="sxs-lookup"><span data-stu-id="6ec70-112">Remarks</span></span>



| <span data-ttu-id="6ec70-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="6ec70-113">Pixel shader versions</span></span> | <span data-ttu-id="6ec70-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ec70-114">1\_1</span></span> | <span data-ttu-id="6ec70-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="6ec70-115">1\_2</span></span> | <span data-ttu-id="6ec70-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6ec70-116">1\_3</span></span> | <span data-ttu-id="6ec70-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ec70-117">1\_4</span></span> | <span data-ttu-id="6ec70-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ec70-118">2\_0</span></span> | <span data-ttu-id="6ec70-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ec70-119">2\_x</span></span> | <span data-ttu-id="6ec70-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6ec70-120">2\_sw</span></span> | <span data-ttu-id="6ec70-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ec70-121">3\_0</span></span> | <span data-ttu-id="6ec70-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="6ec70-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6ec70-123">max</span><span class="sxs-lookup"><span data-stu-id="6ec70-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="6ec70-124">x</span><span class="sxs-lookup"><span data-stu-id="6ec70-124">x</span></span>    | <span data-ttu-id="6ec70-125">x</span><span class="sxs-lookup"><span data-stu-id="6ec70-125">x</span></span>    | <span data-ttu-id="6ec70-126">x</span><span class="sxs-lookup"><span data-stu-id="6ec70-126">x</span></span>     | <span data-ttu-id="6ec70-127">x</span><span class="sxs-lookup"><span data-stu-id="6ec70-127">x</span></span>    | <span data-ttu-id="6ec70-128">x</span><span class="sxs-lookup"><span data-stu-id="6ec70-128">x</span></span>     |



 

<span data-ttu-id="6ec70-129">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="6ec70-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="6ec70-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ec70-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ec70-131">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="6ec70-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




