---
description: CounterData 資料表會針對在特定時間收集的每個計數器，各包含一個資料列。 這些資料列會有很多。
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b352b9ec6bde6e644d80e7556ac46211212b66b4d92601deedaecaa5dd07344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033988"
---
# <a name="counterdata"></a>CounterData

**CounterData** 資料表會針對在特定時間收集的每個計數器，各包含一個資料列。 這些資料列會有很多。

**CounterData** 資料表會定義下欄欄位：

-   **GUID：** 此資料集的 GUID。 使用此索引鍵與 [**DisplayToID**](displaytoid.md) 資料表聯結。
-   **CounterID：** 識別計數器。 使用此索引鍵與 [**CounterDetails**](counterdetails.md) 資料表聯結。
-   **RecordIndex：** 特定計數器識別碼和集合 GUID 的範例索引。 此記錄檔中每個後續範例的值會增加。
-   **CounterDateTime：** 收集開始的時間（UTC 時間）。
-   **CounterValue：** 計數器的格式化值。 如果計數器需要兩個樣本來計算可顯示的值，則第一筆記錄的這個值可能是零。
-   **FirstValueA：** 將此32位值與 **FirstValueB** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **FirstValue** 成員。 **FirstValueA** 包含低序位位。
-   **FirstValueB：** 將此32位值與 **FirstValueA** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **FirstValue** 成員。 **FirstValueB** 包含高序位位。
-   **SecondValueA：** 將此32位值與 **SecondValueB** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **SecondValue** 成員。 **SecondValueA** 包含低序位位。
-   **SecondValueB：** 將此32位值與 **SecondValueA** 的值結合，以建立 [**PDH \_ RAW \_ 計數器**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)的 **SecondValue** 成員。 **SecondValueB** 包含高序位位。

**GUID**、 **CounterID** 和 **RecordIndex** 欄位構成這個資料表的主鍵。

 

 



