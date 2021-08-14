---
title: 'D3DX11UnsetAllDeviceObjects 函式 (D3DX11core) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 >id3d11devicecoNtext ClearState 方法。
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- D3DX11UnsetAllDeviceObjects 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e046bbb67cfaf5e13a22e5b704e202c21ebc8fa82dfde3a21fb83f09dfc3a345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535969"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>D3DX11UnsetAllDeviceObjects 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您使用 [**>id3d11devicecoNtext：： ClearState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) 方法，而不是使用此函數。

 

將所有資源的指標設為 **Null**，以移除裝置中的所有資源。 這應該會在應用程式關閉時呼叫。 這有助於確保當某個資源釋出所有資源時，都不會將這些資源系結至裝置。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtext* \[在\]
</dt> <dd>

類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

[**>Id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





