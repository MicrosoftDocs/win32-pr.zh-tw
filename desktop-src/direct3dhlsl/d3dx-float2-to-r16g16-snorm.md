---
title: D3DX_FLOAT2_to_R16G16_SNORM 函式
description: 將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ SNORM。
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946132"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ SNORM function

將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ SNORM。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
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

 

 





