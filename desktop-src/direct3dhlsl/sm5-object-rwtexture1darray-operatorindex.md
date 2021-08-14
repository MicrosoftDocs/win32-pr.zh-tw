---
title: RWTexture1DArray：： Operator 函數
description: 傳回資源變數。 |RWTexture1DArray：： Operator 函數
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
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
ms.openlocfilehash: 2e0735e3d9945d15c2f8473155612a40cbf652349eb531f089f5a4aa44451484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509280"
---
# <a name="rwtexture1darrayoperator--function"></a>RWTexture1DArray：： Operator 函數

傳回資源變數。

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

資源變數。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




