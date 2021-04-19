---
description: 定義支援的 blend 作業。 請參閱備註中的詞彙定義。
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: 'D3DBLENDOP 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988174"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="e5ab2-104">D3DBLENDOP 列舉</span><span class="sxs-lookup"><span data-stu-id="e5ab2-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="e5ab2-105">定義支援的 blend 作業。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-105">Defines the supported blend operations.</span></span> <span data-ttu-id="e5ab2-106">請參閱備註中的詞彙定義。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ab2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ab2-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="e5ab2-108">常數</span><span class="sxs-lookup"><span data-stu-id="e5ab2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5ab2-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="e5ab2-110">結果會是新增至來源的目的地。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-110">The result is the destination added to the source.</span></span> <span data-ttu-id="e5ab2-111">結果 = 來源 + 目的地</span><span class="sxs-lookup"><span data-stu-id="e5ab2-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="e5ab2-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP \_ 減**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="e5ab2-113">結果是從目的地減去至來源的目的地。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="e5ab2-114">結果 = 來源-目的地</span><span class="sxs-lookup"><span data-stu-id="e5ab2-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="e5ab2-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="e5ab2-116">結果會從目的地減去來源。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="e5ab2-117">結果 = 目的地-來源</span><span class="sxs-lookup"><span data-stu-id="e5ab2-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="e5ab2-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ 分鐘**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="e5ab2-119">結果是來源和目的地的最小值。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="e5ab2-120">結果 = 最小 (來源，目的地) </span><span class="sxs-lookup"><span data-stu-id="e5ab2-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="e5ab2-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="e5ab2-122">結果是來源和目的地的最大值。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="e5ab2-123">結果 = 最大 (來源，目的地) </span><span class="sxs-lookup"><span data-stu-id="e5ab2-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="e5ab2-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e5ab2-125">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e5ab2-126">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e5ab2-127">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5ab2-128">備註</span><span class="sxs-lookup"><span data-stu-id="e5ab2-128">Remarks</span></span>

<span data-ttu-id="e5ab2-129">來源、目的地和結果定義如下：</span><span class="sxs-lookup"><span data-stu-id="e5ab2-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="e5ab2-130">詞彙</span><span class="sxs-lookup"><span data-stu-id="e5ab2-130">Term</span></span>        | <span data-ttu-id="e5ab2-131">類型</span><span class="sxs-lookup"><span data-stu-id="e5ab2-131">Type</span></span>   | <span data-ttu-id="e5ab2-132">描述</span><span class="sxs-lookup"><span data-stu-id="e5ab2-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="e5ab2-133">來源</span><span class="sxs-lookup"><span data-stu-id="e5ab2-133">Source</span></span>      | <span data-ttu-id="e5ab2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e5ab2-134">Input</span></span>  | <span data-ttu-id="e5ab2-135">運算之前的來源圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="e5ab2-136">Destination</span><span class="sxs-lookup"><span data-stu-id="e5ab2-136">Destination</span></span> | <span data-ttu-id="e5ab2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e5ab2-137">Input</span></span>  | <span data-ttu-id="e5ab2-138">作業之前，目的緩衝區中圖元的色彩。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="e5ab2-139">結果</span><span class="sxs-lookup"><span data-stu-id="e5ab2-139">Result</span></span>      | <span data-ttu-id="e5ab2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e5ab2-140">Output</span></span> | <span data-ttu-id="e5ab2-141">傳回的值是作業所產生的混合色彩。</span><span class="sxs-lookup"><span data-stu-id="e5ab2-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="e5ab2-142">這個列舉型別會定義下列轉譯狀態所使用的值：</span><span class="sxs-lookup"><span data-stu-id="e5ab2-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="e5ab2-143">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="e5ab2-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="e5ab2-144">D3DRS \_ BLENDOPALPHA</span><span class="sxs-lookup"><span data-stu-id="e5ab2-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ab2-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5ab2-145">Requirements</span></span>



| <span data-ttu-id="e5ab2-146">需求</span><span class="sxs-lookup"><span data-stu-id="e5ab2-146">Requirement</span></span> | <span data-ttu-id="e5ab2-147">值</span><span class="sxs-lookup"><span data-stu-id="e5ab2-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ab2-148">標頭</span><span class="sxs-lookup"><span data-stu-id="e5ab2-148">Header</span></span><br/> | <dl> <span data-ttu-id="e5ab2-149"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ab2-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ab2-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5ab2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ab2-151">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="e5ab2-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e5ab2-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="e5ab2-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="e5ab2-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
