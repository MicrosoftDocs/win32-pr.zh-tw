---
title: OutputPatch：： Operator 函數
description: 傳回修補程式中的第 n 個控制點。 |OutputPatch：： Operator 函數
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322060"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="c25c4-105">OutputPatch：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="c25c4-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="c25c4-106">傳回修補程式中的 <sup>第</sup> *n* 個控制點。</span><span class="sxs-lookup"><span data-stu-id="c25c4-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c25c4-107">語法</span><span class="sxs-lookup"><span data-stu-id="c25c4-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="c25c4-108">參數</span><span class="sxs-lookup"><span data-stu-id="c25c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c25c4-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c25c4-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c25c4-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c25c4-110">Type: **uint**</span></span>

<span data-ttu-id="c25c4-111">輸入索引。</span><span class="sxs-lookup"><span data-stu-id="c25c4-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c25c4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c25c4-112">Return value</span></span>

<span data-ttu-id="c25c4-113">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="c25c4-113">Type: **T**</span></span>

<span data-ttu-id="c25c4-114">第 *n*<sup></sup>個控制點。</span><span class="sxs-lookup"><span data-stu-id="c25c4-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="c25c4-115">備註</span><span class="sxs-lookup"><span data-stu-id="c25c4-115">Remarks</span></span>

<span data-ttu-id="c25c4-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c25c4-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c25c4-117">頂點</span><span class="sxs-lookup"><span data-stu-id="c25c4-117">Vertex</span></span> | <span data-ttu-id="c25c4-118">船體</span><span class="sxs-lookup"><span data-stu-id="c25c4-118">Hull</span></span> | <span data-ttu-id="c25c4-119">網域</span><span class="sxs-lookup"><span data-stu-id="c25c4-119">Domain</span></span> | <span data-ttu-id="c25c4-120">幾何</span><span class="sxs-lookup"><span data-stu-id="c25c4-120">Geometry</span></span> | <span data-ttu-id="c25c4-121">像素</span><span class="sxs-lookup"><span data-stu-id="c25c4-121">Pixel</span></span> | <span data-ttu-id="c25c4-122">計算</span><span class="sxs-lookup"><span data-stu-id="c25c4-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="c25c4-123">x</span><span class="sxs-lookup"><span data-stu-id="c25c4-123">x</span></span>    | <span data-ttu-id="c25c4-124">x</span><span class="sxs-lookup"><span data-stu-id="c25c4-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="c25c4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c25c4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25c4-126">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="c25c4-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="c25c4-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c25c4-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




