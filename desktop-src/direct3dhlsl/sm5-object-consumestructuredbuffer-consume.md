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
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104022721"
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



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




