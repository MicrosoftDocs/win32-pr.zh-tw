---
title: ConsumeStructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |ConsumeStructuredBuffer：： GetDimensions 函數
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991882"
---
# <a name="consumestructuredbuffergetdimensions-function"></a><span data-ttu-id="33f71-105">ConsumeStructuredBuffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="33f71-105">ConsumeStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="33f71-106">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="33f71-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f71-107">語法</span><span class="sxs-lookup"><span data-stu-id="33f71-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="33f71-108">參數</span><span class="sxs-lookup"><span data-stu-id="33f71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f71-109">*numStructs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="33f71-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33f71-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="33f71-110">Type: **uint**</span></span>

<span data-ttu-id="33f71-111">結構的數目。</span><span class="sxs-lookup"><span data-stu-id="33f71-111">The number of structures.</span></span>

</dd> <dt>

<span data-ttu-id="33f71-112">*stride* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="33f71-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33f71-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="33f71-113">Type: **uint**</span></span>

<span data-ttu-id="33f71-114">每個元素的 stride （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="33f71-114">The stride, in bytes, of each element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33f71-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="33f71-115">Return value</span></span>

<span data-ttu-id="33f71-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="33f71-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33f71-117">備註</span><span class="sxs-lookup"><span data-stu-id="33f71-117">Remarks</span></span>

<span data-ttu-id="33f71-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="33f71-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="33f71-119">頂點</span><span class="sxs-lookup"><span data-stu-id="33f71-119">Vertex</span></span> | <span data-ttu-id="33f71-120">船體</span><span class="sxs-lookup"><span data-stu-id="33f71-120">Hull</span></span> | <span data-ttu-id="33f71-121">網域</span><span class="sxs-lookup"><span data-stu-id="33f71-121">Domain</span></span> | <span data-ttu-id="33f71-122">幾何</span><span class="sxs-lookup"><span data-stu-id="33f71-122">Geometry</span></span> | <span data-ttu-id="33f71-123">像素</span><span class="sxs-lookup"><span data-stu-id="33f71-123">Pixel</span></span> | <span data-ttu-id="33f71-124">計算</span><span class="sxs-lookup"><span data-stu-id="33f71-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="33f71-125">x</span><span class="sxs-lookup"><span data-stu-id="33f71-125">x</span></span>      | <span data-ttu-id="33f71-126">x</span><span class="sxs-lookup"><span data-stu-id="33f71-126">x</span></span>    | <span data-ttu-id="33f71-127">x</span><span class="sxs-lookup"><span data-stu-id="33f71-127">x</span></span>      | <span data-ttu-id="33f71-128">x</span><span class="sxs-lookup"><span data-stu-id="33f71-128">x</span></span>        | <span data-ttu-id="33f71-129">x</span><span class="sxs-lookup"><span data-stu-id="33f71-129">x</span></span>     | <span data-ttu-id="33f71-130">x</span><span class="sxs-lookup"><span data-stu-id="33f71-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="33f71-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33f71-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f71-132">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="33f71-132">ConsumeStructuredBuffer</span></span>](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="33f71-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="33f71-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




