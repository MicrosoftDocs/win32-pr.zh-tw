---
title: RWByteAddressBuffer：： Store4 函數
description: 設定四個值。
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Store4 函式 HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 219cd04e4f68ad6f0d16d964e6685c558fed98b1
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104373515"
---
# <a name="store4-function"></a><span data-ttu-id="c3997-104">Store4 函式</span><span class="sxs-lookup"><span data-stu-id="c3997-104">Store4 function</span></span>

<span data-ttu-id="c3997-105">設定四個值。</span><span class="sxs-lookup"><span data-stu-id="c3997-105">Sets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3997-106">語法</span><span class="sxs-lookup"><span data-stu-id="c3997-106">Syntax</span></span>

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a><span data-ttu-id="c3997-107">參數</span><span class="sxs-lookup"><span data-stu-id="c3997-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3997-108">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3997-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3997-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c3997-109">Type: **uint**</span></span>

<span data-ttu-id="c3997-110">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="c3997-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="c3997-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3997-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3997-112">類型： **uint4**</span><span class="sxs-lookup"><span data-stu-id="c3997-112">Type: **uint4**</span></span>

<span data-ttu-id="c3997-113">四個輸入值。</span><span class="sxs-lookup"><span data-stu-id="c3997-113">Four input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3997-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3997-114">Return value</span></span>

<span data-ttu-id="c3997-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3997-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3997-116">備註</span><span class="sxs-lookup"><span data-stu-id="c3997-116">Remarks</span></span>

<span data-ttu-id="c3997-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c3997-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c3997-118">頂點</span><span class="sxs-lookup"><span data-stu-id="c3997-118">Vertex</span></span> | <span data-ttu-id="c3997-119">船體</span><span class="sxs-lookup"><span data-stu-id="c3997-119">Hull</span></span> | <span data-ttu-id="c3997-120">網域</span><span class="sxs-lookup"><span data-stu-id="c3997-120">Domain</span></span> | <span data-ttu-id="c3997-121">幾何</span><span class="sxs-lookup"><span data-stu-id="c3997-121">Geometry</span></span> | <span data-ttu-id="c3997-122">像素</span><span class="sxs-lookup"><span data-stu-id="c3997-122">Pixel</span></span> | <span data-ttu-id="c3997-123">計算</span><span class="sxs-lookup"><span data-stu-id="c3997-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c3997-124">x</span><span class="sxs-lookup"><span data-stu-id="c3997-124">x</span></span>     | <span data-ttu-id="c3997-125">x</span><span class="sxs-lookup"><span data-stu-id="c3997-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c3997-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3997-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3997-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="c3997-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c3997-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c3997-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




