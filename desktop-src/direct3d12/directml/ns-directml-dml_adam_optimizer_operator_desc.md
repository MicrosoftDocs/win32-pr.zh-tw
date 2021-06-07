---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: 根據 Adam (**ADA** ptive **M** oment 估計) 演算法，使用提供的漸層來計算更新的加權 (參數) 。 這個運算子是優化工具，通常用於定型迴圈的加權更新步驟，以執行梯度下降。
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417346"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="dd47c-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="dd47c-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="dd47c-105">根據 Adam (**ADA** ptive **M** oment 估計) 演算法，使用提供的漸層來計算更新的加權 (參數) 。</span><span class="sxs-lookup"><span data-stu-id="dd47c-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="dd47c-106">這個運算子是優化工具，通常用於定型迴圈的加權更新步驟，以執行梯度下降。</span><span class="sxs-lookup"><span data-stu-id="dd47c-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="dd47c-107">這個運算子會執行下列計算：</span><span class="sxs-lookup"><span data-stu-id="dd47c-107">This operator performs the following computation:</span></span>

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

<span data-ttu-id="dd47c-108">除了計算 (在 *OutputParametersTensor*) 中傳回的更新權數參數之外，此運算子也會分別傳回 *OutputFirstMomentTensor* 和 *OutputSecondMomentTensor* 中更新的第一次和第二次預估值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="dd47c-109">一般而言，您應該儲存這些第一次和第二次的估計值，並在後續定型步驟中提供它們作為輸入。</span><span class="sxs-lookup"><span data-stu-id="dd47c-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd47c-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="dd47c-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="dd47c-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="dd47c-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd47c-112">語法</span><span class="sxs-lookup"><span data-stu-id="dd47c-112">Syntax</span></span>
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="dd47c-113">成員</span><span class="sxs-lookup"><span data-stu-id="dd47c-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="dd47c-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-115">Tensor，其中包含要套用此優化工具)  (權數的參數。</span><span class="sxs-lookup"><span data-stu-id="dd47c-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="dd47c-116">這個運算子會使用漸層、第一個和第二個時間估計、目前的定型步驟，以及超參數 *LearningRate*、 *Beta1* 和 *Beta2*，來對此 tensor 中提供的加權值執行梯度下降。</span><span class="sxs-lookup"><span data-stu-id="dd47c-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="dd47c-117">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-118">Tensor，其中包含每個加權值之漸層的第一次估計。</span><span class="sxs-lookup"><span data-stu-id="dd47c-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="dd47c-119">這些值通常是透過 *OutputFirstMomentTensor* 上一次執行這個運算子的結果來取得的。</span><span class="sxs-lookup"><span data-stu-id="dd47c-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="dd47c-120">當您第一次將此優化工具套用至一組權數時 (例如，在初始定型步驟期間) 此 tensor 的值通常會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="dd47c-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="dd47c-121">後續的執行應該使用 *OutputFirstMomentTensor* 中傳回的值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="dd47c-122">這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="dd47c-123">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-124">Tensor，其中包含每個權數值之漸層的第二個估計值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="dd47c-125">這些值通常是透過 *OutputSecondMomentTensor* 上一次執行這個運算子的結果來取得的。</span><span class="sxs-lookup"><span data-stu-id="dd47c-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="dd47c-126">當您第一次將此優化工具套用至一組權數時 (例如，在初始定型步驟期間) 此 tensor 的值通常會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="dd47c-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="dd47c-127">後續的執行應該使用 *OutputSecondMomentTensor* 中傳回的值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="dd47c-128">這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="dd47c-129">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-130">要套用至輸入參數的漸層 (權數) 用於梯度下降。</span><span class="sxs-lookup"><span data-stu-id="dd47c-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="dd47c-131">在定型期間，通常會在反向傳播階段中取得漸層。</span><span class="sxs-lookup"><span data-stu-id="dd47c-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="dd47c-132">這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="dd47c-133">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-134">純量 tensor，其中包含代表目前定型步驟計數的單一整數值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="dd47c-135">此值連同 *Beta1* 和 *Beta2* 可用來計算第一個和第二次估計張量的指數衰減。</span><span class="sxs-lookup"><span data-stu-id="dd47c-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="dd47c-136">定型步驟值通常會在定型開頭從0開始，而且每個後續的定型步驟會遞增1。</span><span class="sxs-lookup"><span data-stu-id="dd47c-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="dd47c-137">這個運算子不會更新定型步驟值;您應該以手動方式（例如使用 [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc)）來進行。</span><span class="sxs-lookup"><span data-stu-id="dd47c-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="dd47c-138">這個 tensor 必須是純量 (，也就是 *大小* 等於 1) 且資料類型 [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)。</span><span class="sxs-lookup"><span data-stu-id="dd47c-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="dd47c-139">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-140">在套用漸層下降之後，將更新的參數保留 (權數) 值的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="dd47c-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="dd47c-141">在系結期間，此 tensor 可為合格的輸入 tensor 加上別名，可用來執行此 tensor 的就地更新。</span><span class="sxs-lookup"><span data-stu-id="dd47c-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="dd47c-142">如需詳細資訊，請參閱「 [備註](#remarks) 」一節。</span><span class="sxs-lookup"><span data-stu-id="dd47c-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="dd47c-143">這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="dd47c-144">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-145">包含第一次更新估計的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="dd47c-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="dd47c-146">您應該儲存此 tensor 的值，並在後續定型步驟期間于 *InputFirstMomentTensor* 中提供這些值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="dd47c-147">在系結期間，此 tensor 可為合格的輸入 tensor 加上別名，可用來執行此 tensor 的就地更新。</span><span class="sxs-lookup"><span data-stu-id="dd47c-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="dd47c-148">如需詳細資訊，請參閱「 [備註](#remarks) 」一節。</span><span class="sxs-lookup"><span data-stu-id="dd47c-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="dd47c-149">這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="dd47c-150">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="dd47c-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="dd47c-151">包含已更新之第二次預估的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="dd47c-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="dd47c-152">您應該儲存此 tensor 的值，並在後續定型步驟期間于 *InputSecondMomentTensor* 中提供這些值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="dd47c-153">在系結期間，此 tensor 可為合格的輸入 tensor 加上別名，可用來執行此 tensor 的就地更新。</span><span class="sxs-lookup"><span data-stu-id="dd47c-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="dd47c-154">如需詳細資訊，請參閱「 [備註](#remarks) 」一節。</span><span class="sxs-lookup"><span data-stu-id="dd47c-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="dd47c-155">這個 tensor 的大小和資料類型必須完全符合 *InputParametersTensor* 的 *大小* 和 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="dd47c-156">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="dd47c-156">Type: **float**</span></span>

