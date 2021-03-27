---
title: Texture2DMS：： GetSamplePosition 函數
description: 傳回所提供之範例索引的範例位置。
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- GetSamplePosition 函式 HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508272"
---
# <a name="texture2dmsgetsampleposition-function"></a>Texture2DMS：： GetSamplePosition 函數

傳回所提供之範例索引的範例位置。

## <a name="syntax"></a>語法

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*sampleindex* \[在\]
</dt> <dd>

類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**

範例位置以零為基底的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **float2**

範例位置。

## <a name="remarks"></a>備註

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
