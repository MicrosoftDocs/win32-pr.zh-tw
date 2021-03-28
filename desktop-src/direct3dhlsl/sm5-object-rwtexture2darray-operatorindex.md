---
title: RWTexture2DArray：： Operator 函數
description: 傳回資源變數。 |RWTexture2DArray：： Operator 函數
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035245"
---
# <a name="rwtexture2darrayoperator--function"></a>RWTexture2DArray：： Operator 函數

傳回資源變數。

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

索引位置。 第一個和第二個元件包含 (x，y) 座標。 第三個元件表示所要的陣列配量。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

資源變數。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWTexture2DArray](sm5-object-rwtexture2darray.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




