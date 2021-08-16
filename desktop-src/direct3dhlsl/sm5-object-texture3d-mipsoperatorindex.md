---
title: Texture3D：： mips。Operator 函數
description: 傳回唯讀的資源變數。 |Texture3D：： mips。Operator 函數
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
keywords:
- Mips。運算子函式 HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18ad563041c8ad0b601240f4353dad5bbc44ef418c267f72d07f0f753d12d993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724498"
---
# <a name="texture3dmipsoperator----function"></a>Texture3D：： mips。Operator 函數

傳回唯讀的資源變數。

## <a name="syntax"></a>語法

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*mipSlice* \[在\]
</dt> <dd>

類型： **uint**

Mip 配量索引。

</dd> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint3**

索引位置。 包含 (x，y，z) 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

### <a name="usage-example"></a>使用範例


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




