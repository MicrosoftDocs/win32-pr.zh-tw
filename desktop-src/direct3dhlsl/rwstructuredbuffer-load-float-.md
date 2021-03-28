---
title: RWStructuredBuffer：： Load (int) 函數
description: 讀取緩衝區資料。 |RWStructuredBuffer：： Load (int) 函數
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
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
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991906"
---
# <a name="rwstructuredbufferloadint-function"></a><span data-ttu-id="2c0a4-105">RWStructuredBuffer：： Load (int) 函數</span><span class="sxs-lookup"><span data-stu-id="2c0a4-105">RWStructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="2c0a4-106">讀取緩衝區資料。</span><span class="sxs-lookup"><span data-stu-id="2c0a4-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0a4-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c0a4-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="2c0a4-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c0a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c0a4-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c0a4-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c0a4-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="2c0a4-110">Type: **int**</span></span>

<span data-ttu-id="2c0a4-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="2c0a4-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c0a4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c0a4-112">Return value</span></span>

<span data-ttu-id="2c0a4-113">輸入：</span><span class="sxs-lookup"><span data-stu-id="2c0a4-113">Type:</span></span>

<span data-ttu-id="2c0a4-114">傳回型別符合 [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="2c0a4-114">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0a4-115">備註</span><span class="sxs-lookup"><span data-stu-id="2c0a4-115">Remarks</span></span>

<span data-ttu-id="2c0a4-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="2c0a4-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2c0a4-117">頂點</span><span class="sxs-lookup"><span data-stu-id="2c0a4-117">Vertex</span></span> | <span data-ttu-id="2c0a4-118">船體</span><span class="sxs-lookup"><span data-stu-id="2c0a4-118">Hull</span></span> | <span data-ttu-id="2c0a4-119">網域</span><span class="sxs-lookup"><span data-stu-id="2c0a4-119">Domain</span></span> | <span data-ttu-id="2c0a4-120">幾何</span><span class="sxs-lookup"><span data-stu-id="2c0a4-120">Geometry</span></span> | <span data-ttu-id="2c0a4-121">像素</span><span class="sxs-lookup"><span data-stu-id="2c0a4-121">Pixel</span></span> | <span data-ttu-id="2c0a4-122">計算</span><span class="sxs-lookup"><span data-stu-id="2c0a4-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2c0a4-123">x</span><span class="sxs-lookup"><span data-stu-id="2c0a4-123">x</span></span>      | <span data-ttu-id="2c0a4-124">x</span><span class="sxs-lookup"><span data-stu-id="2c0a4-124">x</span></span>    | <span data-ttu-id="2c0a4-125">x</span><span class="sxs-lookup"><span data-stu-id="2c0a4-125">x</span></span>      | <span data-ttu-id="2c0a4-126">x</span><span class="sxs-lookup"><span data-stu-id="2c0a4-126">x</span></span>        | <span data-ttu-id="2c0a4-127">x</span><span class="sxs-lookup"><span data-stu-id="2c0a4-127">x</span></span>     | <span data-ttu-id="2c0a4-128">x</span><span class="sxs-lookup"><span data-stu-id="2c0a4-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2c0a4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c0a4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0a4-130">載入方法</span><span class="sxs-lookup"><span data-stu-id="2c0a4-130">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




