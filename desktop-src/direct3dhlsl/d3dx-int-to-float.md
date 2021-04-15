---
title: D3DX_INT_to_FLOAT 函式
description: 將 INT 值轉換為 FLOAT。
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974695"
---
# <a name="d3dx_int_to_float-function"></a>D3DX \_ INT \_ 至 \_ FLOAT 函數

將 INT 值轉換為 FLOAT。

## <a name="syntax"></a>語法

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
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

已轉換的 int 值。

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

 

 





