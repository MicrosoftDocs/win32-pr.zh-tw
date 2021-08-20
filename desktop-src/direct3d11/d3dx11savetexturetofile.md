---
title: 'D3DX11SaveTextureToFile 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫，CaptureTexture 接著 SaveToXXXFile (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 針對從呈現目標材質建立螢幕擷取畫面的簡化案例，建議您使用 DirectXTK 程式庫 SaveDDSTextureToFile 或 SaveWICTextureToFile。 將材質儲存至檔案。
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- D3DX11SaveTextureToFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74f73eaad167c7c813a8effe93b65ea7558514ae78ecc00926b420014f4a37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118099260"
---
# <a name="d3dx11savetexturetofile-function"></a>D3DX11SaveTextureToFile 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用這個函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫， **CaptureTexture** 接著 **SAVETOXXXFILE** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 針對從呈現目標材質建立螢幕擷取畫面的簡化案例，建議您使用 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SaveDDSTextureToFile** 或 **SaveWICTextureToFile**。

 

將材質儲存至檔案。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pContext* 
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>Id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。

</dd> <dt>

*pSrcTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

要儲存的材質指標。 請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。

</dd> <dt>

*DestFormat* \[在\]
</dt> <dd>

類型： **[ **D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)**

材質儲存格式的格式 (參閱 [**D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)) 。 D3DX11 \_ 如果 \_ DDS 是慣用的格式，因為它是唯一支援 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)格式的選項。

</dd> <dt>

*pDestFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

將儲存材質的目的地輸出檔名稱。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值;使用傳回值來查看是否支援 *DestFormat* 。

## <a name="remarks"></a>備註

**D3DX11SaveTextureToFile** 只會在必要時為輸入材質寫出額外的 [**DDS \_ 標頭 \_ DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) 結構 (例如，因為輸入材質是在標準 RGB (sRGB) 格式) 。 如果 **D3DX11SaveTextureToFile** 寫出 **dds \_ 標頭 \_ DXT10** 結構，則會將材質 [**\_ PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat)結構的 **DwFourCC** 成員設定為 [ **DX10** ]，以指出 **DDS \_ 標頭 \_ prescense** 延伸標頭的 DXT10。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

