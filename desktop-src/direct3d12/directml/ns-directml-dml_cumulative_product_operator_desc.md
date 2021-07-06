---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: 將 tensor 的元素乘以軸，並將執行中的產品計數寫入輸出 tensor 中。
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: cb4006a20dd25751c027ba97e63dcfc60c25faf6
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282557"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml) 

將 tensor 的元素乘以軸，並將執行中的產品計數寫入輸出 tensor 中。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入資料的 tensor。 這通常是在轉寄行程中提供作為 *InputTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。

包含要相乘之元素的輸入 tensor。

`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要將產生的累計產品寫入其中的輸出 tensor。 這個 tensor 的大小和資料類型必須與 *InputTensor* 相同。

`Axis`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

要將元素相乘的維度索引。 這個值必須小於 *InputTensor* 的 *DimensionCount* 。

`AxisDirection`

類型： **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)列舉的其中一個值。 如果設定為 **DML_AXIS_DIRECTION_INCREASING**，則會依指定的軸沿著遞增的元素索引來進行 tensor，以進行產品。 如果設定為 **DML_AXIS_DIRECTION_DECREASING**，則反向會是 true，而產品是藉由遞減索引來進行專案來進行。

`HasExclusiveProduct`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

若 **為 TRUE**，則將執行計數寫入至輸出 tensor 時，會排除目前元素的值。 如果 **為 FALSE**，則表示目前專案的值包含在執行中的計數內。

## <a name="examples"></a>範例

本節中的範例都使用相同的輸入 tensor。

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>範例 1. 跨水準薄片的累積乘積

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>範例 2. 專屬產品

將 *HasExclusiveProduct* 設為 **TRUE** ，會在寫入至輸出 tensor 時，從執行中的計數中排除目前專案的值。

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>範例 3. 軸方向

將 *AxisDirection* 設定為 [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) 具有在計算執行中計數時反轉專案的遍歷順序的效果。

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>範例4。 沿著不同的軸相乘

在此範例中，產品會垂直發生，而且高度軸 (第二個維度) 。

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>備註
這個運算子支援就地執行，這表示在系結期間允許輸出 tensor 別名 *InputTensor* 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputTensor* 和 *OutputTensor* 必須具有相同的 *資料類型*、 *DimensionCount* 和 *大小*。

## <a name="tensor-support"></a>Tensor 支援
### <a name="dml_feature_level_4_0-and-above"></a>DML_FEATURE_LEVEL_4_0 和更新版本
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、UINT32、UINT16 |
| OutputTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、UINT32、UINT16 |

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 和更新版本
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | FLOAT32、FLOAT16、UINT32、UINT16 |
| OutputTensor | 輸出 | 4 | FLOAT32、FLOAT16、UINT32、UINT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |