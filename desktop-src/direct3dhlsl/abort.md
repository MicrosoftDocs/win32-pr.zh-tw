---
title: 'abort 函數 (Corecrt \_ terminate. h) '
description: 將錯誤訊息提交至資訊佇列，並終止目前正在執行的繪圖或分派呼叫。
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- abort 函式 HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974729"
---
# <a name="abort-function"></a>abort 函式

將錯誤訊息提交至資訊佇列，並終止目前正在執行的繪圖或分派呼叫。

## <a name="syntax"></a>語法

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>參數

<dl> <dt>

 
</dt> <dd>

None

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此作業不會在不支援的 rasterizers 上執行任何動作。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4 (DirectX HLSL) 或更新版本。](dx-graphics-hlsl-sm3.md) | 是       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Corecrt \_ terminate。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





