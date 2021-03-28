---
title: dst 函數
description: 計算距離向量。 |dst 函數
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- dst 函數 HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853608"
---
# <a name="dst-function"></a><span data-ttu-id="19e24-105">dst 函數</span><span class="sxs-lookup"><span data-stu-id="19e24-105">dst function</span></span>

<span data-ttu-id="19e24-106">計算距離向量。</span><span class="sxs-lookup"><span data-stu-id="19e24-106">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e24-107">語法</span><span class="sxs-lookup"><span data-stu-id="19e24-107">Syntax</span></span>

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a><span data-ttu-id="19e24-108">參數</span><span class="sxs-lookup"><span data-stu-id="19e24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e24-109">*src0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19e24-109">*src0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e24-110">類型： **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="19e24-110">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="19e24-111">第一個向量。</span><span class="sxs-lookup"><span data-stu-id="19e24-111">The first vector.</span></span>

</dd> <dt>

<span data-ttu-id="19e24-112">*src1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19e24-112">*src1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e24-113">類型： **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="19e24-113">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="19e24-114">第二個向量。</span><span class="sxs-lookup"><span data-stu-id="19e24-114">The second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e24-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="19e24-115">Return value</span></span>

<span data-ttu-id="19e24-116">類型： **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="19e24-116">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="19e24-117">計算距離向量。</span><span class="sxs-lookup"><span data-stu-id="19e24-117">The computed distance vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e24-118">備註</span><span class="sxs-lookup"><span data-stu-id="19e24-118">Remarks</span></span>

<span data-ttu-id="19e24-119">這個內建函式提供的功能與端點著色器的 [dst](dst---vs.md)指示相同。</span><span class="sxs-lookup"><span data-stu-id="19e24-119">This intrinsic function provides the same functionality as the Vertex Shader instruction [dst](dst---vs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="19e24-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19e24-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e24-121">內建函式</span><span class="sxs-lookup"><span data-stu-id="19e24-121">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




