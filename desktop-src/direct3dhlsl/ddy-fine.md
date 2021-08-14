---
title: ddy_fine 函式
description: 計算相對於螢幕空間 x 座標的高精確度部分衍生。 |ddy_fine 函式
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- ddy_fine 函式 HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b59f7ac500658570b19bf932e3abb042f9ecd8e27b63458c25032704c9ba4e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285881"
---
# <a name="ddy_fine-function"></a>ddy \_ 精細函數

計算相對於螢幕空間 x 座標的高精確度部分衍生。

## <a name="syntax"></a>語法

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **float**

輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **float**

*值* 的高精確度部分衍生。

## <a name="remarks"></a>備註

您也可以使用下列多載版本：

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




