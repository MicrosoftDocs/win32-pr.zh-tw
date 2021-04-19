---
description: 本節說明如何規劃、開發及測試事件參考頁面 (ERPs) 以及如何在專家或監視器中部署它們。 如需有關 ERPs 以及如何搭配網路監視器使用它們的詳細資訊，請參閱事件參考頁面。
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: 建立專家和監視事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985444"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>建立專家和監視事件參考頁面

本節說明如何規劃、開發及測試事件參考頁面 (ERPs) 以及如何在專家或監視器中部署它們。 如需有關 ERPs 以及如何搭配網路監視器使用它們的詳細資訊，請參閱 [事件參考頁面](event-reference-page.md)。

若要開發新的 ERP，第一個步驟是判斷需要個別 ERPs 給自訂 [專家](experts.md) 或 [監視器](monitors.md)的事件。 您必須針對想要顯示在網路監視器事件檢視器中的每個事件建立個別的 ERPs。 例如，假設：

-   您會開發一個名為遊戲監視器和股票監看員的監視器。
-   此監視器位於稱為 Gamemon.dll 的檔案中。
-   此監視器會產生兩個事件：執行遊戲的遊戲和我的網際網路股票 Soars。
-   您打算開發兩個 ERPs、Gamemon1.htm 和 Gamemon2.htm。

> [!Note]  
> 不需要 ERPs 的一對一對應來監視或專家的活動。

 

建立唯一 ERPs 清單之後，請遵循下列步驟來建立每個 ERP。

-   [撰寫 HTML 來源文件](writing-an-event-reference-page.md)。
-   將 HTML 原始程式檔[儲存並命名](naming-an-event-reference-page.md)為 .htm 檔。
-   使用已完成的專家或監視器來[測試 ERP](testing-an-event-reference-page.md) 。

 

 



