---
title: RWByteAddressBuffer：： Load2 (uint) 函數
description: 取得兩個值。 |RWByteAddressBuffer：： Load2 (uint) 函數
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
keywords:
- Load2 函式 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974396"
---
# <a name="rwbyteaddressbufferload2uint-function"></a><span data-ttu-id="3a778-105">RWByteAddressBuffer：： Load2 (uint) 函數</span><span class="sxs-lookup"><span data-stu-id="3a778-105">RWByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="3a778-106">取得兩個值。</span><span class="sxs-lookup"><span data-stu-id="3a778-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a778-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a778-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="3a778-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a778-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a778-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a778-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a778-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="3a778-110">Type: **uint**</span></span>

<span data-ttu-id="3a778-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="3a778-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a778-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a778-112">Return value</span></span>

<span data-ttu-id="3a778-113">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="3a778-113">Type: **uint2**</span></span>

<span data-ttu-id="3a778-114">兩個值。</span><span class="sxs-lookup"><span data-stu-id="3a778-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a778-115">備註</span><span class="sxs-lookup"><span data-stu-id="3a778-115">Remarks</span></span>

<span data-ttu-id="3a778-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="3a778-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3a778-117">頂點</span><span class="sxs-lookup"><span data-stu-id="3a778-117">Vertex</span></span> | <span data-ttu-id="3a778-118">船體</span><span class="sxs-lookup"><span data-stu-id="3a778-118">Hull</span></span> | <span data-ttu-id="3a778-119">網域</span><span class="sxs-lookup"><span data-stu-id="3a778-119">Domain</span></span> | <span data-ttu-id="3a778-120">幾何</span><span class="sxs-lookup"><span data-stu-id="3a778-120">Geometry</span></span> | <span data-ttu-id="3a778-121">像素</span><span class="sxs-lookup"><span data-stu-id="3a778-121">Pixel</span></span> | <span data-ttu-id="3a778-122">計算</span><span class="sxs-lookup"><span data-stu-id="3a778-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3a778-123">x</span><span class="sxs-lookup"><span data-stu-id="3a778-123">x</span></span>     | <span data-ttu-id="3a778-124">x</span><span class="sxs-lookup"><span data-stu-id="3a778-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3a778-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a778-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a778-126">Load2 方法</span><span class="sxs-lookup"><span data-stu-id="3a778-126">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="3a778-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3a778-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




