---
title: 命令清單
description: 命令清單是可錄製和播放的 GPU 命令序列。 命令清單可以藉由減少執行時間所產生的額外負荷，來改善效能。
ms.assetid: 4f581bc7-6c5e-4e56-b768-7f3cc5dbcb3e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0f8bd70fdca1f55e5ef0c35f8aa8106f6a7777726afab22bd3ca09901172c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913372"
---
# <a name="command-list"></a>命令清單

命令清單是可錄製和播放的 GPU 命令序列。 命令清單可以藉由減少執行時間所產生的額外負荷，來改善效能。

在下列案例中使用命令清單：

-   在單一框架內，在第二個執行緒上錄製場景的另一個部分時，在一個執行緒上轉譯場景的一部分。 在框架的結尾，播放第一個執行緒上錄製的命令清單。 您可以使用此方法，在多個執行緒或核心之間調整複雜的轉譯工作。
-   預先錄製命令清單之前，您必須先將它轉譯 (例如，將層級載入) ，並在稍後的場景中有效率地播放。 當您需要經常轉譯時，此優化的效果很好。

命令清單是不可變的，其設計是要在應用程式的單一執行期間錄製和播放。 命令清單並非設計為預先錄製遊戲執行，並從媒體載入，因為沒有任何方法可保存清單。

命令清單必須由延遲的內容記錄，但只能在立即內容上播放。 延遲的內容可以同時產生命令清單。

-   若要錄製命令清單，請參閱 [如何：錄製命令清單](overviews-direct3d-11-render-multi-thread-command-list-record.md)。
-   若要播放命令清單，請參閱 [如何：播放命令清單](overviews-direct3d-11-render-multi-thread-command-list-play.md)。
-   使用命令清單時，效能取決於驅動程式中所執行的支援數量。 若要檢查驅動程式支援，請參閱 [如何：檢查驅動程式支援](overviews-direct3d-11-render-multi-thread-support.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[立即和延後轉譯](overviews-direct3d-11-render-multi-thread-render.md)
</dt> <dt>

[多執行緒](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




