---
title: slt-vs
description: 如果第一個來源小於第二個來源，則計算正負號。
ms.assetid: 7573bcee-8f31-49ea-b515-5be59a7a508d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6476ec24f82295d56b04682dfa4320547672b43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022804"
---
# <a name="slt---vs"></a><span data-ttu-id="1abb3-103">slt-vs</span><span class="sxs-lookup"><span data-stu-id="1abb3-103">slt - vs</span></span>

<span data-ttu-id="1abb3-104">如果第一個來源小於第二個來源，則計算正負號。</span><span class="sxs-lookup"><span data-stu-id="1abb3-104">Computes the sign if the first source is less than the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1abb3-105">Syntax</span></span>



| <span data-ttu-id="1abb3-106">slt dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="1abb3-106">slt dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="1abb3-107">其中</span><span class="sxs-lookup"><span data-stu-id="1abb3-107">where</span></span>

-   <span data-ttu-id="1abb3-108">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="1abb3-108">dst is the destination register.</span></span>
-   <span data-ttu-id="1abb3-109">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="1abb3-109">src0 is a source register.</span></span>
-   <span data-ttu-id="1abb3-110">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="1abb3-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1abb3-111">備註</span><span class="sxs-lookup"><span data-stu-id="1abb3-111">Remarks</span></span>



| <span data-ttu-id="1abb3-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="1abb3-112">Vertex shader versions</span></span> | <span data-ttu-id="1abb3-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="1abb3-113">1\_1</span></span> | <span data-ttu-id="1abb3-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1abb3-114">2\_0</span></span> | <span data-ttu-id="1abb3-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1abb3-115">2\_x</span></span> | <span data-ttu-id="1abb3-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1abb3-116">2\_sw</span></span> | <span data-ttu-id="1abb3-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1abb3-117">3\_0</span></span> | <span data-ttu-id="1abb3-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="1abb3-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="1abb3-119">slt</span><span class="sxs-lookup"><span data-stu-id="1abb3-119">slt</span></span>                    | <span data-ttu-id="1abb3-120">x</span><span class="sxs-lookup"><span data-stu-id="1abb3-120">x</span></span>    | <span data-ttu-id="1abb3-121">x</span><span class="sxs-lookup"><span data-stu-id="1abb3-121">x</span></span>    | <span data-ttu-id="1abb3-122">x</span><span class="sxs-lookup"><span data-stu-id="1abb3-122">x</span></span>    | <span data-ttu-id="1abb3-123">x</span><span class="sxs-lookup"><span data-stu-id="1abb3-123">x</span></span>     | <span data-ttu-id="1abb3-124">x</span><span class="sxs-lookup"><span data-stu-id="1abb3-124">x</span></span>    | <span data-ttu-id="1abb3-125">x</span><span class="sxs-lookup"><span data-stu-id="1abb3-125">x</span></span>     |



 

<span data-ttu-id="1abb3-126">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="1abb3-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x < src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y < src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z < src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w < src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="1abb3-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="1abb3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1abb3-128">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="1abb3-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




