---
description: 編目範圍管理員 (CSM) 是一組介面，可提供方法來通知 Windows Search 引擎有關要將容器編目的容器，以及要在目錄中包含或排除的容器底下的專案。
ms.assetid: 7d65d00a-7294-4718-b593-89394b2e416f
title: 使用編目範圍管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a440041c4af9b0ab5e1d282b91cf8fba35c041a546b8247d320884f072a641c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117681204"
---
# <a name="using-the-crawl-scope-manager"></a>使用編目範圍管理員

編目範圍管理員 (CSM) 是一組介面，可提供方法來通知 Windows Search 引擎有關要將容器編目的容器，以及要在目錄中包含或排除的容器底下的專案。 開發人員可以使用 CSM，以程式設計方式為新的資料存放區或通訊協定處理常式定義編目範圍。 系統管理員可以使用 CSM 來查看所有使用者的索引、搜尋根和範圍規則。

本節的組織方式如下：

-   [什麼是編目範圍管理員？](#what-is-the-crawl-scope-manager)
-   [搜尋根和範圍規則](#search-roots-and-scope-rules)
    -   [搜尋根目錄](#search-roots-and-scope-rules)
    -   [範圍規則](#scope-rules)
-   [編目範圍管理員支援的群組原則](#group-policies-supported-by-the-crawl-scope-manager)
-   [相關主題](#related-topics)

## <a name="what-is-the-crawl-scope-manager"></a>什麼是編目範圍管理員？

若要瞭解編目範圍管理員，您必須瞭解下列詞彙：

-   編目 *範圍* 是指向資料存放區或容器的一組 url (電子郵件資料存放區、資料庫、網路檔案共用等) ，索引子會進行編目以索引項目目。 若為階層式資料存放區，編目範圍可以包含父 URL，但會排除子 URL，反之亦然。 編目範圍內的專案會編制索引;系統會忽略編目範圍外的專案。
-   *搜尋根目錄* 是識別與特定通訊協定處理常式相關聯之容器或資料存放區的最上層 URL。 搜尋根可以識別特定于使用者、位於遠端電腦上，或符合萬用字元模式的位置。 當您加入新的資料存放區或通訊協定處理常式時，您也應該在編目範圍中新增搜尋根。
-   *範圍規則* 是一種規則，包含或排除搜尋根內的 url，使其無法進行編目及編制索引。 例如，假設您想要將 ProjectFiles 資料夾中的所有專案編制索引，但子資料夾原型除外。 您需要 file:///C： WorkteamA ProjectFiles 的包含規則 \\ \\ \\ ，以及 File:///C： \\ WorkteamA ProjectFiles 原型的排除規則 \\ \\ \\ 。

**編目範圍管理員 (CSM)** 是一組 api，可讓您新增、移除和列舉 Windows Search 索引子的搜尋根和範圍規則。 當您想要讓索引子開始編目新的容器時，您可以使用 CSM 來設定搜尋根目錄 (s) 和範圍規則，以尋找搜尋根 () 中的路徑。 例如，如果您安裝新的通訊協定處理常式，您可以建立搜尋根，並新增一或多個包含規則。然後，索引子就可以開始進行初始索引編制的爬網。 CSM 提供下列介面來協助您以程式設計方式執行這項作業。

-   [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
-   [IEnumSearchScopeRules](/windows/win32/api/searchapi/nn-searchapi-ienumsearchscoperules)
-   [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   [ISearchCrawlScopeManager2](/windows/win32/api/searchapi/nn-searchapi-isearchcrawlscopemanager2)
-   [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
-   [**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
-   [ISearchItem](./-search-isearchitem.md)

雖然您可以使用 CSM Api 以程式設計方式定義編目範圍，但 CSM 也是設計來支援終端使用者。 例如，假設您已開發新資料存放區的通訊協定處理常式，而您想要讓使用者或系統管理員管理應該編制索引的路徑。 您可以使用編目範圍管理員設定一或多個搜尋根 (例如，file:///C： \\ MyContainer \\) ，而設定索引編制選項的 Windows Search 使用者介面會顯示每個具有核取方塊的搜尋根。 然後，使用者可以包含或排除該路徑或該路徑的子系。

## <a name="search-roots-and-scope-rules"></a>搜尋根和範圍規則

搜尋根和範圍規則，並定義一組工作中的 Url，以組成索引子的編目範圍。

### <a name="search-roots"></a>搜尋根目錄

設定搜尋根目錄並不會指定應編制此存放區的哪些部分的索引;它只會指出內容存放區存在，且與已註冊的通訊協定處理常式相關聯。 搜尋根目錄的語法包含通訊協定、網站或使用者安全識別碼，以及要進行編目之位置 () 的路徑。

當您執行下列動作時，您應該建立新的搜尋根目錄：

-   安裝通訊協定處理常式或
-   想要為新的資料存放區編制索引

AND

-   該資料存放區尚未存在於索引子的編目範圍中。

如需新增、移除和列舉搜尋根的指示，請參閱 [管理搜尋根](-search-3x-wds-extidx-csm-searchroots.md) 。

### <a name="scope-rules"></a>範圍規則

範圍規則包括或排除搜尋根內的 Url，使其無法進行編目及編制索引。 範圍規則可以由終端使用者、群組原則或協力廠商開發人員設定。 當您定義新的搜尋根目錄時，您應該以程式設計的方式定義範圍規則。 您的搜尋根目錄和範圍規則，包含資料存放區和通訊協定處理常式的預設編目範圍。

> [!Note]  
> 具有主控台存取權的使用者可以修改預設編目範圍。 因此，任何提供範圍管理的應用程式都應該一律使用列舉方法，直接從 CSM 取得規則，而不是依賴其本身儲存的使用者規則複本。

 

如需新增、移除、還原和列舉範圍規則的指示，請參閱 [管理範圍規則](-search-3x-wds-extidx-csm-scoperules.md) 。

## <a name="group-policies-supported-by-the-crawl-scope-manager"></a>編目範圍管理員支援的群組原則

系統管理員可以使用群組原則來定義整個組織的編目範圍。 這些群組原則規則也可以作為使用者可覆寫的預設規則。 例如，您可以為一個使用者群組編制一組目錄，並為另一個使用者群組建立不同的集合，讓使用者可以取消選取這些預設值。 群組原則規則也可以做為使用者無法覆寫的強制排除規則，以防止特定使用者編制特定網路共用的索引。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理搜尋根目錄](-search-3x-wds-extidx-csm-searchroots.md)
</dt> <dt>

[管理範圍規則](-search-3x-wds-extidx-csm-scoperules.md)
</dt> <dt>

[索引處理常式](-search-indexing-process-overview.md)
</dt> </dl>

 

 
