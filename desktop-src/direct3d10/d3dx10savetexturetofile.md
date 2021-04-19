---
description: 將材質儲存至檔案。
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: 'D3DX10SaveTextureToFile 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985728"
---
# <a name="d3dx10savetexturetofile-function"></a>D3DX10SaveTextureToFile 函式

將材質儲存至檔案。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrcTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

要儲存的材質指標。 請參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。

</dd> <dt>

*DestFormat* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)**

材質儲存格式的格式 (參閱 [**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)) 。 D3DX10 \_ 如果 \_ DDS 是慣用的格式，因為它是唯一支援 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)格式的選項。

</dd> <dt>

*pDestFile* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

將儲存材質的目的地輸出檔名稱。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值;使用傳回值來查看是否支援 *DestFormat* 。

## <a name="remarks"></a>備註

**D3DX10SaveTextureToFile** 只會在必要時為輸入材質寫出額外的 [**DDS \_ 標頭 \_ DXT10**](../direct3ddds/dds-header-dxt10.md) 結構 (例如，因為輸入材質是在標準 RGB (sRGB) 格式) 。 如果 **D3DX10SaveTextureToFile** 寫出 **dds \_ 標頭 \_ DXT10** 結構，則會將材質 [**\_ PIXELFORMAT**](../direct3ddds/dds-pixelformat.md)結構的 **DwFourCC** 成員設定為 [ **DX10** ]，以指出 **DDS \_ 標頭 \_ prescense** 延伸標頭的 DXT10。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 10 中的材質函數](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
