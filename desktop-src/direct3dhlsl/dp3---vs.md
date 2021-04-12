---
title: dp3-vs
description: 計算來源註冊的三個元件點乘積。 |dp3-vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81580401f25ddcf7ce1c1d53475d0c3beba74a89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195871"
---
# <a name="dp3---vs"></a><span data-ttu-id="e3707-104">dp3-vs</span><span class="sxs-lookup"><span data-stu-id="e3707-104">dp3 - vs</span></span>

<span data-ttu-id="e3707-105">計算來源註冊的三個元件點乘積。</span><span class="sxs-lookup"><span data-stu-id="e3707-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3707-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3707-106">Syntax</span></span>



| <span data-ttu-id="e3707-107">dp3 dst、src0、src1</span><span class="sxs-lookup"><span data-stu-id="e3707-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="e3707-108">其中</span><span class="sxs-lookup"><span data-stu-id="e3707-108">where</span></span>

-   <span data-ttu-id="e3707-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="e3707-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e3707-110">src0 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="e3707-110">src0 is a source register.</span></span>
-   <span data-ttu-id="e3707-111">src1 是來源註冊。</span><span class="sxs-lookup"><span data-stu-id="e3707-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3707-112">備註</span><span class="sxs-lookup"><span data-stu-id="e3707-112">Remarks</span></span>



| <span data-ttu-id="e3707-113">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="e3707-113">Vertex shader versions</span></span> | <span data-ttu-id="e3707-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e3707-114">1\_1</span></span> | <span data-ttu-id="e3707-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3707-115">2\_0</span></span> | <span data-ttu-id="e3707-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3707-116">2\_x</span></span> | <span data-ttu-id="e3707-117">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3707-117">2\_sw</span></span> | <span data-ttu-id="e3707-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3707-118">3\_0</span></span> | <span data-ttu-id="e3707-119">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="e3707-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e3707-120">dp3</span><span class="sxs-lookup"><span data-stu-id="e3707-120">dp3</span></span>                    | <span data-ttu-id="e3707-121">x</span><span class="sxs-lookup"><span data-stu-id="e3707-121">x</span></span>    | <span data-ttu-id="e3707-122">x</span><span class="sxs-lookup"><span data-stu-id="e3707-122">x</span></span>    | <span data-ttu-id="e3707-123">x</span><span class="sxs-lookup"><span data-stu-id="e3707-123">x</span></span>    | <span data-ttu-id="e3707-124">x</span><span class="sxs-lookup"><span data-stu-id="e3707-124">x</span></span>     | <span data-ttu-id="e3707-125">x</span><span class="sxs-lookup"><span data-stu-id="e3707-125">x</span></span>    | <span data-ttu-id="e3707-126">x</span><span class="sxs-lookup"><span data-stu-id="e3707-126">x</span></span>     |



 

<span data-ttu-id="e3707-127">下列程式碼片段會顯示執行的作業：</span><span class="sxs-lookup"><span data-stu-id="e3707-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="e3707-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3707-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3707-129">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="e3707-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




