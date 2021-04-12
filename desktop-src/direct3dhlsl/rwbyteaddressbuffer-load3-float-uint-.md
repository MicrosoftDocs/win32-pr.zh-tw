---
title: RWByteAddressBuffer：： Load3 (uint，uint) 函數
description: 取得三個值，並傳回作業的狀態。
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
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
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315973"
---
# <a name="load3uintuint-function"></a><span data-ttu-id="c7abf-104">Load3 (uint，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="c7abf-104">Load3(uint,uint) function</span></span>

<span data-ttu-id="c7abf-105">取得三個值，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c7abf-105">Gets three values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7abf-106">語法</span><span class="sxs-lookup"><span data-stu-id="c7abf-106">Syntax</span></span>


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="c7abf-107">參數</span><span class="sxs-lookup"><span data-stu-id="c7abf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7abf-108">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7abf-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7abf-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c7abf-109">Type: **uint**</span></span>

<span data-ttu-id="c7abf-110">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="c7abf-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c7abf-111">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7abf-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7abf-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="c7abf-112">Type: **uint**</span></span>

<span data-ttu-id="c7abf-113">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="c7abf-113">The status of the operation.</span></span> <span data-ttu-id="c7abf-114">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="c7abf-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c7abf-115">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c7abf-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c7abf-116">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c7abf-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7abf-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7abf-117">Return value</span></span>

<span data-ttu-id="c7abf-118">類型： **uint3**</span><span class="sxs-lookup"><span data-stu-id="c7abf-118">Type: **uint3**</span></span>

<span data-ttu-id="c7abf-119">三個值。</span><span class="sxs-lookup"><span data-stu-id="c7abf-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7abf-120">備註</span><span class="sxs-lookup"><span data-stu-id="c7abf-120">Remarks</span></span>

<span data-ttu-id="c7abf-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c7abf-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c7abf-122">頂點</span><span class="sxs-lookup"><span data-stu-id="c7abf-122">Vertex</span></span> | <span data-ttu-id="c7abf-123">船體</span><span class="sxs-lookup"><span data-stu-id="c7abf-123">Hull</span></span> | <span data-ttu-id="c7abf-124">網域</span><span class="sxs-lookup"><span data-stu-id="c7abf-124">Domain</span></span> | <span data-ttu-id="c7abf-125">幾何</span><span class="sxs-lookup"><span data-stu-id="c7abf-125">Geometry</span></span> | <span data-ttu-id="c7abf-126">像素</span><span class="sxs-lookup"><span data-stu-id="c7abf-126">Pixel</span></span> | <span data-ttu-id="c7abf-127">計算</span><span class="sxs-lookup"><span data-stu-id="c7abf-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c7abf-128">x</span><span class="sxs-lookup"><span data-stu-id="c7abf-128">x</span></span>     | <span data-ttu-id="c7abf-129">x</span><span class="sxs-lookup"><span data-stu-id="c7abf-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c7abf-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7abf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7abf-131">Load3 方法</span><span class="sxs-lookup"><span data-stu-id="c7abf-131">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 