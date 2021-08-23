---
description: 使用 GraphEdit 模擬 Graph 建立
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: 使用 GraphEdit 模擬 Graph 建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4f5bee201e2bd5b771348596b46caa513944aa148c7ec17a9e2974a360e60c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583191"
---
# <a name="simulating-graph-building-with-graphedit"></a>使用 GraphEdit 模擬 Graph 建立

DirectShow 提供稱為 GraphEdit 的偵錯工具，可讓您用來建立及測試篩選圖形。

GraphEdit 是用來建立篩選圖形的視覺化檢視。 透過 GraphEdit，您可以在撰寫任何應用程式程式碼之前，先實驗篩選圖形。 您也可以載入應用程式所建立的篩選圖形，以確認您的應用程式正在建立正確的圖形。 如果您開發自訂篩選器，GraphEdit 會提供快速測試的方法：只要使用您的自訂篩選載入圖形，並嘗試執行圖形即可。 如果您是 DirectShow 的新手，GraphEdit 是熟悉篩選圖形和 DirectShow 架構的好方法。

下圖顯示 GraphEdit 如何代表簡單的篩選圖形。

![graphedit 中的簡單篩選圖形](images/gedit09.png)

每個篩選都會以矩形表示。 沿著篩選邊緣的較小平方表示圖釘。 輸入圖釘位於篩選器的左側，輸出則是在右邊。 箭號代表圖釘之間的連接。

透過 GraphEdit，您可以：

-   使用視覺效果拖放介面建立和修改篩選圖形。
-   模擬以程式設計方式呼叫來建立圖形。
-   執行、暫停、停止和搜尋圖形。
-   查看電腦上已註冊的篩選器，並查看每個篩選器的登錄資訊。
-   視圖篩選屬性頁。
-   查看 pin 連接的媒體類型。

本節包含下列主題：

-   [使用 GraphEdit](using-graphedit.md)
-   [從外部進程載入 Graph](loading-a-graph-from-an-external-process.md)
-   [將篩選 Graph 儲存至 GraphEdit 檔案](saving-a-filter-graph-to-a-graphedit-file.md)
-   [以程式設計方式載入 GraphEdit 檔案](loading-a-graphedit-file-programmatically.md)
-   [GraphEdit 檔案格式](graphedit-file-format.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow](using-directshow.md)
</dt> </dl>

 

 



