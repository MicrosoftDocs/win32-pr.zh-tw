---
title: 追蹤變更
description: 某些應用程式必須維持儲存在 Active Directory 目錄服務和其他資料中的特定資料之間的一致性。
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory，使用追蹤變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3d8521fbd7b04d2c317246d81e0b9af7bce888bcc8e78b7bc9fcbbdd05b0c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024566"
---
# <a name="tracking-changes"></a>追蹤變更

某些應用程式必須維持儲存在 Active Directory 目錄服務和其他資料中的特定資料之間的一致性。 其他資料可能儲存在目錄、SQL Server 資料表、檔案或登錄中。 當儲存在目錄中的資料變更時，可能需要變更其他資料，才能保持一致。 具有這項需求的應用程式包括：

本節不涵蓋監視應用程式所使用的機制。 這些應用程式會監視目錄變更，而不是為了維護不同存放區之間的一致資料，而是系統管理工具。 雖然監視應用程式可以使用支援變更追蹤應用程式的相同機制，但是下列機制特別針對監視應用程式而設計：

-   安全性審核。 藉由修改系統存取控制清單 (SACL) 部分的物件安全描述項，您可能會對指定網域控制站上的物件進行存取，以在該 DC 上的安全性事件記錄檔中產生審核記錄。 您可以同時審核讀取、寫入或兩者。您可以審核整個物件或特定屬性。 如需詳細資訊，請參閱抓取 [物件的 SACL](retrieving-an-objectampaposs-sacl.md) 和 [審核產生](/windows/desktop/SecAuthZ/audit-generation)。
-   事件記錄。 藉由修改指定網域控制站上的登錄設定，您可以變更記錄到目錄服務事件記錄檔的事件種類。 明確地說，若要記錄所有修改，請將下列登錄機碼底下的 **8 目錄存取** 值設定為4。

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    如需詳細資訊，請參閱 [事件記錄](/windows/desktop/EventLog/event-logging)。

-   事件追蹤。 Windows 2000 引進了事件追蹤 API，可在軟體或硬體中追蹤和記錄感興趣的事件。 Windows 作業系統（特別是 Active Directory Domain Services）支援使用事件追蹤來進行容量規劃和詳細的效能分析。 如需詳細資訊，請參閱 ADSI 中的 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) 和 [事件追蹤](/windows/desktop/ADSI/adsi-and-etw)。

本節包含下列主題：

-   [變更追蹤技術總覽](overview-of-change-tracking-techniques.md)
-   [Active Directory Domain Services 中的變更通知](change-notifications-in-active-directory-domain-services.md)
-   [使用 DirSync 控制項輪詢變更](polling-for-changes-using-the-dirsync-control.md)
-   [使用 USNChanged 輪詢變更](polling-for-changes-using-usnchanged.md)

 

 