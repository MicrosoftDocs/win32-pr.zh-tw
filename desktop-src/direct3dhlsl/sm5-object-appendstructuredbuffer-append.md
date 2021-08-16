---
title: AppendStructuredBuffer：： Append 函數
description: 將值附加至緩衝區的結尾。
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- 附加函式 HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 863269c5127915af82b8ef82aa36b60b17941d8627b3f81a789f75618219c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725392"
---
# <a name="append-function"></a>Append 函數

將值附加至緩衝區的結尾。

## <a name="syntax"></a>語法

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

類型： **T**

輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

無

## <a name="remarks"></a>備註

T 可以是任何資料類型，包括結構。

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

 

 