<span data-ttu-id="dd47c-157">學習率，也通常稱為「 *步驟」大小*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="dd47c-158">學習速率是一種超參數，可在每個定型步驟上判斷加權更新沿著漸層向量的大小。</span><span class="sxs-lookup"><span data-stu-id="dd47c-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="dd47c-159">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="dd47c-159">Type: **float**</span></span>

<span data-ttu-id="dd47c-160">超參數，代表漸層首次估計的指數衰減率。</span><span class="sxs-lookup"><span data-stu-id="dd47c-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="dd47c-161">此值應介於0.0 到1.0 之間。</span><span class="sxs-lookup"><span data-stu-id="dd47c-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="dd47c-162">值為 0.9 f 是典型的。</span><span class="sxs-lookup"><span data-stu-id="dd47c-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="dd47c-163">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="dd47c-163">Type: **float**</span></span>

<span data-ttu-id="dd47c-164">超參數，代表漸層第二個時間估計的指數衰減率。</span><span class="sxs-lookup"><span data-stu-id="dd47c-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="dd47c-165">此值應介於0.0 到1.0 之間。</span><span class="sxs-lookup"><span data-stu-id="dd47c-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="dd47c-166">0.999 f 的值是典型的。</span><span class="sxs-lookup"><span data-stu-id="dd47c-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="dd47c-167">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="dd47c-167">Type: **float**</span></span>

