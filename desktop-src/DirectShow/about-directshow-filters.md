---
description: 關於 DirectShow 篩選
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: 關於 DirectShow 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554026"
---
# <a name="about-directshow-filters"></a>關於 DirectShow 篩選

DirectShow 使用模組化架構，其中每個處理階段都是由稱為篩選的 COM 物件來完成。 DirectShow 針對要使用的應用程式提供一組標準篩選器，而開發人員可以撰寫自己的自訂篩選器，以擴充 DirectShow 的功能。 為了說明，以下是播放 AVI 影片檔案時所需的步驟，以及執行每個步驟的篩選：

-   將檔案中的原始資料讀取為位元組資料流程， (檔案來源篩選) 。
-   檢查 AVI 標頭，並將位元組資料流程剖析為個別的影片框架和音訊範例， (AVI 分隔器篩選) 。
-   根據壓縮格式) ，將影片框架 (各種不同的解碼器篩選器。
-    (影片轉譯器篩選) 繪製影片畫面格。
-   將音訊範例傳送至音效卡 (預設 DirectSound 裝置篩選) 。

下圖顯示這些篩選器。

![使用壓縮影片播放 avi 檔案的篩選圖形](images/avi-filter-graph.png)

如圖所示，每個篩選器都連接到一個或多個其他篩選器。 連接點也是 COM 物件，稱為「 *釘* 選」。 篩選器會使用釘選，在下一個篩選器中移動資料。 圖中的箭號會顯示資料的移動方向。 在 DirectShow 中，一組篩選器稱為 *篩選圖形*。

篩選具有三種可能的狀態：執行中、已停止和已暫停。 當篩選準則正在執行時，它會處理媒體資料。 當它停止時，它會停止處理資料。 暫停狀態是用來在執行之前提示資料; [篩選圖形中](data-flow-in-the-filter-graph.md) 的「資料流程」一節會更詳細地說明此概念。 在極少數的例外狀況下，狀態變更會在整個篩選圖形中進行協調;圖形交換器中的所有篩選準則都有一致的狀態。 因此，整個篩選圖形也稱為「正在執行」、「已停止」或「已暫停」。

篩選可以分為數個廣泛的類別：

-   *來源* 篩選器會將資料引進圖形。 資料可能來自檔案、網路、相機或其他地方。 每個來源篩選器會處理不同類型的資料來源。
-   *轉換* 篩選會接受輸入資料流程、處理資料，以及建立輸出資料流程。 編碼器和解碼器是轉換篩選準則的範例。
-   轉譯 *器篩選* 器位於鏈結尾。 他們會接收資料並向使用者呈現資料。 例如，影片轉譯器會在顯示器上繪製影片畫面;音訊轉譯器會將音訊資料傳送至音效卡;檔案寫入器篩選器會將資料寫入檔案。
-   *分隔* 器篩選器會將輸入資料流程分割成兩個或多個輸出，通常會在一種情況下剖析輸入資料流程。 例如，AVI 分隔器會將位元組資料流程剖析為個別的影片和音訊串流。
-   *Mux* 篩選器會接受多個輸入，並將它們結合成單一資料流程。 例如，AVI Mux 會執行 AVI 分隔器的反向操作。 它會取得音訊和影片串流，並產生 AVI 格式的位元組資料流程。

這些類別之間的差異不是絕對的。 例如，ASF 讀取器篩選器可作為來源篩選器和分隔器篩選器。

所有的 DirectShow 濾波器都會公開 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面，而所有的釘選都會公開 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面。 DirectShow 也會定義許多其他支援更特定功能的介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於篩選圖形管理員](about-the-filter-graph-manager.md)
</dt> <dt>

[篩選圖形中的資料流程](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 



