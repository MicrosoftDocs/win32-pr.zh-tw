---
title: AppendStructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |AppendStructuredBuffer：： GetDimensions 函數
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973920"
---
# <a name="appendstructuredbuffergetdimensions-function"></a><span data-ttu-id="f73b6-105">AppendStructuredBuffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="f73b6-105">AppendStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="f73b6-106">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="f73b6-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f73b6-107">語法</span><span class="sxs-lookup"><span data-stu-id="f73b6-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="f73b6-108">參數</span><span class="sxs-lookup"><span data-stu-id="f73b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f73b6-109">*numStructs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f73b6-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f73b6-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="f73b6-110">Type: **uint**</span></span>

<span data-ttu-id="f73b6-111">結構的數目。</span><span class="sxs-lookup"><span data-stu-id="f73b6-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="f73b6-112">*stride* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f73b6-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f73b6-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="f73b6-113">Type: **uint**</span></span>

<span data-ttu-id="f73b6-114">每個元素中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f73b6-114">The number of bytes in each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f73b6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f73b6-115">Return value</span></span>

<span data-ttu-id="f73b6-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f73b6-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f73b6-117">備註</span><span class="sxs-lookup"><span data-stu-id="f73b6-117">Remarks</span></span>

<span data-ttu-id="f73b6-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="f73b6-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f73b6-119">頂點</span><span class="sxs-lookup"><span data-stu-id="f73b6-119">Vertex</span></span> | <span data-ttu-id="f73b6-120">船體</span><span class="sxs-lookup"><span data-stu-id="f73b6-120">Hull</span></span> | <span data-ttu-id="f73b6-121">網域</span><span class="sxs-lookup"><span data-stu-id="f73b6-121">Domain</span></span> | <span data-ttu-id="f73b6-122">幾何</span><span class="sxs-lookup"><span data-stu-id="f73b6-122">Geometry</span></span> | <span data-ttu-id="f73b6-123">像素</span><span class="sxs-lookup"><span data-stu-id="f73b6-123">Pixel</span></span> | <span data-ttu-id="f73b6-124">計算</span><span class="sxs-lookup"><span data-stu-id="f73b6-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f73b6-125">x</span><span class="sxs-lookup"><span data-stu-id="f73b6-125">x</span></span>      | <span data-ttu-id="f73b6-126">x</span><span class="sxs-lookup"><span data-stu-id="f73b6-126">x</span></span>    | <span data-ttu-id="f73b6-127">x</span><span class="sxs-lookup"><span data-stu-id="f73b6-127">x</span></span>      | <span data-ttu-id="f73b6-128">x</span><span class="sxs-lookup"><span data-stu-id="f73b6-128">x</span></span>        | <span data-ttu-id="f73b6-129">x</span><span class="sxs-lookup"><span data-stu-id="f73b6-129">x</span></span>     | <span data-ttu-id="f73b6-130">x</span><span class="sxs-lookup"><span data-stu-id="f73b6-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f73b6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f73b6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f73b6-132">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="f73b6-132">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="f73b6-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f73b6-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




