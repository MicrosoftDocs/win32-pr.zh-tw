---
description: 從檔案建立紋理。 這是比 D3DXCreateTextureFromFile 更先進的函式。
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: 'D3DXCreateTextureFromFileEx 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5964f7f466dac135d08958ef66c12a1dfe2e61a19180eb45072c5489f9f4a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299243"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>D3DXCreateTextureFromFileEx 函式

從檔案建立紋理。 這是比 [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)更先進的函式。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
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

*寬度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

寬度（以圖元為單位）。 如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度，並將其四捨五入為二的乘冪。 如果裝置支援2個材質的非電源，並指定 [D3DX \_ 預設 \_ NONPOW2](other-d3dx-constants.md) ，則不會將大小四捨五入。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

高度（以圖元為單位）。 如果這個值為零或 D3DX \_ 預設值，則會從檔案取得維度，並將其四捨五入為二的乘冪。 如果裝置支援2個材質的非電源，且 [D3DX \_ 預設 \_ NONPOW2](other-d3dx-constants.md) 為所以，則不會將大小四捨五入。

</dd> <dt>

*MipLevels* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要求的 mip 層級數目。 如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。 如果從檔案 D3DX \_ \_ ，大小會與檔案中的大小相同，而且如果這違反裝置功能，則呼叫會失敗。

</dd> <dt>

*使用* \[ 方式在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

0、 [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)或 **D3DUSAGE \_ DYNAMIC**。 將此旗標設定為 **D3DUSAGE \_ RENDERTARGET** 表示介面要當做轉譯目標使用。 然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api)方法的 *pNewRenderTarget* 參數。 如果指定了 **D3DUSAGE \_ RENDERTARGET** 或 **D3DUSAGE \_ DYNAMIC** ，則 *必須將集區* 設定為 D3DPOOL \_ 預設值，而應用程式應藉由呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項操作。 **D3DUSAGE \_DYNAMIC** 表示介面應該以動態方式處理。 請參閱 [使用動態紋理](performance-optimizations.md)。

</dd> <dt>

*格式* \[在\]
</dt> <dd>

類型： **[D3DFORMAT](d3dformat.md)**

[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。 傳回的材質可能與以 *格式* 指定的格式不同。 應用程式應該檢查傳回的材質格式。 如果 D3DFMT \_ 未知，就會從檔案中取得格式。 如果從檔案 D3DFMT \_ \_ ，格式會與檔案中的格式完全相同，而且如果這違反裝置功能，呼叫就會失敗。

</dd> <dt>

*集* \[ 區在\]
</dt> <dd>

類型： **[ **D3DPOOL**](./d3dpool.md)**

[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選](d3dx-filter.md) 常數的組合，可控制如何篩選影像。 指定此參數的 [D3DX \_ 預設值](other-d3dx-constants.md) ，相當於指定 D3DX \_ 篩選 \_ 三角形 \| D3DX \_ 篩選 \_ 遞色。

</dd> <dt>

*MipFilter* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [D3DX \_ 篩選](d3dx-filter.md) 常數的組合，可控制如何篩選影像。 指定 \_ 此參數的 D3DX 預設值，相當於指定 D3DX \_ 篩選方塊 \_ 。 此外，使用 bits 27-31 來指定當將 dds 材質載入至記憶體時， (從 mipmap 鏈頂端跳過的 mip 層級數目) 。這可讓您略過32層級。

</dd> <dt>

*>Colorkey* \[在\]
</dt> <dd>

類型： **[ **D3DCOLOR**](d3dcolor.md)**

要取代為透明黑色的 [**D3DCOLOR**](d3dcolor.md)值，否則為0以停用色彩索引鍵。 這一律是32位的 ARGB 色彩，與來源影像格式無關。 Alpha 是很重要的，而且通常會針對不透明色彩索引鍵設定為 FF。 因此，若是不透明的黑色，此值會等於0xFF000000。

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

*ppTexture* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

編譯器設定也會決定函式版本。 如果已定義 Unicode，函式呼叫會解析為 D3DXCreateTextureFromFileExW。 否則，函式呼叫會解析為 D3DXCreateTextureFromFileExA，因為正在使用 ANSI 字串。

使用 [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) 來判斷您的裝置是否可以支援指定目前狀態的材質。

此函數支援下列檔案格式： .bmp、dds、.dib、hdr、.jpg、pfm、.png、ppm 和. tga。 請參閱 [**D3DXIMAGE \_ >fileformat**](./d3dximage-fileformat.md)。

Mipmapped 紋理會自動以載入的材質填滿每個層級。 將影像載入 mipmapped 材質時，某些裝置無法進入1x1 影像，而且此函式將會失敗。 如果發生這種情況，則必須以手動方式載入映射。

若要在使用 **D3DXCreateTextureFromFileEx** 時獲得最佳效能：

1.  在載入時間進行映射調整和格式轉換可能會很慢。 以將使用的格式和解析度儲存影像。 如果目標硬體需要2個維度的電源，請使用2個維度的電源來建立和儲存影像。
2.  若要在載入期間建立 mipmap 映射，請 [使用 \_ D3DX \_ 篩選](d3dx-filter.md)方塊進行篩選。 Box 篩選比其他篩選器類型（例如 D3DX 濾波器三角形）更快 \_ \_ 。
3.  請考慮使用 DDS 檔。 由於 DDS 檔案可以用來代表任何 Direct3D 9 材質格式，因此很容易就能 D3DX 閱讀。 此外，他們也可以儲存 mipmap，讓任何 mipmap 產生的演算法都能用來撰寫映射。

在載入 dd 檔案時略過 mipmap 層級時，請使用 D3DX \_ SKIP \_ dds \_ MIP \_ 層級宏來產生 MipFilter 值。 此宏會接受要略過的層級數目和篩選準則類型，並傳回篩選值，然後將其傳遞至 MipFilter 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
