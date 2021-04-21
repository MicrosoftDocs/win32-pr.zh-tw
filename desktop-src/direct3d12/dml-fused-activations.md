---
title: 使用融合的運算子來改善效能
description: 某些 DirectML 運算子支援稱為 *融合* 的概念。 運算子融合是一種改善效能的方法， (一般來說，啟動函式) 至不同的運算子，如此一來，就能在不需要往返記憶體的情況下執行。
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: bba4a9d0ef5c69976a5a344432bf82d31b00c0c7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803986"
---
# <a name="using-fused-operators-to-improve-performance"></a>使用融合的運算子來改善效能

某些 DirectML 運算子支援稱為 *融合* 的概念。 運算子融合是一種改善效能的方法， (一般來說，啟動函式) 至不同的運算子，如此一來，就能在不需要往返記憶體的情況下執行。

## <a name="when-to-fuse-activations"></a>何時要進行保險絲

融合的啟用是一種效能優化。 在許多機器學習服務 (ML) 模型中，非常常見的案例是將非線性 (啟用函式) 到模型中每個圖層的輸出。

通常，這需要對圖形記憶體的往返。 例如，如果卷積後面接著非融合式 Relu 啟用，則 GPU 必須等待卷積的結果寫入 GPU 記憶體，才能開始計算 Relu 啟用層。 因為大部分啟用函式的計算工作負載通常很小，所以這種對圖形記憶體的往返可能會造成重大的效能瓶頸。

運算子融合可讓上述範例中的啟動函式 (Relu) 要做為前一個運算子 (卷積的一部分來執行，例如) 。 這可讓 GPU 計算啟動函式，而不需等待上述運算子的結果寫入記憶體 &mdash; ，進而改善效能。

由於融合式啟用會產生相同的結果，但在許多情況下會更快，因此建議您盡可能將啟用層融合至其前面的運算子，以消除啟用層。

## <a name="how-to-fuse-activations"></a>如何啟用保險絲

支援融合啟用的運算子在其運算子結構中有額外的選擇性參數 `const DML_OPERATOR_DESC* FusedActivation` 。 例如，卷積支援融合的啟用，它的操作員描述中有對應的 *FusedActivation* (查看 [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)) 。

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

若要將啟用保險絲，請建立描述要融合之啟用類型的 [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) 。 例如，若要在 Relu 函式中保險絲，則會 [DML_OPERATOR_ACTI加值稅ION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type)正確的運算子類型。

> [!NOTE]
> 當您針對啟用函式建立運算子描述時，您必須將啟用函式的 *InputTensor* 和 *OutputTensor* 參數設定為 **Null**。

## <a name="example"></a>範例

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

如需完整範例， [DirectMLSuperResolution 範例](https://github.com/microsoft/DirectML/tree/master/Samples) 會利用融合的啟用來改善效能。

## <a name="operators-that-support-fused-activation"></a>支援融合啟用的運算子

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** 和 **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>支援融合的啟用

* [DML_OPERATOR_ACTI加值稅ION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTI加值稅ION_HARD_SIGMOID**
* **DML_OPERATOR_ACTI加值稅ION_IDENTITY**
* **DML_OPERATOR_ACTI加值稅ION_LEAKY_RELU**
* **DML_OPERATOR_ACTI加值稅ION_LINEAR**
* **DML_OPERATOR_ACTI加值稅ION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTI加值稅ION_RELU**
* **DML_OPERATOR_ACTI加值稅ION_SCALED_ELU**
* **DML_OPERATOR_ACTI加值稅ION_SCALED_TANH**
* **DML_OPERATOR_ACTI加值稅ION_SIGMOID**
* **DML_OPERATOR_ACTI加值稅ION_SOFTPLUS**
* **DML_OPERATOR_ACTI加值稅ION_SOFTSIGN**
* **DML_OPERATOR_ACTI加值稅ION_TANH**
* **DML_OPERATOR_ACTI加值稅ION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTI加值稅ION_SHRINK**
* **DML_OPERATOR_ACTI加值稅ION_CELU**

未在此清單中的任何運算子都不支援已融合的啟用。

## <a name="see-also"></a>另請參閱

* [DirectMLSuperResolution 範例](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
