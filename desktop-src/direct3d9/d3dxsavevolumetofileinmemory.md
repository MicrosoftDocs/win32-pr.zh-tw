---
description: 將磁片區儲存到緩衝區。 方法會建立 ID3DXBuffer 緩衝區來儲存資料，並傳回該物件。
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: 'D3DXSaveVolumeToFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7c7326609d6d3c006f3c97aeff18de425a27569db63378864fc34335558117e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298401"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>D3DXSaveVolumeToFileInMemory 函式

將磁片區儲存到緩衝區。 方法會建立 [**ID3DXBuffer**](id3dxbuffer.md) 緩衝區來儲存資料，並傳回該物件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDestBuf* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

將儲存映射之 [**ID3DXBuffer**](id3dxbuffer.md) 緩衝區指標的位址。

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 9 中的材質函數](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
