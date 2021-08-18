---
title: D3DX_SRGB_to_FLOAT_inexact 函式
description: 將 SRGB 值轉換為 FLOAT。 |D3DX_SRGB_to_FLOAT_inexact 函式
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515689"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ SRGB \_ 至 \_ FLOAT 不 \_ 精確函式

將 SRGB 值轉換為 FLOAT。

## <a name="syntax"></a>語法

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*瓦爾* 
</dt> <dd>

要轉換的 SRGB 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

已轉換的 SRGB 值。

## <a name="remarks"></a>備註

這個函式的有效位數沒有足夠的精確度可提供確切的答案。 替代函式 [**D3DX \_ SRGB \_ 至 \_ float**](d3dx-srgb-to-float.md) 使用查閱資料表來提供精確的 SRGB 至 float 轉換。

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

 

 





