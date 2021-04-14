---
title: RWBuffer：： Operator 函數
description: 傳回資源變數。 |RWBuffer：： Operator 函數
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991878"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="e669e-105">RWBuffer：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="e669e-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="e669e-106">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="e669e-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e669e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e669e-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="e669e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e669e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e669e-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e669e-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e669e-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e669e-110">Type: **uint**</span></span>

<span data-ttu-id="e669e-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="e669e-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e669e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e669e-112">Return value</span></span>

<span data-ttu-id="e669e-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="e669e-113">Type: **R**</span></span>

<span data-ttu-id="e669e-114">資源變數。</span><span class="sxs-lookup"><span data-stu-id="e669e-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="e669e-115">備註</span><span class="sxs-lookup"><span data-stu-id="e669e-115">Remarks</span></span>

<span data-ttu-id="e669e-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e669e-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e669e-117">頂點</span><span class="sxs-lookup"><span data-stu-id="e669e-117">Vertex</span></span> | <span data-ttu-id="e669e-118">船體</span><span class="sxs-lookup"><span data-stu-id="e669e-118">Hull</span></span> | <span data-ttu-id="e669e-119">網域</span><span class="sxs-lookup"><span data-stu-id="e669e-119">Domain</span></span> | <span data-ttu-id="e669e-120">幾何</span><span class="sxs-lookup"><span data-stu-id="e669e-120">Geometry</span></span> | <span data-ttu-id="e669e-121">像素</span><span class="sxs-lookup"><span data-stu-id="e669e-121">Pixel</span></span> | <span data-ttu-id="e669e-122">計算</span><span class="sxs-lookup"><span data-stu-id="e669e-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e669e-123">x</span><span class="sxs-lookup"><span data-stu-id="e669e-123">x</span></span>      | <span data-ttu-id="e669e-124">x</span><span class="sxs-lookup"><span data-stu-id="e669e-124">x</span></span>    | <span data-ttu-id="e669e-125">x</span><span class="sxs-lookup"><span data-stu-id="e669e-125">x</span></span>      | <span data-ttu-id="e669e-126">x</span><span class="sxs-lookup"><span data-stu-id="e669e-126">x</span></span>        | <span data-ttu-id="e669e-127">x</span><span class="sxs-lookup"><span data-stu-id="e669e-127">x</span></span>     | <span data-ttu-id="e669e-128">x</span><span class="sxs-lookup"><span data-stu-id="e669e-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e669e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e669e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e669e-130">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="e669e-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="e669e-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e669e-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




