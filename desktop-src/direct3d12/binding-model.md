---
title: 來自 Direct3D 11 的系結模型差異
description: DirectX12 系結背後的主要設計決策之一，是將它與其他管理工作分開。 這會在應用程式上放置一些需求，以管理特定潛在的風險。
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a625bd1b79766990658feba9bf18ddf7f46c3788ca20aea1de0b4ab80ae0a71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632519"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>來自 Direct3D 11 的系結模型差異

DirectX12 系結背後的主要設計決策之一，是將它與其他管理工作分開。 這會在應用程式上放置一些需求，以管理特定潛在的風險。

D3D12 系結模型的主要優點是，它可讓應用程式經常變更材質系結，而不會有很大的 CPU 效能成本。 其他優點是著色器可以存取非常大量的資源、著色器不需要事先知道要系結的資源數量，而且不論硬體或應用程式內容流程為何，都可以使用統一的資源系結模型。

為了改善效能，系結模型不會要求系統追蹤應用程式要求 GPU 使用的系結，而且系結和多執行緒命令清單之間有乾淨的整合。

下列各節將列出自 D3D11 之後的一些資源系結模型變更。

-   [記憶體常駐管理與系結分開](#memory-residency-management-separated-from-binding)
-   [物件存留期管理與系結分開](#object-lifetime-management-separated-from-binding)
-   [與系結分開的驅動程式資源狀態追蹤](#driver-resource-state-tracking-separated-from-binding)
-   [CPU GPU 對應記憶體同步處理與系結分開](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [相關主題](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>記憶體常駐管理與系結分開

應用程式可以明確控制哪些表面必須可用來讓 GPU 直接使用 (稱為「常駐」 ) 。 相反地，他們可以在資源上套用其他狀態，例如明確地將它們設為非常駐，或讓作業系統選擇需要最少記憶體使用量的特定應用程式類別。 這裡的重點是，應用程式的「常駐」管理與它如何提供資源的存取權給著色器完全分離。

從提供著色器存取資源的機制中分離常駐管理，可減少轉譯的系統/硬體成本，因為作業系統不需要持續檢查本機系結狀態，就能知道要做什麼。 此外，著色器不再需要知道它們可能需要參考的確切表面，只要經過一組可能可存取的資源，就會事先進行。

## <a name="object-lifetime-management-separated-from-binding"></a>物件存留期管理與系結分開

不同于先前的 Api，系統不會再追蹤資源系結至管線。 這是用來讓系統維持應用程式發行的存留資源，因為這些資源仍是由未處理的 GPU 工作所參考。

在釋放任何資源（例如紋理）之前，應用程式現在必須確定 GPU 已完成參考。 這表示在應用程式可以安全地釋放資源之前，GPU 必須已完成執行參考資源的命令清單。

## <a name="driver-resource-state-tracking-separated-from-binding"></a>與系結分開的驅動程式資源狀態追蹤

系統不會再檢查資源系結，以瞭解何時發生資源轉換，需要額外的驅動程式或 GPU 工作。 許多 Gpu 和驅動程式的常見範例，都必須知道介面從何種轉換成轉譯目標視圖時 (RTV) 至著色器資源檢視 (SRV) 。 應用程式本身現在必須識別系統可能在意的任何資源轉換是透過專用的 Api 發生。

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>CPU GPU 對應記憶體同步處理與系結分開

系統不會再檢查資源系結，以瞭解轉譯是否需要延遲，因為它相依于已對應以進行 CPU 存取但尚未對應的資源。 應用程式現在必須負責同步處理 CPU 和 GPU 記憶體存取。 為了協助解決這個情況，系統會提供機制讓應用程式要求睡眠中的 CPU 執行緒，直到工作完成為止。 輪詢也可以完成，但效率可能較低。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資源系結](resource-binding.md)
</dt> </dl>

 

 




