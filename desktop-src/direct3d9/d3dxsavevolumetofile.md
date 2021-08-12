---
description: 將磁片區儲存到磁片上的檔案。
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: 'D3DXSaveVolumeToFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e6c5a03f9e1874d7706ecbf43cfd312abc472b8e7127ba9f21a35313374157b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524443"
---
# <a name="d3dxsavevolumetofile-function"></a>D3DXSaveVolumeToFile 函式

將磁片區儲存到磁片上的檔案。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDestFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

字串的指標，指定目的地影像的檔案名。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*DestFormat* \[在\]
</dt> <dd>

類型： **[ **D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_>FILEFORMAT**](./d3dximage-fileformat.md) 指定儲存時要使用的檔案格式。 此函數支援儲存至所有 **D3DXIMAGE \_ >fileformat** 格式，但便攜 Pixmap ( Ppm) 和 Targa/Truevision 圖形介面卡 (. tga) 。

</dd> <dt>

*pSrcVolume* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

[**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)介面的指標，其中包含要儲存的影像。

</dd> <dt>

*pSrcPalette* \[在\]
</dt> <dd>

Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，其中包含256色彩的調色板。 此參數可以是 **Null**。

</dd> <dt>

*pSrcBox* \[在\]
</dt> <dd>

Type： **Const [**D3DBOX**](d3dbox.md) \***

[**D3DBOX**](d3dbox.md)結構的指標。 指定 [來源] 方塊。 將此參數設定為 **Null** ，以指定整個磁片區。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXSaveVolumeToFileW。 否則，函式呼叫會解析為 >D3DXSaveVolumeToFileA，因為正在使用 ANSI 字串。

此函式會處理壓縮材質格式的轉換。

如果磁片區是 nondynamic (因為在建立) 將 usage 參數設定為0，並位於視訊記憶體 (記憶體集區設定為 D3DPOOL \_ 預設) 時， [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) 將會失敗，因為 D3DX 無法鎖定位於視訊記憶體中的 nondynamic 磁片區。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
