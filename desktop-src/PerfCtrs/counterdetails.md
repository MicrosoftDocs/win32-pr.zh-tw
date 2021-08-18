---
description: CounterDetails 資料表描述特定電腦上的特定計數器。
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef429f7f90c38d53f085ed0243e1c799c1d1cfa808c7aa052d8a37ed3a1faf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011356"
---
# <a name="counterdetails"></a>CounterDetails

**CounterDetails** 資料表描述特定電腦上的特定計數器。

**CounterDetails** 資料表會定義下欄欄位：

-   **CounterID：** 資料庫中對應至特定計數器名稱文字字串的唯一識別碼。 此欄位是此資料表的主要索引鍵。
-   **MachineName：** 記錄此資料集的電腦名稱稱。
-   **ObjectName：** 效能物件的名稱。
-   **CounterName：** 計數器的名稱。
-   **CounterType：** 計數器類型。 如需計數器類型及其公式的清單，請參閱[Windows Server 2003 部署套件](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10))的「計數器類型」一節。
-   **DefaultScale：** 要套用至原始效能計數器資料的預設調整。
-   **InstanceName：** 計數器實例的名稱。
-   **InstanceIndex：** 計數器實例的索引編號。
-   **ParentName：** 某些計數器會以邏輯方式與其他計數器相關聯，而且會被稱為父代。 例如，執行緒的父系是一個進程，而邏輯磁片驅動程式的父系是實體磁片磁碟機。 此欄位包含父系的名稱。 這個欄位或 **父** 欄位中的值會識別特定的父實例。 如果此欄位中的值為 **Null**，則必須核取 [ **父** ] 欄位中的值，以識別父代。 如果兩個欄位中的值都是 **Null**，則計數器沒有父系。
-   **父：** 父系的唯一識別碼。 這個欄位或 **ParentName** 欄位中的值會識別特定的父實例。 如果此欄位中的值為 **Null**，則必須核取 [ **ParentName** ] 欄位中的值，以識別父代。

 

 
