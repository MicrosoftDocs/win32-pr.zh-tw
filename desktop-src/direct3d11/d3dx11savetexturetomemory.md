---
title: 'D3DX11SaveTextureToMemory 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫，CaptureTexture 接著 SaveToXXXMemory (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 將材質儲存至記憶體。
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196370"
---
# <a name="d3dx11savetexturetomemory-function"></a>D3DX11SaveTextureToMemory 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用這個函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫， **CaptureTexture** 接著 **SAVETOXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。

 

將材質儲存至記憶體。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pContext* 
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。

</dd> <dt>

*pSrcTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

要儲存的材質指標。 請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。

</dd> <dt>

*DestFormat* \[在\]
</dt> <dd>

類型： **[ **D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)**

材質將儲存成的格式。 請參閱 [**D3DX11 \_ 影像檔案 \_ \_ 格式**](d3dx11-image-file-format.md)。

</dd> <dt>

*ppDestBuf* \[擴展\]
</dt> <dd>

類型： **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

包含已儲存材質之記憶體的指標位址。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

選擇性。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

