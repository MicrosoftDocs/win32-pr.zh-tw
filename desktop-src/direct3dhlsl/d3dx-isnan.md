---
title: D3DX_IsNan 函式
description: 判斷值是否為 NaN (不是) 的數位。
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946230"
---
# <a name="d3dx_isnan-function"></a>D3DX \_ IsNan 函式

判斷值是否為 NaN (不是) 的數位。

## <a name="syntax"></a>語法

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*\_V* 
</dt> <dd>

指定值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果是 NaN，則為 true;否則為 false。

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

 

 





