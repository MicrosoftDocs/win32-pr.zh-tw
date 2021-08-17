---
description: 從檔案建立紋理。
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: 'D3DXCreateTextureFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3ffce68a8044267e67d874412264d5a915c65b88ea5cc13b0cd8d2cd1400828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732157"
---
# <a name="d3dxcreatetexturefromfile-function"></a>D3DXCreateTextureFromFile 函式

從檔案建立紋理。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。

</dd> <dt>

*pSrcFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

指定檔案名之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*ppTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextureFromFileW。 否則，函式呼叫會解析為 D3DXCreateTextureFromFileA，因為正在使用 ANSI 字串。

此函數支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。 請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。

函數相當於 D3DXCreateTextureFromFileEx (pDevice、pSrcFile、D3DX \_ DEFAULT、D3DX \_ DEFAULT、D3DX \_ default、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppTexture) 。

Mipmapped 紋理會自動以載入的材質填滿每個層級。

將影像載入 mipmapped 材質時，某些裝置無法進入1x1 影像，而且此函式將會失敗。 如果發生這種情況，則必須以手動方式載入映射。

請注意，使用此函式建立的資源會放在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。

篩選會自動套用至使用這個方法所建立的材質。 篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。

若要在使用 **D3DXCreateTextureFromFile** 時獲得最佳效能：

1.  在載入時間進行映射調整和格式轉換可能會很慢。 以將使用的格式和解析度儲存影像。 如果目標硬體需要兩個維度的強大功能，請使用兩個維度的強大功能來建立和儲存影像。
2.  請考慮使用 DirectDraw 介面 (DDS) 檔。 因為 DDS 檔案可以用來代表任何 Direct3D 9 材質格式，所以很容易 D3DX 閱讀。 此外，他們也可以儲存 mipmap，讓任何 mipmap 產生的演算法都能用來撰寫映射。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
