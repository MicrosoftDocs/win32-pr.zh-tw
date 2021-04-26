---
title: abs-ps
description: 計算絕對值。 |abs-ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3e7af7b2d30e9d9f2092cb6671610f008ec781d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994875"
---
# <a name="abs---ps"></a><span data-ttu-id="d0327-104">abs-ps</span><span class="sxs-lookup"><span data-stu-id="d0327-104">abs - ps</span></span>

<span data-ttu-id="d0327-105">計算絕對值。</span><span class="sxs-lookup"><span data-stu-id="d0327-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0327-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0327-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="d0327-107">abs dst、src</span><span class="sxs-lookup"><span data-stu-id="d0327-107">abs dst, src</span></span> |



 

<span data-ttu-id="d0327-108">其中</span><span class="sxs-lookup"><span data-stu-id="d0327-108">where</span></span>

-   <span data-ttu-id="d0327-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="d0327-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d0327-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="d0327-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0327-111">備註</span><span class="sxs-lookup"><span data-stu-id="d0327-111">Remarks</span></span>



| <span data-ttu-id="d0327-112">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="d0327-112">Pixel shader versions</span></span> | <span data-ttu-id="d0327-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="d0327-113">1\_1</span></span> | <span data-ttu-id="d0327-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="d0327-114">1\_2</span></span> | <span data-ttu-id="d0327-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d0327-115">1\_3</span></span> | <span data-ttu-id="d0327-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="d0327-116">1\_4</span></span> | <span data-ttu-id="d0327-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0327-117">2\_0</span></span> | <span data-ttu-id="d0327-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d0327-118">2\_x</span></span> | <span data-ttu-id="d0327-119">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d0327-119">2\_sw</span></span> | <span data-ttu-id="d0327-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d0327-120">3\_0</span></span> | <span data-ttu-id="d0327-121">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d0327-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d0327-122">abs</span><span class="sxs-lookup"><span data-stu-id="d0327-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="d0327-123">x</span><span class="sxs-lookup"><span data-stu-id="d0327-123">x</span></span>    | <span data-ttu-id="d0327-124">x</span><span class="sxs-lookup"><span data-stu-id="d0327-124">x</span></span>    | <span data-ttu-id="d0327-125">x</span><span class="sxs-lookup"><span data-stu-id="d0327-125">x</span></span>     | <span data-ttu-id="d0327-126">x</span><span class="sxs-lookup"><span data-stu-id="d0327-126">x</span></span>    | <span data-ttu-id="d0327-127">x</span><span class="sxs-lookup"><span data-stu-id="d0327-127">x</span></span>     |



 

<span data-ttu-id="d0327-128">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="d0327-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="d0327-129">指示資訊</span><span class="sxs-lookup"><span data-stu-id="d0327-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="d0327-130">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="d0327-130">Minimum operating system</span></span> | <span data-ttu-id="d0327-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d0327-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d0327-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0327-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0327-133">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="d0327-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




