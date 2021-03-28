---
title: Texture1D：： Operator 函數
description: 傳回 Texture1D 的唯讀資源變數。
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: 44e5b502c7ae8b766363956920d7922858b4d771
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093667"
---
# <a name="texture1doperator--function"></a>Texture1D：： Operator 函數

傳回 [**Texture1D**](sm5-object-texture1d.md)的唯讀資源變數。

## <a name="syntax"></a>語法

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint**

索引位置。 包含 x 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

## <a name="remarks"></a>備註

這個方法一律會存取第一個 mip 層級。 若要指定其他 mip 層級，請改用 [**mip \[ \] \[ \] . 運算子**](sm5-object-texture1d-mipsoperatorindex.md)。

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

 

 




