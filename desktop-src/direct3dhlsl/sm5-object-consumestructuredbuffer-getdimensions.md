---
title: ConsumeStructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |ConsumeStructuredBuffer：： GetDimensions 函數
ms.assetid: 0710a4fb-23b0-4b19-b9ed-21bbb9874d33
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
ms.openlocfilehash: a204ed44c90c60b327ceb201037c6758763b3a05
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991882"
---
# <a name="consumestructuredbuffergetdimensions-function"></a>ConsumeStructuredBuffer：： GetDimensions 函數

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

每個元素的 stride （以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




