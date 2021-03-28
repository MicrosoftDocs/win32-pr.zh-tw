---
title: RWBuffer：： GetDimensions 函數
description: 取得緩衝區的長度。 |RWBuffer：： GetDimensions 函數
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
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
ms.openlocfilehash: 98e419d3e77a27f211f0e063573caffcd6c61ce8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992066"
---
# <a name="rwbuffergetdimensions-function"></a>RWBuffer：： GetDimensions 函數

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

Nothing

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




