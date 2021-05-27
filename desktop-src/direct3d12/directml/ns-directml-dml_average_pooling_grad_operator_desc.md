---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: 計算平均共用 (的反向傳播梯度，請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)) 。
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550483"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a>DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC 結構 (directml .h) 

計算平均共用 (的反向傳播梯度，請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)) 。

請考慮採用 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**，但不含填補和1的跨距，以執行下列動作。

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

輸入 tensor 中的每個2x2 視窗平均是為了產生輸出的一個元素， (在邊緣) 以外的元素中讀取零。 以下是 **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** 指定類似參數的輸出範例。

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

請注意， *OutputGradientTensor* 中的值代表該元素在原始 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)運算子期間對 *OutputTensor* 的加權貢獻。

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a>成員

`InputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

傳入的漸層 tensor。 這通常是從上一層的反向傳播輸出中取得。 一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)的 *輸出* 相同。

`OutputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 backpropagated 漸層的輸出 tensor。 一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)的 *輸入* 相同。

`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

*進步*、 *WindowSize*、 *StartPadding* 和 *EndPadding* 陣列中的元素數目。 這個值必須等於空間維度計數。 如果提供4D 張量，則空間維度計數是2，如果提供了5D 張量，則為3。

`Strides`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *進步*。

`WindowSize`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *WindowSize* 。

`StartPadding`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *StartPadding* 。

`EndPadding`

類型： \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *EndPadding* 。

`IncludePadding`

類型： <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

請參閱 [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)中的 *IncludePadding* 。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputGradientTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 種類 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | 輸入 | 4到5 | FLOAT32、FLOAT16 |
| OutputGradientTensor | 輸出 | 4到5 | FLOAT32、FLOAT16 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |