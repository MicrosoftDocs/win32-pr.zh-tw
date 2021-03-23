---
title: DirectMLX
description: DirectMLX 是適用于 DirectML 的僅限 c + + 標頭協助程式程式庫，目的是要讓您更輕鬆地將個別運算子撰寫到圖形中。
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 8388edd51b6ad3ca30fe1c65947167cee7dac5e6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548479"
---
# <a name="directmlx"></a><span data-ttu-id="d7a54-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="d7a54-103">DirectMLX</span></span>

<span data-ttu-id="d7a54-104">DirectMLX 是適用于 DirectML 的僅限 c + + 標頭協助程式程式庫，目的是要讓您更輕鬆地將個別運算子撰寫到圖形中。</span><span class="sxs-lookup"><span data-stu-id="d7a54-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="d7a54-105">DirectMLX 為所有 DirectML (DML) 運算子類型以及直覺運算子多載提供便利的包裝函式，讓您更輕鬆地具現化 DML 運算子，並將其連結至複雜的圖形。</span><span class="sxs-lookup"><span data-stu-id="d7a54-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="d7a54-106">哪裡可以找到 `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="d7a54-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="d7a54-107">`DirectMLX.h` 在 MIT 授權下是以開放原始碼軟體的形式散發。</span><span class="sxs-lookup"><span data-stu-id="d7a54-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="d7a54-108">您可以在 [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)上找到最新版本。</span><span class="sxs-lookup"><span data-stu-id="d7a54-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d7a54-109">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="d7a54-109">Tensor constraints</span></span>

<span data-ttu-id="d7a54-110">DirectMLX 需要 DirectML 版本1.4.0 或更新的 (請參閱 [DirectML 版本歷程記錄](dml-version-history.md#version-table)) 。</span><span class="sxs-lookup"><span data-stu-id="d7a54-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="d7a54-111">不支援較舊版本的 DirectML。</span><span class="sxs-lookup"><span data-stu-id="d7a54-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="d7a54-112">DirectMLX 需要 C + + 支援11的編譯器，包括 (但不限於) ：</span><span class="sxs-lookup"><span data-stu-id="d7a54-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="d7a54-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="d7a54-113">Visual Studio 2017</span></span>
* <span data-ttu-id="d7a54-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="d7a54-114">Visual Studio 2019</span></span>
* <span data-ttu-id="d7a54-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="d7a54-115">Clang 10</span></span>

<span data-ttu-id="d7a54-116">請注意，c + + 17 (或較新的) 編譯器是我們建議的選項。</span><span class="sxs-lookup"><span data-stu-id="d7a54-116">Note that a C++17 (or newer) compiler is options that we recommend.</span></span> <span data-ttu-id="d7a54-117">您可以針對 c + + 11 進行編譯，但需要使用協力廠商程式庫 (例如 [GSL](https://github.com/microsoft/GSL) 和 [Abseil](https://github.com/abseil/abseil-cpp)) 來取代遺漏的標準程式庫功能。</span><span class="sxs-lookup"><span data-stu-id="d7a54-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="d7a54-118">如果您有無法編譯的設定 `DirectMLX.h` ，請 [在 GitHub 上提出問題](https://github.com/microsoft/DirectML/issues)。</span><span class="sxs-lookup"><span data-stu-id="d7a54-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="d7a54-119">基本使用方式</span><span class="sxs-lookup"><span data-stu-id="d7a54-119">Basic Usage</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Scope scope(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

<span data-ttu-id="d7a54-120">以下是另一個範例，其會建立能夠計算 [二次方公式](https://en.wikipedia.org/wiki/Quadratic_formula)的 DirectML 圖。</span><span class="sxs-lookup"><span data-stu-id="d7a54-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Scope scope(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(scope, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(scope, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a><span data-ttu-id="d7a54-121">更多範例</span><span class="sxs-lookup"><span data-stu-id="d7a54-121">More examples</span></span>

<span data-ttu-id="d7a54-122">您可以在 [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Samples)存放庫中找到使用 DirectMLX 的完整範例。</span><span class="sxs-lookup"><span data-stu-id="d7a54-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="d7a54-123">Compile-Time 選項</span><span class="sxs-lookup"><span data-stu-id="d7a54-123">Compile-Time Options</span></span>

<span data-ttu-id="d7a54-124">DirectMLX 支援編譯時間 #define，以自訂標頭的各部分。</span><span class="sxs-lookup"><span data-stu-id="d7a54-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="d7a54-125">選項</span><span class="sxs-lookup"><span data-stu-id="d7a54-125">Option</span></span>|<span data-ttu-id="d7a54-126">Description</span><span class="sxs-lookup"><span data-stu-id="d7a54-126">Description</span></span>|
|-|-|
|<span data-ttu-id="d7a54-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="d7a54-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="d7a54-128">如果 #define，則會導致錯誤導致呼叫， `std::abort` 而不是擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d7a54-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="d7a54-129">如果例外狀況無法使用 (例如，如果編譯器選項) 中已停用例外狀況，則預設會定義這項功能。</span><span class="sxs-lookup"><span data-stu-id="d7a54-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="d7a54-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="d7a54-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="d7a54-131">如果 #define，則會使用 [Windows 執行程式庫](https://github.com/microsoft/wil) 例外狀況類型擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d7a54-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="d7a54-132">否則會改用標準例外狀況類型 (例如 `std::runtime_error`) 。</span><span class="sxs-lookup"><span data-stu-id="d7a54-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="d7a54-133">如果定義了 **DMLX_NO_EXCEPTIONS** ，此選項就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d7a54-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="d7a54-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="d7a54-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="d7a54-135">如果 #define，則會使用 [Abseil](https://github.com/abseil/abseil-cpp) 作為 c + + 11 中無法使用之標準程式庫類型的放置取代。</span><span class="sxs-lookup"><span data-stu-id="d7a54-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="d7a54-136">這些類型包括 `absl::optional` (取代 `std::optional`) 、 `absl::Span` (取代 `std::span`) 和 `absl::InlinedVector` 。</span><span class="sxs-lookup"><span data-stu-id="d7a54-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="d7a54-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="d7a54-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="d7a54-138">控制是否要使用 [GSL](https://github.com/microsoft/GSL) 做為的取代 `std::span` 。</span><span class="sxs-lookup"><span data-stu-id="d7a54-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="d7a54-139">如果 #define， `std::span` 則會 `gsl::span` 在沒有原生執行的編譯器上取代使用 `std::span` 。</span><span class="sxs-lookup"><span data-stu-id="d7a54-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="d7a54-140">否則，會改為提供內嵌的拖放實作為。</span><span class="sxs-lookup"><span data-stu-id="d7a54-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="d7a54-141">請注意，只有在不支援的 C + + + + 20 編譯器上編譯時 `std::span` ，以及沒有任何其他的拖放標準程式庫取代 (（例如 Abseil) 正在使用中）時，才會使用此選項。</span><span class="sxs-lookup"><span data-stu-id="d7a54-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="d7a54-142">控制 Tensor 版面配置</span><span class="sxs-lookup"><span data-stu-id="d7a54-142">Controlling Tensor Layout</span></span>

<span data-ttu-id="d7a54-143">針對大部分的運算子，DirectMLX 會代表您計算操作員輸出張量的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7a54-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="d7a54-144">例如 `dml::Reduce` `{ 0, 2, 3 }` ，在具有大小輸入 tensor 的座標軸上執行時 `{ 3, 4, 5, 6 }` ，DirectMLX 將會自動計算輸出 tensor 的屬性，包括的正確圖形 `{ 1, 4, 1, 1 }` 。</span><span class="sxs-lookup"><span data-stu-id="d7a54-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="d7a54-145">但是，輸出 *tensor 的其他* 屬性包括進展、 *TotalTensorSizeInBytes* 和 *GuaranteedBaseOffsetAlignment*。</span><span class="sxs-lookup"><span data-stu-id="d7a54-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="d7a54-146">根據預設，DirectMLX 會設定這些屬性，讓 tensor 沒有是昂首闊步、不保證基底位移對齊，以及 [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize)所計算的總 tensor 大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7a54-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="d7a54-147">DirectMLX 支援使用稱為 *tensor 原則* 的物件來自訂這些輸出 tensor 屬性的功能。</span><span class="sxs-lookup"><span data-stu-id="d7a54-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="d7a54-148">**TensorPolicy** 是可自訂的回呼，會由 DirectMLX 叫用，並在給定 tensor 的計算資料類型、旗標和大小的情況下，傳回輸出 tensor 屬性。</span><span class="sxs-lookup"><span data-stu-id="d7a54-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="d7a54-149">您可以在 **dml：： Scope** 物件上設定 Tensor 原則，並將它用於該圖表上的所有後續運算子。</span><span class="sxs-lookup"><span data-stu-id="d7a54-149">Tensor policies can be set on the **dml::Scope** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="d7a54-150">您也可以在建立 **TensorDesc** 時直接設定 Tensor 原則。</span><span class="sxs-lookup"><span data-stu-id="d7a54-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="d7a54-151">因此，DirectMLX 所產生的張量配置可以藉由設定 **TensorPolicy** ，在其張量上設定適當的進展來控制。</span><span class="sxs-lookup"><span data-stu-id="d7a54-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="d7a54-152">範例 1</span><span class="sxs-lookup"><span data-stu-id="d7a54-152">Example 1</span></span>

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a><span data-ttu-id="d7a54-153">範例 2</span><span class="sxs-lookup"><span data-stu-id="d7a54-153">Example 2</span></span>

<span data-ttu-id="d7a54-154">DirectMLX 也提供一些內建的替代 tensor 原則。</span><span class="sxs-lookup"><span data-stu-id="d7a54-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="d7a54-155">例如， **InterleavedChannel** 原則是為了方便起見而提供，可用來產生張量的進展，使其以 NHWC 順序撰寫。</span><span class="sxs-lookup"><span data-stu-id="d7a54-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="d7a54-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7a54-156">See also</span></span>

* [<span data-ttu-id="d7a54-157">DirectML GitHub</span><span class="sxs-lookup"><span data-stu-id="d7a54-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="d7a54-158">DirectMLX yolov4 範例</span><span class="sxs-lookup"><span data-stu-id="d7a54-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="d7a54-159">使用進展來表示填補和記憶體版面配置</span><span class="sxs-lookup"><span data-stu-id="d7a54-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="d7a54-160">DML_GRAPH_DESC 結構</span><span class="sxs-lookup"><span data-stu-id="d7a54-160">DML_GRAPH_DESC structure</span></span>](./directml/ns-directml-dml_graph_desc.md)