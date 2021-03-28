---
title: RWTexture1D：： Operator 函數
description: 傳回資源變數。 |RWTexture1D：： Operator 函數
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
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
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514401"
---
# <a name="rwtexture1doperator--function"></a>RWTexture1D：： Operator 函數

傳回資源變數。

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

資源變數。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




