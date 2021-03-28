---
title: RWStructuredBuffer：： Operator 函數
description: 傳回資源變數。 |RWStructuredBuffer：： Operator 函數
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514413"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="1d86a-105">RWStructuredBuffer：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="1d86a-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="1d86a-106">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="1d86a-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d86a-107">語法</span><span class="sxs-lookup"><span data-stu-id="1d86a-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="1d86a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1d86a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d86a-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d86a-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d86a-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="1d86a-110">Type: **uint**</span></span>

<span data-ttu-id="1d86a-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="1d86a-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d86a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d86a-112">Return value</span></span>

<span data-ttu-id="1d86a-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="1d86a-113">Type: **R**</span></span>

<span data-ttu-id="1d86a-114">資源變數。</span><span class="sxs-lookup"><span data-stu-id="1d86a-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d86a-115">備註</span><span class="sxs-lookup"><span data-stu-id="1d86a-115">Remarks</span></span>

<span data-ttu-id="1d86a-116">結構化資源可以根據結構的元件名稱進一步編制索引。</span><span class="sxs-lookup"><span data-stu-id="1d86a-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="1d86a-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="1d86a-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1d86a-118">頂點</span><span class="sxs-lookup"><span data-stu-id="1d86a-118">Vertex</span></span> | <span data-ttu-id="1d86a-119">船體</span><span class="sxs-lookup"><span data-stu-id="1d86a-119">Hull</span></span> | <span data-ttu-id="1d86a-120">網域</span><span class="sxs-lookup"><span data-stu-id="1d86a-120">Domain</span></span> | <span data-ttu-id="1d86a-121">幾何</span><span class="sxs-lookup"><span data-stu-id="1d86a-121">Geometry</span></span> | <span data-ttu-id="1d86a-122">像素</span><span class="sxs-lookup"><span data-stu-id="1d86a-122">Pixel</span></span> | <span data-ttu-id="1d86a-123">計算</span><span class="sxs-lookup"><span data-stu-id="1d86a-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1d86a-124">x</span><span class="sxs-lookup"><span data-stu-id="1d86a-124">x</span></span>     | <span data-ttu-id="1d86a-125">x</span><span class="sxs-lookup"><span data-stu-id="1d86a-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1d86a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d86a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d86a-127">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="1d86a-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="1d86a-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1d86a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




