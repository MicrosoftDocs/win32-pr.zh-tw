---
title: reversebits 函式
description: 反轉每個元件的位順序。
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits 函式 HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9f055764c04f552fe9d7afda2adf1e401352cf3fc3dd3ead16c4ca6377bd4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853718"
---
# <a name="reversebits-function"></a>reversebits 函式

反轉每個元件的位順序。

## <a name="syntax"></a>語法

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **uint**

輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint**

輸入值，其位順序反轉。

## <a name="remarks"></a>備註

您也可以使用下列多載版本：

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




