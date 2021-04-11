---
description: 從記憶體中的檔案建立 cube 紋理。 這是比 D3DXCreateCubeTextureFromFileInMemory 更先進的函式。
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: 'D3DXCreateCubeTextureFromFileInMemoryEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035416"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a>D3DXCreateCubeTextureFromFileInMemoryEx 函式

從記憶體中的檔案建立 cube 紋理。 這是比 [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md)更先進的函式。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
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

記憶體中要建立 cube 材質之檔案的指標。 請參閱＜備註＞。

</dd> <dt>

*SrcDataSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

檔案在記憶體中的大小（以位元組為單位）。

</dd> <dt>

*大小* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

寬度 (或高度) （以圖元為單位）。 如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要求的 mip 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。 將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。 然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。 如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。 如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述 cube 材質所要求的像素格式。 傳回的材質可能與以 *格式* 指定的格式不同。 應用程式應該檢查傳回的材質格式。 如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。 如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置 cube 材質的記憶體類別。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。

</dd> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合，可控制影像的篩選方式。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。 此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。

</dd> <dt>

*>colorkey* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。 這一律是32位的 ARGB 色彩，與來源影像格式無關。 Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。 因此，若是不透明的黑色，此值會等於0xFF000000。

</dd> <dt>

*pSrcInfo* \[in、out\]
</dt> <dd>

類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***

[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會以來源影像檔案中的資料描述來填滿，或為 **Null**。

</dd> <dt>

*pPalette* \[擴展\]
</dt> <dd>

類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。 請參閱＜備註＞。

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

此函式支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。 請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。

Cube 紋理不同于其他表面，因為它們是表面的集合。 若要使用 cube 材質來呼叫 [**SetRenderTarget**](/windows/desktop/api) ，您必須使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 選取個別臉部，並將產生的介面傳遞至 **SetRenderTarget** 。

這個方法是設計用來載入儲存為 RT RCDATA 的影像檔 \_ ，這是應用程式定義的資源， (原始資料) 。 否則，此方法將會失敗。

如需 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)的詳細資訊，請參閱 Platform SDK。 請注意，從 DirectX 8.0 起， **PALETTEENTRY** 結構的 peFlags 成員無法如 Platform SDK 中所述運作。 PeFlags 成員現在是8位調色盤格式的 Alpha 通道。

**D3DXCreateCubeTextureFromFileInMemoryEx** 會使用 DirectDraw 介面 (DDS) 檔案格式。 [DirectX 材質編輯器] (Dxtex.exe) 可讓您從其他檔案格式產生 cube 對應，並以 DDS 檔案格式儲存。 您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。 如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。

在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 MipFilter 值。 此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 MipFilter 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
