---
title: Direct3D 11 中的多執行緒簡介
description: 多執行緒的設計目的是要使用一或多個執行緒同時執行工作，以改善效能。
ms.assetid: b4bef1e4-8d34-455c-8aed-01af974c66c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527b78d8b29a507247c8eb067c20739004ace687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315199"
---
# <a name="introduction-to-multithreading-in-direct3d-11"></a>Direct3D 11 中的多執行緒簡介

多執行緒的設計目的是要使用一或多個執行緒同時執行工作，以改善效能。

在過去，這通常是藉由產生單一主執行緒來進行轉譯，以及一或多個執行緒來執行準備工作（例如物件建立、載入、處理等）。 不過，使用 Direct3D 11 內建的同步處理功能時，多執行緒處理背後的目標是要利用每個 CPU 和 GPU 迴圈，而不需讓處理器等待另一個處理器 (特別是因為它會直接影響畫面播放速率) 。 如此一來，您就可以產生最大量的工作，同時維持最佳的畫面播放速率。 因為 API 會執行同步處理，所以不再需要呈現單一框架的概念。

多執行緒需要某種形式的同步處理。 例如，如果在應用程式中執行的多個執行緒必須存取單一裝置內容 ([**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) ，則該應用程式必須使用某些同步處理機制（例如重要區段）來同步存取該裝置內容。 這是因為處理轉譯命令 (通常是在 GPU) 上執行，並產生轉譯命令 (通常是透過建立物件、資料載入、狀態變更、資料處理) 在 CPU 上進行的處理，通常會使用相同的資源 (紋理、著色器、管線狀態等等) 。 跨多個執行緒組織工作需要進行同步處理，以防止某個執行緒修改或讀取其他執行緒正在修改的資料。

雖然使用裝置內容 ([**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) 不是安全線程，但使用 Direct3D 11 裝置 ([**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 是安全線程。 因為每個 **>id3d11devicecoNtext** 都是單一執行緒，所以一次只能有一個執行緒可以呼叫 **>id3d11devicecoNtext** 。 如果多個執行緒必須存取單一 **>id3d11devicecoNtext**，則必須使用某些同步處理機制（例如重要區段）來同步處理對該 **>id3d11devicecoNtext** 的存取。 但是，不需要使用多個執行緒來使用重要區段或同步處理原始物件來存取單一 **ID3D11Device**。 因此，如果應用程式使用 **ID3D11Device** 來建立資源物件，則該應用程式不需要同時使用同步處理來建立多個資源物件。

多執行緒支援將 API 分成兩個不同的功能區域：

-   [使用多執行緒建立物件](overviews-direct3d-11-render-multi-thread-create.md)
-   [立即和延後轉譯](overviews-direct3d-11-render-multi-thread-render.md)

多執行緒效能取決於驅動程式支援。 [如何：檢查驅動程式支援](overviews-direct3d-11-render-multi-thread-support.md) 提供有關查詢驅動程式的詳細資訊，以及結果的意義。

Direct3D 11 已從頭開始設計來支援多執行緒處理。 Direct3D 10 使用 [安全線程層](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers)級，對多執行緒執行的支援有限。 此頁面會列出兩個 DirectX 版本之間的行為差異： [Direct3D 版本之間的執行緒差異](overviews-direct3d-11-render-multi-thread-differences.md)。

## <a name="multithreading-and-dxgi"></a>多執行緒和 DXGI

一次只能有一個執行緒使用立即內容。 不過，您的應用程式也應該針對 Microsoft DirectX Graphic Infrastructure (DXGI) 作業使用相同的執行緒，尤其是當應用程式呼叫 [**IDXGISwapChain：:P 重發**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) 方法時。

> [!Note]  
> 同時搭配大部分的 DXGI 介面函式使用立即內容是不正確。 針對2009年3月和更新版本的 DirectX Sdk，唯一安全的 DXGI 函式為 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)、 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)和 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))。

 

如需搭配多個執行緒使用 DXGI 的詳細資訊，請參閱多執行緒 [考慮](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多執行緒](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 