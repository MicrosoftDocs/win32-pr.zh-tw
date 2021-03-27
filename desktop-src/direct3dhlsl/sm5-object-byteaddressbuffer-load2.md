---
title: ByteAddressBuffer：： Load2 (uint) 函數
description: 取得兩個值。 |ByteAddressBuffer：： Load2 (uint) 函數
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
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
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696361"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="6fb2a-105">ByteAddressBuffer：： Load2 (uint) 函數</span><span class="sxs-lookup"><span data-stu-id="6fb2a-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="6fb2a-106">取得兩個值。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6fb2a-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="6fb2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6fb2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fb2a-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6fb2a-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fb2a-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="6fb2a-110">Type: **uint**</span></span>

<span data-ttu-id="6fb2a-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fb2a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6fb2a-112">Return value</span></span>

<span data-ttu-id="6fb2a-113">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="6fb2a-113">Type: **uint2**</span></span>

<span data-ttu-id="6fb2a-114">兩個值。</span><span class="sxs-lookup"><span data-stu-id="6fb2a-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fb2a-115">備註</span><span class="sxs-lookup"><span data-stu-id="6fb2a-115">Remarks</span></span>

<span data-ttu-id="6fb2a-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="6fb2a-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6fb2a-117">頂點</span><span class="sxs-lookup"><span data-stu-id="6fb2a-117">Vertex</span></span> | <span data-ttu-id="6fb2a-118">船體</span><span class="sxs-lookup"><span data-stu-id="6fb2a-118">Hull</span></span> | <span data-ttu-id="6fb2a-119">網域</span><span class="sxs-lookup"><span data-stu-id="6fb2a-119">Domain</span></span> | <span data-ttu-id="6fb2a-120">幾何</span><span class="sxs-lookup"><span data-stu-id="6fb2a-120">Geometry</span></span> | <span data-ttu-id="6fb2a-121">像素</span><span class="sxs-lookup"><span data-stu-id="6fb2a-121">Pixel</span></span> | <span data-ttu-id="6fb2a-122">計算</span><span class="sxs-lookup"><span data-stu-id="6fb2a-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6fb2a-123">x</span><span class="sxs-lookup"><span data-stu-id="6fb2a-123">x</span></span>      | <span data-ttu-id="6fb2a-124">x</span><span class="sxs-lookup"><span data-stu-id="6fb2a-124">x</span></span>    | <span data-ttu-id="6fb2a-125">x</span><span class="sxs-lookup"><span data-stu-id="6fb2a-125">x</span></span>      | <span data-ttu-id="6fb2a-126">x</span><span class="sxs-lookup"><span data-stu-id="6fb2a-126">x</span></span>        | <span data-ttu-id="6fb2a-127">x</span><span class="sxs-lookup"><span data-stu-id="6fb2a-127">x</span></span>     | <span data-ttu-id="6fb2a-128">x</span><span class="sxs-lookup"><span data-stu-id="6fb2a-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6fb2a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fb2a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb2a-130">Load2 方法</span><span class="sxs-lookup"><span data-stu-id="6fb2a-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="6fb2a-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6fb2a-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




