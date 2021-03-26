---
title: RWByteAddressBuffer：： Load3 (uint) 函數
description: 取得三個值。 |RWByteAddressBuffer：： Load3 (uint) 函數
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- Load3 函式 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974416"
---
# <a name="rwbyteaddressbufferload3uint-function"></a><span data-ttu-id="47d30-105">RWByteAddressBuffer：： Load3 (uint) 函數</span><span class="sxs-lookup"><span data-stu-id="47d30-105">RWByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="47d30-106">取得三個值。</span><span class="sxs-lookup"><span data-stu-id="47d30-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d30-107">語法</span><span class="sxs-lookup"><span data-stu-id="47d30-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="47d30-108">參數</span><span class="sxs-lookup"><span data-stu-id="47d30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d30-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47d30-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d30-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="47d30-110">Type: **uint**</span></span>

<span data-ttu-id="47d30-111">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="47d30-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d30-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="47d30-112">Return value</span></span>

<span data-ttu-id="47d30-113">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="47d30-113">Type: **uint3**</span></span>

<span data-ttu-id="47d30-114">三個值。</span><span class="sxs-lookup"><span data-stu-id="47d30-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d30-115">備註</span><span class="sxs-lookup"><span data-stu-id="47d30-115">Remarks</span></span>

<span data-ttu-id="47d30-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="47d30-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="47d30-117">頂點</span><span class="sxs-lookup"><span data-stu-id="47d30-117">Vertex</span></span> | <span data-ttu-id="47d30-118">船體</span><span class="sxs-lookup"><span data-stu-id="47d30-118">Hull</span></span> | <span data-ttu-id="47d30-119">網域</span><span class="sxs-lookup"><span data-stu-id="47d30-119">Domain</span></span> | <span data-ttu-id="47d30-120">幾何</span><span class="sxs-lookup"><span data-stu-id="47d30-120">Geometry</span></span> | <span data-ttu-id="47d30-121">像素</span><span class="sxs-lookup"><span data-stu-id="47d30-121">Pixel</span></span> | <span data-ttu-id="47d30-122">計算</span><span class="sxs-lookup"><span data-stu-id="47d30-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="47d30-123">x</span><span class="sxs-lookup"><span data-stu-id="47d30-123">x</span></span>     | <span data-ttu-id="47d30-124">x</span><span class="sxs-lookup"><span data-stu-id="47d30-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="47d30-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47d30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d30-126">Load3 方法</span><span class="sxs-lookup"><span data-stu-id="47d30-126">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="47d30-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="47d30-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




