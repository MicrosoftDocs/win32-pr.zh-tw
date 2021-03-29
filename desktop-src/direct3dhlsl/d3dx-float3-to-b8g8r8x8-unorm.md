---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM 函式
description: 將指定的 XMFLOAT3 封裝成 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM UINT。
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992207"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a>D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM function

將指定的 XMFLOAT3 封裝成 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM UINT。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*unpackedInput* 
</dt> <dd>

解壓縮的著色器資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

封裝的著色器資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. .inl</dt> </dl> |



## <a name="see-also"></a>請參閱

<dl> <dt>

[函式](format-conversion-functions.md)
</dt> <dt>

[\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





