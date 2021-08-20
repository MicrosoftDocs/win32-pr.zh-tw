---
description: 繪製 sprite 的陣列。
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: 'ID3DX10Sprite：:D rawSpritesImmediate 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0a3295d64efc3f3ff05b39e0866a15fb7eed9ba2d8c580fe2c7b219d36708e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046896"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite：:D rawSpritesImmediate 方法

繪製 sprite 的陣列。 這會立即將 sprite 傳送至裝置以進行轉譯，這與 ID3DX10Sprite 不同 [**：:D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) ，這會在呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) 時，只將 sprite 的陣列新增至要轉譯的一批 sprite。 此繪製方法最適合用來繪製已在 CPU (上排序的大量 sprite，或不需要) 的排序，例如在物件中。 必須在呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 和 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md)之間呼叫這項功能。

## <a name="syntax"></a>語法


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSprites* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ SPRITE**](d3dx10-sprite.md)\***

要繪製之 sprite 的陣列。 請參閱 [**D3DX10 \_ SPRITE**](d3dx10-sprite.md)。

</dd> <dt>

*cSprites* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

PSprites 中的 sprite 數目。

</dd> <dt>

*cbSprite* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

您要傳遞至 pSprites 之 sprite 結構的大小。 傳入0相當於將 sizeof (D3DX10 \_ SPRITE) 傳入。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
