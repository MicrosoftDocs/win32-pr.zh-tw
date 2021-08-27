---
title: 自動撥號對應資料庫
description: 自動撥號對應資料庫會將網路位址對應到 RAS 電話簿專案。
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e89bd065a136492281adb3424636a8820c76c76bf6867e70db75aecfa0f345d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036718"
---
# <a name="autodial-mapping-database"></a>自動撥號對應資料庫

自動撥號對應資料庫會將網路位址對應到 RAS 電話簿專案。 資料庫可以包含 IP 位址 (例如 "172.21.167.35" ) 、網際網路主機名稱 (例如 "www.microsoft.com" ) 或 NetBIOS 名稱 (例如 "products1" ) 。 與自動撥號資料庫中每個位址相關聯的是一組一或多個 [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) 專案。 其中每個專案都會指定一個電話簿專案，讓 RAS 可以撥號來從特定的電話語音應用程式開發介面連接到位址， (TAPI) 撥號位置。 如需有關 TAPI 撥號位置的詳細資訊，請參閱 TAPI 檔。

自動撥號會在兩種情況下自動在自動撥號對應資料庫中建立專案：

-   嘗試連接到網路位址失敗時

    如果對應資料庫的位址沒有任何專案，且電腦未直接或透過 RAS 連線到網路，自動撥號會提示使用者指定建立撥號連線所需的資訊。 如果使用者提供資訊，而且撥號連線作業成功，自動撥號會將資訊儲存在對應資料庫中。

-   當電腦透過 RAS 連線到網路時

    當使用者連線到網路位址時，自動撥號會在資料庫中建立一個專案。 此專案會將網路位址對應到用來建立 RAS 連線的電話通訊錄專案。

您可以使用 [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) 函數將位址新增至自動撥號對應資料庫、從資料庫中刪除位址，或變更與資料庫中現有位址相關聯的自動撥號專案。 您可以使用 [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) 函式，在自動撥號對應資料庫中取出與指定的網路位址相關聯的自動撥號專案。 [**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa)函數會傳回自動撥號對應資料庫中的所有地址清單。

 

 