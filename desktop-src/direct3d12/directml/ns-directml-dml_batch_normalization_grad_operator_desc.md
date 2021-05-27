---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: 計算 [批次](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)正規化的反向傳播漸層。
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550433"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml) 

計算 [批次](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)正規化的反向傳播漸層。 **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** 會執行多個計算，其詳細說明請見個別的輸出描述。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.5 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>成員

`InputTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含輸入資料的 tensor。 這通常是在轉寄行程中提供作為 *InputTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。

`InputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

傳入的漸層 tensor。 這通常是從上一層的反向傳播輸出中取得。 此 tensor 的維度大小必須與 *InputTensor* 相同。

`MeanTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 mean 資料的 tensor。 這通常是在轉寄行程中提供作為 *MeanTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。

任何大小與 *InputTensor* 相對應的維度大小都不相同的維度，其大小必須為1，才能進行廣播以符合輸入。

例如，以下是可接受的大小。

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

下列是錯誤，因為若要進行廣播相容，任何不相符的維度都必須是大小1。

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含變異數資料的 tensor。 這通常是在轉寄行程中提供作為 *VarianceTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。 此 tensor 的維度大小必須與 *MeanTensor* 相同。

`ScaleTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含調整資料的 tensor。 這通常是在轉寄行程中提供作為 *ScaleTensor* [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) 的相同 tensor。 此 tensor 的維度大小必須與 *MeanTensor* 相同。

`OutputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

輸入中的每個對應值 `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` 。

此 tensor 的維度大小必須與 *InputTensor* / *InputGradientTensor* 相同。

`OutputScaleGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

此 tensor 的維度大小必須與 *MeanTensor* / *VarianceTensor* / *ScaleTensor '* 相同。

下列計算會完成，或輸入中的每個對應值。

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

`sum`會跨任何需要廣播的維度進行計算。 如果不需要廣播，則不需要加總。

以下為範例。

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

元素 [0， **0**，0，0] `OutputScaleGradientTensor` 是 `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 所有 90 (3 \* 5 \* 6) 元素 [[0，2]， **0**，[0，4]，[0，5]] 的總和。

`OutputBiasGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

此 tensor 的維度大小必須與 *MeanTensor* / *VarianceTensor* / *ScaleTensor '* 相同。

下列計算會完成，或輸入中的每個對應值。

`OutputBiasGradient = sum(InputGradient)`  

`sum`會跨任何需要廣播的維度來計算 (請參閱 *OutputScaleGradientTensor*) 的範例。 如果不需要廣播，則不需要加總。

`Epsilon`

類型： **[FLOAT](../../winprog/windows-data-types.md)**

加入至變異數的小值，以避免零。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_1` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputGradientTensor*、 *InputTensor*、 *MeanTensor*、 *OutputBiasGradientTensor*、 *OutputGradientTensor*、 *OutputScaleGradientTensor*、 *ScaleTensor* 和 *VarianceTensor* 必須有相同的 *資料類型* 和 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| InputGradientTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| MeanTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| VarianceTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| ScaleTensor | 輸入 | 1至8 | FLOAT32、FLOAT16 |
| OutputGradientTensor | 輸出 | 1至8 | FLOAT32、FLOAT16 |
| OutputScaleGradientTensor | 輸出 | 1至8 | FLOAT32、FLOAT16 |
| OutputBiasGradientTensor | 輸出 | 1至8 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |