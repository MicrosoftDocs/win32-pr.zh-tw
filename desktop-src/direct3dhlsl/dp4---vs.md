---
title: dp4-vs
description: 計算來源註冊的四個元件點乘積。 |dp4-vs
ms.assetid: ee3d3c8d-6031-4264-80ba-2b200a721310
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 747695436094dd5d2e9787e3eeca525b292f14c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974073"
---
# <a name="dp4---vs"></a><span data-ttu-id="92974-104">dp4-vs</span><span class="sxs-lookup"><span data-stu-id="92974-104">dp4 - vs</span></span>

<span data-ttu-id="92974-105">計算來源註冊的四個元件點乘積。</span><span class="sxs-lookup"><span data-stu-id="92974-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="92974-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="92974-106">Syntax</span></span>



| <span data-ttu-id="92974-107">dp4 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="92974-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="92974-108">其中</span><span class="sxs-lookup"><span data-stu-id="92974-108">where</span></span>

-   <span data-ttu-id="92974-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-109">dst is the destination register.</span></span>
-   <span data-ttu-id="92974-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-110">src0 is a source register.</span></span>
-   <span data-ttu-id="92974-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="92974-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="92974-112">備註</span><span class="sxs-lookup"><span data-stu-id="92974-112">Remarks</span></span>



| <span data-ttu-id="92974-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="92974-113">Vertex shader versions</span></span> | <span data-ttu-id="92974-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="92974-114">1\_1</span></span> | <span data-ttu-id="92974-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92974-115">2\_0</span></span> | <span data-ttu-id="92974-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="92974-116">2\_x</span></span> | <span data-ttu-id="92974-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="92974-117">2\_sw</span></span> | <span data-ttu-id="92974-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92974-118">3\_0</span></span> | <span data-ttu-id="92974-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="92974-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="92974-120">dp4</span><span class="sxs-lookup"><span data-stu-id="92974-120">dp4</span></span>                    | <span data-ttu-id="92974-121">x</span><span class="sxs-lookup"><span data-stu-id="92974-121">x</span></span>    | <span data-ttu-id="92974-122">x</span><span class="sxs-lookup"><span data-stu-id="92974-122">x</span></span>    | <span data-ttu-id="92974-123">x</span><span class="sxs-lookup"><span data-stu-id="92974-123">x</span></span>    | <span data-ttu-id="92974-124">x</span><span class="sxs-lookup"><span data-stu-id="92974-124">x</span></span>     | <span data-ttu-id="92974-125">x</span><span class="sxs-lookup"><span data-stu-id="92974-125">x</span></span>    | <span data-ttu-id="92974-126">x</span><span class="sxs-lookup"><span data-stu-id="92974-126">x</span></span>     |



 

<span data-ttu-id="92974-127">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="92974-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + 
         (src0.z * src1.z) + (src0.w * src1.w);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="92974-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="92974-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92974-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="92974-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




