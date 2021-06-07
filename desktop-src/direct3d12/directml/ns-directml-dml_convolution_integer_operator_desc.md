---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: 使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在整數資料上執行向前卷積。
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417311"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>DML_CONVOLUTION_INTEGER_OPERATOR_DESC 結構 (directml .h) 

使用 *InputTensor* 執行 *FilterTensor* 的卷積。 這個運算子會在整數資料上執行向前卷積。 選擇性的零點張量也可以用來從輸入和篩選 tensor 減去零點值。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
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

包含輸入資料的 tensor。 *InputTensor* 的預期維度是 `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` 。


`InputZeroPointTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入零點資料的選擇性 tensor。 *InputZeroPointTensor* 的預期維度是 `{ 1, 1, 1, 1 }` 。


`FilterTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選資料的 tensor。 *FilterTensor* 的預期維度是 `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` 。


`FilterZeroPointTensor`

類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含篩選零點資料的選擇性 tensor。  `{ 1, 1, 1, 1 }` 如果需要每個 tensor 量化，或 `{ 1, OutputChannelCount, 1, 1 }` 需要每個通道的量化，FilterZeroPointTensor 的預期維度是。


`OutputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

要寫入結果的 tensor。 *OutputTensor* 的預期維度是 `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` 。


`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

卷積運算的空間維度數目。 空間維度是卷積 *FilterTensor* 的較低維度。 此值也會決定進展、 *Dilations*、 *StartPadding* 和 *EndPadding* *陣列的大小*。 唯一支援的值為2。


`Strides`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

陣列，包含卷積運算的進展。 這些進展適用于卷積篩選。 它們與 [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)中包含的 tensor 進步不同。


`Dilations`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

陣列，包含卷積運算的 dilations。 Dilations 是套用至篩選核心元素的進展。 這有藉由以零填補內部篩選核心元素來模擬較大的篩選核心效果。


`StartPadding`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

陣列，包含要套用至卷積作業之篩選和輸入 tensor 的每個空間維度開頭的填補值。


`EndPadding`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

陣列，包含要套用至卷積作業之篩選和輸入 tensor 的每個空間維度結尾的填補值。


`GroupCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

要將卷積作業劃分成的群組數目。 *GroupCount* 可以用來設定等於輸入通道計數的 *GroupCount* ，以達成深度的卷積。 這會將每個輸入通道的卷積分割為不同的卷積。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_2_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
* *FilterTensor* 和 *FilterZeroPointTensor* 必須有相同的 *資料類型*。
* *InputTensor* 和 *InputZeroPointTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 維度 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | 輸入 | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | INT8、UINT8 |
| InputZeroPointTensor | 選擇性輸入 | {1，1，1，1} | 4 | INT8、UINT8 |
| FilterTensor | 輸入 | { FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth } | 4 | INT8、UINT8 |
| FilterZeroPointTensor | 選擇性輸入 | {1，FilterZeroPointChannelCount，1，1} | 4 | INT8、UINT8 |
| OutputTensor | 輸出 | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | INT32 |



## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |