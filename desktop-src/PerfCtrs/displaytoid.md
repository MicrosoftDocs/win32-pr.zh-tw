---
description: DisplayToID 資料表將系統監視器所顯示的使用者易記字串與其他資料表中儲存的 GUID 產生關聯。
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485eab24a2c758b36e190e035a9442a032ebd683f3f5ea052bd37992ad14c85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033908"
---
# <a name="displaytoid"></a>DisplayToID

**DisplayToID** 資料表將系統監視器所顯示的使用者易記字串與其他資料表中儲存的 GUID 產生關聯。

**DisplayToID** 資料表會定義下欄欄位：

-   **GUID：** 為記錄產生的唯一識別碼。 此欄位是此資料表的主要索引鍵。
-   **RunID：** 保留供內部使用。
-   **DisplayString：** 系統監視器中所顯示的記錄檔名稱。
-   **LogStartTime：** 記錄處理常式的開始時間，以 yyyy-mm-dd hh： mm： ss： nnn 格式為限。
-   **LogStopTime：** 記錄進程停止的時間，以 yyyy-mm-dd hh： mm： ss： nnn 格式為限。 您可以使用此和 **LogStartTime** 欄位中的值，來區分具有相同 **DisplayString** 值的多個記錄檔。 **LogStartTime** 和 **LogStopTime** 欄位中的值也可讓您快速存取總收集時間。
-   **NumberOfRecords：** 資料表中為每個記錄收集所儲存的樣本數。
-   **MinutesToUTC：** 用來將 UTC 時間儲存的資料列資料轉換為當地時間的值。
-   **TimeZoneName：** 收集資料的時區名稱。 如果您要從您自己的時區的系統收集或 relogged 資料，此欄位將會陳述位置。

**注意** 在 Windows Vista 之前，資料收集器集會儲存在登錄位置

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services \\ SysmonLog \\ 記錄查詢**

. 上欄欄位未對應至 registry 中的值。 針對 Windows Vista，資料收集器集合器不會儲存在登錄中。

 

 



