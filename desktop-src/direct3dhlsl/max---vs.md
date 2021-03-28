---
title: 最大值-vs
description: 計算來源的最大值。 |最大值-vs
ms.assetid: 93fb8fb2-c722-43e5-bfe4-a2e9d3cd2049
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 923da795210fe2be62a6dd84a53f0127fef21077
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974245"
---
# <a name="max---vs"></a><span data-ttu-id="b8538-104">最大值-vs</span><span class="sxs-lookup"><span data-stu-id="b8538-104">max - vs</span></span>

<span data-ttu-id="b8538-105">計算來源的最大值。</span><span class="sxs-lookup"><span data-stu-id="b8538-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8538-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8538-106">Syntax</span></span>



| <span data-ttu-id="b8538-107">最大 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="b8538-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="b8538-108">其中</span><span class="sxs-lookup"><span data-stu-id="b8538-108">where</span></span>

-   <span data-ttu-id="b8538-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="b8538-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b8538-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="b8538-110">src0 is a source register.</span></span>
-   <span data-ttu-id="b8538-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="b8538-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8538-112">備註</span><span class="sxs-lookup"><span data-stu-id="b8538-112">Remarks</span></span>



| <span data-ttu-id="b8538-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="b8538-113">Vertex shader versions</span></span> | <span data-ttu-id="b8538-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b8538-114">1\_1</span></span> | <span data-ttu-id="b8538-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8538-115">2\_0</span></span> | <span data-ttu-id="b8538-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b8538-116">2\_x</span></span> | <span data-ttu-id="b8538-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b8538-117">2\_sw</span></span> | <span data-ttu-id="b8538-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8538-118">3\_0</span></span> | <span data-ttu-id="b8538-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="b8538-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b8538-120">max</span><span class="sxs-lookup"><span data-stu-id="b8538-120">max</span></span>                    | <span data-ttu-id="b8538-121">x</span><span class="sxs-lookup"><span data-stu-id="b8538-121">x</span></span>    | <span data-ttu-id="b8538-122">x</span><span class="sxs-lookup"><span data-stu-id="b8538-122">x</span></span>    | <span data-ttu-id="b8538-123">x</span><span class="sxs-lookup"><span data-stu-id="b8538-123">x</span></span>    | <span data-ttu-id="b8538-124">x</span><span class="sxs-lookup"><span data-stu-id="b8538-124">x</span></span>     | <span data-ttu-id="b8538-125">x</span><span class="sxs-lookup"><span data-stu-id="b8538-125">x</span></span>    | <span data-ttu-id="b8538-126">x</span><span class="sxs-lookup"><span data-stu-id="b8538-126">x</span></span>     |



 

<span data-ttu-id="b8538-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="b8538-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="b8538-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8538-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8538-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="b8538-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




