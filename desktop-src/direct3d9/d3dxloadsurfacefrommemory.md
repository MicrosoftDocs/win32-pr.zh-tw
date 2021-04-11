---
description: 從記憶體載入介面。
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: 'D3DXLoadSurfaceFromMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035332"
---
# <a name="d3dxloadsurfacefrommemory-function"></a>D3DXLoadSurfaceFromMemory 函式

從記憶體載入介面。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDestSurface* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標。 指定接收影像的目的地介面。

</dd> <dt>

*pDestPalette* \[在\]
</dt> <dd>

Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的目的地調色板或 **Null**。

</dd> <dt>

*pDestRect* \[在\]
</dt> <dd>

Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。 指定目的地矩形。 將此參數設定為 **Null** ，以指定整個表面。

</dd> <dt>

*pSrcMemory* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

記憶體中來源影像左上角的指標。

</dd> <dt>

*SrcFormat* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，也就是來源影像的像素格式。

</dd> <dt>

*SrcPitch* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

來源影像的音調（以位元組為單位）。 若為 DXT 格式，這個數位應該表示一列資料格的寬度（以位元組為單位）。

</dd> <dt>

*pSrcPalette* \[在\]
</dt> <dd>

Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，也就是256色彩的來源調色板或 **Null**。

</dd> <dt>

*pSrcRect* \[在\]
</dt> <dd>

Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。 指定記憶體中來源影像的維度。 此值不可以是 **Null**。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。

</dd> <dt>

*>colorkey* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。 這一律是32位的 ARGB 色彩，與來源影像格式無關。 Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。 因此，若是不透明的黑色，此值會等於0xFF000000。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

此函式會處理壓縮材質格式的轉換。

寫入至非層級零的介面並不會更新中途的矩形。 如果呼叫 **D3DXLoadSurfaceFromMemory** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
