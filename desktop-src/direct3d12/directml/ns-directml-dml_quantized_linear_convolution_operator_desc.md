---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: 使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在量化資料上執行向前卷積。 這個運算子在數學上相當於 dequantizing 輸入、convolving，然後量化輸出。
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 4dd50d80dfe4ae60e3fe7e67124ef00bfbc7bf2b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803880"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC 結構 (directml .h) 
使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在量化資料上執行向前卷積。 這個運算子在數學上相當於 dequantizing 輸入、convolving，然後量化輸出。 

此運算子使用的量化線性函式是線性量化函數

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
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入資料的 tensor。 *InputTensor* 的預期維度是 `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` 。


`InputScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入小數位數資料的 tensor。 的預期維度 `InputScaleTensor` 是 `{ 1, 1, 1, 1 }` 。 此比例值是用來 dequantizing 輸入值。


`InputZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入零點資料的選擇性 tensor。 *InputZeroPointTensor* 的預期維度是 `{ 1, 1, 1, 1 }` 。 這個零點值是用來 dequantizing 輸入值。


`FilterTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選資料的 tensor。 *FilterTensor* 的預期維度是 `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` 。


`FilterScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選調整資料的 tensor。 `FilterScaleTensor` `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, OutputChannelCount, 1, 1 }` 需要每個通道量化，則預期的維度為。 此比例值是用來 dequantizing 篩選值。


`FilterZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選零點資料的選擇性 tensor。  `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, OutputChannelCount, 1, 1 }` 需要每個通道量化，FilterZeroPointTensor 的預期維度是。 這個零點值是用來 dequantizing 篩選值。


`BiasTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含偏差資料的 tensor。 偏差 tensor 是一種 tensor，其中包含的資料會在已新增至結果的卷積結尾的輸出 tensor 之間進行廣播。 BiasTensor 的預期維度是 `{ 1, OutputChannelCount, 1, 1 }` 為4d。


`OutputScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸出小數位數資料的 tensor。 OutputScaleTensor 的預期維度是 `{ 1, 1, 1, 1 }` 。 此輸入小數位數值可用來量化卷積輸出值。


`OutputZeroPointTensor`

Type： _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選零點資料的選擇性 tensor。 OutputZeroPointTensor 的預期維度是 `{ 1, 1, 1, 1 }` 。 這個輸入的零點值是用來量化輸出值的卷積。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 OutputTensor 的預期維度是 `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` 。


`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

卷積運算的空間維度數目。 空間維度是卷積篩選 tensor *FilterTensor* 的較低維度。 此值也會決定進展、 *Dilations*、 *StartPadding* 和 *EndPadding* *陣列的大小*。 唯一支援的值為2。


`Strides`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

積運算的進展。 這些進展適用于卷積篩選。 它們與 [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)中包含的 tensor 進步不同。


`Dilations`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

卷積運算的 Dilations。 Dilations 是套用至篩選核心元素的進展。 這有藉由以零填補內部篩選核心元素來模擬較大的篩選核心效果。


`StartPadding`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

要套用至卷積運算之篩選和輸入 tensor 的每個空間維度開頭的填補值。


`EndPadding`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***

要套用至卷積運算之篩選和輸入 tensor 的每個空間維度結尾的填補值。


`GroupCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

要將卷積作業分割成的群組數目。 *GroupCount* 可以用來設定等於輸入通道計數的 *GroupCount* ，以達成深度的卷積。 這會將每個輸入通道的卷積分割為不同的卷積。 

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *FilterTensor* 和 *FilterZeroPointTensor* 必須有相同的 *資料類型*。
* *InputTensor* 和 *InputZeroPointTensor* 必須有相同的 *資料類型*。
* *OutputTensor* 和 `OutputZeroPointTensor` 必須具有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 4 | INT8、UINT8 |
| InputScaleTensor | 輸入 | 4 | FLOAT32 |
| InputZeroPointTensor | 選擇性輸入 | 4 | INT8、UINT8 |
| FilterTensor | 輸入 | 4 | INT8、UINT8 |
| FilterScaleTensor | 輸入 | 4 | FLOAT32 |
| FilterZeroPointTensor | 選擇性輸入 | 4 | INT8、UINT8 |
| BiasTensor | 選擇性輸入 | 4 | INT32 |
| OutputScaleTensor | 輸入 | 4 | FLOAT32 |
| OutputZeroPointTensor | 選擇性輸入 | 4 | INT8、UINT8 |
| OutputTensor | 輸出 | 4 | INT8、UINT8 |



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |