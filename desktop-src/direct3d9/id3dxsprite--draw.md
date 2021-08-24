---
description: 將 sprite 新增至批次 sprite 的清單。
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: 'ID3DXSprite：:D 原始方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d453a2e03538b7601b5f73033a4749430e8812ef317a90816cac220e61695279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747368"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite：:D 原始方法

將 sprite 新增至批次 sprite 的清單。

## <a name="syntax"></a>語法


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

代表 sprite 材質之 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面的指標。

</dd> <dt>

*pSrcRect* \[在\]
</dt> <dd>

Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，表示要用於 sprite 的來源材質部分。 如果此參數為 **Null**，則會使用整個來源影像作為 sprite。

</dd> <dt>

*pCenter* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)向量的指標，可識別 sprite 的中心。 如果這個引數是 **Null**，則會使用點 (0、0、0) （左上角）。

</dd> <dt>

*pPosition* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)向量的指標，可識別 sprite 的位置。 如果這個引數是 **Null**，則會使用點 (0、0、0) （左上角）。

</dd> <dt>

*色彩* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

[**D3DCOLOR**](d3dcolor.md) 類型。 色彩和 Alpha 通道會以這個值來調製。 0xFFFFFFFF 的值會維護原始來源色彩和 Alpha 資料。 使用 [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) 宏來協助產生此色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

若要調整、旋轉或轉譯 sprite，請在呼叫 ID3DXSprite：:D raw 之前，以包含縮放、旋轉和轉譯 (SRT) 值的矩陣來呼叫 [**ID3DXSprite：： SetTransform**](id3dxsprite--settransform.md) 。 如需有關在矩陣中設定 SRT 值的詳細資訊，請參閱 [矩陣轉換](transforms.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
