---
title: D3DX_R8G8B8A8_UNORM_to_FLOAT4 函式
description: 解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM 著色器資料至 XMFLOAT4。 |D3DX_R8G8B8A8_UNORM_to_FLOAT4 函式
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4 函式 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e366478c12fdab5072a514b4ffea967b9a2b272c98e392fc4b7476ba81bc4efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793454"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ to \_ FLOAT4 function

解壓縮 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM 著色器資料至 XMFLOAT4。

## <a name="syntax"></a>語法

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
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

 

 





