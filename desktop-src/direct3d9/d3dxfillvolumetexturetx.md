---
description: 使用已編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: 'D3DXFillVolumeTextureTX 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000594"
---
# <a name="d3dxfillvolumetexturetx-function"></a>D3DXFillVolumeTextureTX 函式

使用已編譯的高階著色器語言 (HLSL) 函式來填滿材質每個 mipmap 層級的每個材質。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTexture* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)物件的指標，代表要填滿的材質。

</dd> <dt>

*pTextureShader* \[在\]
</dt> <dd>

類型： **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**

[**ID3DXTextureShader**](id3dxtextureshader.md)紋理著色器物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

紋理目標必須是 HLSL 函式，且此函式會包含下列語義：

-   一個輸入參數必須使用位置語義。
-   一個輸入參數必須使用 PSIZE 語義。
-   函數必須傳回使用色彩語義的參數。

輸入參數可以依任何順序排列。 如需範例，請參閱 [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
