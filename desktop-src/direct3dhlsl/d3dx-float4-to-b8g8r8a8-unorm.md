---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM 函式
description: 將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM。
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056dc0e53c5467ef1bff43926da6fa7ca8e28b45ad247b2c4462147c666cdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371338"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a>D3DX \_ FLOAT4 \_ to \_ B8G8R8A8 \_ UNORM function

將指定的 XMFLOAT4 重新封裝回 DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM。

## <a name="syntax"></a>語法

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
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

 

 





