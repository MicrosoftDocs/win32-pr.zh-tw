---
description: 建立會載入資源的資料處理器，然後為其建立著色器資源檢視。 資料處理器是 D3DX10 中使用執行緒抽取的非同步資料載入功能的元件。
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: 'D3DX10CreateAsyncShaderResourceViewProcessor 函式 (D3DX10Async) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986535"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a>D3DX10CreateAsyncShaderResourceViewProcessor 函式

建立會載入資源的資料處理器，然後為其建立著色器資源檢視。 資料處理器是 D3DX10 中使用 [**執行緒抽取**](id3dx10threadpump.md)的非同步資料載入功能的元件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Direct3D 裝置的指標 (請參閱將用來建立資源的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) ，以及該資源的著色器資源檢視。

</dd> <dt>

*pLoadInfo* \[在\]
</dt> <dd>

類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***

選擇性。 識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。

</dd> <dt>

*ppDataProcessor* \[擴展\]
</dt> <dd>

類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Async。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般用途函數](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




