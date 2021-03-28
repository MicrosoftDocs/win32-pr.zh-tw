---
title: RWTexture1DArray：： Operator 函數
description: 傳回資源變數。 |RWTexture1DArray：： Operator 函數
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974228"
---
# <a name="rwtexture1darrayoperator--function"></a><span data-ttu-id="8d477-105">RWTexture1DArray：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="8d477-105">RWTexture1DArray::Operator  function</span></span>

<span data-ttu-id="8d477-106">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="8d477-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d477-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d477-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="8d477-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d477-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d477-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d477-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d477-110">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="8d477-110">Type: **uint2**</span></span>

<span data-ttu-id="8d477-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="8d477-111">The index position.</span></span> <span data-ttu-id="8d477-112">第一個元件包含 x 座標。</span><span class="sxs-lookup"><span data-stu-id="8d477-112">The first component contains the x coordinate.</span></span> <span data-ttu-id="8d477-113">第二個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="8d477-113">The second component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d477-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d477-114">Return value</span></span>

<span data-ttu-id="8d477-115">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="8d477-115">Type: **R**</span></span>

<span data-ttu-id="8d477-116">資源變數。</span><span class="sxs-lookup"><span data-stu-id="8d477-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d477-117">備註</span><span class="sxs-lookup"><span data-stu-id="8d477-117">Remarks</span></span>

<span data-ttu-id="8d477-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8d477-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8d477-119">頂點</span><span class="sxs-lookup"><span data-stu-id="8d477-119">Vertex</span></span> | <span data-ttu-id="8d477-120">船體</span><span class="sxs-lookup"><span data-stu-id="8d477-120">Hull</span></span> | <span data-ttu-id="8d477-121">網域</span><span class="sxs-lookup"><span data-stu-id="8d477-121">Domain</span></span> | <span data-ttu-id="8d477-122">幾何</span><span class="sxs-lookup"><span data-stu-id="8d477-122">Geometry</span></span> | <span data-ttu-id="8d477-123">像素</span><span class="sxs-lookup"><span data-stu-id="8d477-123">Pixel</span></span> | <span data-ttu-id="8d477-124">計算</span><span class="sxs-lookup"><span data-stu-id="8d477-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8d477-125">x</span><span class="sxs-lookup"><span data-stu-id="8d477-125">x</span></span>     | <span data-ttu-id="8d477-126">x</span><span class="sxs-lookup"><span data-stu-id="8d477-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8d477-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d477-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d477-128">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="8d477-128">RWTexture1DArray</span></span>](sm5-object-rwtexture1darray.md)
</dt> <dt>

[<span data-ttu-id="8d477-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8d477-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




