---
title: ByteAddressBuffer：： Load (int，uint) 函數
description: 取得一個值和作業的狀態。
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 319daad35da0256a4d36ef4580df62fd4d295854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093599"
---
# <a name="byteaddressbufferloadint-uint-function"></a><span data-ttu-id="855af-104">ByteAddressBuffer：： Load (int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="855af-104">ByteAddressBuffer::Load(int, uint) function</span></span>

<span data-ttu-id="855af-105">取得一個值和作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="855af-105">Gets one value and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="855af-106">語法</span><span class="sxs-lookup"><span data-stu-id="855af-106">Syntax</span></span>

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="855af-107">參數</span><span class="sxs-lookup"><span data-stu-id="855af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="855af-108">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="855af-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="855af-109">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="855af-109">Type: **int**</span></span>

<span data-ttu-id="855af-110">輸入位址（以位元組為單位），必須是4的倍數。</span><span class="sxs-lookup"><span data-stu-id="855af-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="855af-111">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="855af-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="855af-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="855af-112">Type: **uint**</span></span>

<span data-ttu-id="855af-113">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="855af-113">The status of the operation.</span></span> <span data-ttu-id="855af-114">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="855af-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="855af-115">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="855af-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="855af-116">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="855af-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="855af-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="855af-117">Return value</span></span>

<span data-ttu-id="855af-118">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="855af-118">Type: **uint**</span></span>

<span data-ttu-id="855af-119">一個值。</span><span class="sxs-lookup"><span data-stu-id="855af-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="855af-120">備註</span><span class="sxs-lookup"><span data-stu-id="855af-120">Remarks</span></span>

<span data-ttu-id="855af-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="855af-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="855af-122">頂點</span><span class="sxs-lookup"><span data-stu-id="855af-122">Vertex</span></span> | <span data-ttu-id="855af-123">船體</span><span class="sxs-lookup"><span data-stu-id="855af-123">Hull</span></span> | <span data-ttu-id="855af-124">網域</span><span class="sxs-lookup"><span data-stu-id="855af-124">Domain</span></span> | <span data-ttu-id="855af-125">幾何</span><span class="sxs-lookup"><span data-stu-id="855af-125">Geometry</span></span> | <span data-ttu-id="855af-126">像素</span><span class="sxs-lookup"><span data-stu-id="855af-126">Pixel</span></span> | <span data-ttu-id="855af-127">計算</span><span class="sxs-lookup"><span data-stu-id="855af-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="855af-128">x</span><span class="sxs-lookup"><span data-stu-id="855af-128">x</span></span>      | <span data-ttu-id="855af-129">x</span><span class="sxs-lookup"><span data-stu-id="855af-129">x</span></span>    | <span data-ttu-id="855af-130">x</span><span class="sxs-lookup"><span data-stu-id="855af-130">x</span></span>      | <span data-ttu-id="855af-131">x</span><span class="sxs-lookup"><span data-stu-id="855af-131">x</span></span>        | <span data-ttu-id="855af-132">x</span><span class="sxs-lookup"><span data-stu-id="855af-132">x</span></span>     | <span data-ttu-id="855af-133">x</span><span class="sxs-lookup"><span data-stu-id="855af-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="855af-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="855af-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="855af-135">載入方法</span><span class="sxs-lookup"><span data-stu-id="855af-135">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="855af-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="855af-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
