---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact 函式
description: 解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。 |D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact 函式
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f696381402d8ad42c92310029631e66b457e3b211d22d8f9de3dd98c1f1312ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986868"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3 不 \_ 精確的函式

解壓縮 DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT3。

## <a name="syntax"></a>語法

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
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

## <a name="remarks"></a>備註

此函式會使用沒有足夠精確度的著色器指令來提供確切的答案。 替代函式 [**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) 會使用儲存在著色器中的查閱資料表，提供確切的 SRGB 給 float 轉換。

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

 

 





