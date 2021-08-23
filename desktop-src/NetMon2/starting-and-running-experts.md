---
description: 按一下網路監視器 UI 的 [專家] 視窗中的 [執行專家]，即可啟動針對 capture 檔案選取的專家，並呼叫 Run 函數。 啟動時，專家會使用數個專家框架函式來分析 capture 檔案。
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: 啟動及執行專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc85ba39c393ac253ca688a826bc77747c8d17bea29b089250a63f6f833066c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555314"
---
# <a name="starting-and-running-experts"></a>啟動及執行專家

按一下網路監視器 UI 的 [專家] 視窗中的 [ **執行專家** ]，即可啟動針對 capture 檔案選取的專家，並呼叫 [**Run**](run.md) 函數。 啟動時，專家會使用數個專家框架函式來分析 capture 檔案。

[**ExpertIndicateStatus**](expertindicatestatus.md)函式會提供專家提供的狀態資訊。 當您執行網路監視器的專家時，專家狀態視圖視窗會顯示定期更新的狀態資訊 (從0到100% 的完成) 。

![專家狀態視圖視窗](images/exview.png)

在資料透過 capture 檔案完成通過之前，專家會處於作用中狀態。 當 pass 完成時，會出現事件檢視器視窗。 此視窗中的資訊取決於分析資料的專家類型。 下圖顯示內容散發專家的觀點，其中摘要了專家分析的框架資料。

![屬性散發專家觀點](images/exview1.png)

第二份報表 (未顯示) ，摘要說明傳輸控制通訊協定 (TCP) 重新傳輸專家的結果。

您也可以：

-   建立事件參考頁面 (ERP) 的專案，以建議使用者偵測到的狀況或問題 (如 [分析] 視窗) 所示。
-   建立建議的修正或說明資料的專案，以提供其他資訊 (如 [解決方式] 視窗) 所示。

當專家完成其工作之後，網路監視器會從使用中記憶體中移除專家。 專家應使用平臺軟體發展工具組中包含的受保護記憶體函式 (SDK) ;如果專家在執行時間失敗，這些函式會清除記憶體。

 

 



