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
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a>DirectML 中的 UAV 障礙和資源狀態阻礙

## <a name="unordered-access-view-uav-barrier-requirements"></a>未排序的存取視圖 (UAV) 關卡需求

### <a name="uav-barriers-in-direct3d-12"></a>Direct3D 12 中的 UAV 障礙

在 Direct3D 12 中，相同命令清單內的相鄰計算著色器分派可在 GPU 上平行執行，除非它們與仲介未排序的存取權 UAV 同步處理， () 關卡。 這可以提高 GPU 硬體的使用率，進而改善效能。 不過，根據預設，如果沒有使用 UAV 屏障，則如果兩個分派之間存在資料相依性，則平行執行兩個連續的分派可能會造成競爭情形。或者，如果兩個分派都執行 UAV 寫入至相同的記憶體區域。

UAV 關卡會強制所有先前提交的分派在 GPU 上完成執行，之後才能開始後續的分派。 UAV 屏障可用來在相同命令清單上的分派之間進行同步處理，以避免資料爭用。 您可以使用 [ **ID3D12GraphicsCommandList：： ResourceBarrier** 方法](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)發出 UAV 關卡。

### <a name="uav-barriers-in-directml"></a>DirectML 中的 UAV 障礙

在 DirectML 中，運算子的分派方式類似于在 Direct3D 12 中分派計算著色器的方式。 亦即，允許連續的運算子分派在 GPU 上平行執行，除非它們之間有中間的 UAV 關卡。 一般機器學習模型包含其運算子之間的資料相依性;例如，某個運算子的輸出會送入另一個運算子的輸入。 因此，請務必使用 UAV 障礙正確地同步處理分派。

DirectML 保證它只會從 (讀取，且永遠不會寫入) 的輸入張量。 此外，它也保證永遠不會製造在 tensor 的 [**DML_BUFFER_TENSOR_DESC：： TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) 成員範圍之外的輸出 tensor 寫入。 這表示在 DirectML 中的運算子之間的資料相依性，只能透過查看運算子的輸入和輸出系結來再則。

例如，這些保證可讓您分派兩個運算子，以系結資源的相同區域作為輸入，而不需要發出仲介 UAV 關卡。 這一律是安全的，因為 DirectML 絕不會寫入至輸入張量。 另一個範例是，只要將兩個並行運算子分派的輸出張量系結至相同的 Direct3D 12 資源 (，只要它們的張量不會重迭) ，因為 DirectML 絕不會寫出 tensor (的界限，如 tensor 的 **DML_BUFFER_TENSOR_DESC：： TotalTensorSizeInBytes**) 所定義。

由於 UAV 障礙是一種同步處理的形式，因此不必要使用 UAV 障礙可能會對效能造成負面影響。 因此，您最好使用正確地同步處理命令清單內的分派所需的最少 UAV 障礙。

### <a name="example-1"></a>範例 1

在下列範例中，會將卷積運算子的輸出送入 ReLU 啟用，然後再進行批次正規化。

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

因為所有三個運算子之間都有資料相依性，所以您需要每個後續分派之間的 UAV 屏障 (請參閱 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)) 。

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
2. `d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`
4. `d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`
5. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`

### <a name="example-2"></a>範例 2

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

在這裡，共用的輸出會送入兩個迴旋，然後使用聯結運算子將輸出串連在一起。 和兩者之間都有資料相依性，以及和和兩者之間的相依性 `pool1` `conv1` `conv2` `conv1` `conv2` `join1` 。 以下是一個執行此圖形的有效方式。

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`
2. `d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
4. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**>conv2**`)`
5. `d3d12CommandList->ResourceBarrier(`**UAV 關卡**`)`
6. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**join1**`)`

在此情況下， `conv1` 和 `conv2` 能夠同時在 GPU 上執行，這可能會改善效能。

## <a name="resource-barrier-state-requirements"></a>資源屏障狀態需求

身為呼叫者，您必須負責確保所有 Direct3D 12 資源在 GPU 上執行 DirectML 分派之前都處於正確的資源屏障狀態。 DirectML 不會代表您執行任何轉換阻礙。

在 GPU 上執行 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) 之前，您必須將所有的系結資源轉換為 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態，或轉換成可隱含提升為 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 的狀態，例如 **D3D12_RESOURCE_STATE_COMMON**。 此呼叫完成後，資源會維持 **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** 狀態。 如需詳細資訊，請參閱 [DirectML 中](dml-binding.md)的系結。

## <a name="see-also"></a>另請參閱

* [在 Direct3D 12 中使用資源阻礙來同步處理資源狀態](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [在 DirectML 中繫結](dml-binding.md)
