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
ms.openlocfilehash: 612ed14fb538a419a0e7f0b1cf07904d654bb010
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343313"
---
# <a name="abs---vs"></a><span data-ttu-id="cabe1-104">abs-vs</span><span class="sxs-lookup"><span data-stu-id="cabe1-104">abs - vs</span></span>

<span data-ttu-id="cabe1-105">計算絕對值。</span><span class="sxs-lookup"><span data-stu-id="cabe1-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cabe1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cabe1-106">Syntax</span></span>

<span data-ttu-id="cabe1-107">**abs dst、src**</span><span class="sxs-lookup"><span data-stu-id="cabe1-107">**abs dst, src**</span></span>

<span data-ttu-id="cabe1-108">其中</span><span class="sxs-lookup"><span data-stu-id="cabe1-108">where</span></span>

- <span data-ttu-id="cabe1-109">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="cabe1-109">dst is the destination register.</span></span>
- <span data-ttu-id="cabe1-110">src 是來源暫存器。</span><span class="sxs-lookup"><span data-stu-id="cabe1-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cabe1-111">備註</span><span class="sxs-lookup"><span data-stu-id="cabe1-111">Remarks</span></span>



| <span data-ttu-id="cabe1-112">頂點著色器版本</span><span class="sxs-lookup"><span data-stu-id="cabe1-112">Vertex shader versions</span></span> | <span data-ttu-id="cabe1-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="cabe1-113">1\_1</span></span> | <span data-ttu-id="cabe1-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cabe1-114">2\_0</span></span> | <span data-ttu-id="cabe1-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cabe1-115">2\_x</span></span> | <span data-ttu-id="cabe1-116">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cabe1-116">2\_sw</span></span> | <span data-ttu-id="cabe1-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cabe1-117">3\_0</span></span> | <span data-ttu-id="cabe1-118">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="cabe1-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cabe1-119">abs</span><span class="sxs-lookup"><span data-stu-id="cabe1-119">abs</span></span>                    |      | <span data-ttu-id="cabe1-120">x</span><span class="sxs-lookup"><span data-stu-id="cabe1-120">x</span></span>    | <span data-ttu-id="cabe1-121">x</span><span class="sxs-lookup"><span data-stu-id="cabe1-121">x</span></span>    | <span data-ttu-id="cabe1-122">x</span><span class="sxs-lookup"><span data-stu-id="cabe1-122">x</span></span>     | <span data-ttu-id="cabe1-123">x</span><span class="sxs-lookup"><span data-stu-id="cabe1-123">x</span></span>    | <span data-ttu-id="cabe1-124">x</span><span class="sxs-lookup"><span data-stu-id="cabe1-124">x</span></span>     |



 

<span data-ttu-id="cabe1-125">此指示的運作方式如下所示。</span><span class="sxs-lookup"><span data-stu-id="cabe1-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="cabe1-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="cabe1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cabe1-127">頂點著色器指示</span><span class="sxs-lookup"><span data-stu-id="cabe1-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




