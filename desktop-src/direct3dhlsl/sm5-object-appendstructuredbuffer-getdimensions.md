---
title: AppendStructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |AppendStructuredBuffer：： GetDimensions 函數
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96f40417834b8e23a9e746e4e4e3df93b96c1fc2affc7cd9147842e389dc99d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790649"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>AppendStructuredBuffer：： GetDimensions 函數

取得資源維度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*numStructs* \[擴展\]
</dt> <dd>

類型： **uint**

結構的數目。

</dd> <dt>

*stride* \[擴展\]
</dt> <dd>

類型： **uint**

每個元素中的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




