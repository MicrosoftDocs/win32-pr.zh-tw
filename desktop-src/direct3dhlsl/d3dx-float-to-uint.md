---
title: D3DX_FLOAT_to_UINT 函式
description: 將浮點值轉換成 UINT。
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37665d3630979dee3fad7c109152a852883455f5de40c064faa8f1ea4f0645cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855618"
---
# <a name="d3dx_float_to_uint-function"></a>D3DX \_ FLOAT \_ 到 \_ UINT 函數

將浮點值轉換成 UINT。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*\_V* 
</dt> <dd>

V 向量。

</dd> <dt>

*\_調整* 
</dt> <dd>

比例值。

</dd> </dl>

## <a name="return-value"></a>傳回值

轉換的 FLOAT 值

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

 

 





