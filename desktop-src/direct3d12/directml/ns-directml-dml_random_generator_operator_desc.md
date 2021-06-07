---
UID: NS:directml.DML_RANDOM_GENERATOR_OPERATOR_DESC
title: DML_RANDOM_GENERATOR_OPERATOR_DESC
description: 以決定性產生的虛擬隨機、一致分散式位來填滿輸出 tensor。 這個運算子也可能會輸出已更新的內部產生器狀態，可在後續執行運算子期間使用。
helpviewer_keywords:
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- DML_RANDOM_GENERATOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_OPERATOR_DESC, DML_RANDOM_GENERATOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
- directml/DML_RANDOM_GENERATOR_OPERATOR_DESC
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
- DML_RANDOM_GENERATOR_OPERATOR_DESC
ms.openlocfilehash: 6807c3a1ac91716739075f51196a75ae76ca479b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417051"
---
# <a name="dml_random_generator_operator_desc-structure-directmlh"></a><span data-ttu-id="851b9-104">DML_RANDOM_GENERATOR_OPERATOR_DESC 結構 (directml .h) </span><span class="sxs-lookup"><span data-stu-id="851b9-104">DML_RANDOM_GENERATOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="851b9-105">以決定性產生的虛擬隨機、一致分散式位來填滿輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="851b9-105">Fills an output tensor with deterministically-generated, pseudo-random, uniformly-distributed bits.</span></span> <span data-ttu-id="851b9-106">這個運算子也可能會輸出已更新的內部產生器狀態，可在後續執行運算子期間使用。</span><span class="sxs-lookup"><span data-stu-id="851b9-106">This operator optionally may also output an updated internal generator state, which can be used during subsequent executions of the operator.</span></span>

<span data-ttu-id="851b9-107">這個運算子具有決定性，而且行為就像是純虛擬函式，它的 &mdash; 執行不會產生副作用，也不會使用全域狀態。</span><span class="sxs-lookup"><span data-stu-id="851b9-107">This operator is deterministic, and behaves as if it were a pure function&mdash;that is, its execution produces no side-effects, and uses no global state.</span></span> <span data-ttu-id="851b9-108">這個運算子所產生的虛擬隨機輸出，只取決於 *InputStateTensor* 中提供的值。</span><span class="sxs-lookup"><span data-stu-id="851b9-108">The pseudo-random output produced by this operator is solely dependent on the values supplied in the *InputStateTensor*.</span></span>

<span data-ttu-id="851b9-109">這個運算子所執行的產生器不會以密碼編譯方式安全;因此，此操作員不應用於加密、金鑰產生，或需要以密碼編譯安全亂數產生的其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="851b9-109">The generators implemented by this operator are not cryptographically secure; therefore, this operator should not be used for encryption, key generation, or other applications which require cryptographically secure random number generation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="851b9-110">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="851b9-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="851b9-111">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="851b9-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="851b9-112">語法</span><span class="sxs-lookup"><span data-stu-id="851b9-112">Syntax</span></span>

```cpp
struct DML_RANDOM_GENERATOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputStateTensor;
  const DML_TENSOR_DESC* OutputTensor;
  _Maybenull_ const DML_TENSOR_DESC* OutputStateTensor;
  DML_RANDOM_GENERATOR_TYPE Type;
};
```

## <a name="members"></a><span data-ttu-id="851b9-113">成員</span><span class="sxs-lookup"><span data-stu-id="851b9-113">Members</span></span>

`InputStateTensor`

<span data-ttu-id="851b9-114">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="851b9-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="851b9-115">包含內部產生器狀態的輸入 tensor。</span><span class="sxs-lookup"><span data-stu-id="851b9-115">An input tensor containing the internal generator state.</span></span> <span data-ttu-id="851b9-116">此輸入 tensor 的大小和格式取決於 [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)。</span><span class="sxs-lookup"><span data-stu-id="851b9-116">The size and format of this input tensor depends on the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md).</span></span>

<span data-ttu-id="851b9-117">針對 **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**，此 tensor 必須屬於 **UINT32** 類型，而且具有大小 `{1,1,1,6}` 。</span><span class="sxs-lookup"><span data-stu-id="851b9-117">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, this tensor must be of type **UINT32**, and have sizes `{1,1,1,6}`.</span></span> <span data-ttu-id="851b9-118">第一個 4 32 位值包含單純增加的128位計數器。</span><span class="sxs-lookup"><span data-stu-id="851b9-118">The first four 32-bit values contain a monotonically increasing 128-bit counter.</span></span> <span data-ttu-id="851b9-119">最後一個 2 32 位值包含產生器的64位索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="851b9-119">The last two 32-bit values contain the 64-bit key value for the generator.</span></span>

```
    Element        0       1       2       3       4       5
(32-bits each) |-------|-------|-------|-------|-------|-------|
                <--------128-bit counter------> <-64-bit key-->
```

