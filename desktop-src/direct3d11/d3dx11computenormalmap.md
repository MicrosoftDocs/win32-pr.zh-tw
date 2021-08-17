---
title: 'D3DX11ComputeNormalMap 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫 ComputeNormalMap。
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747b8b01834126beb12e42d2fa26e15ea99c7471935af8ad74d078d15e9233ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124913"
---
# <a name="d3dx11computenormalmap-function"></a>D3DX11ComputeNormalMap 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用此函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 **ComputeNormalMap**。

 

將高度地圖轉換成一般地圖。 每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtext* \[在\]
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>Id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)介面的指標，代表來源的高度地圖材質。

</dd> <dt>

*pSrcTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)介面的指標，代表來源的高度地圖材質。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

\_控制正常對應產生的一或多個 D3DX NORMALMAP 旗標。

</dd> <dt>

*頻道* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

一個 D3DX \_ 通道旗標，指定高度資訊的來源。

</dd> <dt>

*振幅* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

常數值乘數，可增加 (或減少標準對應中的值) 。 較高的值通常會使凹凸變得更明顯，較低的值通常會讓顯示的偏低。

</dd> <dt>

*pDestTexture* \[在\]
</dt> <dd>

類型： **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)介面的指標，表示目的地材質。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這個方法會使用核心大小為3x3 的中央差異來計算正常。 目的地中的 RGB 通道包含一般 (x、y、z) 元件的偏誤。 中央差異分母會硬式編碼為2.0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11tex。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

