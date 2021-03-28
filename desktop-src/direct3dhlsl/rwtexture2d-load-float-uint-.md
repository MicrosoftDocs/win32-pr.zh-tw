---
title: RWTexture2D：： Load (int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |RWTexture2D：： Load (int，uint) 函數
ms.assetid: E61E1EFD-BDD1-4415-9993-0CD7203B5BDC
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
ms.openlocfilehash: dcc8619caea715f1e752ba2768cca1d4e5f330ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974233"
---
# <a name="rwtexture2dloadintuint-function"></a><span data-ttu-id="e1add-105">RWTexture2D：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="e1add-105">RWTexture2D::Load(int,uint) function</span></span>

<span data-ttu-id="e1add-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e1add-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1add-107">語法</span><span class="sxs-lookup"><span data-stu-id="e1add-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="e1add-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1add-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1add-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1add-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1add-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="e1add-110">Type: **int**</span></span>

<span data-ttu-id="e1add-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="e1add-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e1add-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e1add-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1add-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e1add-113">Type: **uint**</span></span>

<span data-ttu-id="e1add-114">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e1add-114">The status of the operation.</span></span> <span data-ttu-id="e1add-115">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="e1add-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e1add-116">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e1add-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e1add-117">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e1add-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1add-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1add-118">Return value</span></span>

<span data-ttu-id="e1add-119">輸入：</span><span class="sxs-lookup"><span data-stu-id="e1add-119">Type:</span></span>

<span data-ttu-id="e1add-120">傳回型別符合 [**RWTexture2D**](sm5-object-rwtexture2d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="e1add-120">The return type matches the type in the declaration for the [**RWTexture2D**](sm5-object-rwtexture2d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1add-121">備註</span><span class="sxs-lookup"><span data-stu-id="e1add-121">Remarks</span></span>

<span data-ttu-id="e1add-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e1add-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e1add-123">頂點</span><span class="sxs-lookup"><span data-stu-id="e1add-123">Vertex</span></span> | <span data-ttu-id="e1add-124">船體</span><span class="sxs-lookup"><span data-stu-id="e1add-124">Hull</span></span> | <span data-ttu-id="e1add-125">網域</span><span class="sxs-lookup"><span data-stu-id="e1add-125">Domain</span></span> | <span data-ttu-id="e1add-126">幾何</span><span class="sxs-lookup"><span data-stu-id="e1add-126">Geometry</span></span> | <span data-ttu-id="e1add-127">像素</span><span class="sxs-lookup"><span data-stu-id="e1add-127">Pixel</span></span> | <span data-ttu-id="e1add-128">計算</span><span class="sxs-lookup"><span data-stu-id="e1add-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e1add-129">x</span><span class="sxs-lookup"><span data-stu-id="e1add-129">x</span></span>     | <span data-ttu-id="e1add-130">x</span><span class="sxs-lookup"><span data-stu-id="e1add-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e1add-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1add-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1add-132">載入方法</span><span class="sxs-lookup"><span data-stu-id="e1add-132">Load methods</span></span>](rwtexture2d-load.md)
</dt> </dl>

 

 
