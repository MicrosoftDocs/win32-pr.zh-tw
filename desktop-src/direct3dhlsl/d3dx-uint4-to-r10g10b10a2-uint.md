---
title: D3DX_UINT4_to_R10G10B10A2_UINT 函式
description: 將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R10G10B10A2 \_ UINT。
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- D3DX_UINT4_to_R10G10B10A2_UINT 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc7076b9e44ab1491bb8abbf8d4edb82158282c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992194"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a>D3DX \_ UINT4 \_ to \_ R10G10B10A2 \_ UINT 函數

將指定的 XMINT4 重新封裝回 DXGI \_ 格式 \_ R10G10B10A2 \_ UINT。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
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

 

 





