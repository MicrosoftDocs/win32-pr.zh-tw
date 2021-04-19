---
title: DirectML 介面
description: 下列介面是在 DirectML 中宣告。
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 9752b52f1d9a311a1ada6b609a86691a336b77e7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "106976347"
---
# <a name="directml-interfaces"></a>DirectML 介面

下列介面是在 DirectML 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | 為指定的 Direct3D 12 裝置建立 DirectML 裝置。 |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | 將 DirectML 工作的分派記錄至 Direct3D 12 命令清單。 |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | 代表適合在 GPU 上執行的已編譯、有效率的運算子形式。 |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | 控制 DirectML 的調試層。 |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | 代表用來建立運算子、系結資料表、命令記錄器和其他物件的 DirectML 裝置。 |
| [**IDMLDevice1**](/windows/desktop/direct3d12/directml/nn-directml-idmldevice1) | 代表用來建立運算子、系結資料表、命令記錄器和其他物件的 DirectML 裝置。 |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | 由 DirectML 裝置建立的所有物件所執行的介面。 |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | 由可記錄到命令清單中的物件所執行，以便在 GPU 上使用 [IDMLCommandRecorder：： RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)進行分派。 |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)和[IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild)直接繼承 (和所有其他介面的介面，間接) 。 因此，它會提供所有 DirectML 介面通用的方法，特別是用來建立私用資料相關聯的方法，以及為物件名稱加上批註。 |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | 表示 DirectML 運算子。 |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | 表示專門用來初始化編譯運算子的特殊物件。 |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | 由可以從 GPU 記憶體收回的物件所執行，因此可提供給 [IDMLDevice：：收回](/windows/desktop/api/directml/nf-directml-idmldevice-evict) 和 [IDMLDevice：： MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident)。 |

## <a name="related-topics"></a>相關主題

* [DirectML 參考](direct3d-directml-reference.md)
* [核心參考](direct3d-12-core-reference.md)
* [Direct3D 12 參考](direct3d-12-reference.md)
