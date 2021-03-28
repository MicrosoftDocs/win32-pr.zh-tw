---
title: RWByteAddressBuffer：： Load2 (uint，uint) 函數
description: 取得兩個值，並傳回作業的狀態。
ms.assetid: E6BBA8A7-D53F-4718-B007-EBDE50FADB06
keywords:
- Load2 函式 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92fc492fddb6ad024a4507829e81dab4886af590
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092739"
---
# <a name="load2uintuint-function"></a><span data-ttu-id="5b198-104">Load2 (uint，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="5b198-104">Load2(uint,uint) function</span></span>

<span data-ttu-id="5b198-105">取得兩個值，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5b198-105">Gets two values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b198-106">語法</span><span class="sxs-lookup"><span data-stu-id="5b198-106">Syntax</span></span>


``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="5b198-107">參數</span><span class="sxs-lookup"><span data-stu-id="5b198-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b198-108">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b198-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b198-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="5b198-109">Type: **uint**</span></span>

<span data-ttu-id="5b198-110">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="5b198-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b198-111">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b198-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b198-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="5b198-112">Type: **uint**</span></span>

<span data-ttu-id="5b198-113">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5b198-113">The status of the operation.</span></span> <span data-ttu-id="5b198-114">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="5b198-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5b198-115">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5b198-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5b198-116">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5b198-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b198-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b198-117">Return value</span></span>

<span data-ttu-id="5b198-118">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="5b198-118">Type: **uint2**</span></span>

<span data-ttu-id="5b198-119">兩個值。</span><span class="sxs-lookup"><span data-stu-id="5b198-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b198-120">備註</span><span class="sxs-lookup"><span data-stu-id="5b198-120">Remarks</span></span>

<span data-ttu-id="5b198-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="5b198-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5b198-122">頂點</span><span class="sxs-lookup"><span data-stu-id="5b198-122">Vertex</span></span> | <span data-ttu-id="5b198-123">船體</span><span class="sxs-lookup"><span data-stu-id="5b198-123">Hull</span></span> | <span data-ttu-id="5b198-124">網域</span><span class="sxs-lookup"><span data-stu-id="5b198-124">Domain</span></span> | <span data-ttu-id="5b198-125">幾何</span><span class="sxs-lookup"><span data-stu-id="5b198-125">Geometry</span></span> | <span data-ttu-id="5b198-126">像素</span><span class="sxs-lookup"><span data-stu-id="5b198-126">Pixel</span></span> | <span data-ttu-id="5b198-127">計算</span><span class="sxs-lookup"><span data-stu-id="5b198-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5b198-128">x</span><span class="sxs-lookup"><span data-stu-id="5b198-128">x</span></span>     | <span data-ttu-id="5b198-129">x</span><span class="sxs-lookup"><span data-stu-id="5b198-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5b198-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b198-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b198-131">Load2 方法</span><span class="sxs-lookup"><span data-stu-id="5b198-131">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> </dl>

 

 