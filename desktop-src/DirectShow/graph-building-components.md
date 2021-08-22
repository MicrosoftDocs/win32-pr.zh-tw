---
description: Graph-Building 元件
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aabcf31f55d0d42117e39cb22fa286b383641c94fe21f386345fd8db1cc890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564638"
---
# <a name="graph-building-components"></a>Graph-Building 元件

DirectShow 提供數個可用於建立篩選圖形的元件。 這些選項包括：

-   [篩選 Graph 管理員](filter-graph-manager.md)。 此物件控制篩選圖形。 它支援 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)、 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)和 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面，還有其他介面。 所有 DirectShow 的應用程式會在某個時間點使用此物件，不過在某些情況下，另一個物件會為應用程式建立篩選 Graph 管理員。
-   [Capture Graph Builder](capture-graph-builder.md)。 此物件提供建立篩選圖形的其他方法。 它原本是設計來建立可執行影片捕獲的圖形 (因此，名稱) 但對許多其他類型的自訂篩選圖形都很有用。 它支援 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面。
-   [篩選](filter-mapper.md) 對應程式和 [系統裝置枚舉](system-device-enumerator.md)器。 這些物件會尋找在使用者系統上或代表硬體裝置註冊的篩選準則。
-   [DVD Graph Builder](dvd-graph-builder.md)。 這個物件會建立用於 DVD 播放和流覽的篩選圖形。 它支援 [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) 介面。

### <a name="intelligent-connect"></a>智慧型連線

「智慧型連線」一詞涵蓋了一組演算法，篩選器 Graph 管理員會使用這些演算法來建立全部或部分的篩選圖形。 每當篩選 Graph 管理員需要額外的篩選器才能完成圖形時，它會大致地執行下列動作：

1.  如果圖形目前有篩選，而且至少有一個未連接的輸入 pin，則篩選 Graph 管理員會嘗試使用該篩選準則。
2.  否則，篩選準則 Graph 管理員會在登錄中尋找可以接受正確媒體類型進行連接的篩選準則。 每個篩選器都有一個稱為「提供」的登錄值，這表示篩選器在完成圖形時大概會有多大的説明。 篩選 Graph 管理員會依最高階的值來嘗試篩選。 針對每個資料流程類型 (例如音訊、影片或 MIDI) ，預設轉譯器的優點很高。 這些解碼器也有很多優點。 特殊用途的篩選具有較低的業績。

如果篩選 Graph 管理員停滯，則會返回並嘗試不同的篩選組合。 您可以在[智慧型連線](intelligent-connect.md)主題中找到確切的詳細資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選 Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



