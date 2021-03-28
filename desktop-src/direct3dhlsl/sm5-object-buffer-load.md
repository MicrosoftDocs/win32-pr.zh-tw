---
title: Buffer：： Load (int，uint) 函數
description: 讀取緩衝區資料並傳回作業的狀態。 |Buffer：： Load (int，uint) 函數
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
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
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973916"
---
# <a name="bufferloadint-uint-function"></a><span data-ttu-id="cae26-105">Buffer：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="cae26-105">Buffer::Load(int, uint) function</span></span>

<span data-ttu-id="cae26-106">讀取緩衝區資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="cae26-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae26-107">語法</span><span class="sxs-lookup"><span data-stu-id="cae26-107">Syntax</span></span>

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="cae26-108">參數</span><span class="sxs-lookup"><span data-stu-id="cae26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae26-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cae26-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae26-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="cae26-110">Type: **int**</span></span>

<span data-ttu-id="cae26-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="cae26-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cae26-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cae26-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cae26-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="cae26-113">Type: **uint**</span></span>

<span data-ttu-id="cae26-114">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="cae26-114">The status of the operation.</span></span> <span data-ttu-id="cae26-115">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="cae26-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cae26-116">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="cae26-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cae26-117">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cae26-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae26-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="cae26-118">Return value</span></span>

<span data-ttu-id="cae26-119">輸入：</span><span class="sxs-lookup"><span data-stu-id="cae26-119">Type:</span></span>

<span data-ttu-id="cae26-120">傳回型別符合 [**緩衝區**](sm5-object-buffer.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="cae26-120">The return type matches the type in the declaration for the [**Buffer**](sm5-object-buffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae26-121">備註</span><span class="sxs-lookup"><span data-stu-id="cae26-121">Remarks</span></span>

<span data-ttu-id="cae26-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="cae26-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cae26-123">頂點</span><span class="sxs-lookup"><span data-stu-id="cae26-123">Vertex</span></span> | <span data-ttu-id="cae26-124">船體</span><span class="sxs-lookup"><span data-stu-id="cae26-124">Hull</span></span> | <span data-ttu-id="cae26-125">網域</span><span class="sxs-lookup"><span data-stu-id="cae26-125">Domain</span></span> | <span data-ttu-id="cae26-126">幾何</span><span class="sxs-lookup"><span data-stu-id="cae26-126">Geometry</span></span> | <span data-ttu-id="cae26-127">像素</span><span class="sxs-lookup"><span data-stu-id="cae26-127">Pixel</span></span> | <span data-ttu-id="cae26-128">計算</span><span class="sxs-lookup"><span data-stu-id="cae26-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cae26-129">x</span><span class="sxs-lookup"><span data-stu-id="cae26-129">x</span></span>      | <span data-ttu-id="cae26-130">x</span><span class="sxs-lookup"><span data-stu-id="cae26-130">x</span></span>    | <span data-ttu-id="cae26-131">x</span><span class="sxs-lookup"><span data-stu-id="cae26-131">x</span></span>      | <span data-ttu-id="cae26-132">x</span><span class="sxs-lookup"><span data-stu-id="cae26-132">x</span></span>        | <span data-ttu-id="cae26-133">x</span><span class="sxs-lookup"><span data-stu-id="cae26-133">x</span></span>     | <span data-ttu-id="cae26-134">x</span><span class="sxs-lookup"><span data-stu-id="cae26-134">x</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="cae26-135">範例</span><span class="sxs-lookup"><span data-stu-id="cae26-135">Examples</span></span>

<span data-ttu-id="cae26-136">此範例示範如何使用 **Load**：</span><span class="sxs-lookup"><span data-stu-id="cae26-136">This example shows how to use **Load**:</span></span>

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a><span data-ttu-id="cae26-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cae26-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae26-138">載入方法</span><span class="sxs-lookup"><span data-stu-id="cae26-138">Load methods</span></span>](buffer-load.md)
</dt> </dl>

 

 
