---
title: DirectML 功能等級歷程記錄
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: fdc489184b3220afd0b8c75738fa1d40de207c8d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387047"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="4058a-103">DirectML 功能等級歷程記錄</span><span class="sxs-lookup"><span data-stu-id="4058a-103">DirectML feature level history</span></span>

<span data-ttu-id="4058a-104">如需一般 DirectML 版本歷程記錄，請參閱 [DirectML 版本歷程記錄](./dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="4058a-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="4058a-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="4058a-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="4058a-106">在 DirectML 1.5.0 版中引進。</span><span class="sxs-lookup"><span data-stu-id="4058a-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="4058a-107">已新增下列 [運算子](/windows/win32/api/directml/ne-directml-dml_operator_type)的支援。</span><span class="sxs-lookup"><span data-stu-id="4058a-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="4058a-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="4058a-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="4058a-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="4058a-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="4058a-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="4058a-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="4058a-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="4058a-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="4058a-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="4058a-114">下列運算子支援的維度數目上限已從4增加為8。</span><span class="sxs-lookup"><span data-stu-id="4058a-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="4058a-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="4058a-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="4058a-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="4058a-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="4058a-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="4058a-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="4058a-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="4058a-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="4058a-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="4058a-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="4058a-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="4058a-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="4058a-121">**DML_OPERATOR_ACTI加值稅ION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="4058a-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="4058a-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="4058a-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="4058a-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="4058a-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="4058a-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="4058a-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="4058a-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="4058a-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="4058a-127">在 DirectML 版本1.4.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="4058a-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="4058a-128">已新增下列 [運算子](/windows/win32/api/directml/ne-directml-dml_operator_type)的支援。</span><span class="sxs-lookup"><span data-stu-id="4058a-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="4058a-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="4058a-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="4058a-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="4058a-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="4058a-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="4058a-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="4058a-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="4058a-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="4058a-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="4058a-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="4058a-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="4058a-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="4058a-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="4058a-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="4058a-136">**DML_OPERATOR_ACTI加值稅ION_CELU**</span><span class="sxs-lookup"><span data-stu-id="4058a-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="4058a-137">**DML_OPERATOR_ACTI加值稅ION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="4058a-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="4058a-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="4058a-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="4058a-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="4058a-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="4058a-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="4058a-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="4058a-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="4058a-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="4058a-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="4058a-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="4058a-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="4058a-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="4058a-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="4058a-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="4058a-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="4058a-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="4058a-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="4058a-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="4058a-149">已新增下列增強功能。</span><span class="sxs-lookup"><span data-stu-id="4058a-149">Added the following enhancements.</span></span>

* <span data-ttu-id="4058a-150">Tensor 維度的最大數目已從5增加為8。</span><span class="sxs-lookup"><span data-stu-id="4058a-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="4058a-151">請參閱 [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4058a-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="4058a-152">對整數資料類型的其他支援已新增至下列運算子。</span><span class="sxs-lookup"><span data-stu-id="4058a-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="4058a-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="4058a-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="4058a-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="4058a-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="4058a-155">**DML_OPERATOR_MAX_POOLING**、 **DML_OPERATOR_MAX_POOLING1** 和 **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="4058a-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="4058a-156">使用 **DML_REDUCE_FUNCTION_ARGMIN** 或 **DML_REDUCE_FUNCTION_ARGMAX** 時 **DML_OPERATOR_REDUCE**</span><span class="sxs-lookup"><span data-stu-id="4058a-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="4058a-157">以下是已加入的64位資料類型，並受到 select 運算子的支援。</span><span class="sxs-lookup"><span data-stu-id="4058a-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="4058a-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="4058a-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="4058a-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="4058a-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="4058a-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="4058a-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="4058a-161">已淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4058a-161">Deprecated functionality.</span></span>

* <span data-ttu-id="4058a-162">**DML_REDUCE_FUNCTION_ARGMAX** 與 **DML_REDUCE_FUNCTION_ARGMIN** 已被取代。</span><span class="sxs-lookup"><span data-stu-id="4058a-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="4058a-163">您應偏好在其位置使用獨立 **DML_OPERATOR_ARGMIN** 和 **DML_OPERATOR_ARGMAX** 運算子。</span><span class="sxs-lookup"><span data-stu-id="4058a-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="4058a-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="4058a-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="4058a-165">在 DirectML 版本1.2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="4058a-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="4058a-166">已新增下列 Api。</span><span class="sxs-lookup"><span data-stu-id="4058a-166">Added the following APIs.</span></span>

* [<span data-ttu-id="4058a-167">IDMLDevice1 介面</span><span class="sxs-lookup"><span data-stu-id="4058a-167">IDMLDevice1 interface</span></span>](./directml/nn-directml-idmldevice1.md)
* <span data-ttu-id="4058a-168">Operator graph 支援 (參閱 [IDMLDevice1：： CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span><span class="sxs-lookup"><span data-stu-id="4058a-168">Operator graph support (see [IDMLDevice1::CompileGraph](./directml/nf-directml-idmldevice1-compilegraph.md)</span></span>

<span data-ttu-id="4058a-169">已新增下列運算子的支援。</span><span class="sxs-lookup"><span data-stu-id="4058a-169">Added support for the following operators.</span></span>

* <span data-ttu-id="4058a-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="4058a-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="4058a-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="4058a-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="4058a-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="4058a-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="4058a-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="4058a-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="4058a-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="4058a-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="4058a-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="4058a-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="4058a-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="4058a-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="4058a-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="4058a-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="4058a-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="4058a-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="4058a-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="4058a-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="4058a-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="4058a-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="4058a-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="4058a-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="4058a-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="4058a-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="4058a-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="4058a-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="4058a-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="4058a-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="4058a-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="4058a-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="4058a-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="4058a-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="4058a-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="4058a-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="4058a-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="4058a-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="4058a-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="4058a-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="4058a-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="4058a-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="4058a-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="4058a-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="4058a-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="4058a-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="4058a-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="4058a-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="4058a-194">已新增下列增強功能。</span><span class="sxs-lookup"><span data-stu-id="4058a-194">Added the following enhancements.</span></span>

* <span data-ttu-id="4058a-195">對整數資料類型的其他支援已新增至下列運算子。</span><span class="sxs-lookup"><span data-stu-id="4058a-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="4058a-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="4058a-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="4058a-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="4058a-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="4058a-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="4058a-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="4058a-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="4058a-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="4058a-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="4058a-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="4058a-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="4058a-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="4058a-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="4058a-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="4058a-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="4058a-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="4058a-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="4058a-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="4058a-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="4058a-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="4058a-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="4058a-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="4058a-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="4058a-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="4058a-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="4058a-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="4058a-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="4058a-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="4058a-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="4058a-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="4058a-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="4058a-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="4058a-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="4058a-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="4058a-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="4058a-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="4058a-214">**DML_OPERATOR_ACTI加值稅ION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="4058a-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="4058a-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="4058a-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="4058a-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="4058a-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="4058a-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="4058a-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="4058a-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="4058a-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="4058a-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="4058a-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="4058a-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="4058a-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="4058a-221">**DML_OPERATOR_TOP_K** 和 **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="4058a-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="4058a-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="4058a-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="4058a-223">使用下列其中一個縮減函數時 **DML_OPERATOR_REDUCE**。</span><span class="sxs-lookup"><span data-stu-id="4058a-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="4058a-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="4058a-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="4058a-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="4058a-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="4058a-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="4058a-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="4058a-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="4058a-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="4058a-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="4058a-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="4058a-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="4058a-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="4058a-230">**DML_OPERATOR_GATHER** 的寬鬆 tensor 圖形限制</span><span class="sxs-lookup"><span data-stu-id="4058a-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="4058a-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="4058a-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="4058a-232">在 DirectML 版本1.1.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="4058a-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="4058a-233">已新增下列 Api。</span><span class="sxs-lookup"><span data-stu-id="4058a-233">Added the following APIs.</span></span>
* [<span data-ttu-id="4058a-234">DMLCreateDevice1 函式</span><span class="sxs-lookup"><span data-stu-id="4058a-234">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="4058a-235">DML_FEATURE_LEVEL 列舉</span><span class="sxs-lookup"><span data-stu-id="4058a-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="4058a-236">功能等級查詢 (查看 [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)) </span><span class="sxs-lookup"><span data-stu-id="4058a-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="4058a-237">已新增下列運算子的支援。</span><span class="sxs-lookup"><span data-stu-id="4058a-237">Added support for the following operators.</span></span>

* <span data-ttu-id="4058a-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="4058a-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="4058a-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="4058a-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="4058a-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="4058a-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="4058a-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="4058a-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="4058a-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="4058a-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="4058a-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="4058a-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="4058a-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="4058a-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="4058a-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="4058a-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="4058a-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="4058a-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="4058a-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="4058a-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="4058a-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="4058a-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="4058a-249">**DML_OPERATOR_ACTI加值稅ION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="4058a-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="4058a-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="4058a-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="4058a-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="4058a-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="4058a-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="4058a-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="4058a-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="4058a-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="4058a-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="4058a-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="4058a-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="4058a-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="4058a-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="4058a-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="4058a-257">已新增下列增強功能。</span><span class="sxs-lookup"><span data-stu-id="4058a-257">Added the following enhancements.</span></span>

* <span data-ttu-id="4058a-258">當您系結輸入資源以進行 [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer)的分派時，只要也設定了適當的堆積屬性，就能提供具有 [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type)) **D3D12_HEAP_TYPE_DEFAULT** (的資源。</span><span class="sxs-lookup"><span data-stu-id="4058a-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="4058a-259">請參閱 [DirectML 中的](./dml-binding.md)系結。</span><span class="sxs-lookup"><span data-stu-id="4058a-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="4058a-260">除了對 **UINT32** 的現有支援之外，下列邏輯布林運算子現在還支援 **UINT8** 輸出張量。</span><span class="sxs-lookup"><span data-stu-id="4058a-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="4058a-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="4058a-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="4058a-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="4058a-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="4058a-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="4058a-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="4058a-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="4058a-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="4058a-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="4058a-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="4058a-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="4058a-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="4058a-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="4058a-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="4058a-268">5D 啟用函式現在支援在其輸入和輸出張量上使用進展。</span><span class="sxs-lookup"><span data-stu-id="4058a-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="4058a-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="4058a-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="4058a-270">引進 DirectML 的功能層級。</span><span class="sxs-lookup"><span data-stu-id="4058a-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="4058a-271">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4058a-271">See also</span></span>

* [<span data-ttu-id="4058a-272">DirectML 版本歷程記錄</span><span class="sxs-lookup"><span data-stu-id="4058a-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="4058a-273">DML_FEATURE_LEVEL 列舉</span><span class="sxs-lookup"><span data-stu-id="4058a-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="4058a-274">DMLCreateDevice1 函式</span><span class="sxs-lookup"><span data-stu-id="4058a-274">DMLCreateDevice1 function</span></span>](./directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="4058a-275">DML_FEATURE_QUERY_FEATURE_LEVELS 結構</span><span class="sxs-lookup"><span data-stu-id="4058a-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