<span data-ttu-id="851b9-120">第一次初始化產生器的輸入狀態時，通常是128位計數器 (第一個 4 32 位 UINT32 值) 應該初始化為0。</span><span class="sxs-lookup"><span data-stu-id="851b9-120">When initializing the generator's input state for the first time, typically the 128-bit counter (the first four 32-bit UINT32 values) should be initialized to 0.</span></span> <span data-ttu-id="851b9-121">您可以任意選擇此金鑰;不同的索引鍵值會產生不同的數位序列。</span><span class="sxs-lookup"><span data-stu-id="851b9-121">The key can be arbitrarily chosen; different key values will produce different sequences of numbers.</span></span> <span data-ttu-id="851b9-122">通常會使用使用者提供的 *種子* 來產生金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="851b9-122">The value for the key is usually generated using a user-provided *seed*.</span></span>

`OutputTensor`

<span data-ttu-id="851b9-123">Type： **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="851b9-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="851b9-124">包含所產生之虛擬隨機值的輸出 tensor。</span><span class="sxs-lookup"><span data-stu-id="851b9-124">An output tensor which holds the resulting pseudo-random values.</span></span> <span data-ttu-id="851b9-125">此 tensor 可以是任何大小。</span><span class="sxs-lookup"><span data-stu-id="851b9-125">This tensor can be of any size.</span></span>

`OutputStateTensor`

<span data-ttu-id="851b9-126">類型： \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="851b9-126">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="851b9-127">選用的輸出 tensor，其中保留已更新的內部產生器狀態。</span><span class="sxs-lookup"><span data-stu-id="851b9-127">An optional output tensor THAT holds the updated internal generator state.</span></span> <span data-ttu-id="851b9-128">如果有提供，這個運算子會使用 *InputStateTensor* 來計算適當的已更新產生器狀態，並將結果寫入 *OutputStateTensor*。</span><span class="sxs-lookup"><span data-stu-id="851b9-128">If supplied, this operator uses the *InputStateTensor* to compute an appropriate updated generator state, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="851b9-129">一般而言，呼叫端會儲存此結果，並在後續執行此運算子時，提供它做為輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="851b9-129">Typically, callers would save this result and supply it as the input state on a subsequent execution of this operator.</span></span>

`Type`

<span data-ttu-id="851b9-130">類型： **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span><span class="sxs-lookup"><span data-stu-id="851b9-130">Type: **[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)**</span></span>

<span data-ttu-id="851b9-131">[DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md)列舉中的其中一個值，表示要使用之產生器的類型。</span><span class="sxs-lookup"><span data-stu-id="851b9-131">One of the values from the [DML_RANDOM_GENERATOR_TYPE](./ne-directml-dml_random_generator_type.md) enum, indicating the type of generator to use.</span></span> <span data-ttu-id="851b9-132">目前唯一有效的值是 **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**，這會根據 [PHILOX 4X32-10 演算法](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf)產生虛擬亂數。</span><span class="sxs-lookup"><span data-stu-id="851b9-132">Currently the only valid value is **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, which generates pseudo-random numbers according to the [Philox 4x32-10 algorithm](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf).</span></span>

## <a name="remarks"></a><span data-ttu-id="851b9-133">備註</span><span class="sxs-lookup"><span data-stu-id="851b9-133">Remarks</span></span>
<span data-ttu-id="851b9-134">在每次執行此運算子時，128位計數器應遞增。</span><span class="sxs-lookup"><span data-stu-id="851b9-134">On each execution of this operator, the 128-bit counter should be incremented.</span></span> <span data-ttu-id="851b9-135">如果提供了 *OutputStateTensor* ，則這個運算子會代表您以正確的值遞增計數器，並將結果寫入 *OutputStateTensor*。</span><span class="sxs-lookup"><span data-stu-id="851b9-135">If the *OutputStateTensor* is supplied, THEN this operator increments the counter with the correct value on your behalf, and writes the result into the *OutputStateTensor*.</span></span> <span data-ttu-id="851b9-136">應該遞增的數量取決於所產生的32位輸出元素數目，以及產生器的類型。</span><span class="sxs-lookup"><span data-stu-id="851b9-136">The amount it should be incremented by depends on the number of 32-bit output elements generated, and the type of the generator.</span></span>

<span data-ttu-id="851b9-137">針對 **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**，128位計數器應該 `ceil(outputSize / 4)` 在每次執行時遞增，其中 `outputSize` 是 *OutputTensor* 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="851b9-137">For **DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10**, the 128-bit counter should be incremented by `ceil(outputSize / 4)` on each execution, where `outputSize` is the number of elements in the *OutputTensor*.</span></span>

