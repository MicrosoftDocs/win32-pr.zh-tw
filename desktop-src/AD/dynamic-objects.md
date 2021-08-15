---
title: 動態物件
description: 在 Windows Server 2003 和更新版本的 Windows 中，Active Directory Domain Services 提供將動態專案儲存在目錄中的支援。
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- 動態物件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74660728179365f6585bce2462cd22f2508e68318eb84312d039a431330329b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191716"
---
# <a name="dynamic-objects"></a>動態物件

在 Windows Server 2003 和更新版本的 Windows 中，Active Directory Domain Services 提供將動態專案儲存在目錄中的支援。 動態專案是目錄中的物件，具有相關聯的存留時間 (TTL) 值。 建立專案時，會設定專案的 TTL。 存留時間會自動遞減，當它過期時，動態專案就會消失。 用戶端可能會藉由重新整理 (修改) 的 TTL 值，使動態專案維持比目前剩餘的存留期還要久。 將動態資料儲存在目錄中的用戶端必須定期重新整理該資料，以防止它消失。

許多應用程式和服務使用 LDAP 來儲存及存取 Active Directory 伺服器中相對靜態和全球感興趣的資料，也會想要繼續針對其動態資料需求使用 LDAP 存取。 此外，在某些應用程式中，可能會想要在 DS 中將垃圾收集物件的垃圾收集到目錄服務的使用年限有所限制。 應用程式目錄分割 (有能力控制複本的放置) 和每個物件的 TTLs，將可提供在 Active Directory Domain Services 中裝載動態資料的功能，進而允許 LDAP 存取它。

名為 **dynamicObject** 的新輔助物件類別（具有 OID = 1.3.6.1.4.1.1466.101.119.2）將在基底 AD 架構中定義，以供動態專案使用。 這個輔助類別包含名為 **entryTTL** 的屬性，其 OID = 1.3.6.1.4.1.1466.101.119.3 是系統可能包含的屬性。 這個屬性的值是在從目錄消失之前，對應的目錄專案將繼續存在的「時間（以秒為單位）。 如果用戶端未在建立物件時明確提供此屬性的值，則 DS 會提供預設值，如稍後所指定。

具有 OID = 1.3.6.1.4.1.1466.101.119.1 的新擴充 LDAP 作業，會在目錄中的動態專案重新整理時，定義併發布在根 DSE 物件的 **supportedExtension** 屬性中。

在實際的實作為中， **entryTTL** 是一個結構化屬性。 實際物件到期時間會儲存為絕對時間，當物件可以在稱為「 **ms-DS-輸入存留時間**」的系統屬性中終結時。

所有動態物件都有下列限制：

-   因為已刪除的動態物件的 TTL 即將到期，所以不會留下標記。
-   所有保存動態物件複本的 dc 都必須在 Windows Server 2003 上執行。
-   除了設定分割區和架構分割之外，所有磁碟分割都支援具有 TTL 值的動態專案。
-   Active Directory Domain Services 不會在根 DSE 物件中發佈選用 **dynamicSubtrees** 屬性，如 RFC 2589 中所述。
-   處理搜尋、比較、加入、刪除、修改和 modifyDN 作業時，動態專案的處理方式類似非動態專案。
-   沒有任何方法可將靜態專案變更為動態專案，反之亦然。
-   非動態專案無法加入至動態專案。

 

 




