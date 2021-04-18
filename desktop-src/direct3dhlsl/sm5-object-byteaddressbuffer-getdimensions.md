---
title: ByteAddressBuffer：： GetDimensions 函數
description: 取得緩衝區的長度。 |ByteAddressBuffer：： GetDimensions 函數
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991870"
---
# <a name="byteaddressbuffergetdimensions-function"></a><span data-ttu-id="34d2c-105">ByteAddressBuffer：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="34d2c-105">ByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="34d2c-106">取得緩衝區的長度。</span><span class="sxs-lookup"><span data-stu-id="34d2c-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d2c-107">語法</span><span class="sxs-lookup"><span data-stu-id="34d2c-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="34d2c-108">參數</span><span class="sxs-lookup"><span data-stu-id="34d2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34d2c-109">*dim* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34d2c-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34d2c-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="34d2c-110">Type: **uint**</span></span>

<span data-ttu-id="34d2c-111">緩衝區的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="34d2c-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34d2c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="34d2c-112">Return value</span></span>

<span data-ttu-id="34d2c-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="34d2c-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d2c-114">備註</span><span class="sxs-lookup"><span data-stu-id="34d2c-114">Remarks</span></span>

<span data-ttu-id="34d2c-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="34d2c-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="34d2c-116">頂點</span><span class="sxs-lookup"><span data-stu-id="34d2c-116">Vertex</span></span> | <span data-ttu-id="34d2c-117">船體</span><span class="sxs-lookup"><span data-stu-id="34d2c-117">Hull</span></span> | <span data-ttu-id="34d2c-118">網域</span><span class="sxs-lookup"><span data-stu-id="34d2c-118">Domain</span></span> | <span data-ttu-id="34d2c-119">幾何</span><span class="sxs-lookup"><span data-stu-id="34d2c-119">Geometry</span></span> | <span data-ttu-id="34d2c-120">像素</span><span class="sxs-lookup"><span data-stu-id="34d2c-120">Pixel</span></span> | <span data-ttu-id="34d2c-121">計算</span><span class="sxs-lookup"><span data-stu-id="34d2c-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="34d2c-122">x</span><span class="sxs-lookup"><span data-stu-id="34d2c-122">x</span></span>      | <span data-ttu-id="34d2c-123">x</span><span class="sxs-lookup"><span data-stu-id="34d2c-123">x</span></span>    | <span data-ttu-id="34d2c-124">x</span><span class="sxs-lookup"><span data-stu-id="34d2c-124">x</span></span>      | <span data-ttu-id="34d2c-125">x</span><span class="sxs-lookup"><span data-stu-id="34d2c-125">x</span></span>        | <span data-ttu-id="34d2c-126">x</span><span class="sxs-lookup"><span data-stu-id="34d2c-126">x</span></span>     | <span data-ttu-id="34d2c-127">x</span><span class="sxs-lookup"><span data-stu-id="34d2c-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="34d2c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34d2c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d2c-129">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="34d2c-129">ByteAddressBuffer</span></span>](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="34d2c-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="34d2c-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




