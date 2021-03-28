---
title: mad-ps
description: 乘以並加入指令。 將目的地註冊設定為 (src0 \ src1) + src2 收取。
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373827"
---
# <a name="mad---ps"></a><span data-ttu-id="840ad-104">mad-ps</span><span class="sxs-lookup"><span data-stu-id="840ad-104">mad - ps</span></span>

<span data-ttu-id="840ad-105">乘以並加入指令。</span><span class="sxs-lookup"><span data-stu-id="840ad-105">Multiply and add instruction.</span></span> <span data-ttu-id="840ad-106">將目的地登錄設定為 (src0 \* src1) + src2 收取。</span><span class="sxs-lookup"><span data-stu-id="840ad-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="840ad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="840ad-107">Syntax</span></span>



| <span data-ttu-id="840ad-108">mad dst、src0、src1、src2 收取</span><span class="sxs-lookup"><span data-stu-id="840ad-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="840ad-109">其中</span><span class="sxs-lookup"><span data-stu-id="840ad-109">where</span></span>

-   <span data-ttu-id="840ad-110">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="840ad-110">dst is the destination register.</span></span>
-   <span data-ttu-id="840ad-111">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="840ad-111">src0 is a source register.</span></span>
-   <span data-ttu-id="840ad-112">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="840ad-112">src1 is a source register.</span></span>
-   <span data-ttu-id="840ad-113">src2 收取是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="840ad-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="840ad-114">備註</span><span class="sxs-lookup"><span data-stu-id="840ad-114">Remarks</span></span>



| <span data-ttu-id="840ad-115">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="840ad-115">Pixel shader versions</span></span> | <span data-ttu-id="840ad-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="840ad-116">1\_1</span></span> | <span data-ttu-id="840ad-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="840ad-117">1\_2</span></span> | <span data-ttu-id="840ad-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="840ad-118">1\_3</span></span> | <span data-ttu-id="840ad-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="840ad-119">1\_4</span></span> | <span data-ttu-id="840ad-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="840ad-120">2\_0</span></span> | <span data-ttu-id="840ad-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="840ad-121">2\_x</span></span> | <span data-ttu-id="840ad-122">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="840ad-122">2\_sw</span></span> | <span data-ttu-id="840ad-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="840ad-123">3\_0</span></span> | <span data-ttu-id="840ad-124">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="840ad-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="840ad-125">瘋狂</span><span class="sxs-lookup"><span data-stu-id="840ad-125">mad</span></span>                   | <span data-ttu-id="840ad-126">x</span><span class="sxs-lookup"><span data-stu-id="840ad-126">x</span></span>    | <span data-ttu-id="840ad-127">x</span><span class="sxs-lookup"><span data-stu-id="840ad-127">x</span></span>    | <span data-ttu-id="840ad-128">x</span><span class="sxs-lookup"><span data-stu-id="840ad-128">x</span></span>    | <span data-ttu-id="840ad-129">x</span><span class="sxs-lookup"><span data-stu-id="840ad-129">x</span></span>    | <span data-ttu-id="840ad-130">x</span><span class="sxs-lookup"><span data-stu-id="840ad-130">x</span></span>    | <span data-ttu-id="840ad-131">x</span><span class="sxs-lookup"><span data-stu-id="840ad-131">x</span></span>    | <span data-ttu-id="840ad-132">x</span><span class="sxs-lookup"><span data-stu-id="840ad-132">x</span></span>     | <span data-ttu-id="840ad-133">x</span><span class="sxs-lookup"><span data-stu-id="840ad-133">x</span></span>    | <span data-ttu-id="840ad-134">x</span><span class="sxs-lookup"><span data-stu-id="840ad-134">x</span></span>     |



 

<span data-ttu-id="840ad-135">下列程式碼片段會顯示已執行的作業。</span><span class="sxs-lookup"><span data-stu-id="840ad-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="840ad-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="840ad-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="840ad-137">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="840ad-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




