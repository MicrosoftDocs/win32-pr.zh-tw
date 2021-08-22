---
title: 使用 Active Directory 網域服務
description: 本節提供撰寫應用程式的指導方針，這些應用程式會使用或發佈 Active Directory 目錄服務中的資料。
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory，使用
- Active Directory Domain Services Active Directory，使用
- Active Directory 範例 Active Directory
- Active Directory Domain Services 範例 Active Directory
- 範例 Active Directory
- Active Directory Active Directory 的範例，請參閱 Active Directory Domain Services 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e1ef5428242e6d83fcb0c517c91abaee24de8181689a3aa1922eafea4d76703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024536"
---
# <a name="using-active-directory-domain-services"></a>使用 Active Directory 網域服務

本節提供撰寫應用程式的指導方針，這些應用程式會使用或發佈 Active Directory 目錄服務中的資料。

> [!Note]  
> 下列檔適用于電腦程式設計人員。 如果您嘗試解決 Active Directory 首頁列印錯誤，請參閱 Microsoft 社區頁面的 [下列建議](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) ：如果沒有説明，請嘗試從 [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint)提出這些建議。

 

Active Directory Domain Services 符合輕量型目錄存取協定3.0 （由 RFC 2251 和其他 Rfc 所定義）。 您可以使用下列任何 API 集合來存取 Active Directory Domain Services。 每個 API 集合都有優缺點，取決於程式設計語言、程式設計環境和預定的執行方法。 本指南中的大部分範例都會使用「ADSI」（c 和 c + + 等語言所支援的）以及符合自動化規範的語言，例如 Microsoft Visual Basic 和 Visual Basic 腳本撰寫版。

如需特定 Active Directory Domain Services 技術的詳細資訊，請參閱：

-   [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Active Directory 服務介面](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

本節將討論下列主題：

-   [系結至 Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [在 Active Directory Domain Services 中搜尋](searching-in-active-directory-domain-services.md)
-   [在 Active Directory Domain Services 中建立和刪除物件](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [移動物件](moving-objects.md)
-   [在 Active Directory Domain Services 中讀取和寫入物件的屬性](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [控制 Active Directory Domain Services 中的物件存取](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [擴充架構](extending-the-schema.md)
-   [擴充目錄物件的消費者介面](extending-the-user-interface-for-directory-objects.md)
-   [管理使用者](managing-users.md)
-   [管理群組](managing-groups.md)
-   [追蹤變更](tracking-changes.md)
-   [服務發行](service-publication.md)
-   [服務登入帳戶](service-logon-accounts.md)
-   [使用 Kerberos 進行相互驗證](mutual-authentication-using-kerberos.md)
-   [備份與還原 Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [儲存動態資料](storing-dynamic-data.md)
-   [應用程式目錄分割](application-directory-partitions.md)
-   [偵測網域的操作模式](detecting-the-operation-mode-of-a-domain.md)

 

 