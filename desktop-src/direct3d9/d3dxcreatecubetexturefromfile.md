---
description: 從檔案建立 cube 紋理。
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: 'D3DXCreateCubeTextureFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981837"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a>D3DXCreateCubeTextureFromFile 函式

從檔案建立 cube 紋理。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。

</dd> <dt>

*pSrcFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

指定檔案名之字串的指標。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，字串資料類型會解析為 LPCSTR。 請參閱＜備註＞。

</dd> <dt>

*ppCubeTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 **D3DXCreateCubeTextureFromFileW**。 否則，函式呼叫會解析為 **D3DXCreateCubeTextureFromFileA** ，因為正在使用 ANSI 字串。

函數相當於 D3DXCreateCubeTextureFromFileEx (pDevice、pSrcFile、D3DX \_ DEFAULT、D3DX \_ DEFAULT、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppCubeTexture) 。

此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。 請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。

請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。 從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。

篩選會自動套用至使用這個方法所建立的材質。 篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。

**D3DXCreateCubeTextureFromFile** 會使用 DirectDraw 介面 (DDS) 檔案格式。 [DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。 您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3DXCreateCubeTextureFromFileEx**](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
