---
description: 將 sprite 的陣列新增至要轉譯的 sprite 批次。
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: 'ID3DX10Sprite：:D rawSpritesBuffered 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975717"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite：:D rawSpritesBuffered 方法

將 sprite 的陣列新增至要轉譯的 sprite 批次。 您必須在呼叫 [**ID3DX10Sprite：： Begin**](id3dx10sprite-begin.md) 和 [**ID3DX10Sprite：： end**](id3dx10sprite-end.md)之間呼叫這一點，而且必須在結束之前呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) ，才能將所有批次內建的子內容傳送到裝置以進行轉譯。 這種繪製方法最適合用來繪製少量的 sprite，而您想要將它緩衝至大型批次，例如字型。

## <a name="syntax"></a>語法


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

 

 
