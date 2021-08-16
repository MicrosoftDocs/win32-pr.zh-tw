---
title: asdouble 函式
description: 向量轉換值 (2 32 位值) 成為雙精度浮點數。
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- asdouble 函式 HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e191a2bf9ee7fb46337c3c7dfef7f8dea3525acf936ab745c07e7720f1ac509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626638"
---
# <a name="asdouble-function"></a>asdouble 函式

向量轉換值 (2 32 位值) 成為雙精度浮點數。

## <a name="syntax"></a>語法

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*lowbits* \[在\]
</dt> <dd>

類型： **uint**

輸入值的低32位模式。

</dd> <dt>

*highbits* \[在\]
</dt> <dd>

類型： **uint**

輸入值的高32位模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **double**

輸入 (2 32 位值) 重新轉換為雙精度浮點數。

## <a name="remarks"></a>備註

您也可以使用下列多載版本：

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

如果輸入值為 2 32 位元件，則傳回類型將會包含一個雙精度浮點數。 如果輸入值為 4 32 位元件，則傳回類型將包含兩個雙精度浮點數。 如果輸入值是64位型別，則傳回的值會與輸入值具有相同數目的元件。

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

 

 




