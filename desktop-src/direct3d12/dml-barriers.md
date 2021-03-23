---
title: DirectML 中的 UAV 障礙和資源狀態阻礙
description: 描述阻礙的正確性優點，以及如何在 DirectML 中使用它們。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 9bfc93d4fb28cff5d7d196287c6573e3e494d1d5
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548399"
---
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a><span data-ttu-id="faeba-103">DirectML 中的 UAV 障礙和資源狀態阻礙</span><span class="sxs-lookup"><span data-stu-id="faeba-103">UAV barriers and resource state barriers in DirectML</span></span>

## <a name="unordered-access-view-uav-barrier-requirements"></a><span data-ttu-id="faeba-104">未排序的存取視圖 (UAV) 關卡需求</span><span class="sxs-lookup"><span data-stu-id="faeba-104">Unordered Access View (UAV) barrier requirements</span></span>

### <a name="uav-barriers-in-direct3d-12"></a><span data-ttu-id="faeba-105">Direct3D 12 中的 UAV 障礙</span><span class="sxs-lookup"><span data-stu-id="faeba-105">UAV barriers in Direct3D 12</span></span>

<span data-ttu-id="faeba-106">在 Direct3D 12 中，相同命令清單內的相鄰計算著色器分派可在 GPU 上平行執行，除非它們與仲介未排序的存取權 UAV 同步處理， () 關卡。</span><span class="sxs-lookup"><span data-stu-id="faeba-106">In Direct3D 12, adjacent compute shader dispatches within the same command list are permitted to execute in parallel on the GPU unless they're synchronized with an intervening unordered access view (UAV) barrier.</span></span> <span data-ttu-id="faeba-107">這可以提高 GPU 硬體的使用率，進而改善效能。</span><span class="sxs-lookup"><span data-stu-id="faeba-107">This can improve performance by increasing utilization of GPU hardware.</span></span> <span data-ttu-id="faeba-108">不過，根據預設，如果沒有使用 UAV 屏障，則如果兩個分派之間存在資料相依性，則平行執行兩個連續的分派可能會造成競爭情形。或者，如果兩個分派都執行 UAV 寫入至相同的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="faeba-108">However, by default, without the use of a UAV barrier, the parallel execution of two adjacent dispatches can cause a race condition if there exists a data dependency between the two dispatches; or if both dispatches perform UAV writes to the same regions of memory.</span></span>

