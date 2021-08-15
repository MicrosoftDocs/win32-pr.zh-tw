---
title: Buffer：： GetDimensions 函數
description: 取得緩衝區的長度。 |Buffer：： GetDimensions 函數
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: d7c56d673e533b4626a57669cf884d80da63d7848cfc7a3e248762f6c4f42088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986098"
---
# <a name="buffergetdimensions-function"></a>Buffer：： GetDimensions 函數

取得緩衝區的長度。

## <a name="syntax"></a>語法

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*dim* \[ out\]
</dt> <dd>

類型： **uint**

緩衝區的長度（以位元組為單位）。

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

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




