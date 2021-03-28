---
title: Buffer：： GetDimensions 函數
description: 取得緩衝區的長度。 |Buffer：： GetDimensions 函數
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973917"
---
# <a name="buffergetdimensions-function"></a><span data-ttu-id="b8f5b-105">Buffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="b8f5b-105">Buffer::GetDimensions function</span></span>

<span data-ttu-id="b8f5b-106">取得緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="b8f5b-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f5b-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8f5b-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="b8f5b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8f5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f5b-109">*dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b8f5b-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8f5b-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b8f5b-110">Type: **uint**</span></span>

<span data-ttu-id="b8f5b-111">緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8f5b-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f5b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8f5b-112">Return value</span></span>

<span data-ttu-id="b8f5b-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b8f5b-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f5b-114">備註</span><span class="sxs-lookup"><span data-stu-id="b8f5b-114">Remarks</span></span>

<span data-ttu-id="b8f5b-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b8f5b-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b8f5b-116">頂點</span><span class="sxs-lookup"><span data-stu-id="b8f5b-116">Vertex</span></span> | <span data-ttu-id="b8f5b-117">船體</span><span class="sxs-lookup"><span data-stu-id="b8f5b-117">Hull</span></span> | <span data-ttu-id="b8f5b-118">網域</span><span class="sxs-lookup"><span data-stu-id="b8f5b-118">Domain</span></span> | <span data-ttu-id="b8f5b-119">幾何</span><span class="sxs-lookup"><span data-stu-id="b8f5b-119">Geometry</span></span> | <span data-ttu-id="b8f5b-120">像素</span><span class="sxs-lookup"><span data-stu-id="b8f5b-120">Pixel</span></span> | <span data-ttu-id="b8f5b-121">計算</span><span class="sxs-lookup"><span data-stu-id="b8f5b-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b8f5b-122">x</span><span class="sxs-lookup"><span data-stu-id="b8f5b-122">x</span></span>      | <span data-ttu-id="b8f5b-123">x</span><span class="sxs-lookup"><span data-stu-id="b8f5b-123">x</span></span>    | <span data-ttu-id="b8f5b-124">x</span><span class="sxs-lookup"><span data-stu-id="b8f5b-124">x</span></span>      | <span data-ttu-id="b8f5b-125">x</span><span class="sxs-lookup"><span data-stu-id="b8f5b-125">x</span></span>        | <span data-ttu-id="b8f5b-126">x</span><span class="sxs-lookup"><span data-stu-id="b8f5b-126">x</span></span>     | <span data-ttu-id="b8f5b-127">x</span><span class="sxs-lookup"><span data-stu-id="b8f5b-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b8f5b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8f5b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f5b-129">Buffer</span><span class="sxs-lookup"><span data-stu-id="b8f5b-129">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="b8f5b-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b8f5b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




