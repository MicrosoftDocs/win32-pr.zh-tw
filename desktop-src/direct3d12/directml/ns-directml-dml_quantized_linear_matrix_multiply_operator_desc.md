---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: 在量化資料上執行矩陣乘法函數。 這個運算子在數學上相當於 dequantizing 輸入，然後執行矩陣相乘，然後量化輸出。
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803570"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC 結構 (directml .h) 
在量化資料上執行矩陣乘法函數。 這個運算子在數學上相當於 dequantizing 輸入，然後執行矩陣相乘，然後量化輸出。

此運算子要求矩陣乘以輸入張量為4D，格式為 `{ BatchCount, ChannelCount, Height, Width }` 。 矩陣乘法運算子將會執行 BatchCount * ChannelCount number of 獨立矩陣乘法運算。 

例如，如果 *ATensor* 的 *大小* 為， `{ BatchCount, ChannelCount, M, K }` 且 *BTensor* *的大小* 為 `{ BatchCount, ChannelCount, K, N }` ，而 *OutputTensor* 的大小為， `{ BatchCount, ChannelCount, M, N }` 則矩陣乘法運算子將會執行 BatchCount * ChannelCount 獨立矩陣乘法運算的維度 {M，K} x {K，n} = {M，n}。 

### <a name="dequantize-function"></a>Dequantize 函式

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>量化函式

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>成員

`ATensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含資料的 tensor。 此 tensor 的維度應該是 `{ BatchCount, ChannelCount, M, K }` 。


`AScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 ATensor 規模資料的 tensor。 `AScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或需要個別的資料列量化，則預期的維度為 `{ 1, 1, M, 1 }` 。 這些刻度值是用來 dequantizing 值。


`AZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 *ATensor* 零點資料的選擇性 tensor。 `{ 1, 1, 1, 1 }`如果需要每個 tensor 量化，或需要個別的資料列量化，AZeroPointTensor 的預期維度是 `{ 1, 1, M, 1 }` 。 這些零點值是用來 dequantizing ATensor 值。


`BTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 B 資料的 tensor。 此 tensor 的維度應該是 `{ BatchCount, ChannelCount, K, N }` 。


`BScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 *BTensor* 規模資料的 tensor。 `BScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。 這些縮放值會用來 dequantizing *BTensor* 值。


`BZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 *BTensor* 零點資料的選擇性 tensor。 `BZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。 這些零點值是用來 dequantizing *BTensor* 值。


`OutputScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選調整資料的 tensor。 `OutputScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或需要個別的資料列量化，則預期的維度為 `{ 1, 1, M, 1 }` 。 此比例值是用來 dequantizing 篩選值。


`OutputZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選零點資料的選擇性 tensor。 `OutputZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, M, 1 }` 每個資料列的量化是必要的，則預期的維度為。 這個零點值是用來 dequantizing 篩選值。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 這個 tensor 的維度是 `{ BatchCount, ChannelCount, M, N }` 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *ATensor* 和 `AZeroPointTensor` 必須具有相同的 *資料類型*。
* *BTensor* 和 `BZeroPointTensor` 必須具有相同的 *資料類型*。
* *OutputTensor* 和 `OutputZeroPointTensor` 必須具有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | 輸入 | 4 | INT8、UINT8 |
| AScaleTensor | 輸入 | 4 | FLOAT32 |
| AZeroPointTensor | 選擇性輸入 | 4 | INT8、UINT8 |
| BTensor | 輸入 | 4 | INT8、UINT8 |
| BScaleTensor | 輸入 | 4 | FLOAT32 |
| BZeroPointTensor | 選擇性輸入 | 4 | INT8、UINT8 |
| OutputScaleTensor | 輸入 | 4 | FLOAT32 |
| OutputZeroPointTensor | 選擇性輸入 | 4 | INT8、UINT8 |
| OutputTensor | 輸出 | 4 | INT8、UINT8 |



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |