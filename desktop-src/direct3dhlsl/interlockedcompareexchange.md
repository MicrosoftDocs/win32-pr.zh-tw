---
title: 'InterlockedCompareExchange 函式 (HLSL 參考) '
description: 以原子方式將目的地與比較值進行比較。 如果兩者相同，則會以輸入值覆寫目的地。 原始值會設定為目的地的原始值。
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- InterlockedCompareExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104990882"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a>InterlockedCompareExchange 函式 (HLSL 參考) 

以原子方式將目的地與比較值進行比較。 如果兩者相同，則會以輸入值覆寫目的地。 原始值會設定為目的地的原始值。

## <a name="syntax"></a>語法

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a>參數

<dl> <dt>

*目的地* \[在\]
</dt> <dd>

類型： **R**

目的地位址。

</dd> <dt>

*比較 \_ 值* \[\]
</dt> <dd>

類型： **T**

比較值。

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

以不可部分完成的方式，將 *dest* 所參考的值與 *compare \_ 值* 進行比較，如果值相符，則會將 *值* 儲存在 *dest* 所參考的位置中，並以 *原始 \_ 值* 傳回 *dest* 的原始值。 此作業只能在 **int** 或 **uint** 型別資源和共用記憶體變數上執行。 此函式有兩種可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會在 *dest* 所參考的共用記憶體暫存器上執行作業。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會在 *dest* 所參考的資源位置上執行作業。 只有當 R 可讀取和寫入時，才能使用此作業。

> [!Note]  
> 如果您在 [**for**](dx-graphics-hlsl-for.md)或 [**while**](dx-graphics-hlsl-while.md)計算著色器迴圈中呼叫 **InterlockedCompareExchange** ，以便正確編譯，您必須在該迴圈中使用 [ **\[ 允許 \_ uav \_ 條件 \]** ] 屬性。

 

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| x      |  x   |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




