---
title: RWTexture1DArray：： Load (int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |RWTexture1DArray：： Load (int，uint) 函數
ms.assetid: EF1D51CC-E037-4E04-9DD6-6A9C5950E5B5
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
ms.openlocfilehash: 5a46dde9b75d3194cc081409fe2b450c5453d7c1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973992"
---
# <a name="rwtexture1darrayloadintuint-function"></a><span data-ttu-id="b34a7-105">RWTexture1DArray：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="b34a7-105">RWTexture1DArray::Load(int,uint) function</span></span>

<span data-ttu-id="b34a7-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b34a7-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34a7-107">語法</span><span class="sxs-lookup"><span data-stu-id="b34a7-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="b34a7-108">參數</span><span class="sxs-lookup"><span data-stu-id="b34a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34a7-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b34a7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b34a7-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="b34a7-110">Type: **int**</span></span>

<span data-ttu-id="b34a7-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="b34a7-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="b34a7-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b34a7-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b34a7-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b34a7-113">Type: **uint**</span></span>

<span data-ttu-id="b34a7-114">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b34a7-114">The status of the operation.</span></span> <span data-ttu-id="b34a7-115">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="b34a7-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b34a7-116">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b34a7-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b34a7-117">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b34a7-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34a7-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b34a7-118">Return value</span></span>

<span data-ttu-id="b34a7-119">輸入：</span><span class="sxs-lookup"><span data-stu-id="b34a7-119">Type:</span></span>

<span data-ttu-id="b34a7-120">傳回型別符合 [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="b34a7-120">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b34a7-121">備註</span><span class="sxs-lookup"><span data-stu-id="b34a7-121">Remarks</span></span>

<span data-ttu-id="b34a7-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b34a7-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b34a7-123">頂點</span><span class="sxs-lookup"><span data-stu-id="b34a7-123">Vertex</span></span> | <span data-ttu-id="b34a7-124">船體</span><span class="sxs-lookup"><span data-stu-id="b34a7-124">Hull</span></span> | <span data-ttu-id="b34a7-125">網域</span><span class="sxs-lookup"><span data-stu-id="b34a7-125">Domain</span></span> | <span data-ttu-id="b34a7-126">幾何</span><span class="sxs-lookup"><span data-stu-id="b34a7-126">Geometry</span></span> | <span data-ttu-id="b34a7-127">像素</span><span class="sxs-lookup"><span data-stu-id="b34a7-127">Pixel</span></span> | <span data-ttu-id="b34a7-128">計算</span><span class="sxs-lookup"><span data-stu-id="b34a7-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b34a7-129">x</span><span class="sxs-lookup"><span data-stu-id="b34a7-129">x</span></span>     | <span data-ttu-id="b34a7-130">x</span><span class="sxs-lookup"><span data-stu-id="b34a7-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b34a7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b34a7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34a7-132">載入方法</span><span class="sxs-lookup"><span data-stu-id="b34a7-132">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 
