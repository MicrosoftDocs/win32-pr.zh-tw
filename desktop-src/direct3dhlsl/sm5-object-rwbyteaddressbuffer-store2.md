---
title: RWByteAddressBuffer：： Store2 函數
description: 設定兩個值。
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Store2 函式 HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022718"
---
# <a name="store2-function"></a><span data-ttu-id="04bea-104">Store2 函式</span><span class="sxs-lookup"><span data-stu-id="04bea-104">Store2 function</span></span>

<span data-ttu-id="04bea-105">設定兩個值。</span><span class="sxs-lookup"><span data-stu-id="04bea-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="04bea-106">語法</span><span class="sxs-lookup"><span data-stu-id="04bea-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="04bea-107">參數</span><span class="sxs-lookup"><span data-stu-id="04bea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04bea-108">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04bea-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04bea-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="04bea-109">Type: **uint**</span></span>

<span data-ttu-id="04bea-110">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="04bea-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="04bea-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04bea-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04bea-112">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="04bea-112">Type: **uint2**</span></span>

<span data-ttu-id="04bea-113">兩個輸入值。</span><span class="sxs-lookup"><span data-stu-id="04bea-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04bea-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="04bea-114">Return value</span></span>

<span data-ttu-id="04bea-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="04bea-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04bea-116">備註</span><span class="sxs-lookup"><span data-stu-id="04bea-116">Remarks</span></span>

<span data-ttu-id="04bea-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="04bea-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="04bea-118">頂點</span><span class="sxs-lookup"><span data-stu-id="04bea-118">Vertex</span></span> | <span data-ttu-id="04bea-119">船體</span><span class="sxs-lookup"><span data-stu-id="04bea-119">Hull</span></span> | <span data-ttu-id="04bea-120">網域</span><span class="sxs-lookup"><span data-stu-id="04bea-120">Domain</span></span> | <span data-ttu-id="04bea-121">幾何</span><span class="sxs-lookup"><span data-stu-id="04bea-121">Geometry</span></span> | <span data-ttu-id="04bea-122">像素</span><span class="sxs-lookup"><span data-stu-id="04bea-122">Pixel</span></span> | <span data-ttu-id="04bea-123">計算</span><span class="sxs-lookup"><span data-stu-id="04bea-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="04bea-124">x</span><span class="sxs-lookup"><span data-stu-id="04bea-124">x</span></span>     | <span data-ttu-id="04bea-125">x</span><span class="sxs-lookup"><span data-stu-id="04bea-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="04bea-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04bea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bea-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="04bea-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="04bea-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="04bea-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




