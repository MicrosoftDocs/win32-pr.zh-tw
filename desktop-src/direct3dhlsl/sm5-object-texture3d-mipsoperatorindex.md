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
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195933"
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




