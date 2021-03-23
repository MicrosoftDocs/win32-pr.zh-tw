---
title: 資源存留期和同步處理
description: 為了避免未定義的行為，您的 DirectML 應用程式必須正確地管理 CPU 與 GPU 之間的物件存留期和同步處理。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 6e8ab30c5c87c135ef3bdac0c1bc2a3d64040787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104031"
---
# <a name="resource-lifetime-and-synchronization"></a>資源存留期和同步處理

如同 Direct3D 12，您的 DirectML 應用程式必須 (，才能避免未定義的行為) 正確地管理 CPU 與 GPU 之間的物件存留期和同步處理。 DirectML 會遵循與 Direct3D 12 相同的資源存留期模型。

- 使用強式參考計數的 DirectML 會維護兩個 CPU 物件之間的存留期相依性。 您的應用程式不會手動管理 CPU 存留期相依性。 例如，每個子裝置都會保存其父裝置的強式參考。
- GPU 物件或跨 CPU 和 GPU 的相依性之間的存留期相依性 &mdash; &mdash; 不會自動受到管理。 您的應用程式必須負責確保 GPU 資源至少存留到所有使用該資源的工作在 GPU 上執行完畢。

## <a name="directml-devices"></a>DirectML 裝置

DirectML 裝置是安全線程的無狀態 factory 物件。 每個子裝置 (查看 [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmldevicechild)) 保存其父 DirectML 裝置的強式參考 (查看 [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice)) 。 這表示您一律可以從任何裝置子介面取出父裝置介面。

接著，DirectML 裝置會保存用來建立它之 Direct3D 12 裝置的強式參考 (請參閱 [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)和衍生介面) 。

因為 DirectML 裝置是無狀態的，所以它是隱含執行緒安全的。 您可以同時從多個執行緒呼叫 DirectML 裝置上的方法，而不需要外部同步處理。

不過，與 Direct3D 12 裝置不同的是，DirectML 裝置不是單一物件。 您可以視需要任意建立多個 DirectML 裝置。 不過，您不能混搭屬於不同裝置的裝置子系。 例如， [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) 和 [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) 是兩種裝置子系 (這兩個介面都是直接或間接衍生自 **IDMLDeviceChild**) 。 當運算子和系結資料表屬於不同的 DirectML 裝置實例時，您可能不會使用系結表 (**IDMLBindingTable**) 系結 (**IDMLCompiledOperator**) 。

由於 DirectML 裝置不是單一裝置，因此裝置移除會以每個裝置為基礎，而不是整個進程的事件，因為它適用于 Direct3D 12 裝置。 如需詳細資訊，請參閱 [在 DirectML 中處理錯誤和移除裝置](dml-errors.md)。

## <a name="lifetime-requirements-of-gpu-resources"></a>GPU 資源的存留期需求

和 Direct3D 12 一樣，DirectML 不會自動在 CPU 與 GPU 之間進行同步處理。此外，它也不會在 GPU 使用資源時，自動將資源保持在運作狀態。 相反地，這些是您應用程式的責任。

執行包含 DirectML 分派的命令清單時，您的應用程式必須確保 GPU 資源保持運作，直到使用這些資源的所有工作都已在 GPU 上執行完畢為止。

若為 DirectML 運算子的 [**IDMLCommandRecorder：： RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) ，其中包含下列物件。

-  (或 [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)執行的 [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)會改為執行) 的運算子初始化。
- **IDMLCompiledOperator** 支援用來系結運算子的系結資料表。
- 系結為運算子之輸入/輸出的 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 物件。
- 系結為持續性和暫存資源的 **ID3D12Resource** 物件（如果適用）。
- 支援命令清單本身的 [**ID3D12CommandAllocator**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator) 。

並非所有 DirectML 介面都代表 GPU 資源。 例如，系結資料表 *不* 需要保持運作，直到使用它的所有分派都已在 GPU 上完成執行為止。 這是因為系結資料表本身不會擁有任何 GPU 資源。 相反地，描述項堆積會執行。 因此，基礎 *描述元堆積* 是必須保持運作，直到執行完成為止，而不是系結資料表本身的物件。

Direct3D 12 中有類似的概念。 *命令配置* 器必須保持運作，直到所有使用它的執行都已在 GPU 上完成為止;因為它擁有 GPU 記憶體。 但是，命令 *清單* 不會擁有 GPU 記憶體，因此可以在提交執行時立即重設或釋放。

在 DirectML 中，編譯的運算子 ([**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)) 和運算子初始化運算式 ([**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)) 直接的 gpu 資源，因此必須保持運作，直到使用它們的所有分派都已在 GPU 上完成執行為止。 此外，使用 (命令配置器、描述元堆積、緩衝區) 的任何 Direct3D 12 資源，都必須以同樣的方式，讓應用程式保持運作。

如果您在 GPU 仍在使用時，提前釋出物件，結果會是未定義的行為，這可能會導致裝置移除或其他錯誤。

## <a name="cpu-and-gpu-synchronization"></a>CPU 和 GPU 同步處理

DirectML 本身不會提交在 GPU 上執行的任何工作。 相反地， [ **IDMLCommandRecorder：： RecordDispatch** 方法](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)會將該工作的分派 *記錄* 到命令清單中，以供稍後執行。 然後，您的應用程式必須藉由呼叫 [**ID3D12CommandQueue：： ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)（如同任何 Direct3D 12 命令清單）來關閉並提交其命令清單以供執行。

因為 DirectML 本身不會提交任何在 GPU 上執行的工作，所以它也不會建立任何 GPU，也不會代表您執行任何形式的 CPU/GPU 同步處理。 您的應用程式必須負責使用適當的 Direct3D 12 基本專案，以等候提交的工作在 GPU 上完成執行（如有必要）。 如需詳細資訊，請參閱 [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) 和 [**ID3D12CommandQueue：：信號**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal)。

## <a name="see-also"></a>另請參閱

* [執行和同步處理命令清單](/windows/desktop/direct3d12/executing-and-synchronizing-command-lists)
* [處理 DirectML 中的錯誤和裝置移除](dml-errors.md)