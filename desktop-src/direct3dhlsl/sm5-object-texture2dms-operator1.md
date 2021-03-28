---
title: Texture2DMS：： Operator 函數
description: 從位於範例索引0所提供位置的資源抓取值。
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104971852"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="b621e-104">Texture2DMS：： Operator 函數</span><span class="sxs-lookup"><span data-stu-id="b621e-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="b621e-105">從位於範例索引0所提供位置的資源抓取值。</span><span class="sxs-lookup"><span data-stu-id="b621e-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="b621e-106">語法</span><span class="sxs-lookup"><span data-stu-id="b621e-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="b621e-107">參數</span><span class="sxs-lookup"><span data-stu-id="b621e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b621e-108">*pos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b621e-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b621e-109">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="b621e-109">Type: **uint2**</span></span>

<span data-ttu-id="b621e-110">索引位置。</span><span class="sxs-lookup"><span data-stu-id="b621e-110">The index position.</span></span> <span data-ttu-id="b621e-111">包含 (x，y) 座標。</span><span class="sxs-lookup"><span data-stu-id="b621e-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b621e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b621e-112">Return value</span></span>

<span data-ttu-id="b621e-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="b621e-113">Type: **R**</span></span>

<span data-ttu-id="b621e-114">唯讀的資源變數。</span><span class="sxs-lookup"><span data-stu-id="b621e-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b621e-115">備註</span><span class="sxs-lookup"><span data-stu-id="b621e-115">Remarks</span></span>

<span data-ttu-id="b621e-116">若要選取特定的範例，請參閱 [**範例。\[運算子 \] 。 \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="b621e-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="b621e-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b621e-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b621e-118">頂點</span><span class="sxs-lookup"><span data-stu-id="b621e-118">Vertex</span></span> | <span data-ttu-id="b621e-119">船體</span><span class="sxs-lookup"><span data-stu-id="b621e-119">Hull</span></span> | <span data-ttu-id="b621e-120">網域</span><span class="sxs-lookup"><span data-stu-id="b621e-120">Domain</span></span> | <span data-ttu-id="b621e-121">幾何</span><span class="sxs-lookup"><span data-stu-id="b621e-121">Geometry</span></span> | <span data-ttu-id="b621e-122">像素</span><span class="sxs-lookup"><span data-stu-id="b621e-122">Pixel</span></span> | <span data-ttu-id="b621e-123">計算</span><span class="sxs-lookup"><span data-stu-id="b621e-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b621e-124">x</span><span class="sxs-lookup"><span data-stu-id="b621e-124">x</span></span>      | <span data-ttu-id="b621e-125">x</span><span class="sxs-lookup"><span data-stu-id="b621e-125">x</span></span>    | <span data-ttu-id="b621e-126">x</span><span class="sxs-lookup"><span data-stu-id="b621e-126">x</span></span>      | <span data-ttu-id="b621e-127">x</span><span class="sxs-lookup"><span data-stu-id="b621e-127">x</span></span>        | <span data-ttu-id="b621e-128">x</span><span class="sxs-lookup"><span data-stu-id="b621e-128">x</span></span>     | <span data-ttu-id="b621e-129">x</span><span class="sxs-lookup"><span data-stu-id="b621e-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b621e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b621e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b621e-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="b621e-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="b621e-132">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b621e-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




