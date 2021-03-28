---
title: 'InterlockedCompareStore 函式 (HLSL 參考) '
description: 以不可部分完成的方式將目的地與比較值進行比較。 如果兩者相同，則會以輸入值覆寫目的地。
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104374231"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a>InterlockedCompareStore 函式 (HLSL 參考) 

以不可部分完成的方式將目的地與比較值進行比較。 如果兩者相同，則會以輸入值覆寫目的地。

## <a name="syntax"></a>語法

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
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

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

如果值相符，則以原子方式將 *dest* 所參考的值與 *dest* 所參考的位置 *值* 進行比較。 *\_* 此作業只能在 **int** 或 **uint** 型別資源和共用記憶體變數上執行。 此函式有兩種可能的用途。 第一個是當 R 是共用記憶體變數型別時。 在此情況下，此函式會在 *dest* 所參考的共用記憶體暫存器上執行作業。 第二個案例是 R 是資源變數類型。 在此案例中，此函式會在 *dest* 所參考的資源位置上執行作業。

### <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|  x     | x    |  x     |  x       | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[內建函式](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[著色器模型5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




