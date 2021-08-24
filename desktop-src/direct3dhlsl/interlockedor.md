---
title: 'InterlockedOr 函式 (HLSL 參考) '
description: 執行保證的不可部分完成或。
ms.assetid: ecbe6b2f-8eff-41d7-9ca3-4487c9ffeaf6
keywords:
- InterlockedOr 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c426237ec112a08fb7d422181a0efcd9ec0277d0628eda780492dae568ffaf38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854248"
---
# <a name="interlockedor-function-hlsl-reference"></a>InterlockedOr 函式 (HLSL 參考) 

執行保證的不可部分完成或。

## <a name="syntax"></a>語法

``` syntax
void InterlockedOr(
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

此作業只能在 int 或 uint 型別資源和共用記憶體變數上執行。 此函式有兩種可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器執行不可部分完成或值。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會針對 dest 所參考的資源位置執行不可部分完成或值。 多載函式有額外的輸出變數，其會設定為目的地的原始值。 只有在 R 可讀取和可寫入時，才能使用此多載作業。

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

 

 




