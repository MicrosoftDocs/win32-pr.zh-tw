---
title: ConsumeStructuredBuffer：：取用函式
description: 從緩衝區的結尾移除值。
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- 使用函式 HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a76f8c27ed50c7d7eab1b37cd5c60257691b8db5e5af412f5b3bfe678c283bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486698"
---
# <a name="consume-function"></a>取用函式

從緩衝區的結尾移除值。

## <a name="syntax"></a>語法

``` syntax
T Consume(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

類型： **T**

 (移除的值可以是結構) 。

## <a name="remarks"></a>備註

T 可以是任何資料類型，包括結構。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




