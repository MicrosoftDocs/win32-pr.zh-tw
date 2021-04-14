---
title: D3DX_FLOAT2_to_R16G16_FLOAT 函式
description: 將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ FLOAT。
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- D3DX_FLOAT2_to_R16G16_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849eb4dde5ab11e98675a1581519aabbeeb1e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992130"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a>D3DX \_ FLOAT2 \_ 到 \_ R16G16 \_ FLOAT 函數

將指定的 XMFLOAT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ FLOAT。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
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

 

 





