---
title: D3DX_R8G8B8A8_SINT_to_INT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ 聖著色器資料到 XMINT4。
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- D3DX_R8G8B8A8_SINT_to_INT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116245"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a>D3DX \_ R8G8B8A8 \_ 聖 \_ 至 \_ INT4 函式

解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ 聖著色器資料到 XMINT4。

## <a name="syntax"></a>語法

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
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

 

 





