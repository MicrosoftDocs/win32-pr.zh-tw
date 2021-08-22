---
title: Texture2DMS：： sample。Operator 函數
description: 在提供的位置和樣本索引上，抓取資源的值。 |Texture2DMS：： sample。Operator 函數
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
keywords:
- 樣品。運算子函式 HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5d7082ee72c49d3aa4be131491151b1bab65502e6fe85884b2a03573c497b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508470"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS：： sample。Operator 函數

在提供的位置和樣本索引上，抓取資源的值。

## <a name="syntax"></a>語法

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*sampleSlice* \[在\]
</dt> <dd>

類型： **uint**

範例配量索引。

</dd> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint2**

索引位置。 元件包含 (x，y) 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

### <a name="usage-example"></a>使用範例


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




