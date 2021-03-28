---
title: RWStructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |RWStructuredBuffer：： GetDimensions 函數
ms.assetid: 842b3d21-2e2b-4906-93ee-0252b2e8cf85
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
ms.openlocfilehash: 0e3868f33e372472999c29bffdd8e12bc8ef09b7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973913"
---
# <a name="rwstructuredbuffergetdimensions-function"></a><span data-ttu-id="61402-105">RWStructuredBuffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="61402-105">RWStructuredBuffer::GetDimensions function</span></span>

<span data-ttu-id="61402-106">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="61402-106">Gets the resource dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="61402-107">語法</span><span class="sxs-lookup"><span data-stu-id="61402-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a><span data-ttu-id="61402-108">參數</span><span class="sxs-lookup"><span data-stu-id="61402-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61402-109">*numStructs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61402-109">*numStructs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61402-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="61402-110">Type: **uint**</span></span>

<span data-ttu-id="61402-111">資源中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="61402-111">The number of structures in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="61402-112">*stride* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61402-112">*stride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61402-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="61402-113">Type: **uint**</span></span>

<span data-ttu-id="61402-114">每個結構元素的 stride （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="61402-114">The stride, in bytes, of each structure element.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61402-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="61402-115">Return value</span></span>

<span data-ttu-id="61402-116">Nothing</span><span class="sxs-lookup"><span data-stu-id="61402-116">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="61402-117">備註</span><span class="sxs-lookup"><span data-stu-id="61402-117">Remarks</span></span>

<span data-ttu-id="61402-118">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="61402-118">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="61402-119">頂點</span><span class="sxs-lookup"><span data-stu-id="61402-119">Vertex</span></span> | <span data-ttu-id="61402-120">船體</span><span class="sxs-lookup"><span data-stu-id="61402-120">Hull</span></span> | <span data-ttu-id="61402-121">網域</span><span class="sxs-lookup"><span data-stu-id="61402-121">Domain</span></span> | <span data-ttu-id="61402-122">幾何</span><span class="sxs-lookup"><span data-stu-id="61402-122">Geometry</span></span> | <span data-ttu-id="61402-123">像素</span><span class="sxs-lookup"><span data-stu-id="61402-123">Pixel</span></span> | <span data-ttu-id="61402-124">計算</span><span class="sxs-lookup"><span data-stu-id="61402-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="61402-125">x</span><span class="sxs-lookup"><span data-stu-id="61402-125">x</span></span>     | <span data-ttu-id="61402-126">x</span><span class="sxs-lookup"><span data-stu-id="61402-126">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="61402-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61402-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61402-128">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="61402-128">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="61402-129">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="61402-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




