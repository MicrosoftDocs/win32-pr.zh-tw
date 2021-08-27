---
description: 從檔案建立磁片區材質。 這是比 D3DXCreateVolumeTextureFromFileInMemory 更先進的函式。
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: 'D3DXCreateVolumeTextureFromFileInMemoryEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8e273cbdb8e65d751cad4679e7c8a38ec5de2ea2e7e6a62f59d396d44ead24a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119238"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a>D3DXCreateVolumeTextureFromFileInMemoryEx 函式

從檔案建立磁片區材質。 這是比 [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)更先進的函式。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。

</dd> <dt>

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

用來建立磁片區材質之記憶體中檔案的指標。

</dd> <dt>

*SrcDataSize* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

檔案在記憶體中的大小（以位元組為單位）。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

寬度（以圖元為單位）。 如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。 驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

高度（以圖元為單位）。 如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。 驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。

</dd> <dt>

*深度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

深度（以圖元為單位）。 如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度。 驅動程式支援 (寬度、高度和深度) 的最大維度可在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 MaxVolumeExtent 中找到。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要求的 mip 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

0、D3DUSAGE \_ RENDERTARGET 或 D3DUSAGE \_ DYNAMIC。 將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。 然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)方法的 *pNewRenderTarget* 參數。 如果 \_ 指定了 D3DUSAGE RENDERTARGET 或 D3DUSAGE \_ DYNAMIC，則必須將集區設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。 D3DUSAGE \_ DYNAMIC 表示介面應該以動態方式處理。 如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。 傳回的材質可能與以 *格式* 指定的格式不同。 應用程式應該檢查傳回的材質格式。 如果 [D3DFMT \_ 未知](other-d3dx-constants.md)，就會從檔案中取得格式。 如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。

</dd> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

用來控制如何篩選影像的一或多個 [D3DX \_ 篩選器](d3dx-filter.md) 的組合。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。 此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。

</dd> <dt>

*>Colorkey* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用 >colorkey。 這一律是32位的 ARGB 色彩，與來源影像格式無關。 Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。 因此，若是不透明的黑色，此值會等於0xFF000000。

</dd> <dt>

*pSrcInfo* \[in、out\]
</dt> <dd>

類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***

要填入的 [**D3DXIMAGE \_ 資訊**](d3dximage-info.md) 結構的指標，其中包含來源影像檔案中的資料描述或 **Null**。

</dd> <dt>

*pPalette* \[擴展\]
</dt> <dd>

類型： **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板或 **Null**。

</dd> <dt>

*ppVolumeTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面指標的位址，表示所建立的材質物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函數支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。 請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。

在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 *MipFilter* 值。 此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 *MipFilter* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
