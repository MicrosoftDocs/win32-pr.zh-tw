---
title: Direct3D 12 interop
description: D3D12 可以用來撰寫元件化應用程式。
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548460"
---
# <a name="direct3d-12-interop"></a>Direct3D 12 interop

D3D12 可以用來撰寫元件化應用程式。

-   [Interop 總覽](#interop-overview)
-   [使用 interop 的原因](#reasons-for-using-interop)
    -   [共用命令清單](#sharing-a-command-list)
    -   [共用命令佇列](#sharing-a-command-queue)
    -   [共用同步處理基本專案](#sharing-sync-primitives)
    -   [共用資源](#sharing-resources)
    -   [選擇 interop 模型](#choosing-an-interop-model)
-   [Interop Api](#interop-apis)
-   [相關主題](#related-topics)

## <a name="interop-overview"></a>Interop 總覽

D3D12 可能非常強大，而且可讓應用程式使用類似主控台的效率來撰寫圖形程式碼，但並非每個應用程式都需要重新編寫輪子並從頭撰寫整個轉譯引擎。 在某些情況下，另一個元件或程式庫已經更妥善地執行，或在其他情況下，部分程式碼的效能並不像正確性和可讀性那麼重要。

本節涵蓋下列 interop 技術：

-   在相同裝置上的 D3D12 和 D3D12
-   在不同裝置上的 D3D12 和 D3D12
-   相同裝置上的 D3D12 和 D3D11、D3D10 或 D2D 的任意組合
-   不同裝置上的 D3D12 和 D3D11、D3D10 或 D2D 的任意組合
-   D3D12 和 GDI，或 D3D12 和 D3D11 和 GDI

## <a name="reasons-for-using-interop"></a>使用 interop 的原因

有幾個原因會讓應用程式 D3D12 interop 與其他 Api。 以下是一些範例：

-   增量移植：希望將整個應用程式從 D3D10 或 D3D11 移植到 D3D12，同時讓它在移植程式的中繼階段運作 (，以啟用) 的測試和偵錯工具。
-   黑色方塊代碼：希望應用程式的特定部分保持原狀，同時移植其餘程式碼。 例如，可能不需要將遊戲的 UI 元素移植。
-   無法變更的元件：需要使用不是由應用程式所擁有的元件，而這些元件不會寫入目標 D3D12。
-   新的元件：不希望移植整個應用程式，而是想要使用以 D3D12 撰寫的新元件。

在 D3D12 中，interop 有四種主要的方法：

-   應用程式可以選擇將開啟的命令清單提供給元件，該元件會將一些額外的轉譯命令記錄至已系結的呈現目標。 這相當於提供備妥的裝置內容給 D3D11 中的另一個元件，很適合用來將 UI/文字新增至已系結的背景緩衝區。
-   應用程式可以選擇提供命令佇列給元件，以及所需的目的地資源。 這相當於在 D3D11 中使用 [**ClearState**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) 或 [**DeviceCoNtextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) api，以提供乾淨的裝置內容給另一個元件。 這就是像是 D2D 的元件的運作方式。
-   元件可以選擇一個模型，它會產生一個命令清單（可能會以平行方式處理，而應用程式會負責稍後提交）。 必須在元件界限之間提供至少一個資源。 使用延遲的內容可以在 D3D11 中使用這個相同的技術，不過 D3D12 中的效能比較理想。
-   每個元件都有自己的佇列 (s) 和/或裝置 (s) ，而應用程式和元件則需要跨元件界限共用資源和同步處理資訊。 這與舊版 `ISurfaceQueue` 和新式 [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)相似。

這些案例之間的差異在於元件界限之間的共用。 裝置會假設為共用，但因為它基本上是無狀態的，所以並不是真正相關。 索引鍵物件是命令清單、命令佇列、同步物件和資源。 在共用它們時，每一個都有自己的複雜。

### <a name="sharing-a-command-list"></a>共用命令清單

Interop 的最簡單方法只需要與部分引擎共用命令清單。 完成轉譯作業之後，命令清單擁有權會傳回給呼叫者。 您可以透過堆疊追蹤命令清單的擁有權。 由於命令清單是單一執行緒，因此應用程式無法使用這項技術來進行獨特或創新的作業。

### <a name="sharing-a-command-queue"></a>共用命令佇列

在相同的程式中共用裝置的多個元件可能是最常見的技巧。

當命令佇列是共用的單位時，需要呼叫元件，讓它知道所有未處理的命令清單都必須立即提交到命令佇列 (而且任何內部命令佇列都必須) 同步處理。 這相當於 D3D11 [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) API，它是應用程式可以提交自己的命令清單或同步處理基本專案的唯一方式。

### <a name="sharing-sync-primitives"></a>共用同步處理基本專案

在其本身的裝置及/或命令佇列上運作的元件預期模式是接受 [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) 或共用的控制碼，並在開始其工作時使用 uint64 組（它會等待，然後是第二個 ID3D12Fence 或共用的控制碼），以及 uint64 組（當所有工作都完成時，它會發出信號）。 這個模式會比對 [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) 和 DWM/DXGI 翻轉模型同步處理設計的目前實作為。

### <a name="sharing-resources"></a>共用資源

到目前為止，撰寫 D3D12 應用程式以利用多個元件最複雜的部分，就是如何處理跨元件界限共用的資源。 這主要是因為資源狀態的概念。 雖然資源狀態設計的某些層面是為了處理命令清單間的同步處理，但有些層面會影響命令清單，而影響資源配置以及存取資源資料的一組有效作業或效能特性。

有兩種模式可處理這種複雜的情況，這兩種模式基本上牽涉到元件之間的合約。

-   合約可以由元件開發人員定義並記載。 這可能會像是「工作開始時，資源必須處於預設狀態，並會在工作完成時恢復為預設狀態」，或是有更複雜的規則，以允許共用深度緩衝區，而不需要強制進行中繼深度解析。
-   合約可在執行時間由應用程式定義，同時在元件界限之間共用資源。 它是由相同的兩項資訊所組成：當元件開始使用資源時，該資源將在其中的狀態，以及元件在完成時應保留的狀態。

### <a name="choosing-an-interop-model"></a>選擇 interop 模型

針對大部分的 D3D12 應用程式，共用命令佇列可能是理想的模型。 它可讓工作建立和提交擁有完整的擁有權，而不需要額外的記憶體額外負荷，因為有多餘的佇列，而且沒有處理 GPU 同步處理基本專案的效能影響。

當元件需要處理不同的佇列屬性（例如類型或優先順序），或一旦共用需要跨越進程界限時，就需要共用同步處理基本專案。

協力廠商元件無法從外部使用共用或產生命令清單，但可能廣泛地用於遊戲引擎內部的元件中。

## <a name="interop-apis"></a>Interop Api

《 [Direct3D 11 on 12](./direct3d-11-on-12.md) 》主題將逐步引導您使用與本主題中所述之互操作類型相關的大部分 API 介面。

另請參閱 [ID3D12Device：： CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) 方法，您可以使用此方法，在 Windows 圖形 api 之間共用表面。

## <a name="related-topics"></a>相關主題

* [瞭解 Direct3D 12](directx-12-getting-started.md)
* [使用 Direct3D 11、Direct3D 10 和 Direct2D](direct3d-12-interop.md)
* [Direct3D 11 on 12](./direct3d-11-on-12.md)