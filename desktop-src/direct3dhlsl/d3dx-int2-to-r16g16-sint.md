---
title: D3DX_INT2_to_R16G16_SINT 函式
description: 將指定的 XMINT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ 聖。
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974703"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a>D3DX \_ INT2 \_ to \_ R16G16 \_ 聖函數

將指定的 XMINT2 重新封裝回 DXGI \_ 格式 \_ R16G16 \_ 聖。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
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

 

 





