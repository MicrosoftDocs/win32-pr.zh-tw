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
# <a name="d3dx10_sprite_flag-enumeration"></a>D3DX10 \_ SPRITE \_ 旗標列舉

可告知 sprite 繪製 API 如何運作的 sprite 旗標。 這些會傳遞至 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md)。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10 \_ SPRITE \_ 排序 \_ 材質**
</dt> <dd>

在轉譯之前依材質排序子層級，如此一來，當有多個 sprite 具有相同材質時，會同時轉譯所有的 sprite，進而改善效能。

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 \_ SPRITE \_ 排序 \_ 深度 \_ 回 \_ \_ FRONT**
</dt> <dd>

從後到前將 sprite 排序，以先繪製離相機更遠的動畫。

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ SPRITE \_ 排序 \_ 深度 \_ 向前 \_ \_ 復原**
</dt> <dd>

將 sprite 從前方排序至背面，以便先繪製更接近相機的動畫。

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ SPRITE \_ 儲存 \_ 狀態**
</dt> <dd>

儲存狀態，以便在呼叫 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md) 時，將狀態還原到呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 之前的方式。

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10 \_ SPRITE \_ ADDREF \_ 材質**
</dt> <dd>

將 AddRef 傳遞至 ID3DX10Sprite 時，會在所有紋理上呼叫 [**：:D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md)。

</dd> </dl>

## <a name="remarks"></a>備註

在進行從前對後或後端排序之後，它會自動依材質執行次要排序。 當相同的平面上有許多具有相同材質的 sprite 時（例如在遊戲中繪製使用者介面時），這會很有説明。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Core。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




