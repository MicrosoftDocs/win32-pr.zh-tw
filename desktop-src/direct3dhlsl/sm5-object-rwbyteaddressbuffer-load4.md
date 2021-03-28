---
title: RWByteAddressBuffer：： Load4 (uint) 函數
description: 取得四個值。 |RWByteAddressBuffer：： Load4 (uint) 函數
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Load4 函式 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974409"
---
# <a name="rwbyteaddressbufferload4uint-function"></a><span data-ttu-id="c3ec3-105">RWByteAddressBuffer：： Load4 (uint) 函數</span><span class="sxs-lookup"><span data-stu-id="c3ec3-105">RWByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="c3ec3-106">取得四個值。</span><span class="sxs-lookup"><span data-stu-id="c3ec3-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ec3-107">語法</span><span class="sxs-lookup"><span data-stu-id="c3ec3-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="c3ec3-108">參數</span><span class="sxs-lookup"><span data-stu-id="c3ec3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ec3-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3ec3-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ec3-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c3ec3-110">Type: **uint**</span></span>

<span data-ttu-id="c3ec3-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="c3ec3-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ec3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3ec3-112">Return value</span></span>

<span data-ttu-id="c3ec3-113">類型： **uint4**</span><span class="sxs-lookup"><span data-stu-id="c3ec3-113">Type: **uint4**</span></span>

<span data-ttu-id="c3ec3-114">四個值。</span><span class="sxs-lookup"><span data-stu-id="c3ec3-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ec3-115">備註</span><span class="sxs-lookup"><span data-stu-id="c3ec3-115">Remarks</span></span>

<span data-ttu-id="c3ec3-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c3ec3-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3ec3-117">頂點</span><span class="sxs-lookup"><span data-stu-id="c3ec3-117">Vertex</span></span> | <span data-ttu-id="c3ec3-118">船體</span><span class="sxs-lookup"><span data-stu-id="c3ec3-118">Hull</span></span> | <span data-ttu-id="c3ec3-119">網域</span><span class="sxs-lookup"><span data-stu-id="c3ec3-119">Domain</span></span> | <span data-ttu-id="c3ec3-120">幾何</span><span class="sxs-lookup"><span data-stu-id="c3ec3-120">Geometry</span></span> | <span data-ttu-id="c3ec3-121">像素</span><span class="sxs-lookup"><span data-stu-id="c3ec3-121">Pixel</span></span> | <span data-ttu-id="c3ec3-122">計算</span><span class="sxs-lookup"><span data-stu-id="c3ec3-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c3ec3-123">x</span><span class="sxs-lookup"><span data-stu-id="c3ec3-123">x</span></span>     | <span data-ttu-id="c3ec3-124">x</span><span class="sxs-lookup"><span data-stu-id="c3ec3-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3ec3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3ec3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ec3-126">Load4 方法</span><span class="sxs-lookup"><span data-stu-id="c3ec3-126">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="c3ec3-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c3ec3-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