<span data-ttu-id="faeba-109">UAV 關卡會強制所有先前提交的分派在 GPU 上完成執行，之後才能開始後續的分派。</span><span class="sxs-lookup"><span data-stu-id="faeba-109">A UAV barrier forces all previously-submitted dispatches to complete exection on the GPU before subsequent dispatches may begin.</span></span> <span data-ttu-id="faeba-110">UAV 屏障可用來在相同命令清單上的分派之間進行同步處理，以避免資料爭用。</span><span class="sxs-lookup"><span data-stu-id="faeba-110">UAV barriers are used to synchronize between dispatches on the same command list to avoid data races.</span></span> <span data-ttu-id="faeba-111">您可以使用 [ **ID3D12GraphicsCommandList：： ResourceBarrier** 方法](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)發出 UAV 關卡。</span><span class="sxs-lookup"><span data-stu-id="faeba-111">You can issue a UAV barrier by using the [**ID3D12GraphicsCommandList::ResourceBarrier** method](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>

### <a name="uav-barriers-in-directml"></a><span data-ttu-id="faeba-112">DirectML 中的 UAV 障礙</span><span class="sxs-lookup"><span data-stu-id="faeba-112">UAV barriers in DirectML</span></span>

<span data-ttu-id="faeba-113">在 DirectML 中，運算子的分派方式類似于在 Direct3D 12 中分派計算著色器的方式。</span><span class="sxs-lookup"><span data-stu-id="faeba-113">In DirectML, operators are dispatched in a way that's similar to the way compute shaders are dispatched in Direct3D 12.</span></span> <span data-ttu-id="faeba-114">亦即，允許連續的運算子分派在 GPU 上平行執行，除非它們之間有中間的 UAV 關卡。</span><span class="sxs-lookup"><span data-stu-id="faeba-114">That is, adjacent dispatches of operators are permitted to execute in parallel on the GPU unless there exists an intervening UAV barrier between them.</span></span> <span data-ttu-id="faeba-115">一般機器學習模型包含其運算子之間的資料相依性;例如，某個運算子的輸出會送入另一個運算子的輸入。</span><span class="sxs-lookup"><span data-stu-id="faeba-115">A typical machine learning model contains data dependencies between its operators; for instance, the output of one operator feeds into the input of another.</span></span> <span data-ttu-id="faeba-116">因此，請務必使用 UAV 障礙正確地同步處理分派。</span><span class="sxs-lookup"><span data-stu-id="faeba-116">It's therefore important to use UAV barriers to correctly synchronize dispatches.</span></span>

<span data-ttu-id="faeba-117">DirectML 保證它只會從 (讀取，且永遠不會寫入) 的輸入張量。</span><span class="sxs-lookup"><span data-stu-id="faeba-117">DirectML guarantees that it will only ever read from (and never write to) input tensors.</span></span> <span data-ttu-id="faeba-118">此外，它也保證永遠不會製造在 tensor 的 [**DML_BUFFER_TENSOR_DESC：： TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) 成員範圍之外的輸出 tensor 寫入。</span><span class="sxs-lookup"><span data-stu-id="faeba-118">It also guarantees that it will never manufacture writes to an output tensor outside the range of the tensor's [**DML_BUFFER_TENSOR_DESC::TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) member.</span></span> <span data-ttu-id="faeba-119">這表示在 DirectML 中的運算子之間的資料相依性，只能透過查看運算子的輸入和輸出系結來再則。</span><span class="sxs-lookup"><span data-stu-id="faeba-119">This means that data dependencies between operators in DirectML can be reasoned about by looking only at an operator's input and output bindings.</span></span>

<span data-ttu-id="faeba-120">例如，這些保證可讓您分派兩個運算子，以系結資源的相同區域作為輸入，而不需要發出仲介 UAV 關卡。</span><span class="sxs-lookup"><span data-stu-id="faeba-120">For example, these guarantees allow you to dispatch two operators that bind the same region of a resource as an input, without having to issue an intervening UAV barrier.</span></span> <span data-ttu-id="faeba-121">這一律是安全的，因為 DirectML 絕不會寫入至輸入張量。</span><span class="sxs-lookup"><span data-stu-id="faeba-121">This is always safe because DirectML never writes to input tensors.</span></span> <span data-ttu-id="faeba-122">另一個範例是，只要將兩個並行運算子分派的輸出張量系結至相同的 Direct3D 12 資源 (，只要它們的張量不會重迭) ，因為 DirectML 絕不會寫出 tensor (的界限，如 tensor 的 **DML_BUFFER_TENSOR_DESC：： TotalTensorSizeInBytes**) 所定義。</span><span class="sxs-lookup"><span data-stu-id="faeba-122">As another example, it's always safe to bind the output tensors of two concurrent operator dispatches to the same Direct3D 12 resource (so long as their tensors don't overlap), because DirectML never writes outside the bounds of a tensor (as defined by the tensor's **DML_BUFFER_TENSOR_DESC::TotalTensorSizeInBytes**).</span></span>

<span data-ttu-id="faeba-123">由於 UAV 障礙是一種同步處理的形式，因此不必要使用 UAV 障礙可能會對效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="faeba-123">As UAV barriers are a form of synchronization, unnecessary use of UAV barriers might negatively impact performance.</span></span> <span data-ttu-id="faeba-124">因此，您最好使用正確地同步處理命令清單內的分派所需的最少 UAV 障礙。</span><span class="sxs-lookup"><span data-stu-id="faeba-124">Therefore, it's best for you to use the minimum number of UAV barriers necessary to correctly synchronize the dispatches within a command list.</span></span>

### <a name="example-1"></a><span data-ttu-id="faeba-125">範例 1</span><span class="sxs-lookup"><span data-stu-id="faeba-125">Example 1</span></span>

<span data-ttu-id="faeba-126">在下列範例中，會將卷積運算子的輸出送入 ReLU 啟用，然後再進行批次正規化。</span><span class="sxs-lookup"><span data-stu-id="faeba-126">In the following example, a convolution operator's output is fed into a ReLU activation, followed by a batch normalization.</span></span>

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

<span data-ttu-id="faeba-127">因為所有三個運算子之間都有資料相依性，所以您需要每個後續分派之間的 UAV 屏障 (請參閱 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)) 。</span><span class="sxs-lookup"><span data-stu-id="faeba-127">Since a data dependency exists between all three operators, you'll need a UAV barrier between each successive dispatch (see [**IDMLCommandRecorder::RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)).</span></span>

1. <span data-ttu-id="faeba-128">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-128">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`</span></span>
2. <span data-ttu-id="faeba-129">`d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-129">`d3d12CommandList->ResourceBarrier(`**UAV barrier**`)`</span></span>
3. <span data-ttu-id="faeba-130">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-130">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`</span></span>
4. <span data-ttu-id="faeba-131">`d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-131">`d3d12CommandList->ResourceBarrier(`**UAV barrier**`)`</span></span>
5. <span data-ttu-id="faeba-132">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-132">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`</span></span>

### <a name="example-2"></a><span data-ttu-id="faeba-133">範例 2</span><span class="sxs-lookup"><span data-stu-id="faeba-133">Example 2</span></span>

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

<span data-ttu-id="faeba-134">在這裡，共用的輸出會送入兩個迴旋，然後使用聯結運算子將輸出串連在一起。</span><span class="sxs-lookup"><span data-stu-id="faeba-134">Here the output of pooling is fed into two convolutions, whose outputs are then concatenated together using the JOIN operator.</span></span> <span data-ttu-id="faeba-135">和兩者之間都有資料相依性，以及和和兩者之間的相依性 `pool1` `conv1` `conv2` `conv1` `conv2` `join1` 。</span><span class="sxs-lookup"><span data-stu-id="faeba-135">A data dependency exists between `pool1` and both `conv1` and `conv2`; as well as between both `conv1` and `conv2` and `join1`.</span></span> <span data-ttu-id="faeba-136">以下是一個執行此圖形的有效方式。</span><span class="sxs-lookup"><span data-stu-id="faeba-136">Here's one valid way to execute this graph.</span></span>

1. <span data-ttu-id="faeba-137">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-137">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`</span></span>
2. <span data-ttu-id="faeba-138">`d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-138">`d3d12CommandList->ResourceBarrier(`**UAV barrier**`)`</span></span>
3. <span data-ttu-id="faeba-139">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-139">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`</span></span>
4. <span data-ttu-id="faeba-140">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**>conv2**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-140">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv2**`)`</span></span>
5. <span data-ttu-id="faeba-141">`d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-141">`d3d12CommandList->ResourceBarrier(`**UAV barrier**`)`</span></span>
6. <span data-ttu-id="faeba-142">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**join1**`)`</span><span class="sxs-lookup"><span data-stu-id="faeba-142">`dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**join1**`)`</span></span>

<span data-ttu-id="faeba-143">在此情況下， `conv1` 和 `conv2` 能夠同時在 GPU 上執行，這可能會改善效能。</span><span class="sxs-lookup"><span data-stu-id="faeba-143">In this case, `conv1` and `conv2` are able to execute concurrently on the GPU, which may improve performance.</span></span>

## <a name="resource-barrier-state-requirements"></a><span data-ttu-id="faeba-144">資源屏障狀態需求</span><span class="sxs-lookup"><span data-stu-id="faeba-144">Resource barrier state requirements</span></span>

<span data-ttu-id="faeba-145">身為呼叫者，您必須負責確保所有 Direct3D 12 資源在 GPU 上執行 DirectML 分派之前都處於正確的資源屏障狀態。</span><span class="sxs-lookup"><span data-stu-id="faeba-145">As the caller, it's your responsibility to ensure that all Direct3D 12 resources are in the correct resource barrier state prior to executing DirectML dispatches on the GPU.</span></span> <span data-ttu-id="faeba-146">DirectML 不會代表您執行任何轉換阻礙。</span><span class="sxs-lookup"><span data-stu-id="faeba-146">DirectML doesn't perform any transition barriers on your behalf.</span></span>

<span data-ttu-id="faeba-147">在 GPU 上執行 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) 之前，您必須將所有的系結資源轉換為 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態，或轉換成可隱含提升為 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 的狀態，例如 **D3D12_RESOURCE_STATE_COMMON**。</span><span class="sxs-lookup"><span data-stu-id="faeba-147">Prior to execution of [**IDMLCommandRecorder::RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) on the GPU, you must transition all bound resources to the **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** state, or to a state implicitly promotable to **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, such as **D3D12_RESOURCE_STATE_COMMON**.</span></span> <span data-ttu-id="faeba-148">此呼叫完成後，資源會維持 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態。</span><span class="sxs-lookup"><span data-stu-id="faeba-148">After this call completes, the resources remain in the **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** state.</span></span> <span data-ttu-id="faeba-149">如需詳細資訊，請參閱 [DirectML 中](dml-binding.md)的系結。</span><span class="sxs-lookup"><span data-stu-id="faeba-149">For more details, see [Binding in DirectML](dml-binding.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="faeba-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faeba-150">See also</span></span>

* [<span data-ttu-id="faeba-151">在 Direct3D 12 中使用資源阻礙來同步處理資源狀態</span><span class="sxs-lookup"><span data-stu-id="faeba-151">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [<span data-ttu-id="faeba-152">在 DirectML 中繫結</span><span class="sxs-lookup"><span data-stu-id="faeba-152">Binding in DirectML</span></span>](dml-binding.md)
