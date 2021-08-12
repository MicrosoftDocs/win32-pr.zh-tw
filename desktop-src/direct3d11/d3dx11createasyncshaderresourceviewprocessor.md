---
title: 'D3DX11CreateAsyncShaderResourceViewProcessor 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- D3DX11CreateAsyncShaderResourceViewProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305705a4fd82b7f2267e3d56630b78c8c8d98473d946b1629e713162f4a6ae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536567"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a>D3DX11CreateAsyncShaderResourceViewProcessor 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。 請參閱＜備註＞。

 

建立會載入資源的資料處理器，然後為其建立著色器資源檢視。 資料處理器是 D3DX11 中使用 [**執行緒抽取**](id3dx11threadpump.md)的非同步資料載入功能的元件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Direct3D 裝置的指標 (請參閱將用來建立資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) ，以及該資源的著色器資源檢視。

</dd> <dt>

*pLoadInfo* \[在\]
</dt> <dd>

類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***

選擇性。 識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。

</dd> <dt>

*ppDataProcessor* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。

針對 Windows Store 應用程式，DirectX 範例 (例如， [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。

針對 Win32 傳統型應用程式，您可以使用[並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100))來執行類似于 Windows 執行階段非同步程式設計模型的內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11async。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

