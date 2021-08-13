---
title: D3DX_FLOAT_to_INT 函式
description: 將浮點值轉換為 INT。
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb76c5c459daaaba4dd7d038b65b9dc34e895f283b66545684ef1f5fb10c95cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516661"
---
# <a name="d3dx_float_to_int-function"></a>\_將 FLOAT D3DX \_ 至 \_ INT 函數

將浮點值轉換為 INT。

## <a name="syntax"></a>語法

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*\_V* 
</dt> <dd>

V 值。

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

 

 





