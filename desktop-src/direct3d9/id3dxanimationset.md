---
description: 這個介面會封裝動畫控制器所設定之動畫所需的最小功能。
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: 'ID3DXAnimationSet 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196441"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="a9297-103">ID3DXAnimationSet 介面</span><span class="sxs-lookup"><span data-stu-id="a9297-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="a9297-104">這個介面會封裝動畫控制器所設定之動畫所需的最小功能。</span><span class="sxs-lookup"><span data-stu-id="a9297-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="a9297-105">Advanced users 可能會想要自行執行這個介面，以符合其特殊需求;不過，對於大多數的使用者而言，衍生的 [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) 和 [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) 介面應該已經足夠。</span><span class="sxs-lookup"><span data-stu-id="a9297-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="a9297-106">成員</span><span class="sxs-lookup"><span data-stu-id="a9297-106">Members</span></span>

<span data-ttu-id="a9297-107">**ID3DXAnimationSet** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a9297-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9297-108">**ID3DXAnimationSet** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9297-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="a9297-109">方法</span><span class="sxs-lookup"><span data-stu-id="a9297-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9297-110">方法</span><span class="sxs-lookup"><span data-stu-id="a9297-110">Methods</span></span>

<span data-ttu-id="a9297-111">**ID3DXAnimationSet** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a9297-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="a9297-112">方法</span><span class="sxs-lookup"><span data-stu-id="a9297-112">Method</span></span>                                                                        | <span data-ttu-id="a9297-113">描述</span><span class="sxs-lookup"><span data-stu-id="a9297-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="a9297-114">**GetAnimationIndexByName**</span><span class="sxs-lookup"><span data-stu-id="a9297-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="a9297-115">取得動畫的索引，並指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="a9297-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="a9297-116">**GetAnimationNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="a9297-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="a9297-117">取得動畫的名稱，指定其索引。</span><span class="sxs-lookup"><span data-stu-id="a9297-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="a9297-118">**GetCallback**</span><span class="sxs-lookup"><span data-stu-id="a9297-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="a9297-119">取得動畫集中特定回呼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9297-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="a9297-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a9297-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="a9297-121">取得動畫集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9297-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="a9297-122">**GetNumAnimations**</span><span class="sxs-lookup"><span data-stu-id="a9297-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="a9297-123">取得動畫集中的動畫數目。</span><span class="sxs-lookup"><span data-stu-id="a9297-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="a9297-124">**GetPeriod**</span><span class="sxs-lookup"><span data-stu-id="a9297-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="a9297-125">取得動畫集合的期間。</span><span class="sxs-lookup"><span data-stu-id="a9297-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="a9297-126">**GetPeriodicPosition**</span><span class="sxs-lookup"><span data-stu-id="a9297-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="a9297-127">傳回動畫集合的當地時間範圍內的時間位置。</span><span class="sxs-lookup"><span data-stu-id="a9297-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="a9297-128">**GetSRT**</span><span class="sxs-lookup"><span data-stu-id="a9297-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="a9297-129">取得動畫集合的縮放、旋轉和轉譯值。</span><span class="sxs-lookup"><span data-stu-id="a9297-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9297-130">備註</span><span class="sxs-lookup"><span data-stu-id="a9297-130">Remarks</span></span>

<span data-ttu-id="a9297-131">動畫組是由相同動畫的許多節點動畫所組成。</span><span class="sxs-lookup"><span data-stu-id="a9297-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="a9297-132">LPD3DXANIMATIONSET 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a9297-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="a9297-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9297-133">Requirements</span></span>



| <span data-ttu-id="a9297-134">需求</span><span class="sxs-lookup"><span data-stu-id="a9297-134">Requirement</span></span> | <span data-ttu-id="a9297-135">值</span><span class="sxs-lookup"><span data-stu-id="a9297-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9297-136">標頭</span><span class="sxs-lookup"><span data-stu-id="a9297-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a9297-137"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9297-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a9297-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9297-138">Library</span></span><br/> | <dl> <span data-ttu-id="a9297-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9297-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9297-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9297-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9297-141">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="a9297-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
