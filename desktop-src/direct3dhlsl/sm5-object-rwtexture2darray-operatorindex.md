---
title: RWTexture2DArray：： Operator 函數
description: 傳回資源變數。 |RWTexture2DArray：： Operator 函數
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035245"
---
# <a name="rwtexture2darrayoperator--function"></a><span data-ttu-id="1628f-105">RWTexture2DArray：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="1628f-105">RWTexture2DArray::Operator  function</span></span>

<span data-ttu-id="1628f-106">傳回資源變數。</span><span class="sxs-lookup"><span data-stu-id="1628f-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="1628f-107">語法</span><span class="sxs-lookup"><span data-stu-id="1628f-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="1628f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1628f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1628f-109">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1628f-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1628f-110">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="1628f-110">Type: **uint3**</span></span>

<span data-ttu-id="1628f-111">索引位置。</span><span class="sxs-lookup"><span data-stu-id="1628f-111">The index position.</span></span> <span data-ttu-id="1628f-112">第一個和第二個元件包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="1628f-112">The first and second components contain the (x, y) coordinates.</span></span> <span data-ttu-id="1628f-113">第三個元件表示所要的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="1628f-113">The third component indicates the desired array slice.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1628f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1628f-114">Return value</span></span>

<span data-ttu-id="1628f-115">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="1628f-115">Type: **R**</span></span>

<span data-ttu-id="1628f-116">資源變數。</span><span class="sxs-lookup"><span data-stu-id="1628f-116">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="1628f-117">備註</span><span class="sxs-lookup"><span data-stu-id="1628f-117">Remarks</span></span>

<span data-ttu-id="1628f-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="1628f-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1628f-119">頂點</span><span class="sxs-lookup"><span data-stu-id="1628f-119">Vertex</span></span> | <span data-ttu-id="1628f-120">船體</span><span class="sxs-lookup"><span data-stu-id="1628f-120">Hull</span></span> | <span data-ttu-id="1628f-121">網域</span><span class="sxs-lookup"><span data-stu-id="1628f-121">Domain</span></span> | <span data-ttu-id="1628f-122">幾何</span><span class="sxs-lookup"><span data-stu-id="1628f-122">Geometry</span></span> | <span data-ttu-id="1628f-123">像素</span><span class="sxs-lookup"><span data-stu-id="1628f-123">Pixel</span></span> | <span data-ttu-id="1628f-124">計算</span><span class="sxs-lookup"><span data-stu-id="1628f-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1628f-125">x</span><span class="sxs-lookup"><span data-stu-id="1628f-125">x</span></span>     | <span data-ttu-id="1628f-126">x</span><span class="sxs-lookup"><span data-stu-id="1628f-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1628f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1628f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1628f-128">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="1628f-128">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="1628f-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1628f-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




