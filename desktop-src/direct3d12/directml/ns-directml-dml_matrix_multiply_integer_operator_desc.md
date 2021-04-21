---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: 在整數資料上執行矩陣乘法函數。
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802839"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC 結構 (directml .h) 
在整數資料上執行矩陣乘法函數。

此運算子要求矩陣乘以輸入張量為4D，格式為 `{ BatchCount, ChannelCount, Height, Width }` 。 矩陣乘法運算子將會執行 BatchCount * ChannelCount number of 獨立矩陣乘法運算。

例如，如果 *ATensor* 的 *大小* 為， `{ BatchCount, ChannelCount, M, K }` 且 *BTensor* *的大小* 為 `{ BatchCount, ChannelCount, K, N }` ，而 *OutputTensor* 的大小為， `{ BatchCount, ChannelCount, M, N }` 則矩陣乘法運算子將會執行 BatchCount * ChannelCount 獨立矩陣乘法運算的維度 {M，K} x {K，n} = {M，n}。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>成員

`ATensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含資料的 tensor。 此 tensor 的維度應該是 `{ BatchCount, ChannelCount, M, K }` 。


`AZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 ATensor 零點資料的選擇性 tensor。 `AZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, M, 1 }` 需要針對每個資料列的量化，則預期的維度為。 這些零點值是用來 dequantizing *ATensor* 值。


`BTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 B 資料的 tensor。 此 tensor 的維度應該是 `{ BatchCount, ChannelCount, K, N }` 。


`BZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 *BTensor* 零點資料的選擇性 tensor。 `BZeroPointTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, 1, 1, N }` 每個資料行的量化是必要的，則預期的維度為。 這些零點值是用來 dequantizing BTensor 值。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 這個 tensor 的維度是 `{ BatchCount, ChannelCount, M, N }` 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *ATensor* 和 `AZeroPointTensor` 必須具有相同的 *資料類型*。
* *BTensor* 和 `BZeroPointTensor` 必須具有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 維度 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | 輸入 | {BatchCount，ChannelCount，M，K} | 4 | INT8、UINT8 |
| AZeroPointTensor | 選擇性輸入 | {1，1，AZeroPointCount，1} | 4 | INT8、UINT8 |
| BTensor | 輸入 | {BatchCount，ChannelCount，K，N} | 4 | INT8、UINT8 |
| BZeroPointTensor | 選擇性輸入 | {1，1，1，BZeroPointCount} | 4 | INT8、UINT8 |
| OutputTensor | 輸出 | {BatchCount，ChannelCount，M，N} | 4 | INT32 |



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |