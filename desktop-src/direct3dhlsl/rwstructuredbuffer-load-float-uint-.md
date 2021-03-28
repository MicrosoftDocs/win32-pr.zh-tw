---
title: RWStructuredBuffer：： Load (int，uint) 函數
description: 讀取緩衝區資料並傳回操作的狀態。 |RWStructuredBuffer：： Load (int，uint) 函數
ms.assetid: 19FAA031-F31E-4B73-BC69-489CDF0CF184
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
ms.openlocfilehash: 74a153d4b56ec16b80dec180287005666747d259
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973997"
---
# <a name="rwstructuredbufferloadintuint-function"></a><span data-ttu-id="b7acf-105">RWStructuredBuffer：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="b7acf-105">RWStructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="b7acf-106">讀取緩衝區資料並傳回操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="b7acf-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7acf-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7acf-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="b7acf-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7acf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7acf-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7acf-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7acf-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="b7acf-110">Type: **int**</span></span>

<span data-ttu-id="b7acf-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="b7acf-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b7acf-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7acf-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7acf-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b7acf-113">Type: **uint**</span></span>

<span data-ttu-id="b7acf-114">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b7acf-114">The status of the operation.</span></span> <span data-ttu-id="b7acf-115">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="b7acf-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b7acf-116">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b7acf-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b7acf-117">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b7acf-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7acf-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7acf-118">Return value</span></span>

<span data-ttu-id="b7acf-119">輸入：</span><span class="sxs-lookup"><span data-stu-id="b7acf-119">Type:</span></span>

<span data-ttu-id="b7acf-120">傳回型別符合 [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="b7acf-120">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7acf-121">備註</span><span class="sxs-lookup"><span data-stu-id="b7acf-121">Remarks</span></span>

<span data-ttu-id="b7acf-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b7acf-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b7acf-123">頂點</span><span class="sxs-lookup"><span data-stu-id="b7acf-123">Vertex</span></span> | <span data-ttu-id="b7acf-124">船體</span><span class="sxs-lookup"><span data-stu-id="b7acf-124">Hull</span></span> | <span data-ttu-id="b7acf-125">網域</span><span class="sxs-lookup"><span data-stu-id="b7acf-125">Domain</span></span> | <span data-ttu-id="b7acf-126">幾何</span><span class="sxs-lookup"><span data-stu-id="b7acf-126">Geometry</span></span> | <span data-ttu-id="b7acf-127">像素</span><span class="sxs-lookup"><span data-stu-id="b7acf-127">Pixel</span></span> | <span data-ttu-id="b7acf-128">計算</span><span class="sxs-lookup"><span data-stu-id="b7acf-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b7acf-129">x</span><span class="sxs-lookup"><span data-stu-id="b7acf-129">x</span></span>      | <span data-ttu-id="b7acf-130">x</span><span class="sxs-lookup"><span data-stu-id="b7acf-130">x</span></span>    | <span data-ttu-id="b7acf-131">x</span><span class="sxs-lookup"><span data-stu-id="b7acf-131">x</span></span>      | <span data-ttu-id="b7acf-132">x</span><span class="sxs-lookup"><span data-stu-id="b7acf-132">x</span></span>        | <span data-ttu-id="b7acf-133">x</span><span class="sxs-lookup"><span data-stu-id="b7acf-133">x</span></span>     | <span data-ttu-id="b7acf-134">x</span><span class="sxs-lookup"><span data-stu-id="b7acf-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b7acf-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7acf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7acf-136">載入方法</span><span class="sxs-lookup"><span data-stu-id="b7acf-136">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 
