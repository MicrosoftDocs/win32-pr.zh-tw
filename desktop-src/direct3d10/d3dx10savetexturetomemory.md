---
description: 將材質儲存至記憶體。
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: 'D3DX10SaveTextureToMemory 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001789"
---
# <a name="d3dx10savetexturetomemory-function"></a>D3DX10SaveTextureToMemory 函式

將材質儲存至記憶體。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
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

材質將儲存成的格式。 請參閱 [**D3DX10 \_ 影像檔案 \_ \_ 格式**](d3dx10-image-file-format.md)。

</dd> <dt>

*ppDestBuf* \[擴展\]
</dt> <dd>

類型： **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

包含已儲存材質之記憶體的指標位址。 請參閱 [**ID3D10Blob 介面**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

選擇性。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

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

 

 
