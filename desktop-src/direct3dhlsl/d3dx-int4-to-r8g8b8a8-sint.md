---
title: D3DX_INT4_to_R8G8B8A8_SINT 函式
description: 將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ 聖。
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- D3DX_INT4_to_R8G8B8A8_SINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992154"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a>D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ 聖函數

將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R8G8B8A8 \_ 聖。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
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

 

 





