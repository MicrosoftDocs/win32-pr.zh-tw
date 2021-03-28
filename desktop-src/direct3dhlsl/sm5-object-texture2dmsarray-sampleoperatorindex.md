---
title: Texture2DMSArray：： sample。Operator 函數
description: 傳回唯讀的資源變數。 |Texture2DMSArray：： sample。Operator 函數
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
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
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974380"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray：： sample。Operator 函數

傳回唯讀的資源變數。

## <a name="syntax"></a>語法

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
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

類型： **uint3**

索引位置。 第一個和第二個元件包含 (x，y) 座標。 第三個元件表示所要的陣列配量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

### <a name="usage-example"></a>使用範例


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




