---
title: StructuredBuffer：： GetDimensions 函數
description: 取得資源維度。 |StructuredBuffer：： GetDimensions 函數
ms.assetid: 423ea79c-4440-4837-b637-95180a1d5019
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
ms.openlocfilehash: e63adbdca4813ee89b61fb9a88ab8bbffaf6f6caf50260ab68588f29b8828410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905599"
---
# <a name="structuredbuffergetdimensions-function"></a>StructuredBuffer：： GetDimensions 函數

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

資源中的結構數目。

</dd> <dt>

*stride* \[擴展\]
</dt> <dd>

類型： **uint**

每個結構元素的 stride （以位元組為單位）。

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

[StructuredBuffer](sm5-object-structuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