<span data-ttu-id="dd47c-168">用來防止零除的較小值。</span><span class="sxs-lookup"><span data-stu-id="dd47c-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="dd47c-169">若為32位浮點數輸入，則一般值包括 1e-8 或 `FLT_EPSILON` 。</span><span class="sxs-lookup"><span data-stu-id="dd47c-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd47c-170">備註</span><span class="sxs-lookup"><span data-stu-id="dd47c-170">Remarks</span></span>
<span data-ttu-id="dd47c-171">這個運算子支援就地執行，這表示每個輸出 tensor 都允許在系結期間為合格的輸入 tensor 加上別名。</span><span class="sxs-lookup"><span data-stu-id="dd47c-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="dd47c-172">例如，您可以為 *InputParametersTensor* 和 *OutputParametersTensor* 系結相同的資源，以便有效地達成輸入參數的就地更新。</span><span class="sxs-lookup"><span data-stu-id="dd47c-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="dd47c-173">這個運算子的所有輸入張量（ *TrainingStepTensor* 除外）都有資格以這種方式為別名。</span><span class="sxs-lookup"><span data-stu-id="dd47c-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="dd47c-174">可用性</span><span class="sxs-lookup"><span data-stu-id="dd47c-174">Availability</span></span>
<span data-ttu-id="dd47c-175">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="dd47c-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="dd47c-176">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="dd47c-176">Tensor constraints</span></span>
* <span data-ttu-id="dd47c-177">*GradientTensor*、 *InputFirstMomentTensor*、 *InputParametersTensor*、 *InputSecondMomentTensor*、 *OutputFirstMomentTensor*、 *OutputParametersTensor*、 *OutputSecondMomentTensor* 和 *TrainingStepTensor* 必須有相同的 *資料類型*。</span><span class="sxs-lookup"><span data-stu-id="dd47c-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="dd47c-178">*GradientTensor*、 *InputFirstMomentTensor*、 *InputParametersTensor*、 *InputSecondMomentTensor*、 *OutputFirstMomentTensor*、 *OutputParametersTensor* 和 *OutputSecondMomentTensor* 的 *大小* 必須相同。</span><span class="sxs-lookup"><span data-stu-id="dd47c-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="dd47c-179">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="dd47c-179">Tensor support</span></span>
| <span data-ttu-id="dd47c-180">張</span><span class="sxs-lookup"><span data-stu-id="dd47c-180">Tensor</span></span> | <span data-ttu-id="dd47c-181">種類</span><span class="sxs-lookup"><span data-stu-id="dd47c-181">Kind</span></span> | <span data-ttu-id="dd47c-182">維度</span><span class="sxs-lookup"><span data-stu-id="dd47c-182">Dimensions</span></span> | <span data-ttu-id="dd47c-183">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="dd47c-183">Supported dimension counts</span></span> | <span data-ttu-id="dd47c-184">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="dd47c-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="dd47c-185">InputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-185">InputParametersTensor</span></span> | <span data-ttu-id="dd47c-186">輸入</span><span class="sxs-lookup"><span data-stu-id="dd47c-186">Input</span></span> | <span data-ttu-id="dd47c-187">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-188">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-188">4</span></span> | <span data-ttu-id="dd47c-189">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-190">InputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="dd47c-191">輸入</span><span class="sxs-lookup"><span data-stu-id="dd47c-191">Input</span></span> | <span data-ttu-id="dd47c-192">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-193">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-193">4</span></span> | <span data-ttu-id="dd47c-194">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-195">InputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="dd47c-196">輸入</span><span class="sxs-lookup"><span data-stu-id="dd47c-196">Input</span></span> | <span data-ttu-id="dd47c-197">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-198">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-198">4</span></span> | <span data-ttu-id="dd47c-199">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-200">GradientTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-200">GradientTensor</span></span> | <span data-ttu-id="dd47c-201">輸入</span><span class="sxs-lookup"><span data-stu-id="dd47c-201">Input</span></span> | <span data-ttu-id="dd47c-202">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-203">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-203">4</span></span> | <span data-ttu-id="dd47c-204">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-205">TrainingStepTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-205">TrainingStepTensor</span></span> | <span data-ttu-id="dd47c-206">輸入</span><span class="sxs-lookup"><span data-stu-id="dd47c-206">Input</span></span> | <span data-ttu-id="dd47c-207">{1，1，1，1}</span><span class="sxs-lookup"><span data-stu-id="dd47c-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="dd47c-208">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-208">4</span></span> | <span data-ttu-id="dd47c-209">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-210">OutputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-210">OutputParametersTensor</span></span> | <span data-ttu-id="dd47c-211">輸出</span><span class="sxs-lookup"><span data-stu-id="dd47c-211">Output</span></span> | <span data-ttu-id="dd47c-212">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-213">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-213">4</span></span> | <span data-ttu-id="dd47c-214">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-215">OutputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="dd47c-216">輸出</span><span class="sxs-lookup"><span data-stu-id="dd47c-216">Output</span></span> | <span data-ttu-id="dd47c-217">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-218">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-218">4</span></span> | <span data-ttu-id="dd47c-219">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="dd47c-220">OutputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="dd47c-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="dd47c-221">輸出</span><span class="sxs-lookup"><span data-stu-id="dd47c-221">Output</span></span> | <span data-ttu-id="dd47c-222">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="dd47c-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="dd47c-223">4</span><span class="sxs-lookup"><span data-stu-id="dd47c-223">4</span></span> | <span data-ttu-id="dd47c-224">FLOAT32、FLOAT16</span><span class="sxs-lookup"><span data-stu-id="dd47c-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="dd47c-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd47c-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="dd47c-226">**標頭**</span><span class="sxs-lookup"><span data-stu-id="dd47c-226">**Header**</span></span> | <span data-ttu-id="dd47c-227">directml。h</span><span class="sxs-lookup"><span data-stu-id="dd47c-227">directml.h</span></span> |