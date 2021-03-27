---
title: RWByteAddressBuffer：： Store 函數
description: 設定一個值。
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- 存放區函式 HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104971485"
---
# <a name="store-function"></a><span data-ttu-id="b3bca-104">Store 函數</span><span class="sxs-lookup"><span data-stu-id="b3bca-104">Store function</span></span>

<span data-ttu-id="b3bca-105">設定一個值。</span><span class="sxs-lookup"><span data-stu-id="b3bca-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3bca-106">語法</span><span class="sxs-lookup"><span data-stu-id="b3bca-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="b3bca-107">參數</span><span class="sxs-lookup"><span data-stu-id="b3bca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3bca-108">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3bca-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bca-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b3bca-109">Type: **uint**</span></span>

<span data-ttu-id="b3bca-110">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="b3bca-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="b3bca-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3bca-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3bca-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b3bca-112">Type: **uint**</span></span>

<span data-ttu-id="b3bca-113">一個輸入值。</span><span class="sxs-lookup"><span data-stu-id="b3bca-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3bca-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3bca-114">Return value</span></span>

<span data-ttu-id="b3bca-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b3bca-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3bca-116">備註</span><span class="sxs-lookup"><span data-stu-id="b3bca-116">Remarks</span></span>

<span data-ttu-id="b3bca-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b3bca-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b3bca-118">頂點</span><span class="sxs-lookup"><span data-stu-id="b3bca-118">Vertex</span></span> | <span data-ttu-id="b3bca-119">船體</span><span class="sxs-lookup"><span data-stu-id="b3bca-119">Hull</span></span> | <span data-ttu-id="b3bca-120">網域</span><span class="sxs-lookup"><span data-stu-id="b3bca-120">Domain</span></span> | <span data-ttu-id="b3bca-121">幾何</span><span class="sxs-lookup"><span data-stu-id="b3bca-121">Geometry</span></span> | <span data-ttu-id="b3bca-122">像素</span><span class="sxs-lookup"><span data-stu-id="b3bca-122">Pixel</span></span> | <span data-ttu-id="b3bca-123">計算</span><span class="sxs-lookup"><span data-stu-id="b3bca-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b3bca-124">x</span><span class="sxs-lookup"><span data-stu-id="b3bca-124">x</span></span>     | <span data-ttu-id="b3bca-125">x</span><span class="sxs-lookup"><span data-stu-id="b3bca-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b3bca-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3bca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bca-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="b3bca-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="b3bca-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b3bca-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




