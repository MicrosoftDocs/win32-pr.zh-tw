---
title: 'RWStructuredBuffer：:D ecrementCounter 函數 (Httpserv .h) '
description: 遞減物件的隱藏計數器。
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter 函式 HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974636"
---
# <a name="decrementcounter-function"></a>DecrementCounter 函式

遞減物件的隱藏計數器。

## <a name="syntax"></a>語法

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

類型： **uint**

減少後的計數器值。

## <a name="remarks"></a>備註

在 creationfor 此方法期間，系結的未排序存取視圖必須設定 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 計數器計數器**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) 。

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
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

 

