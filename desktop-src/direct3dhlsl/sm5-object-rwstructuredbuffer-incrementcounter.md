---
title: 'RWStructuredBuffer：： IncrementCounter 函數 (Httpserv .h) '
description: 遞增物件的隱藏計數器。
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter 函式 HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323175"
---
# <a name="incrementcounter-function"></a><span data-ttu-id="299b4-104">IncrementCounter 函式</span><span class="sxs-lookup"><span data-stu-id="299b4-104">IncrementCounter function</span></span>

<span data-ttu-id="299b4-105">遞增物件的隱藏計數器。</span><span class="sxs-lookup"><span data-stu-id="299b4-105">Increments the object's hidden counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="299b4-106">語法</span><span class="sxs-lookup"><span data-stu-id="299b4-106">Syntax</span></span>

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a><span data-ttu-id="299b4-107">參數</span><span class="sxs-lookup"><span data-stu-id="299b4-107">Parameters</span></span>

<span data-ttu-id="299b4-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="299b4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="299b4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="299b4-109">Return value</span></span>

<span data-ttu-id="299b4-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="299b4-110">Type: **uint**</span></span>

<span data-ttu-id="299b4-111">預先遞增的計數器值。</span><span class="sxs-lookup"><span data-stu-id="299b4-111">The pre-incremented counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="299b4-112">備註</span><span class="sxs-lookup"><span data-stu-id="299b4-112">Remarks</span></span>

<span data-ttu-id="299b4-113">系結的未排序存取視圖必須在建立期間設定 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 計數器計數器**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) ，才能讓此方法運作。</span><span class="sxs-lookup"><span data-stu-id="299b4-113">The bound unordered access view must have [**D3D11\_BUFFER\_UAV\_FLAG\_COUNTER**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) set during creation for this method to work.</span></span>

<span data-ttu-id="299b4-114">結構化資源可以根據結構的元件名稱進一步編制索引。</span><span class="sxs-lookup"><span data-stu-id="299b4-114">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="299b4-115">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="299b4-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="299b4-116">頂點</span><span class="sxs-lookup"><span data-stu-id="299b4-116">Vertex</span></span> | <span data-ttu-id="299b4-117">船體</span><span class="sxs-lookup"><span data-stu-id="299b4-117">Hull</span></span> | <span data-ttu-id="299b4-118">網域</span><span class="sxs-lookup"><span data-stu-id="299b4-118">Domain</span></span> | <span data-ttu-id="299b4-119">幾何</span><span class="sxs-lookup"><span data-stu-id="299b4-119">Geometry</span></span> | <span data-ttu-id="299b4-120">像素</span><span class="sxs-lookup"><span data-stu-id="299b4-120">Pixel</span></span> | <span data-ttu-id="299b4-121">計算</span><span class="sxs-lookup"><span data-stu-id="299b4-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="299b4-122">x</span><span class="sxs-lookup"><span data-stu-id="299b4-122">x</span></span>     | <span data-ttu-id="299b4-123">x</span><span class="sxs-lookup"><span data-stu-id="299b4-123">x</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="299b4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="299b4-124">Requirements</span></span>



| <span data-ttu-id="299b4-125">需求</span><span class="sxs-lookup"><span data-stu-id="299b4-125">Requirement</span></span> | <span data-ttu-id="299b4-126">值</span><span class="sxs-lookup"><span data-stu-id="299b4-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="299b4-127">標頭</span><span class="sxs-lookup"><span data-stu-id="299b4-127">Header</span></span><br/> | <dl> <span data-ttu-id="299b4-128"><dt>Httpserv。h</dt></span><span class="sxs-lookup"><span data-stu-id="299b4-128"><dt>Httpserv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299b4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="299b4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299b4-130">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="299b4-130">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="299b4-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="299b4-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

