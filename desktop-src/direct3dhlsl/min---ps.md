---
title: 最小-ps
description: 計算來源的最小值。 |最小-ps
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974156"
---
# <a name="min---ps"></a><span data-ttu-id="397ce-104">最小-ps</span><span class="sxs-lookup"><span data-stu-id="397ce-104">min - ps</span></span>

<span data-ttu-id="397ce-105">計算來源的最小值。</span><span class="sxs-lookup"><span data-stu-id="397ce-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="397ce-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="397ce-106">Syntax</span></span>



| <span data-ttu-id="397ce-107">最小 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="397ce-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="397ce-108">其中</span><span class="sxs-lookup"><span data-stu-id="397ce-108">where</span></span>

-   <span data-ttu-id="397ce-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="397ce-109">dst is the destination register.</span></span>
-   <span data-ttu-id="397ce-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="397ce-110">src0 is a source register.</span></span>
-   <span data-ttu-id="397ce-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="397ce-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="397ce-112">備註</span><span class="sxs-lookup"><span data-stu-id="397ce-112">Remarks</span></span>



| <span data-ttu-id="397ce-113">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="397ce-113">Pixel shader versions</span></span> | <span data-ttu-id="397ce-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="397ce-114">1\_1</span></span> | <span data-ttu-id="397ce-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="397ce-115">1\_2</span></span> | <span data-ttu-id="397ce-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="397ce-116">1\_3</span></span> | <span data-ttu-id="397ce-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="397ce-117">1\_4</span></span> | <span data-ttu-id="397ce-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="397ce-118">2\_0</span></span> | <span data-ttu-id="397ce-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="397ce-119">2\_x</span></span> | <span data-ttu-id="397ce-120">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="397ce-120">2\_sw</span></span> | <span data-ttu-id="397ce-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="397ce-121">3\_0</span></span> | <span data-ttu-id="397ce-122">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="397ce-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="397ce-123">分鐘</span><span class="sxs-lookup"><span data-stu-id="397ce-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="397ce-124">x</span><span class="sxs-lookup"><span data-stu-id="397ce-124">x</span></span>    | <span data-ttu-id="397ce-125">x</span><span class="sxs-lookup"><span data-stu-id="397ce-125">x</span></span>    | <span data-ttu-id="397ce-126">x</span><span class="sxs-lookup"><span data-stu-id="397ce-126">x</span></span>     | <span data-ttu-id="397ce-127">x</span><span class="sxs-lookup"><span data-stu-id="397ce-127">x</span></span>    | <span data-ttu-id="397ce-128">x</span><span class="sxs-lookup"><span data-stu-id="397ce-128">x</span></span>     |



 

<span data-ttu-id="397ce-129">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="397ce-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="397ce-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="397ce-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="397ce-131">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="397ce-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




