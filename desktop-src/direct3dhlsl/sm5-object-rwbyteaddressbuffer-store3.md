---
title: RWByteAddressBuffer：： Store3 函數
description: 設定三個值。
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Store3 函式 HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313346"
---
# <a name="store3-function"></a><span data-ttu-id="48005-104">Store3 函式</span><span class="sxs-lookup"><span data-stu-id="48005-104">Store3 function</span></span>

<span data-ttu-id="48005-105">設定三個值。</span><span class="sxs-lookup"><span data-stu-id="48005-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="48005-106">語法</span><span class="sxs-lookup"><span data-stu-id="48005-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="48005-107">參數</span><span class="sxs-lookup"><span data-stu-id="48005-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48005-108">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48005-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48005-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="48005-109">Type: **uint**</span></span>

<span data-ttu-id="48005-110">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="48005-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="48005-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48005-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48005-112">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="48005-112">Type: **uint3**</span></span>

<span data-ttu-id="48005-113">三個輸入值。</span><span class="sxs-lookup"><span data-stu-id="48005-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48005-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="48005-114">Return value</span></span>

<span data-ttu-id="48005-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="48005-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48005-116">備註</span><span class="sxs-lookup"><span data-stu-id="48005-116">Remarks</span></span>

<span data-ttu-id="48005-117">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="48005-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="48005-118">頂點</span><span class="sxs-lookup"><span data-stu-id="48005-118">Vertex</span></span> | <span data-ttu-id="48005-119">船體</span><span class="sxs-lookup"><span data-stu-id="48005-119">Hull</span></span> | <span data-ttu-id="48005-120">網域</span><span class="sxs-lookup"><span data-stu-id="48005-120">Domain</span></span> | <span data-ttu-id="48005-121">幾何</span><span class="sxs-lookup"><span data-stu-id="48005-121">Geometry</span></span> | <span data-ttu-id="48005-122">像素</span><span class="sxs-lookup"><span data-stu-id="48005-122">Pixel</span></span> | <span data-ttu-id="48005-123">計算</span><span class="sxs-lookup"><span data-stu-id="48005-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="48005-124">x</span><span class="sxs-lookup"><span data-stu-id="48005-124">x</span></span>     | <span data-ttu-id="48005-125">x</span><span class="sxs-lookup"><span data-stu-id="48005-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="48005-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48005-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48005-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="48005-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="48005-128">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="48005-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




