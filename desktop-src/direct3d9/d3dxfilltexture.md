---
description: 使用使用者提供的函式來填滿給定材質之每個 mip 層級的每個材質。
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: 'D3DXFillTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28df3b7396ea0c34c39a87d2285f565f25d6ff6dc89dcfb8613890e79c4c5cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849768"
---
# <a name="d3dxfilltexture-function"></a>D3DXFillTexture 函式

使用使用者提供的函式來填滿給定材質之每個 mip 層級的每個材質。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，代表填滿的材質。

</dd> <dt>

*pFunction* \[在\]
</dt> <dd>

類型： **[LPD3DXFILL2D](lpd3dxfill2d.md)**

使用者提供的評估工具函式的指標，該函式將用來計算每個材質的值。 函數會遵循 [LPD3DXFILL2D](lpd3dxfill2d.md)的原型。

</dd> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

使用者定義資料之任意區塊的指標。 此指標會傳遞至 *pFunction* 中提供的函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

以下範例會建立一個名為 ColorFill 的函式，該函式依賴 D3DXFillTexture。


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
