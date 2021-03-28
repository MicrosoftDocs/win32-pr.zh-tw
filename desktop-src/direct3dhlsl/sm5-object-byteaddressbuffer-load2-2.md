---
title: ByteAddressBuffer：： Load2 (uint，uint) 函數
description: 取得兩個值和作業的狀態。
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
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
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023862"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="e1fa6-104">Load2 (uint，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="e1fa6-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="e1fa6-105">取得兩個值和作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1fa6-106">語法</span><span class="sxs-lookup"><span data-stu-id="e1fa6-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="e1fa6-107">參數</span><span class="sxs-lookup"><span data-stu-id="e1fa6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1fa6-108">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1fa6-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa6-109">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e1fa6-109">Type: **uint**</span></span>

<span data-ttu-id="e1fa6-110">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="e1fa6-111">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e1fa6-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1fa6-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e1fa6-112">Type: **uint**</span></span>

<span data-ttu-id="e1fa6-113">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-113">The status of the operation.</span></span> <span data-ttu-id="e1fa6-114">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e1fa6-115">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e1fa6-116">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1fa6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1fa6-117">Return value</span></span>

<span data-ttu-id="e1fa6-118">類型： **uint2**</span><span class="sxs-lookup"><span data-stu-id="e1fa6-118">Type: **uint2**</span></span>

<span data-ttu-id="e1fa6-119">兩個值。</span><span class="sxs-lookup"><span data-stu-id="e1fa6-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1fa6-120">備註</span><span class="sxs-lookup"><span data-stu-id="e1fa6-120">Remarks</span></span>

<span data-ttu-id="e1fa6-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e1fa6-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e1fa6-122">頂點</span><span class="sxs-lookup"><span data-stu-id="e1fa6-122">Vertex</span></span> | <span data-ttu-id="e1fa6-123">船體</span><span class="sxs-lookup"><span data-stu-id="e1fa6-123">Hull</span></span> | <span data-ttu-id="e1fa6-124">網域</span><span class="sxs-lookup"><span data-stu-id="e1fa6-124">Domain</span></span> | <span data-ttu-id="e1fa6-125">幾何</span><span class="sxs-lookup"><span data-stu-id="e1fa6-125">Geometry</span></span> | <span data-ttu-id="e1fa6-126">像素</span><span class="sxs-lookup"><span data-stu-id="e1fa6-126">Pixel</span></span> | <span data-ttu-id="e1fa6-127">計算</span><span class="sxs-lookup"><span data-stu-id="e1fa6-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e1fa6-128">x</span><span class="sxs-lookup"><span data-stu-id="e1fa6-128">x</span></span>      | <span data-ttu-id="e1fa6-129">x</span><span class="sxs-lookup"><span data-stu-id="e1fa6-129">x</span></span>    | <span data-ttu-id="e1fa6-130">x</span><span class="sxs-lookup"><span data-stu-id="e1fa6-130">x</span></span>      | <span data-ttu-id="e1fa6-131">x</span><span class="sxs-lookup"><span data-stu-id="e1fa6-131">x</span></span>        | <span data-ttu-id="e1fa6-132">x</span><span class="sxs-lookup"><span data-stu-id="e1fa6-132">x</span></span>     | <span data-ttu-id="e1fa6-133">x</span><span class="sxs-lookup"><span data-stu-id="e1fa6-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e1fa6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1fa6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fa6-135">Load2 方法</span><span class="sxs-lookup"><span data-stu-id="e1fa6-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="e1fa6-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="e1fa6-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 