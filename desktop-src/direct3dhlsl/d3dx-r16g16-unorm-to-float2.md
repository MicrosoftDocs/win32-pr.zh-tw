---
title: D3DX_R16G16_UNORM_to_FLOAT2 函式
description: 解壓縮 DXGI \_ FORMAT \_ R16G16 \_ UNORM 著色器資料至 XMFLOAT2。
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- D3DX_R16G16_UNORM_to_FLOAT2 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba4ca1bb02e66289ec66d0ec4f58978800f6538
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322799"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a>D3DX \_ R16G16 \_ UNORM \_ to \_ FLOAT2 function

解壓縮 DXGI \_ FORMAT \_ R16G16 \_ UNORM 著色器資料至 XMFLOAT2。

## <a name="syntax"></a>語法

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
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

 

 





