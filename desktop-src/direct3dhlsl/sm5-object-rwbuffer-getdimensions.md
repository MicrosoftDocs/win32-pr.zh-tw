---
title: RWBuffer：： GetDimensions 函數
description: 取得緩衝區的長度。 |RWBuffer：： GetDimensions 函數
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992066"
---
# <a name="rwbuffergetdimensions-function"></a><span data-ttu-id="d8116-105">RWBuffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="d8116-105">RWBuffer::GetDimensions function</span></span>

<span data-ttu-id="d8116-106">取得緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="d8116-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8116-107">語法</span><span class="sxs-lookup"><span data-stu-id="d8116-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="d8116-108">參數</span><span class="sxs-lookup"><span data-stu-id="d8116-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8116-109">*dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d8116-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8116-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="d8116-110">Type: **uint**</span></span>

<span data-ttu-id="d8116-111">緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d8116-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8116-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8116-112">Return value</span></span>

<span data-ttu-id="d8116-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="d8116-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="d8116-114">備註</span><span class="sxs-lookup"><span data-stu-id="d8116-114">Remarks</span></span>

<span data-ttu-id="d8116-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="d8116-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d8116-116">頂點</span><span class="sxs-lookup"><span data-stu-id="d8116-116">Vertex</span></span> | <span data-ttu-id="d8116-117">船體</span><span class="sxs-lookup"><span data-stu-id="d8116-117">Hull</span></span> | <span data-ttu-id="d8116-118">網域</span><span class="sxs-lookup"><span data-stu-id="d8116-118">Domain</span></span> | <span data-ttu-id="d8116-119">幾何</span><span class="sxs-lookup"><span data-stu-id="d8116-119">Geometry</span></span> | <span data-ttu-id="d8116-120">像素</span><span class="sxs-lookup"><span data-stu-id="d8116-120">Pixel</span></span> | <span data-ttu-id="d8116-121">計算</span><span class="sxs-lookup"><span data-stu-id="d8116-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d8116-122">x</span><span class="sxs-lookup"><span data-stu-id="d8116-122">x</span></span>     | <span data-ttu-id="d8116-123">x</span><span class="sxs-lookup"><span data-stu-id="d8116-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d8116-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8116-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8116-125">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="d8116-125">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="d8116-126">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d8116-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




