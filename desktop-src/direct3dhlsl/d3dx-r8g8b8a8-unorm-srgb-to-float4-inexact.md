---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT4。 |D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact 函式
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ede0d10bd8c90514771fa6520eb41e0bd555a3d969b230bb2932665ec0c81796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727343"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4 不 \_ 精確的函式

解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT4。

## <a name="syntax"></a>語法

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

此函式會使用沒有足夠精確度的著色器指令來提供確切的答案。 替代函式 [**D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) 會使用儲存在著色器中的查閱資料表，提供確切的 SRGB 給 float 轉換。

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

 

 





