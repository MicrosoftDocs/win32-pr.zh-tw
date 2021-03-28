---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact 函式
description: 解壓縮 DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT4。 |D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact 函式
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992131"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4 不 \_ 精確的函式

解壓縮 DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB 著色器資料至 XMFLOAT4。

## <a name="syntax"></a>語法

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

此函式會使用沒有足夠精確度的著色器指令來提供確切的答案。 替代函式 [**D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ to \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) 會使用儲存在著色器中的查閱資料表，提供確切的 SRGB 給 float 轉換。

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

 

 





