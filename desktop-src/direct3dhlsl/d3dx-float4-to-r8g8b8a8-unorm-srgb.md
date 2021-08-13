---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB 函式
description: 將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB。
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e930935e34ff1aa76c99949949e12b5c57254eeea59262cf2ec7828482965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516276"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a>D3DX \_ FLOAT4 \_ 到 \_ R8G8B8A8 \_ UNORM \_ SRGB 函數

將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*unpackedInput* 
</dt> <dd>

要封裝的著色器資料。

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

 

 





