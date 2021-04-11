---
description: 準備用來繪製 sprite 的裝置。
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite：： Begin 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196350"
---
# <a name="id3dx10spritebegin-method"></a>ID3DX10Sprite：： Begin 方法

準備用來繪製 sprite 的裝置。

## <a name="syntax"></a>語法


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

控制如何繪製 sprite 的旗標。 請參閱 [**D3DX10 \_ SPRITE \_ 旗**](d3dx10-sprite-flag.md)標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

每次開始呼叫都必須與 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md)的呼叫相符。

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

 

 
