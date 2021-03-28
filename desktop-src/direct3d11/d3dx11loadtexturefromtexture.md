---
title: 'D3DX11LoadTextureFromTexture 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 DirectXTex 程式庫、調整大小、轉換、壓縮、解壓縮和/或 CopyRectangle。 從材質載入紋理。
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- D3DX11LoadTextureFromTexture 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974592"
---
# <a name="d3dx11loadtexturefromtexture-function"></a>D3DX11LoadTextureFromTexture 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用此函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫、重 **設大小**、 **轉換**、 **壓縮**、 **解壓縮** 和/或 **CopyRectangle**。

 

從材質載入紋理。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pContext* 
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。

</dd> <dt>

*pSrcTexture* 
</dt> <dd>

類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

來源紋理的指標。 請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。

</dd> <dt>

*pLoadInfo* 
</dt> <dd>

類型： **[ **D3DX11 \_ 材質 \_ 載入 \_ 資訊**](d3dx11-texture-load-info.md)\***

材質載入參數的指標。 請參閱 [**D3DX11 \_ 材質 \_ 載入 \_ 資訊**](d3dx11-texture-load-info.md)。

</dd> <dt>

*pDstTexture* 
</dt> <dd>

類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

目的地材質的指標。 請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。

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

 

 





