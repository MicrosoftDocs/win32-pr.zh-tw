---
title: 'InterlockedExchange 函式 (HLSL 參考) '
description: 將值指派給 dest，並傳回原始值。
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- InterlockedExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3880a85af5658d0d50eb079c2dd1fc300e6a4de4b7f606688ab9d7a317cf321c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511318"
---
# <a name="interlockedexchange-function-hlsl-reference"></a>InterlockedExchange 函式 (HLSL 參考) 

將值指派給 dest，並傳回原始值。

## <a name="syntax"></a>語法

``` syntax
void InterlockedExchange(
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

原始的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

這種作業只能對純量類型的資源和共用記憶體變數執行。 此函式有兩種可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會在 dest 所參考的共用記憶體暫存器上執行作業。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會在 dest 所參考的資源位置上執行作業。 只有當 R 可讀取和寫入時，才能使用此作業。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      |  x   | x      |  x       | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




