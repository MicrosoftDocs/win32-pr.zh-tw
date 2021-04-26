---
title: abs-vs
description: 計算絕對值。 |abs-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994745"
---
# <a name="abs---vs"></a><span data-ttu-id="60738-104">abs-vs</span><span class="sxs-lookup"><span data-stu-id="60738-104">abs - vs</span></span>

<span data-ttu-id="60738-105">計算絕對值。</span><span class="sxs-lookup"><span data-stu-id="60738-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="60738-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="60738-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="60738-107">abs dst、src</span><span class="sxs-lookup"><span data-stu-id="60738-107">abs dst, src</span></span> |



 

<span data-ttu-id="60738-108">其中</span><span class="sxs-lookup"><span data-stu-id="60738-108">where</span></span>

-   <span data-ttu-id="60738-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="60738-109">dst is the destination register.</span></span>
-   <span data-ttu-id="60738-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="60738-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="60738-111">備註</span><span class="sxs-lookup"><span data-stu-id="60738-111">Remarks</span></span>



| <span data-ttu-id="60738-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="60738-112">Vertex shader versions</span></span> | <span data-ttu-id="60738-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="60738-113">1\_1</span></span> | <span data-ttu-id="60738-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60738-114">2\_0</span></span> | <span data-ttu-id="60738-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="60738-115">2\_x</span></span> | <span data-ttu-id="60738-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="60738-116">2\_sw</span></span> | <span data-ttu-id="60738-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="60738-117">3\_0</span></span> | <span data-ttu-id="60738-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="60738-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="60738-119">abs</span><span class="sxs-lookup"><span data-stu-id="60738-119">abs</span></span>                    |      | <span data-ttu-id="60738-120">x</span><span class="sxs-lookup"><span data-stu-id="60738-120">x</span></span>    | <span data-ttu-id="60738-121">x</span><span class="sxs-lookup"><span data-stu-id="60738-121">x</span></span>    | <span data-ttu-id="60738-122">x</span><span class="sxs-lookup"><span data-stu-id="60738-122">x</span></span>     | <span data-ttu-id="60738-123">x</span><span class="sxs-lookup"><span data-stu-id="60738-123">x</span></span>    | <span data-ttu-id="60738-124">x</span><span class="sxs-lookup"><span data-stu-id="60738-124">x</span></span>     |



 

<span data-ttu-id="60738-125">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="60738-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="60738-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="60738-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60738-127">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="60738-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




