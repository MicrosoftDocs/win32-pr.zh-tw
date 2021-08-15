---
title: RWTexture3D：： Operator 函數
description: 傳回 RWTexture3D 的資源變數。
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: 8db7073ef20976ecb6c39839d5639a1f0fcfe1fad765c2cf9b0ecdf086622b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509134"
---
# <a name="rwtexture3doperator--function"></a>RWTexture3D：： Operator 函數

傳回 [**RWTexture3D**](sm5-object-rwtexture3d.md)的資源變數。

## <a name="syntax"></a>語法

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*pos* \[在\]
</dt> <dd>

類型： **uint3**

索引位置。 包含 (x，y，z) 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

資源變數。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




