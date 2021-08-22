---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB 函式
description: 將指定的 XMFLOAT3 重新封裝回 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB。
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e74519248f84890f29ebe9e00e02c76bce63775e938b40468041218025b0a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371328"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a>D3DX \_ FLOAT3 \_ 到 \_ B8G8R8X8 \_ UNORM \_ SRGB 函數

將指定的 XMFLOAT3 重新封裝回 DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
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

 

 





