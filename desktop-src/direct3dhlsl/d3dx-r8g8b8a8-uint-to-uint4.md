---
title: D3DX_R8G8B8A8_UINT_to_UINT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT 著色器資料到 XMUINT4。
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- D3DX_R8G8B8A8_UINT_to_UINT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f97c46400f1ba08f1b9e72b867cb66fda37e7bb4cd3a2b2b871271a6858a4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286563"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a>D3DX \_ R8G8B8A8 \_ UINT \_ to \_ UINT4 function

解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT 著色器資料到 XMUINT4。

## <a name="syntax"></a>語法

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
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

 

 





