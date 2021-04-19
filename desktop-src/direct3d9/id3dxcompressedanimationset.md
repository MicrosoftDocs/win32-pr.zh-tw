---
description: 應用程式會使用這個介面的方法，來執行以壓縮資料格式儲存的主要畫面格動畫集合。
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: 'ID3DXCompressedAnimationSet 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993885"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="e69ca-103">ID3DXCompressedAnimationSet 介面</span><span class="sxs-lookup"><span data-stu-id="e69ca-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="e69ca-104">應用程式會使用這個介面的方法，來執行以壓縮資料格式儲存的主要畫面格動畫集合。</span><span class="sxs-lookup"><span data-stu-id="e69ca-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="e69ca-105">成員</span><span class="sxs-lookup"><span data-stu-id="e69ca-105">Members</span></span>

<span data-ttu-id="e69ca-106">**ID3DXCompressedAnimationSet** 介面繼承自 [**ID3DXAnimationSet**](id3dxanimationset.md)。</span><span class="sxs-lookup"><span data-stu-id="e69ca-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="e69ca-107">**ID3DXCompressedAnimationSet** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e69ca-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="e69ca-108">方法</span><span class="sxs-lookup"><span data-stu-id="e69ca-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e69ca-109">方法</span><span class="sxs-lookup"><span data-stu-id="e69ca-109">Methods</span></span>

<span data-ttu-id="e69ca-110">**ID3DXCompressedAnimationSet** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e69ca-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="e69ca-111">方法</span><span class="sxs-lookup"><span data-stu-id="e69ca-111">Method</span></span>                                                                                  | <span data-ttu-id="e69ca-112">描述</span><span class="sxs-lookup"><span data-stu-id="e69ca-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="e69ca-113">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="e69ca-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="e69ca-114">使用主要畫面格動畫所用的回呼金鑰資料來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="e69ca-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="e69ca-115">**GetCompressedData**</span><span class="sxs-lookup"><span data-stu-id="e69ca-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="e69ca-116">取得儲存已壓縮之主要畫面格動畫資料的資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e69ca-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="e69ca-117">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="e69ca-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="e69ca-118">取得動畫集中的回呼索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="e69ca-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="e69ca-119">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="e69ca-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="e69ca-120">取得動畫集合播放迴圈的型別。</span><span class="sxs-lookup"><span data-stu-id="e69ca-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="e69ca-121">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="e69ca-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="e69ca-122">取得每秒發生的動畫主要畫面格刻度數目。</span><span class="sxs-lookup"><span data-stu-id="e69ca-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="e69ca-123">備註</span><span class="sxs-lookup"><span data-stu-id="e69ca-123">Remarks</span></span>

<span data-ttu-id="e69ca-124">使用 [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md)建立壓縮格式的主要畫面格動畫。</span><span class="sxs-lookup"><span data-stu-id="e69ca-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="e69ca-125">LPD3DXCOMPRESSEDANIMATIONSET 型別定義為這個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e69ca-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="e69ca-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e69ca-126">Requirements</span></span>



| <span data-ttu-id="e69ca-127">需求</span><span class="sxs-lookup"><span data-stu-id="e69ca-127">Requirement</span></span> | <span data-ttu-id="e69ca-128">值</span><span class="sxs-lookup"><span data-stu-id="e69ca-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e69ca-129">標頭</span><span class="sxs-lookup"><span data-stu-id="e69ca-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e69ca-130"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e69ca-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e69ca-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="e69ca-131">Library</span></span><br/> | <dl> <span data-ttu-id="e69ca-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e69ca-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e69ca-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e69ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69ca-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="e69ca-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="e69ca-135">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e69ca-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




