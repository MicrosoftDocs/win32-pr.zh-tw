---
description: 從資源載入介面。
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: 'D3DXLoadSurfaceFromResource 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9aef57ec03066e8783f104282c770f1143c00b87fd0221b5c477ca5227fe398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095989"
---
# <a name="d3dxloadsurfacefromresource-function"></a>D3DXLoadSurfaceFromResource 函式

從資源載入介面。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
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

*hSrcModule* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](../winprog/windows-data-types.md)**

資源所在之模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組的 **Null** 。

</dd> <dt>

*pSrcResource* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

指定資源名稱之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*pSrcRect* \[在\]
</dt> <dd>

Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。 指定來源矩形。 將此參數設定為 **Null** ，以指定整個映射。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。

</dd> <dt>

*>Colorkey* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。 這一律是32位的 ARGB 色彩，與來源影像格式無關。 Alpha 是很重要的，而且通常會針對不透明的色彩索引鍵設定為 FF，因此，若為不透明的黑色，此值會等於0xFF000000。

</dd> <dt>

*pSrcInfo* \[in、out\]
</dt> <dd>

類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***

[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXLoadSurfaceFromResourceW。 否則，函式呼叫會解析為 D3DXLoadSurfaceFromResourceA，因為正在使用 ANSI 字串。

要載入的資源必須是 RT \_ 點陣圖或 rt RCDATA 類型 \_ 。 資源類型 RT \_ RCDATA 可用來載入點陣圖以外的格式 (例如 tga、.jpg 和 dds) 。

此函式會處理壓縮材質格式的轉換。

寫入至非層級零的介面並不會更新中途的矩形。 如果呼叫 [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在介面上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
