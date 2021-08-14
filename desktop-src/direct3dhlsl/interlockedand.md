---
title: 'InterlockedAnd 函式 (HLSL 參考) '
description: 執行保證的不可部分完成和。
ms.assetid: 7dc5185a-ea37-493d-975d-dbb803c886d3
keywords:
- InterlockedAnd 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b058b5d235e04761c24ace1d6f1bb5cca1187f01d8fe0eb1a9d0178c036bf5f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511328"
---
# <a name="interlockedand-function-hlsl-reference"></a>InterlockedAnd 函式 (HLSL 參考) 

執行保證的不可部分完成和。

## <a name="syntax"></a>語法

``` syntax
void InterlockedAnd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*目的地* \[在\]
</dt> <dd>

類型： **R**

目的地位址。

</dd> <dt>

*值* \[在\]
</dt> <dd>

類型： **T**

輸入值。

</dd> <dt>

*原始 \_ 值* \[ 輸出\]
</dt> <dd>

類型： **T**

選擇性。 原始的輸入值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此作業只能在 int 或 uint 型別資源和共用記憶體變數上執行。 此函式有兩種可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器執行不可部分完成的值。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會針對 dest 所參考的資源位置執行不可部分完成的值。 多載函式有額外的輸出變數，其會設定為目的地的原始值。 只有在 R 可讀取和可寫入時，才能使用此多載作業。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




