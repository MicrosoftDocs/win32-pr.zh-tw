---
title: StructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |StructuredBuffer：： GetDimensions 函數
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: 2b3d7c879c77386ddee80a63053711b8ae34ee8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322160"
---
# <a name="structuredbuffergetdimensions-function"></a><span data-ttu-id="a174e-105">StructuredBuffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="a174e-105">StructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="a174e-106">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="a174e-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a174e-107">語法</span><span class="sxs-lookup"><span data-stu-id="a174e-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="a174e-108">參數</span><span class="sxs-lookup"><span data-stu-id="a174e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a174e-109">*numStructs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a174e-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a174e-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="a174e-110">Type: **uint**</span></span>

<span data-ttu-id="a174e-111">資源中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="a174e-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a174e-112">*stride* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a174e-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a174e-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="a174e-113">Type: **uint**</span></span>

<span data-ttu-id="a174e-114">每個結構元素的 stride （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a174e-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a174e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a174e-115">Return value</span></span>

<span data-ttu-id="a174e-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a174e-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a174e-117">備註</span><span class="sxs-lookup"><span data-stu-id="a174e-117">Remarks</span></span>

<span data-ttu-id="a174e-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="a174e-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a174e-119">頂點</span><span class="sxs-lookup"><span data-stu-id="a174e-119">Vertex</span></span> | <span data-ttu-id="a174e-120">船體</span><span class="sxs-lookup"><span data-stu-id="a174e-120">Hull</span></span> | <span data-ttu-id="a174e-121">網域</span><span class="sxs-lookup"><span data-stu-id="a174e-121">Domain</span></span> | <span data-ttu-id="a174e-122">幾何</span><span class="sxs-lookup"><span data-stu-id="a174e-122">Geometry</span></span> | <span data-ttu-id="a174e-123">像素</span><span class="sxs-lookup"><span data-stu-id="a174e-123">Pixel</span></span> | <span data-ttu-id="a174e-124">計算</span><span class="sxs-lookup"><span data-stu-id="a174e-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a174e-125">x</span><span class="sxs-lookup"><span data-stu-id="a174e-125">x</span></span>      | <span data-ttu-id="a174e-126">x</span><span class="sxs-lookup"><span data-stu-id="a174e-126">x</span></span>    | <span data-ttu-id="a174e-127">x</span><span class="sxs-lookup"><span data-stu-id="a174e-127">x</span></span>      | <span data-ttu-id="a174e-128">x</span><span class="sxs-lookup"><span data-stu-id="a174e-128">x</span></span>        | <span data-ttu-id="a174e-129">x</span><span class="sxs-lookup"><span data-stu-id="a174e-129">x</span></span>     | <span data-ttu-id="a174e-130">x</span><span class="sxs-lookup"><span data-stu-id="a174e-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a174e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a174e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a174e-132">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="a174e-132">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="a174e-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="a174e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




