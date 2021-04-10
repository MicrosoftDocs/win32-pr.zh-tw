---
description: 公告欄可以在安裝期間，于對話方塊中顯示一系列的影像和文字。 一般而言，公告欄是用來建立投影片放映或動畫的視覺效果，以通知使用者安裝進度。
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: 在非強制回應對話方塊上顯示公告欄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114573"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>在非強制回應對話方塊上顯示公告欄

公告欄可以在安裝期間，于對話方塊中顯示一系列的影像和文字。 一般而言，公告欄是用來建立投影片放映或動畫的視覺效果，以通知使用者安裝進度。

**在非強制回應對話方塊上顯示公告欄**

1.  在包含佈告欄之非強制回應對話方塊的 [對話方塊資料表](dialog-table.md) 中包含記錄。 在顯示佈告欄之後，非強制回應對話方塊會將控制權傳回給安裝程式。 這可讓安裝程式處理訊息，並更新對話方塊和佈告欄。 若要建立非強制回應對話方塊，請勿在 [對話方塊資料表](dialog-table.md)的 [屬性] 欄位中設定強制回應對話方塊樣式位。 下列 [對話方塊資料表](dialog-table.md) 記錄會指定 [ActionDialog] 對話方塊。

    [對話方塊資料表](dialog-table.md) (部分) 

    | 對話\_     | HCentering | VCentering | 寬度 | 高度 | 屬性 | 標題  | \_先控制項 | 控制項 \_ 預設值 | 控制 \_ 取消 |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | 動作 | 取消         | 取消           | 取消          |

    

     

2.  將記錄加入至 [控制資料表](control-table.md) ，以指定對話方塊顯示佈告欄。 記錄會在對話方塊中定義區域的大小和位置，在此對話方塊中會顯示 [BBControl 資料表](bbcontrol-table.md) 中所列的佈告欄控制項。 下列 [控制資料表](control-table.md) 記錄會在 [ActionDialog] 對話方塊上定義佈告欄的位置和大小。

    [控制資料表](control-table.md) (部分) 

    | 對話\_     | 控制   | 類型      | X   | Y   | 寬度 | 高度 | 屬性 |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | 廣告 牌 | 廣告 牌 | 0   | 110 | 480   | 130    | 1          |

    

     

3.  [佈告欄表格](billboard-table.md)會列出佈告欄控制項，並指定何時會顯示特定的佈告欄控制項。 針對每個佈告欄控制項將記錄新增至 [佈告欄資料表](billboard-table.md) 。 [佈告欄資料表](billboard-table.md)會監看安裝期間傳送的進度訊息。 只有在 [ [佈告欄] 資料表](billboard-table.md)的 [動作] 資料行中所列的動作傳送進度訊息時，而且只有在選取 [功能] 欄位中的功能來安裝時，才會顯示佈告欄 \_ 。 在顯示佈告欄之後，它會一直顯示到另一個佈告欄所涵蓋的範圍內，或直到對話方塊關閉為止。 如果針對某個動作指定了多個公告欄，則會依 [排序] 欄位所指定的順序，一次顯示一個。 例如，下列 [佈告欄資料表](billboard-table.md) 專案會先顯示 BB1，然後 BB2 [佈告欄會控制](billboard-control.md) [InstallFiles](installfiles-action.md) 動作的執行和已選取要安裝的 QuickTest 功能。

    [佈告欄資料表](billboard-table.md) (部分) 

    | 廣告 牌 | 功能   | 動作       | 排序 |
    |-----------|-----------|--------------|----------|
    | BB1       | QuickTest | InstallFiles | 1        |
    | BB2       | QuickTest | InstallFiles | 2        |

    

     

4.  [BBControl 資料表](bbcontrol-table.md)指定的控制項屬於[佈告欄資料表](billboard-table.md)中所列的[佈告欄控制項](billboard-control.md)。 [文字控制項](text-control.md)、[點陣圖控制項](bitmap-control.md)和[圖示控制項](icon-control.md)是唯一可進入佈告欄的控制項類型。 每個佈告欄都可以放置多個控制項。 在 [BBControl] 資料表的 [佈告欄] 欄位中輸入佈告欄的名稱， \_ 與[佈告欄資料表](billboard-table.md)中所顯示的完全相同。 [](bbcontrol-table.md)

    每個控制項位置都指定為控制項左上角的座標。 座標系統原點位於佈告欄控制項的左上角，而不是在對話方塊的角落。 座標是在安裝程式單位中，而不是對話方塊單位。 安裝程式單位等於10點 MS sans-serif 字型大小的一到第十二個高度。 下列 [BBControl 表](bbcontrol-table.md) 記錄將控制項系結至公告欄。

    [BBControl 資料表](bbcontrol-table.md) (部分) 

    | 廣告 牌 | BBControl | 類型   | X   | Y   | 寬度 | 高度 | 屬性 | Text             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Text      | Text   | 100 | 30  | 280   | 280    | 3          | 第一個佈告欄  |
    | BB1       | Bitmap1   | 點陣圖 | 0   | 0   | 100   | 100    | 3          | 軟體         |
    | BB1       | Bitmap2   | 點陣圖 | 380 | 0   | 100   | 100    | 3          | 音樂            |
    | BB2       | Text      | Text   | 100 | 30  | 280   | 20     | 3          | 第二個佈告欄 |
    | BB2       | Bitmap1   | 點陣圖 | 0   | 0   | 100   | 100    | 3          | 音樂            |
    | BB2       | Bitmap2   | 點陣圖 | 380 | 0   | 100   | 100    | 3          | 軟體         |

    

     

5.  若要在 [ActionDialog] 對話方塊上顯示佈告欄，您必須將記錄新增至[EventMapping 資料表](eventmapping-table.md)，以將佈告欄控制項訂閱[SetProgress ControlEvent](setprogress-controlevent.md) 。 當安裝程式發佈在事件資料行中指定的 SetProgress ControlEvent 時，安裝程式會設定在 [屬性] 欄位中指定的控制項屬性。 事件欄位包含 SetProgress ControlEvent 的字串識別碼， (沒有引號) 。 [屬性] 欄位包含要設定之屬性的字串識別碼 (沒有引號) 。 對話方塊 \_ 和控制項 \_ 欄位會識別佈告欄控制項，而且應該符合 [控制資料表](control-table.md)中的欄位。 例如，下列 [EventMapping 資料表](eventmapping-table.md) 會訂閱事件的控制項。

    [EventMapping 資料表](eventmapping-table.md) (部分) 

    | 對話\_     | 控制項\_ | 事件       | 屬性 |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | 廣告 牌 | SetProgress | 進度  |

    

     

 

 



