---
description: 可告知 sprite 繪製 API 如何運作的 sprite 旗標。 這些會傳遞至 ID3DX10Sprite：： Begin。
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: 'D3DX10_SPRITE_FLAG 列舉 (D3DX10Core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986765"
---
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="f010d-104">D3DX10 \_ SPRITE \_ 旗標列舉</span><span class="sxs-lookup"><span data-stu-id="f010d-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="f010d-105">可告知 sprite 繪製 API 如何運作的 sprite 旗標。</span><span class="sxs-lookup"><span data-stu-id="f010d-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="f010d-106">這些會傳遞至 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md)。</span><span class="sxs-lookup"><span data-stu-id="f010d-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f010d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f010d-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="f010d-108">常數</span><span class="sxs-lookup"><span data-stu-id="f010d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f010d-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10 \_ SPRITE \_ 排序 \_ 材質**</span><span class="sxs-lookup"><span data-stu-id="f010d-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="f010d-110">在轉譯之前依材質排序子層級，如此一來，當有多個 sprite 具有相同材質時，會同時轉譯所有的 sprite，進而改善效能。</span><span class="sxs-lookup"><span data-stu-id="f010d-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="f010d-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 \_ SPRITE \_ 排序 \_ 深度 \_ 回 \_ \_ FRONT**</span><span class="sxs-lookup"><span data-stu-id="f010d-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="f010d-112">從後到前將 sprite 排序，以先繪製離相機更遠的動畫。</span><span class="sxs-lookup"><span data-stu-id="f010d-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="f010d-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ SPRITE \_ 排序 \_ 深度 \_ 向前 \_ \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="f010d-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="f010d-114">將 sprite 從前方排序至背面，以便先繪製更接近相機的動畫。</span><span class="sxs-lookup"><span data-stu-id="f010d-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="f010d-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ SPRITE \_ 儲存 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="f010d-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="f010d-116">儲存狀態，以便在呼叫 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md) 時，將狀態還原到呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 之前的方式。</span><span class="sxs-lookup"><span data-stu-id="f010d-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="f010d-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10 \_ SPRITE \_ ADDREF \_ 材質**</span><span class="sxs-lookup"><span data-stu-id="f010d-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="f010d-118">將 AddRef 傳遞至 ID3DX10Sprite 時，會在所有紋理上呼叫 [**：:D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md)。</span><span class="sxs-lookup"><span data-stu-id="f010d-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f010d-119">備註</span><span class="sxs-lookup"><span data-stu-id="f010d-119">Remarks</span></span>

<span data-ttu-id="f010d-120">在進行從前對後或後端排序之後，它會自動依材質執行次要排序。</span><span class="sxs-lookup"><span data-stu-id="f010d-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="f010d-121">當相同的平面上有許多具有相同材質的 sprite 時（例如在遊戲中繪製使用者介面時），這會很有説明。</span><span class="sxs-lookup"><span data-stu-id="f010d-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="f010d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f010d-122">Requirements</span></span>



| <span data-ttu-id="f010d-123">需求</span><span class="sxs-lookup"><span data-stu-id="f010d-123">Requirement</span></span> | <span data-ttu-id="f010d-124">值</span><span class="sxs-lookup"><span data-stu-id="f010d-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f010d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f010d-125">Header</span></span><br/> | <dl> <span data-ttu-id="f010d-126"><dt>D3DX10Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="f010d-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f010d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f010d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f010d-128">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="f010d-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




