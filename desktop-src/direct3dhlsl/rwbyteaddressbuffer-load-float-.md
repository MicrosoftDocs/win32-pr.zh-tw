---
title: RWByteAddressBuffer：： Load (int) 函數
description: 取得一個值。 |RWByteAddressBuffer：： Load (int) 函數
ms.assetid: C95C865E-E44D-46DC-A076-BD2903758432
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
ms.openlocfilehash: 6efff2363f844e6940b489dd2dda48cbdc0c6b75
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974036"
---
# <a name="rwbyteaddressbufferloadint-function"></a><span data-ttu-id="9e3fe-105">RWByteAddressBuffer：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="9e3fe-105">RWByteAddressBuffer::Load(int) function</span></span>

<span data-ttu-id="9e3fe-106">取得一個值。</span><span class="sxs-lookup"><span data-stu-id="9e3fe-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="9e3fe-107">Syntax</span></span>


``` syntax
uint Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="9e3fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="9e3fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3fe-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e3fe-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e3fe-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="9e3fe-110">Type: **int**</span></span>

<span data-ttu-id="9e3fe-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="9e3fe-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3fe-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e3fe-112">Return value</span></span>

<span data-ttu-id="9e3fe-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="9e3fe-113">Type: **uint**</span></span>

<span data-ttu-id="9e3fe-114">一個值。</span><span class="sxs-lookup"><span data-stu-id="9e3fe-114">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e3fe-115">備註</span><span class="sxs-lookup"><span data-stu-id="9e3fe-115">Remarks</span></span>

<span data-ttu-id="9e3fe-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="9e3fe-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9e3fe-117">頂點</span><span class="sxs-lookup"><span data-stu-id="9e3fe-117">Vertex</span></span> | <span data-ttu-id="9e3fe-118">船體</span><span class="sxs-lookup"><span data-stu-id="9e3fe-118">Hull</span></span> | <span data-ttu-id="9e3fe-119">網域</span><span class="sxs-lookup"><span data-stu-id="9e3fe-119">Domain</span></span> | <span data-ttu-id="9e3fe-120">幾何</span><span class="sxs-lookup"><span data-stu-id="9e3fe-120">Geometry</span></span> | <span data-ttu-id="9e3fe-121">像素</span><span class="sxs-lookup"><span data-stu-id="9e3fe-121">Pixel</span></span> | <span data-ttu-id="9e3fe-122">計算</span><span class="sxs-lookup"><span data-stu-id="9e3fe-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9e3fe-123">x</span><span class="sxs-lookup"><span data-stu-id="9e3fe-123">x</span></span>     | <span data-ttu-id="9e3fe-124">x</span><span class="sxs-lookup"><span data-stu-id="9e3fe-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9e3fe-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e3fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3fe-126">載入方法</span><span class="sxs-lookup"><span data-stu-id="9e3fe-126">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 




