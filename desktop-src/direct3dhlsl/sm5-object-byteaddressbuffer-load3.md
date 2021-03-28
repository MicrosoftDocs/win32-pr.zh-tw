---
title: ByteAddressBuffer：： Load3 (uint) 函數
description: 取得三個值。 |ByteAddressBuffer：： Load3 (uint) 函數
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Load3 函式 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e3975d454fcbb8c5dfa8cdef8d7f5718143546f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974337"
---
# <a name="byteaddressbufferload3uint-function"></a><span data-ttu-id="cb1bc-105">ByteAddressBuffer：： Load3 (uint) 函數</span><span class="sxs-lookup"><span data-stu-id="cb1bc-105">ByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="cb1bc-106">取得三個值。</span><span class="sxs-lookup"><span data-stu-id="cb1bc-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1bc-107">語法</span><span class="sxs-lookup"><span data-stu-id="cb1bc-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="cb1bc-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb1bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb1bc-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb1bc-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb1bc-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-110">Type: **uint**</span></span>

<span data-ttu-id="cb1bc-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="cb1bc-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb1bc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb1bc-112">Return value</span></span>

<span data-ttu-id="cb1bc-113">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-113">Type: **uint3**</span></span>

<span data-ttu-id="cb1bc-114">三個值。</span><span class="sxs-lookup"><span data-stu-id="cb1bc-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb1bc-115">備註</span><span class="sxs-lookup"><span data-stu-id="cb1bc-115">Remarks</span></span>

<span data-ttu-id="cb1bc-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="cb1bc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cb1bc-117">頂點</span><span class="sxs-lookup"><span data-stu-id="cb1bc-117">Vertex</span></span> | <span data-ttu-id="cb1bc-118">船體</span><span class="sxs-lookup"><span data-stu-id="cb1bc-118">Hull</span></span> | <span data-ttu-id="cb1bc-119">網域</span><span class="sxs-lookup"><span data-stu-id="cb1bc-119">Domain</span></span> | <span data-ttu-id="cb1bc-120">幾何</span><span class="sxs-lookup"><span data-stu-id="cb1bc-120">Geometry</span></span> | <span data-ttu-id="cb1bc-121">像素</span><span class="sxs-lookup"><span data-stu-id="cb1bc-121">Pixel</span></span> | <span data-ttu-id="cb1bc-122">計算</span><span class="sxs-lookup"><span data-stu-id="cb1bc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cb1bc-123">x</span><span class="sxs-lookup"><span data-stu-id="cb1bc-123">x</span></span>      | <span data-ttu-id="cb1bc-124">x</span><span class="sxs-lookup"><span data-stu-id="cb1bc-124">x</span></span>    | <span data-ttu-id="cb1bc-125">x</span><span class="sxs-lookup"><span data-stu-id="cb1bc-125">x</span></span>      | <span data-ttu-id="cb1bc-126">x</span><span class="sxs-lookup"><span data-stu-id="cb1bc-126">x</span></span>        | <span data-ttu-id="cb1bc-127">x</span><span class="sxs-lookup"><span data-stu-id="cb1bc-127">x</span></span>     | <span data-ttu-id="cb1bc-128">x</span><span class="sxs-lookup"><span data-stu-id="cb1bc-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cb1bc-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb1bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb1bc-130">Load3 方法</span><span class="sxs-lookup"><span data-stu-id="cb1bc-130">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="cb1bc-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="cb1bc-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




