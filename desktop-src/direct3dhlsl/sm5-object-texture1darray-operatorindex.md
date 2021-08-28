---
title: Texture1DArray：： Operator 函數
description: 傳回唯讀的資源變數。 |Texture1DArray：： Operator 函數
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
keywords:
- 運算子函式 HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed214b4c4ccc55dfe6500f70659f4f81b2188de68b8cea7b5ba69c495108d730
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788348"
---
# <a name="texture1darrayoperator--function"></a>Texture1DArray：： Operator 函數

傳回唯讀的資源變數。

## <a name="syntax"></a>語法

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint2**

索引位置。 第一個元件包含 x 座標。 第二個元件表示所要的陣列配量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

這個方法一律會存取第一個 mip 層級。 若要指定其他 mip 層級，請改用 [**mip \[ \] \[ \] . operator**](sm5-object-texture1darray-mipsoperatorindex.md)方法。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




