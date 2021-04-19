---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: 計算配量的反向傳播漸層 (請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)) 。
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 63ea67454965d976247c3cdd50aa183f6a676138
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106982132"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>DML_SLICE_GRAD_OPERATOR_DESC 結構 (directml .h) 

計算配量的反向傳播漸層 (請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)) 。

回想一下， [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) 會解壓縮輸入 tensor 的子領域。 由於 *InputGradientTensor* 的大小與對等 **DML_SLICE1_OPERATOR_DESC** 的 *輸出* 相同，因此這個運算子會產生與 **DML_SLICE1_OPERATOR_DESC***輸入* 相同大小的 *OutputGradientTensor* 。 配量的元素會傳播至輸出，而所有其他元素則會設定為0。

例如，請考慮從 tensor 中解壓縮下列元素的 **DML_SLICE1_OPERATOR_DESC** ：

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

如果提供的 *InputWindowOffsets* / *大小* / *與* 上述範例相同，則此運算子接著會執行下列轉換。

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> 此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)。 另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。

## <a name="syntax"></a>語法

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a>成員

`InputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

傳入的漸層 tensor。 這通常是從上一層的反向傳播輸出中取得。 一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)的 *輸出* 大小相同。

`OutputGradientTensor`

Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

包含 backpropagated 漸層的輸出 tensor。 一般來說，這個 tensor 的大小會和向前傳遞中對應 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)的 *輸入* 相同。

`DimensionCount`

類型： [ **UINT**](/windows/desktop/winprog/windows-data-types)

*InputWindowOffsets*、 *InputWindowSizes* 和 *InputWindowStrides* 陣列中的元素數目。 此值必須等於 *InputGradientTensor* 和 *OutputGradientTensor* 中提供的 *DimensionCount* 。

`InputWindowOffsets`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)中的 *InputWindowOffsets* 。

`InputWindowSizes`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)中的 *InputWindowSizes* 。

`InputWindowStrides`

類型： \_ 欄位 \_ 大小 \_ (DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types) * </b>

請參閱 [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)中的 *InputWindowStrides* 。

請注意，與 **DML_SLICE1_OPERATOR_DESC** 不同的是，此運算子需要非零的進步。 這是因為如果有零個 stride，則不明確的是輸入元素應對應至每個輸出元素，因此無法執行反向傳播。 如同 **DML_SLICE1_OPERATOR_DESC**，負的進展會沿著該軸翻轉輸入視窗的方向。

## <a name="availability"></a>可用性
這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。

## <a name="tensor-constraints"></a>Tensor 條件約束
*InputGradientTensor* 和 *OutputGradientTensor* 必須具有相同的 *資料類型* 和 *DimensionCount*。

## <a name="tensor-support"></a>Tensor 支援
| 張 | 類型 | 支援的維度計數 | 支援的資料類型 |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | 輸入 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |
| OutputGradientTensor | 輸出 | 1至8 | FLOAT32、FLOAT16、INT32、INT16、INT8、UINT32、UINT16、UINT8 |

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **標頭** | directml。h |