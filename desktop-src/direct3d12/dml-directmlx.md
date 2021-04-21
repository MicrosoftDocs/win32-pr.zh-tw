---
title: DirectMLX
description: DirectMLX 是適用于 DirectML 的僅限 c + + 標頭協助程式程式庫，目的是要讓您更輕鬆地將個別運算子撰寫到圖形中。
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 2ddd6d9063002b76449224ebafdb6dd021b27fa0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803357"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX 是適用于 DirectML 的僅限 c + + 標頭協助程式程式庫，目的是要讓您更輕鬆地將個別運算子撰寫到圖形中。

DirectMLX 為所有 DirectML (DML) 運算子類型以及直覺運算子多載提供便利的包裝函式，讓您更輕鬆地具現化 DML 運算子，並將其連結至複雜的圖形。

## <a name="where-to-find-directmlxh"></a>哪裡可以找到 `DirectMLX.h`

`DirectMLX.h` 在 MIT 授權下是以開放原始碼軟體的形式散發。 您可以在 [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)上找到最新版本。

## <a name="tensor-constraints"></a>Tensor 條件約束

DirectMLX 需要 DirectML 版本1.4.0 或更新的 (請參閱 [DirectML 版本歷程記錄](dml-version-history.md#version-table)) 。 不支援較舊版本的 DirectML。

DirectMLX 需要 C + + 支援11的編譯器，包括 (但不限於) ：

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

請注意，c + + 17 (或較新的) 編譯器是我們建議的選項。 您可以針對 c + + 11 進行編譯，但需要使用協力廠商程式庫 (例如 [GSL](https://github.com/microsoft/GSL) 和 [Abseil](https://github.com/abseil/abseil-cpp)) 來取代遺漏的標準程式庫功能。

如果您有無法編譯的設定 `DirectMLX.h` ，請 [在 GitHub 上提出問題](https://github.com/microsoft/DirectML/issues)。

## <a name="basic-usage"></a>基本使用方式

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

以下是另一個範例，其會建立能夠計算 [二次方公式](https://en.wikipedia.org/wiki/Quadratic_formula)的 DirectML 圖。

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

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a>更多範例

您可以在 [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Samples)存放庫中找到使用 DirectMLX 的完整範例。

## <a name="compile-time-options"></a>編譯時間選項

DirectMLX 支援編譯時間 #define，以自訂標頭的各部分。

|選項|Description|
|-|-|
|**DMLX_NO_EXCEPTIONS**|如果 #define，則會導致錯誤導致呼叫， `std::abort` 而不是擲回例外狀況。 如果例外狀況無法使用 (例如，如果編譯器選項) 中已停用例外狀況，則預設會定義這項功能。|
|**DMLX_USE_WIL**|如果 #define，則會使用 [Windows 執行程式庫](https://github.com/microsoft/wil) 例外狀況類型擲回例外狀況。 否則會改用標準例外狀況類型 (例如 `std::runtime_error`) 。 如果定義了 **DMLX_NO_EXCEPTIONS** ，此選項就不會有任何作用。|
|**DMLX_USE_ABSEIL**|如果 #define，則會使用 [Abseil](https://github.com/abseil/abseil-cpp) 作為 c + + 11 中無法使用之標準程式庫類型的放置取代。 這些類型包括 `absl::optional` (取代 `std::optional`) 、 `absl::Span` (取代 `std::span`) 和 `absl::InlinedVector` 。|
|**DMLX_USE_GSL**|控制是否要使用 [GSL](https://github.com/microsoft/GSL) 做為的取代 `std::span` 。 如果 #define， `std::span` 則會 `gsl::span` 在沒有原生執行的編譯器上取代使用 `std::span` 。 否則，會改為提供內嵌的拖放實作為。 請注意，只有在不支援的 C + + + + 20 編譯器上編譯時 `std::span` ，以及沒有任何其他的拖放標準程式庫取代 (（例如 Abseil) 正在使用中）時，才會使用此選項。|

## <a name="controlling-tensor-layout"></a>控制 tensor 版面配置

針對大部分的運算子，DirectMLX 會代表您計算操作員輸出張量的屬性。 例如 `dml::Reduce` `{ 0, 2, 3 }` ，在具有大小輸入 tensor 的座標軸上執行時 `{ 3, 4, 5, 6 }` ，DirectMLX 將會自動計算輸出 tensor 的屬性，包括的正確圖形 `{ 1, 4, 1, 1 }` 。

但是，輸出 *tensor 的其他* 屬性包括進展、 *TotalTensorSizeInBytes* 和 *GuaranteedBaseOffsetAlignment*。 根據預設，DirectMLX 會設定這些屬性，讓 tensor 沒有是昂首闊步、不保證基底位移對齊，以及 [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize)所計算的總 tensor 大小（以位元組為單位）。

DirectMLX 支援使用稱為 *tensor 原則* 的物件來自訂這些輸出 tensor 屬性的功能。 **TensorPolicy** 是可自訂的回呼，會由 DirectMLX 叫用，並在給定 tensor 的計算資料類型、旗標和大小的情況下，傳回輸出 tensor 屬性。

您可以在 **dml：： Graph** 物件上設定 Tensor 原則，並將它用於該圖表上的所有後續運算子。 您也可以在建立 **TensorDesc** 時直接設定 Tensor 原則。

因此，DirectMLX 所產生的張量配置可以藉由設定 **TensorPolicy** ，在其張量上設定適當的進展來控制。

### <a name="example-1"></a>範例 1

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

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>範例 2

DirectMLX 也提供一些內建的替代 tensor 原則。 例如， **InterleavedChannel** 原則是為了方便起見而提供，可用來產生張量的進展，使其以 NHWC 順序撰寫。

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>另請參閱

* [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [DirectMLX yolov4 範例](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [使用進展來表示填補和記憶體版面配置](./dml-strides.md)
* [DML_GRAPH_DESC 結構](./directml/ns-directml-dml_graph_desc.md)