---
title: 'RWStructuredBuffer：:D ecrementCounter 函數 (Httpserv .h) '
description: 遞減物件的隱藏計數器。
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter 函式 HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974636"
---
# <a name="decrementcounter-function"></a><span data-ttu-id="8755a-104">DecrementCounter 函式</span><span class="sxs-lookup"><span data-stu-id="8755a-104">DecrementCounter function</span></span>

<span data-ttu-id="8755a-105">遞減物件的隱藏計數器。</span><span class="sxs-lookup"><span data-stu-id="8755a-105">Decrements the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8755a-106">語法</span><span class="sxs-lookup"><span data-stu-id="8755a-106">Syntax</span></span>

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="8755a-107">參數</span><span class="sxs-lookup"><span data-stu-id="8755a-107">Parameters</span></span>

<span data-ttu-id="8755a-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="8755a-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8755a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8755a-109">Return value</span></span>

<span data-ttu-id="8755a-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="8755a-110">Type: **uint**</span></span>

<span data-ttu-id="8755a-111">減少後的計數器值。</span><span class="sxs-lookup"><span data-stu-id="8755a-111">The post-decremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8755a-112">備註</span><span class="sxs-lookup"><span data-stu-id="8755a-112">Remarks</span></span>

<span data-ttu-id="8755a-113">在 creationfor 此方法期間，系結的未排序存取視圖必須設定 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 計數器計數器**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) 。</span><span class="sxs-lookup"><span data-stu-id="8755a-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creationfor this method to work.</span></span>

<span data-ttu-id="8755a-114">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8755a-114">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8755a-115">頂點</span><span class="sxs-lookup"><span data-stu-id="8755a-115">Vertex</span></span> | <span data-ttu-id="8755a-116">船體</span><span class="sxs-lookup"><span data-stu-id="8755a-116">Hull</span></span> | <span data-ttu-id="8755a-117">網域</span><span class="sxs-lookup"><span data-stu-id="8755a-117">Domain</span></span> | <span data-ttu-id="8755a-118">幾何</span><span class="sxs-lookup"><span data-stu-id="8755a-118">Geometry</span></span> | <span data-ttu-id="8755a-119">像素</span><span class="sxs-lookup"><span data-stu-id="8755a-119">Pixel</span></span> | <span data-ttu-id="8755a-120">計算</span><span class="sxs-lookup"><span data-stu-id="8755a-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="8755a-121">x</span><span class="sxs-lookup"><span data-stu-id="8755a-121">x</span></span>     | <span data-ttu-id="8755a-122">x</span><span class="sxs-lookup"><span data-stu-id="8755a-122">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="8755a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8755a-123">Requirements</span></span>



| <span data-ttu-id="8755a-124">需求</span><span class="sxs-lookup"><span data-stu-id="8755a-124">Requirement</span></span> | <span data-ttu-id="8755a-125">值</span><span class="sxs-lookup"><span data-stu-id="8755a-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8755a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8755a-126">Header</span></span><br/> | <dl> <span data-ttu-id="8755a-127"><dt>Httpserv。h</dt></span><span class="sxs-lookup"><span data-stu-id="8755a-127"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8755a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8755a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8755a-129">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="8755a-129">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="8755a-130">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8755a-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

