---
description: 安裝資料庫的開發人員必須留意 Win32 OLE 結構化儲存體實作為資料流程處理的兩項限制。
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: 資料流程的 OLE 限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a3a1c606a4446129d9e6592c9b352dd0b3e06ae5c77bb378c2430a32cbc568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754248"
---
# <a name="ole-limitations-on-streams"></a>資料流程的 OLE 限制

安裝資料庫的開發人員必須留意 Win32 OLE 結構化儲存體實作為資料流程處理的兩項限制。 這些限制可能會透過轉換和其他可能儲存在資料庫中做為資料流程的資料，間接影響安裝程式函數。

有兩個相關的限制：

-   使用句號分隔符號來串連資料表名稱和記錄主鍵的值，以建立的索引名稱會儲存二進位資料。 OLE 會將資料流程名稱限制為32個字元 (31 + null 結束字元) 。 Windows安裝程式會使用壓縮演算法，以根據字元將限制擴展為62個字元。 請注意，雙位元組字元計數為2。
-   雖然您可以一次開啟多個資料流程，但您無法在第一次參考關閉之前再次開啟資料流程。 這表示您無法選取要同時在多個記錄中開啟的相同二進位資料流程。 嘗試從第二筆記錄讀取二進位資料失敗。 此外，當該記錄中的二進位資料流程已開啟時，您也無法重新命名記錄的主鍵。

 

 



