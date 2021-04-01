---
title: StructuredBuffer：： Load (int，uint) 函數
description: 讀取緩衝區資料並傳回操作的狀態。 |StructuredBuffer：： Load (int，uint) 函數
ms.assetid: d71c6057-6651-4b70-91cf-892fde6d0188
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
ms.openlocfilehash: 957b85631bbd19742cb7afe52f6bf061de323614
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195970"
---
# <a name="structuredbufferloadintuint-function"></a><span data-ttu-id="5f791-105">StructuredBuffer：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="5f791-105">StructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="5f791-106">讀取緩衝區資料並傳回操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="5f791-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f791-107">語法</span><span class="sxs-lookup"><span data-stu-id="5f791-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="5f791-108">參數</span><span class="sxs-lookup"><span data-stu-id="5f791-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f791-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f791-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f791-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="5f791-110">Type: **int**</span></span>

<span data-ttu-id="5f791-111">緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="5f791-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5f791-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f791-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f791-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="5f791-113">Type: **uint**</span></span>

<span data-ttu-id="5f791-114">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5f791-114">The status of the operation.</span></span> <span data-ttu-id="5f791-115">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="5f791-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5f791-116">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5f791-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5f791-117">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5f791-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f791-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f791-118">Return value</span></span>

<span data-ttu-id="5f791-119">輸入：</span><span class="sxs-lookup"><span data-stu-id="5f791-119">Type:</span></span>

<span data-ttu-id="5f791-120">傳回型別符合 [**StructuredBuffer**](sm5-object-structuredbuffer.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="5f791-120">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f791-121">備註</span><span class="sxs-lookup"><span data-stu-id="5f791-121">Remarks</span></span>

<span data-ttu-id="5f791-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="5f791-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5f791-123">頂點</span><span class="sxs-lookup"><span data-stu-id="5f791-123">Vertex</span></span> | <span data-ttu-id="5f791-124">船體</span><span class="sxs-lookup"><span data-stu-id="5f791-124">Hull</span></span> | <span data-ttu-id="5f791-125">網域</span><span class="sxs-lookup"><span data-stu-id="5f791-125">Domain</span></span> | <span data-ttu-id="5f791-126">幾何</span><span class="sxs-lookup"><span data-stu-id="5f791-126">Geometry</span></span> | <span data-ttu-id="5f791-127">像素</span><span class="sxs-lookup"><span data-stu-id="5f791-127">Pixel</span></span> | <span data-ttu-id="5f791-128">計算</span><span class="sxs-lookup"><span data-stu-id="5f791-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5f791-129">x</span><span class="sxs-lookup"><span data-stu-id="5f791-129">x</span></span>     | <span data-ttu-id="5f791-130">x</span><span class="sxs-lookup"><span data-stu-id="5f791-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5f791-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f791-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f791-132">載入方法</span><span class="sxs-lookup"><span data-stu-id="5f791-132">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 
