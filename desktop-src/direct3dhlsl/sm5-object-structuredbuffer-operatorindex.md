---
title: StructuredBuffer：： Operator 函數
description: 傳回 StructuredBuffer 的唯讀資源變數。
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093668"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="5a8d0-104">StructuredBuffer：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="5a8d0-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="5a8d0-105">傳回 [**StructuredBuffer**](sm5-object-structuredbuffer.md)的唯讀資源變數。</span><span class="sxs-lookup"><span data-stu-id="5a8d0-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8d0-106">語法</span><span class="sxs-lookup"><span data-stu-id="5a8d0-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="5a8d0-107">參數</span><span class="sxs-lookup"><span data-stu-id="5a8d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a8d0-108">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a8d0-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a8d0-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="5a8d0-109">Type: **uint**</span></span>

<span data-ttu-id="5a8d0-110">索引位置。</span><span class="sxs-lookup"><span data-stu-id="5a8d0-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a8d0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a8d0-111">Return value</span></span>

<span data-ttu-id="5a8d0-112">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="5a8d0-112">Type: **R**</span></span>

<span data-ttu-id="5a8d0-113">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="5a8d0-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a8d0-114">備註</span><span class="sxs-lookup"><span data-stu-id="5a8d0-114">Remarks</span></span>

<span data-ttu-id="5a8d0-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="5a8d0-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5a8d0-116">頂點</span><span class="sxs-lookup"><span data-stu-id="5a8d0-116">Vertex</span></span> | <span data-ttu-id="5a8d0-117">船體</span><span class="sxs-lookup"><span data-stu-id="5a8d0-117">Hull</span></span> | <span data-ttu-id="5a8d0-118">網域</span><span class="sxs-lookup"><span data-stu-id="5a8d0-118">Domain</span></span> | <span data-ttu-id="5a8d0-119">幾何</span><span class="sxs-lookup"><span data-stu-id="5a8d0-119">Geometry</span></span> | <span data-ttu-id="5a8d0-120">像素</span><span class="sxs-lookup"><span data-stu-id="5a8d0-120">Pixel</span></span> | <span data-ttu-id="5a8d0-121">計算</span><span class="sxs-lookup"><span data-stu-id="5a8d0-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5a8d0-122">x</span><span class="sxs-lookup"><span data-stu-id="5a8d0-122">x</span></span>      | <span data-ttu-id="5a8d0-123">x</span><span class="sxs-lookup"><span data-stu-id="5a8d0-123">x</span></span>    | <span data-ttu-id="5a8d0-124">x</span><span class="sxs-lookup"><span data-stu-id="5a8d0-124">x</span></span>      | <span data-ttu-id="5a8d0-125">x</span><span class="sxs-lookup"><span data-stu-id="5a8d0-125">x</span></span>        | <span data-ttu-id="5a8d0-126">x</span><span class="sxs-lookup"><span data-stu-id="5a8d0-126">x</span></span>     | <span data-ttu-id="5a8d0-127">x</span><span class="sxs-lookup"><span data-stu-id="5a8d0-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5a8d0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a8d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8d0-129">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="5a8d0-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="5a8d0-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="5a8d0-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