<span data-ttu-id="851b9-138">假設有一個範例，其中128位計數器的值目前為 `0x48656c6c'6f46726f'6d536561'74746c65` ，而 OutputTensor 的大小為 `{3,3,20,7219}` 。</span><span class="sxs-lookup"><span data-stu-id="851b9-138">Consider an example where the value of the 128-bit counter is currently `0x48656c6c'6f46726f'6d536561'74746c65`, and the OutputTensor's size is `{3,3,20,7219}`.</span></span> <span data-ttu-id="851b9-139">執行這個運算子一次之後，計數器應遞增 324855 (所產生的輸出元素數目除以4，進位) 產生的計數器值 `0x48656c6c'6f46726f'6d536561'746f776e` 。</span><span class="sxs-lookup"><span data-stu-id="851b9-139">After executing this operator once, the counter should be incremented by 324,855 (the number of output elements generated divided by 4, rounded up) resulting in a counter value of `0x48656c6c'6f46726f'6d536561'746f776e`.</span></span> <span data-ttu-id="851b9-140">接著，您應該將這個更新的值做為輸入，提供給這個運算子的下一次執行。</span><span class="sxs-lookup"><span data-stu-id="851b9-140">This updated value should then be supplied as an input for the next execution of this operator.</span></span>

## <a name="availability"></a><span data-ttu-id="851b9-141">可用性</span><span class="sxs-lookup"><span data-stu-id="851b9-141">Availability</span></span>
<span data-ttu-id="851b9-142">這個運算子是在中引進 `DML_FEATURE_LEVEL_3_0` 。</span><span class="sxs-lookup"><span data-stu-id="851b9-142">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="851b9-143">Tensor 條件約束</span><span class="sxs-lookup"><span data-stu-id="851b9-143">Tensor constraints</span></span>
<span data-ttu-id="851b9-144">`InputStateTensor` 和 `OutputStateTensor` 必須有相同的 *大小*。</span><span class="sxs-lookup"><span data-stu-id="851b9-144">`InputStateTensor` and `OutputStateTensor` must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="851b9-145">Tensor 支援</span><span class="sxs-lookup"><span data-stu-id="851b9-145">Tensor support</span></span>
| <span data-ttu-id="851b9-146">張</span><span class="sxs-lookup"><span data-stu-id="851b9-146">Tensor</span></span> | <span data-ttu-id="851b9-147">種類</span><span class="sxs-lookup"><span data-stu-id="851b9-147">Kind</span></span> | <span data-ttu-id="851b9-148">維度</span><span class="sxs-lookup"><span data-stu-id="851b9-148">Dimensions</span></span> | <span data-ttu-id="851b9-149">支援的維度計數</span><span class="sxs-lookup"><span data-stu-id="851b9-149">Supported dimension counts</span></span> | <span data-ttu-id="851b9-150">支援的資料類型</span><span class="sxs-lookup"><span data-stu-id="851b9-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="851b9-151">InputStateTensor</span><span class="sxs-lookup"><span data-stu-id="851b9-151">InputStateTensor</span></span> | <span data-ttu-id="851b9-152">輸入</span><span class="sxs-lookup"><span data-stu-id="851b9-152">Input</span></span> | <span data-ttu-id="851b9-153">{1，1，1，6}</span><span class="sxs-lookup"><span data-stu-id="851b9-153">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="851b9-154">4</span><span class="sxs-lookup"><span data-stu-id="851b9-154">4</span></span> | <span data-ttu-id="851b9-155">UINT32</span><span class="sxs-lookup"><span data-stu-id="851b9-155">UINT32</span></span> |
| <span data-ttu-id="851b9-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="851b9-156">OutputTensor</span></span> | <span data-ttu-id="851b9-157">輸出</span><span class="sxs-lookup"><span data-stu-id="851b9-157">Output</span></span> | <span data-ttu-id="851b9-158">{D0，D1，D2，D3}</span><span class="sxs-lookup"><span data-stu-id="851b9-158">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="851b9-159">4</span><span class="sxs-lookup"><span data-stu-id="851b9-159">4</span></span> | <span data-ttu-id="851b9-160">UINT32</span><span class="sxs-lookup"><span data-stu-id="851b9-160">UINT32</span></span> |
| <span data-ttu-id="851b9-161">OutputStateTensor</span><span class="sxs-lookup"><span data-stu-id="851b9-161">OutputStateTensor</span></span> | <span data-ttu-id="851b9-162">選用輸出</span><span class="sxs-lookup"><span data-stu-id="851b9-162">Optional output</span></span> | <span data-ttu-id="851b9-163">{1，1，1，6}</span><span class="sxs-lookup"><span data-stu-id="851b9-163">{ 1, 1, 1, 6 }</span></span> | <span data-ttu-id="851b9-164">4</span><span class="sxs-lookup"><span data-stu-id="851b9-164">4</span></span> | <span data-ttu-id="851b9-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="851b9-165">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="851b9-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="851b9-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="851b9-167">**標頭**</span><span class="sxs-lookup"><span data-stu-id="851b9-167">**Header**</span></span> | <span data-ttu-id="851b9-168">directml。h</span><span class="sxs-lookup"><span data-stu-id="851b9-168">directml.h</span></span> |