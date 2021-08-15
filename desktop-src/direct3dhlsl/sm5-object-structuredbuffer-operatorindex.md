---
title: StructuredBuffer：： Operator 函數
description: 傳回 StructuredBuffer 的唯讀資源變數。
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: c852a56769df2179daf6055542c9ebf4724a353312e295daecd59af08163711c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509114"
---
# <a name="structuredbufferoperator--function"></a>StructuredBuffer：： Operator 函數

傳回 [**StructuredBuffer**](sm5-object-structuredbuffer.md)的唯讀資源變數。

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

索引位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **R**

唯讀的資源變數。

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

 

 




