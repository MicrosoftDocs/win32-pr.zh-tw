---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 函式
description: 解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。 |D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 函式
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5f638d827a7b6ebf3543b3cde212fd56b0ace41ffb69bf4b7f79b56c28dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793854"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3 function

解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。

## <a name="syntax"></a>語法

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*packedInput* 
</dt> <dd>

封裝的著色器資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

解壓縮的著色器資料。

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

 

 





