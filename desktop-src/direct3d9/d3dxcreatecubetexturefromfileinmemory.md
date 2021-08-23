---
description: 從記憶體中的檔案建立 cube 紋理。
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: 'D3DXCreateCubeTextureFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c39e3aa96445ddfd6e2aee9df90c16bf52aee6f70759eb310288276ff8b9531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631548"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a>D3DXCreateCubeTextureFromFileInMemory 函式

從記憶體中的檔案建立 cube 紋理。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
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

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

要建立立方體貼圖之記憶體中的檔案指標。 請參閱＜備註＞。

</dd> <dt>

*SrcDataSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

檔案在記憶體中的大小（以位元組為單位）。

</dd> <dt>

*ppCubeTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面指標的位址，表示已建立的 cube 紋理物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函數支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。 請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。

函數相當於 D3DXCreateCubeTextureFromFileInMemoryEx (pDevice、pSrcData、SrcDataSize、D3DX \_ default、D3DX \_ default、0、D3DFMT \_ UNKNOWN、D3DPOOL \_ MANAGED、D3DX \_ default、D3DX \_ default、0、 **null**、 **null**、ppCubeTexture) 。

請注意，從 IDirect3DDevice9 物件呼叫時，使用這個函式所建立的資源將會放置在 D3DPOOL MANAGED 所表示的記憶體類別中 \_ 。 從 IDirect3DDevice9Ex 物件呼叫這個方法時，資源會放在 D3DPOOL 預設值所表示的 memory 類別中 \_ 。

這個方法是設計用來載入儲存為 RT RCDATA 的影像檔 \_ ，這是應用程式定義的資源， (原始資料) 。 否則，此方法將會失敗。

篩選會自動套用至使用這個方法所建立的材質。 篩選相當於 \_ \_ \| \_ \_ 在 [D3DX \_ 篩選](d3dx-filter.md)中 D3DX 篩選三角形 D3DX 篩選遞色。

**D3DXCreateCubeTextureFromFileInMemory** 會使用 DirectDraw 介面 (DDS) 檔案格式。 [DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。 您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
