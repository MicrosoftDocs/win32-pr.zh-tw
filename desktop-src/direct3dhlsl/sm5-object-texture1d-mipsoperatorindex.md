---
title: Texture1D：： mips。Operator 函數
description: 傳回唯讀資源變數或 Texture1D。
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
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
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317068"
---
# <a name="texture1dmipsoperator----function"></a>Texture1D：： mips。Operator 函數

傳回唯讀資源變數或 [**Texture1D**](sm5-object-texture1d.md)。

## <a name="syntax"></a>語法

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
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

類型： **uint**

索引位置。 包含 x 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

### <a name="usage-example"></a>使用範例


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




