---
title: 搜尋 Active Directory
description: Active Directory 的一項重要功能，就是解析人員的資料查詢，以及電腦和服務的設定資料。
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- 搜尋 Active Directory ADSI
- ADSI ADSI，搜尋 Active Directory
- 查詢 ADSI、搜尋 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300056"
---
# <a name="searching-active-directory"></a>搜尋 Active Directory

Active Directory 的一項重要功能，就是解析人員的資料查詢，以及電腦和服務的設定資料。 若要為 Active Directory 撰寫有效率的查詢，最好先熟悉下列各項：

-   判斷查詢的範圍：用戶端是否必須針對可能位於樹系內任何位置的物件尋找屬性，或僅在一個網域內或在指定的組織單位內找到 (OU) ？
-   判斷查詢的深度：查詢必須只搜尋一個層級，或可能會跨越其他 LDAP 目錄？
-   效能和處理大型結果集：用戶端應該如何有效地處理大型結果集的可能性？
-   判斷最佳查詢：何種類型的查詢能提供最有效率的結果？ 開發人員應避免何種查詢？
-   瞭解查詢語法： ADSI 支援 RFC 2254 中所述的 LDAP 語法，以及 SQL 的子集。
-   選擇的介面： ADSI 同時提供 OLE DB 支援以及 C/c + + 介面（稱為 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)）。 因為 ADSI 適用于多個命名空間，所以您可以使用這些介面來查詢其他命名空間（例如 Exchange）以及 Active Directory。 因為 (ADO) 的 ActiveX 資料物件是簡單的可編寫腳本資料存取物件模型，在 OLE DB 上，OLE DB 介面適用于 Visual Basic 程式設計人員和網頁腳本寫入器。 利用 ADO 和 OLE DB 的 Visual Studio 和 Office 應用程式內的新資料存取功能，現在可以用與從其他 OLE DB 提供者（例如 SQL Server）存取資料的相同方式來存取 Active Directory 資料。 但是，如果 C/c + + 開發人員必須執行簡單的目錄搜尋，則 **>idirectorysearch** 介面可能比 OLE DB 介面更適合。

下列主題說明如何搜尋 Active Directory，以確保您的應用程式會根據用戶端的需求，發出最有效率的查詢：

-   [查詢的範圍](scope-of-query.md)
-   [效能和處理大型結果集](performance-and-handling-large-result-sets.md)
-   [搜尋篩選語法](search-filter-syntax.md)
-   [查詢介面](query-interfaces.md)
-   [搜尋二進位資料](searching-binary-data.md)
-   [Distributed Query](distributed-query.md)

 

 




