---
title: sge-vs
description: 如果第一個來源大於或等於第二個來源，則計算正負號。
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7bad8816b87a32c5f10c73df27beb3cc2aef7716
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373807"
---
# <a name="sge---vs"></a><span data-ttu-id="07989-103">sge-vs</span><span class="sxs-lookup"><span data-stu-id="07989-103">sge - vs</span></span>

<span data-ttu-id="07989-104">如果第一個來源大於或等於第二個來源，則計算正負號。</span><span class="sxs-lookup"><span data-stu-id="07989-104">Computes the sign if the first source is greater than or equal to the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="07989-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07989-105">Syntax</span></span>



| <span data-ttu-id="07989-106">sge dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="07989-106">sge dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="07989-107">其中</span><span class="sxs-lookup"><span data-stu-id="07989-107">where</span></span>

-   <span data-ttu-id="07989-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="07989-108">dst is the destination register.</span></span>
-   <span data-ttu-id="07989-109">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="07989-109">src0 is a source register.</span></span>
-   <span data-ttu-id="07989-110">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="07989-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="07989-111">備註</span><span class="sxs-lookup"><span data-stu-id="07989-111">Remarks</span></span>



| <span data-ttu-id="07989-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="07989-112">Vertex shader versions</span></span> | <span data-ttu-id="07989-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="07989-113">1\_1</span></span> | <span data-ttu-id="07989-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07989-114">2\_0</span></span> | <span data-ttu-id="07989-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="07989-115">2\_x</span></span> | <span data-ttu-id="07989-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="07989-116">2\_sw</span></span> | <span data-ttu-id="07989-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07989-117">3\_0</span></span> | <span data-ttu-id="07989-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="07989-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="07989-119">sge</span><span class="sxs-lookup"><span data-stu-id="07989-119">sge</span></span>                    | <span data-ttu-id="07989-120">x</span><span class="sxs-lookup"><span data-stu-id="07989-120">x</span></span>    | <span data-ttu-id="07989-121">x</span><span class="sxs-lookup"><span data-stu-id="07989-121">x</span></span>    | <span data-ttu-id="07989-122">x</span><span class="sxs-lookup"><span data-stu-id="07989-122">x</span></span>    | <span data-ttu-id="07989-123">x</span><span class="sxs-lookup"><span data-stu-id="07989-123">x</span></span>     | <span data-ttu-id="07989-124">x</span><span class="sxs-lookup"><span data-stu-id="07989-124">x</span></span>    | <span data-ttu-id="07989-125">x</span><span class="sxs-lookup"><span data-stu-id="07989-125">x</span></span>     |



 

<span data-ttu-id="07989-126">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="07989-126">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="07989-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="07989-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07989-128">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="07989-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




