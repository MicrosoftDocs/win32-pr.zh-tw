---
title: 新增-vs
description: 新增兩個向量。 |新增-vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853580"
---
# <a name="add---vs"></a><span data-ttu-id="cecf6-104">新增-vs</span><span class="sxs-lookup"><span data-stu-id="cecf6-104">add - vs</span></span>

<span data-ttu-id="cecf6-105">新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="cecf6-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="cecf6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cecf6-106">Syntax</span></span>



| <span data-ttu-id="cecf6-107">新增 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="cecf6-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="cecf6-108">其中</span><span class="sxs-lookup"><span data-stu-id="cecf6-108">where</span></span>

-   <span data-ttu-id="cecf6-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="cecf6-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cecf6-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="cecf6-110">src0 is a source register.</span></span>
-   <span data-ttu-id="cecf6-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="cecf6-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cecf6-112">備註</span><span class="sxs-lookup"><span data-stu-id="cecf6-112">Remarks</span></span>



| <span data-ttu-id="cecf6-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="cecf6-113">Vertex shader versions</span></span> | <span data-ttu-id="cecf6-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="cecf6-114">1\_1</span></span> | <span data-ttu-id="cecf6-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cecf6-115">2\_0</span></span> | <span data-ttu-id="cecf6-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cecf6-116">2\_x</span></span> | <span data-ttu-id="cecf6-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cecf6-117">2\_sw</span></span> | <span data-ttu-id="cecf6-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cecf6-118">3\_0</span></span> | <span data-ttu-id="cecf6-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cecf6-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cecf6-120">add</span><span class="sxs-lookup"><span data-stu-id="cecf6-120">add</span></span>                    | <span data-ttu-id="cecf6-121">x</span><span class="sxs-lookup"><span data-stu-id="cecf6-121">x</span></span>    | <span data-ttu-id="cecf6-122">x</span><span class="sxs-lookup"><span data-stu-id="cecf6-122">x</span></span>    | <span data-ttu-id="cecf6-123">x</span><span class="sxs-lookup"><span data-stu-id="cecf6-123">x</span></span>    | <span data-ttu-id="cecf6-124">x</span><span class="sxs-lookup"><span data-stu-id="cecf6-124">x</span></span>     | <span data-ttu-id="cecf6-125">x</span><span class="sxs-lookup"><span data-stu-id="cecf6-125">x</span></span>    | <span data-ttu-id="cecf6-126">x</span><span class="sxs-lookup"><span data-stu-id="cecf6-126">x</span></span>     |



 

<span data-ttu-id="cecf6-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="cecf6-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="cecf6-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="cecf6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cecf6-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="cecf6-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




