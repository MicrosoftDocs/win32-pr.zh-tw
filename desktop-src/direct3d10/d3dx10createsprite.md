---
description: 建立用來繪製2D 材質的 sprite。請注意，我們建議您不要使用這個函式，而是使用 Direct2D 和 DirectXTK library SpriteBatch 類別。
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: 'D3DX10CreateSprite 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999003"
---
# <a name="d3dx10createsprite-function"></a>D3DX10CreateSprite 函式

建立用來繪製2D 材質的 sprite。

> [!Note]  
> 我們建議您不要使用這個函式，而是使用 [Direct2D](../direct2d/direct2d-portal.md) 和 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SpriteBatch** 類別。

 

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

裝置的指標 (查看將繪製 sprite 的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。

</dd> <dt>

*cDeviceBufferSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

當呼叫 [**ID3DX10Sprite：： Flush**](id3dx10sprite-flush.md) 或 [**ID3DX10Sprite：:D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) 時，將會傳送至裝置的頂點緩衝區大小（以 sprite 數為限）。 如果您知道將會一次轉譯少量的 sprite (儲存記憶體) ，而如果您知道將會一次轉譯大量的 sprite，則這應該是很小的數位。 最大值為4096。 如果指定0，則會自動將頂點緩衝區大小設定為4096。

</dd> <dt>

*ppSprite* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Sprite 介面之指標的位址 (參閱 [**ID3DX10Sprite 介面**](id3dx10sprite.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
