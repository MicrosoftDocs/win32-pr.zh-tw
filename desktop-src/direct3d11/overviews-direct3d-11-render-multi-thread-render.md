---
title: 立即和延後轉譯
description: Direct3D 11 支援兩種類型的轉譯立即和延後。 兩者都是使用 >id3d11devicecoNtext 介面來執行。
ms.assetid: 8991be9f-c882-4752-9048-704fe4ae1725
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef954a8e794755e1405c8e1e07505a5f39189b03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990634"
---
# <a name="immediate-and-deferred-rendering"></a>立即和延後轉譯

Direct3D 11 支援兩種轉譯類型：立即和延後。 兩者都是使用 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 介面來執行。

## <a name="immediate-rendering"></a>立即轉譯

立即轉譯是指從裝置呼叫轉譯 Api 或命令，這會將緩衝區中的命令排入佇列以在 GPU 上執行。 使用立即內容來呈現、設定管線狀態，以及播放命令清單。

使用 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)建立立即內容。

## <a name="deferred-rendering"></a>延後轉譯

延後轉譯會在命令緩衝區中記錄圖形命令，讓它們可以在其他時間播放。 使用延後的內容，將命令 (轉譯和狀態設定) 記錄到命令清單中。 延遲轉譯是 Direct3D 11 中的新概念;延後轉譯的設計目的是要在錄製命令以在其他執行緒上轉譯時，支援在某個執行緒上轉譯。 這種平行的多執行緒策略可讓您將複雜的場景分解成並行工作。 如需呈現複雜場景的詳細資訊，請參閱 [多重傳遞](overviews-direct3d-11-render-multipass.md)轉譯。

使用 [**ID3D11Device：： CreateDeferredCoNtext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext)建立延遲的內容。

當 Direct3D 在命令緩衝區中將命令排入佇列時，會產生轉譯的額外負荷。 相反地， [命令清單](overviews-direct3d-11-render-multi-thread-command-list.md) 在播放期間會更有效率地執行。 若要使用命令清單，請使用延後內容記錄轉譯命令，並使用立即內容播放這些命令。

您只能以單一執行緒的方式產生單一命令清單。 不過，您可以同時建立和使用多個延遲的內容，每個都在不同的執行緒中。 然後，您可以使用多個延遲的內容，同時建立多個命令清單。

您無法在立即內容中同時播放兩個以上的命令清單。

若要判斷裝置內容是否為立即或延遲的內容，請呼叫 [**>id3d11devicecoNtext：： GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gettype)。

只有在動態資源的延遲內容中才支援 [**>id3d11devicecoNtext：： Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) 方法 ([**D3D11 \_ 使用 \_ 動態**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) ，命令清單中的第一個呼叫是 [**D3D11 \_ Map \_ WRITE \_ 捨棄**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)。 **D3D11 \_如果適用于指定的資源類型，則在後續呼叫上支援對應 \_ 寫入 \_ 不 \_ 覆寫** 。

延遲內容中的查詢僅限於資料產生和前提繪圖。 您無法在延遲的內容上呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) ，以取得查詢的相關資料。您只能在立即 **內容上呼叫** 操作資訊，以取得查詢的相關資料。 您可以呼叫 [**D3D11DeviceCoNtext：： SetPredication**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-setpredication) 來設定轉譯述詞 (一類型的) 查詢，以在 GPU 上使用查詢結果。 您可以透過對 [**>id3d11devicecoNtext：： Begin**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-begin) 和 [**>id3d11devicecoNtext：： End**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-end)的呼叫來產生查詢資料。 不過，您必須在立即內容上呼叫 [**>id3d11devicecoNtext：： ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) 來提交延後的內容命令清單，查詢資料才能使用。 然後，GPU 會處理查詢資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多執行緒](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




