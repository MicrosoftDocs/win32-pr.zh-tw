---
title: 'RWStructuredBuffer：： IncrementCounter 函數 (Httpserv .h) '
description: 遞增物件的隱藏計數器。
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter 函式 HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39a857fc9a7a108cea05060caf86ce61479a382c5160f4f051c11423bc6a5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095168"
---
# <a name="incrementcounter-function"></a>IncrementCounter 函式

遞增物件的隱藏計數器。

## <a name="syntax"></a>語法

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

類型： **uint**

預先遞增的計數器值。

## <a name="remarks"></a>備註

系結的未排序存取視圖必須在建立期間設定 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 計數器計數器**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) ，才能讓此方法運作。

結構化資源可以根據結構的元件名稱進一步編制索引。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Httpserv。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

