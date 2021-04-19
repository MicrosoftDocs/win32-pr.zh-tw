---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: 計算重新取樣的反向傳播漸層 (請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)) 。
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106992629"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC 結構 (directml .h) 

計算重新取樣的反向傳播漸層 (請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)) 。

**DML_RESAMPLE1_OPERATOR_DESC** 使用最接近的鄰近取樣或雙線性插補，方式將輸入 tensor 的任意維度。 由於 *InputGradientTensor* 的大小與對等 **DML_RESAMPLE1_OPERATOR_DESC** 的 *輸出* 相同，因此這個運算子會產生與 **DML_RESAMPLE1_OPERATOR_DESC***輸入* 相同大小的 *OutputGradientTensor* 。

例如，假設有一個 **DML_RESAMPLE1_OPERATOR_DESC** ，其會在寬度中執行 1.5 x 的最接近鄰近比例，以及高度的 0.5 x。

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

請注意，輸入 tensor (值) 1 的第0個元素如何在輸出中提供兩個元素，第1個元素 (值 2) 會提供給輸出中的一個專案，而第二個和第三個元素（值3和4） (則不會構成輸出的元素。

對應的 **DML_RESAMPLE_GRAD_OPERATOR_DESC** 會執行下列動作。

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

請注意， *OutputGradientTensor* 中的值代表該元素在原始 **DML_RESAMPLE1_OPERATOR_DESC** 運算子期間對 *OutputTensor* 的加權貢獻。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>成員

`InputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

傳入的漸層 tensor。 這通常是從上一層的反向傳播輸出中取得。 一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)的 *輸出* 相同。

`OutputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 backpropagated 漸層的輸出 tensor。 一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)的 *輸入* 相同。

`InterpolationMode`

類型： [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *InterpolationMode* 。

`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

*刻度*、 *InputPixelOffsets* 和 *OutputPixelOffsets* 陣列中的元素數目。 此值必須等於 *InputGradientTensor* 和 *OutputGradientTensor* 中提供的 *DimensionCount* 。

`Scales`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types) \***

請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *刻度*。

`InputPixelOffsets`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types) \***

請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *InputPixelOffsets* 。

`OutputPixelOffsets`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types) \***

請參閱 [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)中的 *OutputPixelOffsets* 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputGradientTensor* 和 *OutputGradientTensor* 必須有相同的 *資料類型*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | 輸入 | 4 | FLOAT32、FLOAT16 |
| OutputGradientTensor | 輸出 | 4 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |