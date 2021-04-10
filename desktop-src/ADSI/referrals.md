---
title: ADSI)  (的參考
description: 當您所查詢的伺服器未包含該資料，但可以找到該資料時，就會發生參考。
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- 參考 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79e6b2e8a737f6bb40386effd68f7f31d8d490d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093288"
---
# <a name="referrals-adsi"></a>ADSI)  (的參考

當您所查詢的伺服器未包含該資料，但可以找到該資料時，就會發生參考。 目標伺服器會傳回結果集，其中可能包含實際資料，以及另一部伺服器的參考，以抓取額外的資料。 藉由啟用 *參考追蹤*，基礎 ADSI 用戶端程式代碼將會使用該參考資料來嘗試從參考資料中所描述的伺服器取得目標物件。 請注意，停用的參考追蹤可能會產生較小的結果集，而啟用參考追蹤可能會導致查詢跨越許多伺服器。 可能的話，建議的解決方案是使用通用類別目錄。

如需 Active Directory 中的參考和參考追蹤的詳細資訊，請參閱 [參考](/windows/desktop/AD/referrals)。

例如，當用戶端指示伺服器 A () 來查詢使用者物件 (U) 時，可以建議用戶端在伺服器 B 上繼續搜尋 (B) 如果 U 不是位於，但已知是在 B 上。用戶端可以選擇尋求參考。 搜尋參考可用來讓用戶端不需要針對每部伺服器的功能進行 advanced 辨識。 不過，用戶端必須指定伺服器應該進行的參照類型。

Active Directory 提供搜尋參考服務。 用戶端可以選擇下列任何一種類型的參考追蹤：

-   永遠不會：即使伺服器辨識到另一部伺服器儲存要求的資料，伺服器也不應該產生用戶端的參考。
-   外部：如果要求可在不同目錄樹狀結構的另一部伺服器上解析，則伺服器應產生參考。 例如，用戶端會在 "Fabrikam.com" 網域上的 "fab01" 伺服器上查詢 "OU = Sales，DC = Fabrikam，DC = COM"。 不過，此物件不屬於 "fab01"，但已知在 "Fabrikam.com" 網域上的 "arc01" 伺服器上。 因此，"fab01" 會將用戶端參考至 "arc01"。
-   次級：如果要求可在伺服器上解析，而伺服器的名稱形成來自源伺服器的連續路徑，伺服器就應該產生參考。 搜尋範圍必須位於子樹層級。

    例如，伺服器 A 包含 "DC = Sales，DC = Fabrikam，DC = Com" 中的物件。 伺服器 B 包含 "DC = 西雅圖，DC = Sales，DC = Fabrikam，DC = Com" 中的物件。 請注意，伺服器 B 的名稱會形成伺服器 A 的連續路徑。當用戶端連線到伺服器 A 時，要求子樹搜尋 "DC = Sales，DC = Fabrikam，DC = Com"，並將參考指定為附屬類型時，就會發生下列事件：

    -   Server A 會傳回它在其範圍內所知道的所有物件。
    -   伺服器 A 會通知用戶端，在伺服器 B 上可以找到 "DC = 西雅圖，DC = Sales，DC = Fabrikam，DC = COM" 中的物件。

    用戶端可以選擇聯繫伺服器 B。如果是的話，就會發生下列事件：

    -   伺服器 B 回應要求的物件。
    -   如果伺服器 B 偵測到連續命名路徑上的其他伺服器，且進程繼續進行。

-   永遠：如果可以根據外部類型或從屬類型來解析搜尋，伺服器會產生參考。

> [!Note]  
> 在 Active Directory 中，通用類別目錄包含給定企業中的所有物件。 搜尋通用類別目錄伺服器可產生比從一部伺服器到另一部伺服器的參照更佳的效能。

 

在大多數情況下，呼叫端的參考追蹤將會是透明的。 如果是參考不同網域或樹系中的物件，基礎 LDAP API 將會嘗試使用目前的認證來系結至參考的目標。 如果成功，則參考追蹤將會是透明的。 如果不成功，則會傳回參考和參考錯誤碼。

如需有關搭配特定搜尋介面使用參考追蹤選項的詳細資訊，請參閱：

-   [使用 >idirectorysearch 的參考追蹤](referral-chasing-with-idirectorysearch.md)
-   [使用 ActiveX Data Objects 搜尋](searching-with-activex-data-objects-ado.md)
-   [使用 OLE DB 搜尋](searching-with-ole-db.md)

 

 