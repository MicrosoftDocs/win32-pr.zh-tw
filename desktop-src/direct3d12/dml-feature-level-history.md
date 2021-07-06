---
title: DirectML 功能等級歷程記錄
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 3ddb2eec80448b8119bf2d990afbb998f212db26
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282547"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="ef697-103">DirectML 功能等級歷程記錄</span><span class="sxs-lookup"><span data-stu-id="ef697-103">DirectML feature level history</span></span>

<span data-ttu-id="ef697-104">如需一般 DirectML 版本歷程記錄，請參閱 [DirectML 版本歷程記錄](./dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="ef697-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_4_0"></a><span data-ttu-id="ef697-105">DML_FEATURE_LEVEL_4_0</span><span class="sxs-lookup"><span data-stu-id="ef697-105">DML_FEATURE_LEVEL_4_0</span></span>

<span data-ttu-id="ef697-106">在 DirectML 版本1.6.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ef697-106">Introduced in DirectML version 1.6.0.</span></span>

<span data-ttu-id="ef697-107">已新增下列運算子類型的支援，記載于 [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)中。</span><span class="sxs-lookup"><span data-stu-id="ef697-107">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="ef697-108">針對每個運算子類型常數，該主題會提供對應結構的連結。</span><span class="sxs-lookup"><span data-stu-id="ef697-108">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="ef697-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span><span class="sxs-lookup"><span data-stu-id="ef697-109">**DML_OPERATOR_ELEMENT_WISE_QUANTIZED_LINEAR_ADD**</span></span>
* <span data-ttu-id="ef697-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="ef697-110">**DML_OPERATOR_DYNAMIC_QUANTIZE_LINEAR**</span></span>
* <span data-ttu-id="ef697-111">**DML_OPERATOR_ROI_ALIGN1**</span><span class="sxs-lookup"><span data-stu-id="ef697-111">**DML_OPERATOR_ROI_ALIGN1**</span></span>

<span data-ttu-id="ef697-112">下列運算子的擴充資料類型和維度計數支援，記載于 [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)中。</span><span class="sxs-lookup"><span data-stu-id="ef697-112">Extended data type and dimension count support for the following operators, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="ef697-113">如需 [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level)中新增之特定支援的詳細資訊，請參閱每個運算子的結構主題。</span><span class="sxs-lookup"><span data-stu-id="ef697-113">For details on the specific support added in [**DML_FEATURE_LEVEL_4_0**](/windows/win32/api/directml/ne-directml-dml_feature_level), see each operator's structure topic.</span></span>

* <span data-ttu-id="ef697-114">**DML_OPERATOR_ACTI加值稅ION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-114">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="ef697-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="ef697-115">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="ef697-116">**DML_OPERATOR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="ef697-116">**DML_OPERATOR_CONVOLUTION**</span></span>
* <span data-ttu-id="ef697-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="ef697-117">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="ef697-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="ef697-118">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="ef697-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="ef697-119">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="ef697-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="ef697-120">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="ef697-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="ef697-121">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="ef697-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="ef697-122">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="ef697-123">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="ef697-123">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="ef697-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="ef697-124">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="ef697-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-125">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="ef697-126">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="ef697-126">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="ef697-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="ef697-127">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>
* <span data-ttu-id="ef697-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="ef697-128">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="ef697-129">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="ef697-129">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="ef697-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="ef697-130">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="ef697-131">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="ef697-131">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="ef697-132">在 DirectML 1.5.0 版中引進。</span><span class="sxs-lookup"><span data-stu-id="ef697-132">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="ef697-133">已新增下列運算子類型的支援，記載于 [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)中。</span><span class="sxs-lookup"><span data-stu-id="ef697-133">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="ef697-134">針對每個運算子類型常數，該主題會提供對應結構的連結。</span><span class="sxs-lookup"><span data-stu-id="ef697-134">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="ef697-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="ef697-135">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="ef697-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-136">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="ef697-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="ef697-137">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="ef697-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-138">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="ef697-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="ef697-139">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="ef697-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-140">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="ef697-141">下列運算子支援的維度數目上限已從4增加為8。</span><span class="sxs-lookup"><span data-stu-id="ef697-141">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="ef697-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="ef697-142">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="ef697-143">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="ef697-143">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="ef697-144">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="ef697-144">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="ef697-145">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="ef697-145">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="ef697-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="ef697-146">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="ef697-147">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="ef697-147">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="ef697-148">**DML_OPERATOR_ACTI加值稅ION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-148">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="ef697-149">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-149">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="ef697-150">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="ef697-150">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="ef697-151">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="ef697-151">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="ef697-152">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="ef697-152">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="ef697-153">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="ef697-153">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="ef697-154">在 DirectML 版本1.4.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ef697-154">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="ef697-155">已新增下列運算子類型的支援，記載于 [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)中。</span><span class="sxs-lookup"><span data-stu-id="ef697-155">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="ef697-156">針對每個運算子類型常數，該主題會提供對應結構的連結。</span><span class="sxs-lookup"><span data-stu-id="ef697-156">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="ef697-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="ef697-157">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="ef697-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="ef697-158">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="ef697-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="ef697-159">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="ef697-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="ef697-160">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="ef697-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="ef697-161">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="ef697-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="ef697-162">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="ef697-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="ef697-163">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="ef697-164">**DML_OPERATOR_ACTI加值稅ION_CELU**</span><span class="sxs-lookup"><span data-stu-id="ef697-164">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="ef697-165">**DML_OPERATOR_ACTI加值稅ION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-165">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="ef697-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-166">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="ef697-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-167">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="ef697-168">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="ef697-168">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="ef697-169">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="ef697-169">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="ef697-170">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-170">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="ef697-171">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="ef697-171">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="ef697-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="ef697-172">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="ef697-173">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="ef697-173">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="ef697-174">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="ef697-174">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="ef697-175">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="ef697-175">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="ef697-176">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="ef697-176">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="ef697-177">已新增下列增強功能。</span><span class="sxs-lookup"><span data-stu-id="ef697-177">Added the following enhancements.</span></span>

* <span data-ttu-id="ef697-178">Tensor 維度的最大數目已從5增加為8。</span><span class="sxs-lookup"><span data-stu-id="ef697-178">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="ef697-179">請參閱 [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="ef697-179">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="ef697-180">對整數資料類型的其他支援已新增至下列運算子。</span><span class="sxs-lookup"><span data-stu-id="ef697-180">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="ef697-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="ef697-181">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="ef697-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="ef697-182">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="ef697-183">**DML_OPERATOR_MAX_POOLING**、 **DML_OPERATOR_MAX_POOLING1** 和 **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="ef697-183">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="ef697-184">使用 **DML_REDUCE_FUNCTION_ARGMIN** 或 **DML_REDUCE_FUNCTION_ARGMAX** 時 **DML_OPERATOR_REDUCE**</span><span class="sxs-lookup"><span data-stu-id="ef697-184">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="ef697-185">以下是已加入的64位資料類型，並受到 select 運算子的支援。</span><span class="sxs-lookup"><span data-stu-id="ef697-185">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="ef697-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="ef697-186">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="ef697-187">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="ef697-187">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="ef697-188">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="ef697-188">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="ef697-189">已淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ef697-189">Deprecated functionality.</span></span>

* <span data-ttu-id="ef697-190">**DML_REDUCE_FUNCTION_ARGMAX** 與 **DML_REDUCE_FUNCTION_ARGMIN** 已被取代。</span><span class="sxs-lookup"><span data-stu-id="ef697-190">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="ef697-191">您應偏好在其位置使用獨立 **DML_OPERATOR_ARGMIN** 和 **DML_OPERATOR_ARGMAX** 運算子。</span><span class="sxs-lookup"><span data-stu-id="ef697-191">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="ef697-192">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="ef697-192">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="ef697-193">在 DirectML 版本1.2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ef697-193">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="ef697-194">已新增下列 Api。</span><span class="sxs-lookup"><span data-stu-id="ef697-194">Added the following APIs.</span></span>

* [<span data-ttu-id="ef697-195">IDMLDevice1 介面</span><span class="sxs-lookup"><span data-stu-id="ef697-195">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="ef697-196">Operator graph 支援 (參閱 [IDMLDevice1：： CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="ef697-196">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="ef697-197">已新增下列運算子類型的支援，記載于 [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)中。</span><span class="sxs-lookup"><span data-stu-id="ef697-197">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="ef697-198">針對每個運算子類型常數，該主題會提供對應結構的連結。</span><span class="sxs-lookup"><span data-stu-id="ef697-198">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="ef697-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="ef697-199">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="ef697-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="ef697-200">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="ef697-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="ef697-201">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="ef697-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="ef697-202">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="ef697-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="ef697-203">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="ef697-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="ef697-204">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="ef697-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="ef697-205">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="ef697-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="ef697-206">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="ef697-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="ef697-207">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="ef697-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="ef697-208">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="ef697-209">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="ef697-209">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="ef697-210">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="ef697-210">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="ef697-211">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="ef697-211">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="ef697-212">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="ef697-212">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="ef697-213">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="ef697-213">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="ef697-214">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="ef697-214">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="ef697-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="ef697-215">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="ef697-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="ef697-216">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="ef697-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="ef697-217">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="ef697-218">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="ef697-218">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="ef697-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="ef697-219">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="ef697-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="ef697-220">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="ef697-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="ef697-221">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="ef697-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="ef697-222">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="ef697-223">已新增下列增強功能。</span><span class="sxs-lookup"><span data-stu-id="ef697-223">Added the following enhancements.</span></span>

* <span data-ttu-id="ef697-224">對整數資料類型的其他支援已新增至下列運算子。</span><span class="sxs-lookup"><span data-stu-id="ef697-224">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="ef697-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="ef697-225">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="ef697-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="ef697-226">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="ef697-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="ef697-227">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="ef697-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="ef697-228">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="ef697-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="ef697-229">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="ef697-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="ef697-230">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="ef697-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="ef697-231">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="ef697-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="ef697-232">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="ef697-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="ef697-233">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="ef697-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="ef697-234">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="ef697-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="ef697-235">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="ef697-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="ef697-236">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="ef697-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="ef697-237">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="ef697-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="ef697-238">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="ef697-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="ef697-239">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="ef697-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="ef697-240">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="ef697-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="ef697-241">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="ef697-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="ef697-242">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="ef697-243">**DML_OPERATOR_ACTI加值稅ION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="ef697-243">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="ef697-244">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="ef697-244">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="ef697-245">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="ef697-245">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="ef697-246">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="ef697-246">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="ef697-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="ef697-247">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="ef697-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="ef697-248">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="ef697-249">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="ef697-249">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="ef697-250">**DML_OPERATOR_TOP_K** 和 **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="ef697-250">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="ef697-251">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="ef697-251">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="ef697-252">使用下列其中一個縮減函數時 **DML_OPERATOR_REDUCE**。</span><span class="sxs-lookup"><span data-stu-id="ef697-252">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="ef697-253">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="ef697-253">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="ef697-254">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="ef697-254">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="ef697-255">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="ef697-255">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="ef697-256">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="ef697-256">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="ef697-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="ef697-257">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="ef697-258">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="ef697-258">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="ef697-259">**DML_OPERATOR_GATHER** 的寬鬆 tensor 圖形限制</span><span class="sxs-lookup"><span data-stu-id="ef697-259">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="ef697-260">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="ef697-260">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="ef697-261">在 DirectML 版本1.1.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="ef697-261">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="ef697-262">已新增下列 Api。</span><span class="sxs-lookup"><span data-stu-id="ef697-262">Added the following APIs.</span></span>
* [<span data-ttu-id="ef697-263">DMLCreateDevice1 函式</span><span class="sxs-lookup"><span data-stu-id="ef697-263">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="ef697-264">DML_FEATURE_LEVEL 列舉</span><span class="sxs-lookup"><span data-stu-id="ef697-264">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="ef697-265">功能等級查詢 (查看 [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)) </span><span class="sxs-lookup"><span data-stu-id="ef697-265">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="ef697-266">已新增下列運算子類型的支援，記載于 [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type)中。</span><span class="sxs-lookup"><span data-stu-id="ef697-266">Added support for the following operator types, documented in [**DML_OPERATOR_TYPE**](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span> <span data-ttu-id="ef697-267">針對每個運算子類型常數，該主題會提供對應結構的連結。</span><span class="sxs-lookup"><span data-stu-id="ef697-267">For each operator type constant, that topic provides a link to the corresponding structure.</span></span>

* <span data-ttu-id="ef697-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="ef697-268">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="ef697-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="ef697-269">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="ef697-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="ef697-270">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="ef697-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="ef697-271">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="ef697-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="ef697-272">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="ef697-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="ef697-273">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="ef697-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="ef697-274">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="ef697-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="ef697-275">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="ef697-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="ef697-276">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="ef697-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="ef697-277">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="ef697-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="ef697-278">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="ef697-279">**DML_OPERATOR_ACTI加值稅ION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="ef697-279">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="ef697-280">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="ef697-280">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="ef697-281">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="ef697-281">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="ef697-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="ef697-282">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="ef697-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="ef697-283">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="ef697-284">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="ef697-284">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="ef697-285">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="ef697-285">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="ef697-286">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="ef697-286">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="ef697-287">已新增下列增強功能。</span><span class="sxs-lookup"><span data-stu-id="ef697-287">Added the following enhancements.</span></span>

* <span data-ttu-id="ef697-288">當您系結輸入資源以進行 [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)的分派時，只要也設定了適當的堆積屬性，就能提供具有 [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type)) **D3D12_HEAP_TYPE_DEFAULT** (的資源。</span><span class="sxs-lookup"><span data-stu-id="ef697-288">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="ef697-289">請參閱 [DirectML 中的](./dml-binding.md)系結。</span><span class="sxs-lookup"><span data-stu-id="ef697-289">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="ef697-290">除了對 **UINT32** 的現有支援之外，下列邏輯布林運算子現在還支援 **UINT8** 輸出張量。</span><span class="sxs-lookup"><span data-stu-id="ef697-290">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="ef697-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="ef697-291">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="ef697-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="ef697-292">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="ef697-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="ef697-293">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="ef697-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="ef697-294">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="ef697-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="ef697-295">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="ef697-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="ef697-296">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="ef697-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="ef697-297">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="ef697-298">5D 啟用函式現在支援在其輸入和輸出張量上使用進展。</span><span class="sxs-lookup"><span data-stu-id="ef697-298">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="ef697-299">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="ef697-299">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="ef697-300">引進 DirectML 的功能層級。</span><span class="sxs-lookup"><span data-stu-id="ef697-300">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef697-301">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef697-301">See also</span></span>

* [<span data-ttu-id="ef697-302">DirectML 版本歷程記錄</span><span class="sxs-lookup"><span data-stu-id="ef697-302">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="ef697-303">DML_FEATURE_LEVEL 列舉</span><span class="sxs-lookup"><span data-stu-id="ef697-303">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="ef697-304">DMLCreateDevice1 函式</span><span class="sxs-lookup"><span data-stu-id="ef697-304">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="ef697-305">DML_FEATURE_QUERY_FEATURE_LEVELS 結構</span><span class="sxs-lookup"><span data-stu-id="ef697-305">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
