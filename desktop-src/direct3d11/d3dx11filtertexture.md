---
title: 'D3DX11FilterTexture 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 DirectXTex 程式庫 GenerateMipMaps 和 GenerateMipMaps3D。 使用特定的材質篩選器產生 mipmap 鏈。
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- D3DX11FilterTexture 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 728f76a28a2d97d3e6789a35c2f375d964d331c607c7570e44aa44a17ccbaa8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124693"
---
# <a name="d3dx11filtertexture-function"></a>D3DX11FilterTexture 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用此函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 **GenerateMipMaps** 和 **GenerateMipMaps3D**。

 

使用特定的材質篩選器產生 mipmap 鏈。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pContext* 
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>Id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。

</dd> <dt>

*pTexture* 
</dt> <dd>

類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

要篩選的材質物件。 請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。

</dd> <dt>

*SrcLevel* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Mipmap 層級的資料會用來產生 mipmap 鏈的其餘部分。

</dd> <dt>

*MipFilter* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

旗標，控制每個 miplevel 的篩選方式 (或 D3DX11 \_ D3DX11 \_ 篩選線性) 的預設值 \_ 。 請參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md)標。

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

 

