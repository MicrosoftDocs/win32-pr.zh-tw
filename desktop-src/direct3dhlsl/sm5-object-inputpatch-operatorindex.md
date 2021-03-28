---
title: InputPatch：： Operator 函數
description: 傳回修補程式中的第 n 個控制點。 |InputPatch：： Operator 函數
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- 運算子函式 HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195962"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="e8db6-105">InputPatch：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="e8db6-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="e8db6-106">傳回修補程式中的 <sup>第</sup> *n* 個控制點。</span><span class="sxs-lookup"><span data-stu-id="e8db6-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8db6-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8db6-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="e8db6-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8db6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8db6-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8db6-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8db6-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e8db6-110">Type: **uint**</span></span>

<span data-ttu-id="e8db6-111">輸入索引。</span><span class="sxs-lookup"><span data-stu-id="e8db6-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8db6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8db6-112">Return value</span></span>

<span data-ttu-id="e8db6-113">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="e8db6-113">Type: **T**</span></span>

<span data-ttu-id="e8db6-114">第 *n*<sup></sup>個控制點。</span><span class="sxs-lookup"><span data-stu-id="e8db6-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8db6-115">備註</span><span class="sxs-lookup"><span data-stu-id="e8db6-115">Remarks</span></span>

<span data-ttu-id="e8db6-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e8db6-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e8db6-117">頂點</span><span class="sxs-lookup"><span data-stu-id="e8db6-117">Vertex</span></span> | <span data-ttu-id="e8db6-118">船體</span><span class="sxs-lookup"><span data-stu-id="e8db6-118">Hull</span></span> | <span data-ttu-id="e8db6-119">網域</span><span class="sxs-lookup"><span data-stu-id="e8db6-119">Domain</span></span> | <span data-ttu-id="e8db6-120">幾何</span><span class="sxs-lookup"><span data-stu-id="e8db6-120">Geometry</span></span> | <span data-ttu-id="e8db6-121">像素</span><span class="sxs-lookup"><span data-stu-id="e8db6-121">Pixel</span></span> | <span data-ttu-id="e8db6-122">計算</span><span class="sxs-lookup"><span data-stu-id="e8db6-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e8db6-123">x</span><span class="sxs-lookup"><span data-stu-id="e8db6-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="e8db6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8db6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8db6-125">InputPatch</span><span class="sxs-lookup"><span data-stu-id="e8db6-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="e8db6-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e8db6-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




