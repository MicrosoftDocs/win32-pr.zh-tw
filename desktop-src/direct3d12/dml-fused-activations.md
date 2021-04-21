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
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="e37e0-104">使用融合的運算子來改善效能</span><span class="sxs-lookup"><span data-stu-id="e37e0-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="e37e0-105">某些 DirectML 運算子支援稱為 *融合* 的概念。</span><span class="sxs-lookup"><span data-stu-id="e37e0-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="e37e0-106">運算子融合是一種改善效能的方法， (一般來說，啟動函式) 至不同的運算子，如此一來，就能在不需要往返記憶體的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="e37e0-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="e37e0-107">何時要進行保險絲</span><span class="sxs-lookup"><span data-stu-id="e37e0-107">When to fuse activations</span></span>

<span data-ttu-id="e37e0-108">融合的啟用是一種效能優化。</span><span class="sxs-lookup"><span data-stu-id="e37e0-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="e37e0-109">在許多機器學習服務 (ML) 模型中，非常常見的案例是將非線性 (啟用函式) 到模型中每個圖層的輸出。</span><span class="sxs-lookup"><span data-stu-id="e37e0-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="e37e0-110">通常，這需要對圖形記憶體的往返。</span><span class="sxs-lookup"><span data-stu-id="e37e0-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="e37e0-111">例如，如果卷積後面接著非融合式 Relu 啟用，則 GPU 必須等待卷積的結果寫入 GPU 記憶體，才能開始計算 Relu 啟用層。</span><span class="sxs-lookup"><span data-stu-id="e37e0-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="e37e0-112">因為大部分啟用函式的計算工作負載通常很小，所以這種對圖形記憶體的往返可能會造成重大的效能瓶頸。</span><span class="sxs-lookup"><span data-stu-id="e37e0-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="e37e0-113">運算子融合可讓上述範例中的啟動函式 (Relu) 要做為前一個運算子 (卷積的一部分來執行，例如) 。</span><span class="sxs-lookup"><span data-stu-id="e37e0-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="e37e0-114">這可讓 GPU 計算啟動函式，而不需等待上述運算子的結果寫入記憶體 &mdash; ，進而改善效能。</span><span class="sxs-lookup"><span data-stu-id="e37e0-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="e37e0-115">由於融合式啟用會產生相同的結果，但在許多情況下會更快，因此建議您盡可能將啟用層融合至其前面的運算子，以消除啟用層。</span><span class="sxs-lookup"><span data-stu-id="e37e0-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="e37e0-116">如何啟用保險絲</span><span class="sxs-lookup"><span data-stu-id="e37e0-116">How to fuse activations</span></span>

<span data-ttu-id="e37e0-117">支援融合啟用的運算子在其運算子結構中有額外的選擇性參數 `const DML_OPERATOR_DESC* FusedActivation` 。</span><span class="sxs-lookup"><span data-stu-id="e37e0-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="e37e0-118">例如，卷積支援融合的啟用，它的操作員描述中有對應的 *FusedActivation* (查看 [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="e37e0-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

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

<span data-ttu-id="e37e0-119">若要將啟用保險絲，請建立描述要融合之啟用類型的 [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) 。</span><span class="sxs-lookup"><span data-stu-id="e37e0-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="e37e0-120">例如，若要在 Relu 函式中保險絲，則會 [DML_OPERATOR_ACTI加值稅ION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type)正確的運算子類型。</span><span class="sxs-lookup"><span data-stu-id="e37e0-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="e37e0-121">當您針對啟用函式建立運算子描述時，您必須將啟用函式的 *InputTensor* 和 *OutputTensor* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e37e0-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="e37e0-122">範例</span><span class="sxs-lookup"><span data-stu-id="e37e0-122">Example</span></span>

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

<span data-ttu-id="e37e0-123">如需完整範例， [DirectMLSuperResolution 範例](https://github.com/microsoft/DirectML/tree/master/Samples) 會利用融合的啟用來改善效能。</span><span class="sxs-lookup"><span data-stu-id="e37e0-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="e37e0-124">支援融合啟用的運算子</span><span class="sxs-lookup"><span data-stu-id="e37e0-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="e37e0-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="e37e0-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="e37e0-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="e37e0-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="e37e0-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="e37e0-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="e37e0-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** 和 **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="e37e0-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="e37e0-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="e37e0-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="e37e0-130">支援融合的啟用</span><span class="sxs-lookup"><span data-stu-id="e37e0-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="e37e0-131">DML_OPERATOR_ACTI加值稅ION_ELU</span><span class="sxs-lookup"><span data-stu-id="e37e0-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="e37e0-132">**DML_OPERATOR_ACTI加值稅ION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="e37e0-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="e37e0-133">**DML_OPERATOR_ACTI加值稅ION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="e37e0-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="e37e0-134">**DML_OPERATOR_ACTI加值稅ION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="e37e0-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="e37e0-135">**DML_OPERATOR_ACTI加值稅ION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="e37e0-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="e37e0-136">**DML_OPERATOR_ACTI加值稅ION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="e37e0-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="e37e0-137">**DML_OPERATOR_ACTI加值稅ION_RELU**</span><span class="sxs-lookup"><span data-stu-id="e37e0-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="e37e0-138">**DML_OPERATOR_ACTI加值稅ION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="e37e0-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="e37e0-139">**DML_OPERATOR_ACTI加值稅ION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="e37e0-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="e37e0-140">**DML_OPERATOR_ACTI加值稅ION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="e37e0-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="e37e0-141">**DML_OPERATOR_ACTI加值稅ION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="e37e0-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="e37e0-142">**DML_OPERATOR_ACTI加值稅ION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="e37e0-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="e37e0-143">**DML_OPERATOR_ACTI加值稅ION_TANH**</span><span class="sxs-lookup"><span data-stu-id="e37e0-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="e37e0-144">**DML_OPERATOR_ACTI加值稅ION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="e37e0-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="e37e0-145">**DML_OPERATOR_ACTI加值稅ION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="e37e0-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="e37e0-146">**DML_OPERATOR_ACTI加值稅ION_CELU**</span><span class="sxs-lookup"><span data-stu-id="e37e0-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="e37e0-147">未在此清單中的任何運算子都不支援已融合的啟用。</span><span class="sxs-lookup"><span data-stu-id="e37e0-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="e37e0-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e37e0-148">See also</span></span>

* [<span data-ttu-id="e37e0-149">DirectMLSuperResolution 範例</span><span class="sxs-lookup"><span data-stu-id="e37e0-149">DirectMLSuperResolution sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [<span data-ttu-id="e37e0-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="e37e0-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
