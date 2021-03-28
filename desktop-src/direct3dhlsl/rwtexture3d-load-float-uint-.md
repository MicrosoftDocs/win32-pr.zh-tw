---
title: RWTexture3D：： Load (int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |RWTexture3D：： Load (int，uint) 函數
ms.assetid: 7BC334D3-217A-454F-B205-A9D7D66B5E99
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
ms.openlocfilehash: 69b70f6db45a9020e558fadcd1347cc29948ed46
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973976"
---
# <a name="rwtexture3dloadintuint-function"></a><span data-ttu-id="4ddab-105">RWTexture3D：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="4ddab-105">RWTexture3D::Load(int,uint) function</span></span>

<span data-ttu-id="4ddab-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4ddab-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddab-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ddab-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="4ddab-108">參數</span><span class="sxs-lookup"><span data-stu-id="4ddab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddab-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ddab-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ddab-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="4ddab-110">Type: **int**</span></span>

<span data-ttu-id="4ddab-111">材質的位置。</span><span class="sxs-lookup"><span data-stu-id="4ddab-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="4ddab-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ddab-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ddab-113">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="4ddab-113">Type: **uint**</span></span>

<span data-ttu-id="4ddab-114">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4ddab-114">The status of the operation.</span></span> <span data-ttu-id="4ddab-115">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="4ddab-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4ddab-116">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4ddab-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4ddab-117">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4ddab-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ddab-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ddab-118">Return value</span></span>

<span data-ttu-id="4ddab-119">輸入：</span><span class="sxs-lookup"><span data-stu-id="4ddab-119">Type:</span></span>

<span data-ttu-id="4ddab-120">傳回型別符合 [**RWTexture3D**](sm5-object-rwtexture3d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="4ddab-120">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ddab-121">備註</span><span class="sxs-lookup"><span data-stu-id="4ddab-121">Remarks</span></span>

<span data-ttu-id="4ddab-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="4ddab-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4ddab-123">頂點</span><span class="sxs-lookup"><span data-stu-id="4ddab-123">Vertex</span></span> | <span data-ttu-id="4ddab-124">船體</span><span class="sxs-lookup"><span data-stu-id="4ddab-124">Hull</span></span> | <span data-ttu-id="4ddab-125">網域</span><span class="sxs-lookup"><span data-stu-id="4ddab-125">Domain</span></span> | <span data-ttu-id="4ddab-126">幾何</span><span class="sxs-lookup"><span data-stu-id="4ddab-126">Geometry</span></span> | <span data-ttu-id="4ddab-127">像素</span><span class="sxs-lookup"><span data-stu-id="4ddab-127">Pixel</span></span> | <span data-ttu-id="4ddab-128">計算</span><span class="sxs-lookup"><span data-stu-id="4ddab-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4ddab-129">x</span><span class="sxs-lookup"><span data-stu-id="4ddab-129">x</span></span>     | <span data-ttu-id="4ddab-130">x</span><span class="sxs-lookup"><span data-stu-id="4ddab-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4ddab-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ddab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ddab-132">載入方法</span><span class="sxs-lookup"><span data-stu-id="4ddab-132">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 
