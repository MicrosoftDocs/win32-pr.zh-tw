---
title: mul-vs
description: 將來源乘以目的地。 |mul-vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e33ac35831b19f771f4f5b64d94bcc47c6657db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991966"
---
# <a name="mul---vs"></a><span data-ttu-id="ebc07-104">mul-vs</span><span class="sxs-lookup"><span data-stu-id="ebc07-104">mul - vs</span></span>

<span data-ttu-id="ebc07-105">將來源乘以目的地。</span><span class="sxs-lookup"><span data-stu-id="ebc07-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc07-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebc07-106">Syntax</span></span>



| <span data-ttu-id="ebc07-107">mul dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="ebc07-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="ebc07-108">其中</span><span class="sxs-lookup"><span data-stu-id="ebc07-108">where</span></span>

-   <span data-ttu-id="ebc07-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="ebc07-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ebc07-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="ebc07-110">src0 is a source register.</span></span>
-   <span data-ttu-id="ebc07-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="ebc07-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebc07-112">備註</span><span class="sxs-lookup"><span data-stu-id="ebc07-112">Remarks</span></span>



| <span data-ttu-id="ebc07-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="ebc07-113">Vertex shader versions</span></span> | <span data-ttu-id="ebc07-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ebc07-114">1\_1</span></span> | <span data-ttu-id="ebc07-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ebc07-115">2\_0</span></span> | <span data-ttu-id="ebc07-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ebc07-116">2\_x</span></span> | <span data-ttu-id="ebc07-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ebc07-117">2\_sw</span></span> | <span data-ttu-id="ebc07-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ebc07-118">3\_0</span></span> | <span data-ttu-id="ebc07-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="ebc07-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ebc07-120">mul</span><span class="sxs-lookup"><span data-stu-id="ebc07-120">mul</span></span>                    | <span data-ttu-id="ebc07-121">x</span><span class="sxs-lookup"><span data-stu-id="ebc07-121">x</span></span>    | <span data-ttu-id="ebc07-122">x</span><span class="sxs-lookup"><span data-stu-id="ebc07-122">x</span></span>    | <span data-ttu-id="ebc07-123">x</span><span class="sxs-lookup"><span data-stu-id="ebc07-123">x</span></span>    | <span data-ttu-id="ebc07-124">x</span><span class="sxs-lookup"><span data-stu-id="ebc07-124">x</span></span>     | <span data-ttu-id="ebc07-125">x</span><span class="sxs-lookup"><span data-stu-id="ebc07-125">x</span></span>    | <span data-ttu-id="ebc07-126">x</span><span class="sxs-lookup"><span data-stu-id="ebc07-126">x</span></span>     |



 

<span data-ttu-id="ebc07-127">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="ebc07-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="ebc07-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebc07-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc07-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="ebc07-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




