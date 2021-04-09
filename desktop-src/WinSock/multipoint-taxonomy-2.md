---
description: 本節中所述的分類會先從處理在會話參與者間傳送資料的資料平面，將關注本身與 multipoint 會話建立方式的控制平面區分開來。
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Multipoint 分類法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848011"
---
# <a name="multipoint-taxonomy"></a>Multipoint 分類法

本節中所述的分類會先從處理在會話參與者間傳送資料的資料平面，將關注本身與 multipoint 會話建立方式的控制平面區分開來。

## <a name="session-establishment-in-the-control-plane"></a>控制平面中的會話建立

在控制平面中，有兩種不同類型的會話建立：

-   植根
-   nonrooted

在進行根控制項的情況下，有一個特殊的參與者（c \_ 根）與這個 multipoint 會話的其餘成員不同，每一個都稱為 c 分 \_ 葉。 \_針對 multipoint 會話的整個持續期間，c 根必須保持存在，因為會話會在沒有 c 根的情況下中斷 \_ 。 C \_ 根通常會藉由設定與 c 分葉的連接 \_ ，或多個 c 葉子來起始 multipoint 會話 \_ 。 在 \_ 某些情況下，c 根可能會新增更多 \_ 的 c 葉子或 () c 分 \_ 葉可以 \_ 在稍後加入 c 根。 您可以在 ATM 和聖 II 中找到根控制項平面的範例。

針對 nonrooted 控制平面，屬於 multipoint 會話的所有成員都是離開的，也就是說，沒有任何特殊的參與者可作為 c \_ 根。 每個 c 分 \_ 葉都必須將自己新增到預先存在的 multipoint 會話，此會話永遠可用 (例如 IP 多播位址) 的情況，或已透過部分超出 Windows 通訊端規格範圍的頻外 (OOB) 機制來進行設定。

另一種查看方法的方法是，c \_ 根仍然存在，但是可以被視為是在網路雲端中，而不是其中一個參與者。 由於控制項根目錄仍然存在，因此也可以將 nonrooted 控制平面視為隱含根。 這種隱含根目錄的 multipoint 配置範例如下：

-   電話會議橋接器。
-   IP 多播系統。
-   Multipoint 控制項單位 (MCU) 在 320 video 會議中。

## <a name="data-transfer-in-the-data-plane"></a>資料平面中的資料傳輸

在資料平面中，有兩種類型的資料傳輸樣式：

-   植根
-   nonrooted

在根資料平面中，有一個稱為 d root 的特殊參與者 \_ 存在。 資料傳輸只會發生在 d \_ 根和這個 multipoint 會話的其餘成員之間，每個都稱為 d 分 \_ 葉。 流量可能是單向或雙向。 從 d 根目錄送出的資料 \_ 會在必要時重複 (如有需要) 並傳遞至每個 d 分 \_ 葉，而 d 葉子的資料 \_ 只會移至 d \_ 根。 在根資料平面的情況下，d 葉子之間不允許流量 \_ 。 位於資料平面中的通訊協定範例是 ST-II。

在 nonrooted 資料平面中，所有參與者都相等，也就是它們傳送的任何資料都會傳遞給相同 multipoint 會話中的所有其他參與者。 同樣地，每個 d 分 \_ 葉節點都可以接收來自其他所有 d 葉子的資料 \_ ，而在某些情況下，則是從其他未參與 multipoint 會話的節點接收。 沒有特殊 \_ 的 d 根節點。 IP-多播是在資料平面中 nonrooted。

請注意，資料單位重複發生的位置，或共用的單一樹狀結構或多個最短路徑樹狀結構是否用於 multipoint 分佈是通訊協定問題，以及應用程式用來執行 multipoint 通訊的介面不相關的問題。 因此，這些問題不會在此附錄或 Windows 通訊端介面中解決。

下表描述上述的分類，並指出現有的配置如何符合每個類別。 請注意，沒有任何現有的配置會採用 nonrooted 控制平面以及根資料平面。

|                      | 根控制項平面 | Nonrooted (隱含根目錄) 控制平面 |
|----------------------|----------------------|-------------------------------------------|
| 根資料平面    | ATM，聖 II           | 沒有已知的範例。                        |
| Nonrooted 資料平面 | T. 120                | IP-多播、.H 320 (MCU)                  |



 

 

 



