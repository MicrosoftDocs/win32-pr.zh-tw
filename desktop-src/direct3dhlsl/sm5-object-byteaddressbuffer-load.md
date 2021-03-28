---
title: ByteAddressBuffer：： Load (int) 函數
description: 取得一個值。 |ByteAddressBuffer：： Load (int) 函數
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Load function HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991915"
---
# <a name="byteaddressbufferloadint-function"></a><span data-ttu-id="60aed-105">ByteAddressBuffer：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="60aed-105">ByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="60aed-106">取得一個值。</span><span class="sxs-lookup"><span data-stu-id="60aed-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="60aed-107">語法</span><span class="sxs-lookup"><span data-stu-id="60aed-107">Syntax</span></span>

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a><span data-ttu-id="60aed-108">參數</span><span class="sxs-lookup"><span data-stu-id="60aed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60aed-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60aed-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60aed-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="60aed-110">Type: **int**</span></span>

<span data-ttu-id="60aed-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="60aed-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60aed-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="60aed-112">Return value</span></span>

<span data-ttu-id="60aed-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="60aed-113">Type: **uint**</span></span>

<span data-ttu-id="60aed-114">一個值。</span><span class="sxs-lookup"><span data-stu-id="60aed-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60aed-115">備註</span><span class="sxs-lookup"><span data-stu-id="60aed-115">Remarks</span></span>

<span data-ttu-id="60aed-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="60aed-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="60aed-117">頂點</span><span class="sxs-lookup"><span data-stu-id="60aed-117">Vertex</span></span> | <span data-ttu-id="60aed-118">船體</span><span class="sxs-lookup"><span data-stu-id="60aed-118">Hull</span></span> | <span data-ttu-id="60aed-119">網域</span><span class="sxs-lookup"><span data-stu-id="60aed-119">Domain</span></span> | <span data-ttu-id="60aed-120">幾何</span><span class="sxs-lookup"><span data-stu-id="60aed-120">Geometry</span></span> | <span data-ttu-id="60aed-121">像素</span><span class="sxs-lookup"><span data-stu-id="60aed-121">Pixel</span></span> | <span data-ttu-id="60aed-122">計算</span><span class="sxs-lookup"><span data-stu-id="60aed-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="60aed-123">x</span><span class="sxs-lookup"><span data-stu-id="60aed-123">x</span></span>      | <span data-ttu-id="60aed-124">x</span><span class="sxs-lookup"><span data-stu-id="60aed-124">x</span></span>    | <span data-ttu-id="60aed-125">x</span><span class="sxs-lookup"><span data-stu-id="60aed-125">x</span></span>      | <span data-ttu-id="60aed-126">x</span><span class="sxs-lookup"><span data-stu-id="60aed-126">x</span></span>        | <span data-ttu-id="60aed-127">x</span><span class="sxs-lookup"><span data-stu-id="60aed-127">x</span></span>     | <span data-ttu-id="60aed-128">x</span><span class="sxs-lookup"><span data-stu-id="60aed-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="60aed-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60aed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60aed-130">載入方法</span><span class="sxs-lookup"><span data-stu-id="60aed-130">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="60aed-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="60aed-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




