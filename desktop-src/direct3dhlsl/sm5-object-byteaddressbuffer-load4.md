---
title: ByteAddressBuffer：： Load4 (uint) 函數
description: 取得四個值。 |ByteAddressBuffer：： Load4 (uint) 函數
ms.assetid: bc74bf29-1c22-4e47-bafc-ecef194f54b8
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
ms.openlocfilehash: 18ce27e7d02a414165aab169e40a6ab14cdd8c4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974336"
---
# <a name="byteaddressbufferload4uint-function"></a><span data-ttu-id="1a20f-105">ByteAddressBuffer：： Load4 (uint) 函數</span><span class="sxs-lookup"><span data-stu-id="1a20f-105">ByteAddressBuffer::Load4(uint) function</span></span>

<span data-ttu-id="1a20f-106">取得四個值。</span><span class="sxs-lookup"><span data-stu-id="1a20f-106">Gets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a20f-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a20f-107">Syntax</span></span>

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="1a20f-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a20f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a20f-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a20f-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a20f-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="1a20f-110">Type: **uint**</span></span>

<span data-ttu-id="1a20f-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="1a20f-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a20f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a20f-112">Return value</span></span>

<span data-ttu-id="1a20f-113">類型： **uint4**</span><span class="sxs-lookup"><span data-stu-id="1a20f-113">Type: **uint4**</span></span>

<span data-ttu-id="1a20f-114">四個值。</span><span class="sxs-lookup"><span data-stu-id="1a20f-114">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a20f-115">備註</span><span class="sxs-lookup"><span data-stu-id="1a20f-115">Remarks</span></span>

<span data-ttu-id="1a20f-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="1a20f-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1a20f-117">頂點</span><span class="sxs-lookup"><span data-stu-id="1a20f-117">Vertex</span></span> | <span data-ttu-id="1a20f-118">船體</span><span class="sxs-lookup"><span data-stu-id="1a20f-118">Hull</span></span> | <span data-ttu-id="1a20f-119">網域</span><span class="sxs-lookup"><span data-stu-id="1a20f-119">Domain</span></span> | <span data-ttu-id="1a20f-120">幾何</span><span class="sxs-lookup"><span data-stu-id="1a20f-120">Geometry</span></span> | <span data-ttu-id="1a20f-121">像素</span><span class="sxs-lookup"><span data-stu-id="1a20f-121">Pixel</span></span> | <span data-ttu-id="1a20f-122">計算</span><span class="sxs-lookup"><span data-stu-id="1a20f-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1a20f-123">x</span><span class="sxs-lookup"><span data-stu-id="1a20f-123">x</span></span>      | <span data-ttu-id="1a20f-124">x</span><span class="sxs-lookup"><span data-stu-id="1a20f-124">x</span></span>    | <span data-ttu-id="1a20f-125">x</span><span class="sxs-lookup"><span data-stu-id="1a20f-125">x</span></span>      | <span data-ttu-id="1a20f-126">x</span><span class="sxs-lookup"><span data-stu-id="1a20f-126">x</span></span>        | <span data-ttu-id="1a20f-127">x</span><span class="sxs-lookup"><span data-stu-id="1a20f-127">x</span></span>     | <span data-ttu-id="1a20f-128">x</span><span class="sxs-lookup"><span data-stu-id="1a20f-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1a20f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a20f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a20f-130">Load4 方法</span><span class="sxs-lookup"><span data-stu-id="1a20f-130">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="1a20f-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="1a20f-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




