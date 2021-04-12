---
description: 一般 Graph-Building 技術
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: 一般 Graph-Building 技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187394"
---
# <a name="general-graph-building-techniques"></a>一般 Graph-Building 技術

每個 DirectShow 應用程式一開始都會建立篩選圖形。 當您閱讀 DirectShow 檔中的「總覽」主題時，您會發現最重要的是，它會說明所需的篩選圖形種類。 在某些情況下，有一種方法或協助程式物件專門設計來建立該類型的圖形。 例如， [Dvd 圖形](dvd-graph-builder.md) 產生器物件會建立 dvd 播放圖形。 在其他情況下，應用程式必須藉由新增篩選並加以連接來建立圖形。

本節提供一些協助程式函式，這些函式會執行基本的圖形組建作業。 任何需要建立或修改篩選圖形的 DirectShow 應用程式都可以使用這些應用程式。 本節包含下列主題：

-   [依 CLSID 新增篩選](add-a-filter-by-clsid.md)
-   [在篩選器上尋找未連接的 Pin](find-an-unconnected-pin-on-a-filter.md)
-   [連接兩個篩選器](connect-two-filters.md)
-   [尋找篩選或釘選上的介面](find-an-interface-on-a-filter-or-pin.md)
-   [尋找篩選準則的對等](find-a-filters-peer.md)
-   [移除圖形中的所有篩選](remove-all-the-filters-in-the-graph.md)
-   [使用 Capture Graph Builder 建立圖形](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本的 DirectShow 工作](basic-directshow-tasks.md)
</dt> <dt>

[列舉裝置和篩選器](enumerating-devices-and-filters.md)
</dt> <dt>

[列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[智慧型連接](intelligent-connect.md)
</dt> </dl>

 

 



