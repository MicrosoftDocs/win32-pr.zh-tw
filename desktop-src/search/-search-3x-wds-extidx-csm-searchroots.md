---
description: 編目範圍管理員 (CSM) 可讓您新增和移除資料存放區與 Windows Search 編目範圍之間的搜尋根。
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: 管理搜尋根目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191211"
---
# <a name="managing-search-roots"></a>管理搜尋根目錄

編目範圍管理員 (CSM) 可讓您新增和移除資料存放區與 Windows Search 編目範圍之間的搜尋根。

本主題包含下列主旨：

-   [關於搜尋根目錄](#about-search-roots)
-   [開始之前](#before-you-begin)
-   [Windows 7：新的編目範圍管理員 API](#windows-7-new-crawl-scope-manager-api)
-   [將根目錄新增至編目範圍](#adding-roots-to-the-crawl-scope)
-   [從編目範圍中移除根目錄](#removing-roots-from-the-crawl-scope)
-   [列舉編目範圍中的根](#enumerating-roots-in-the-crawl-scope)
-   [相關主題](#related-topics)

 

## <a name="about-search-roots"></a>關於搜尋根目錄

搜尋根目錄會定義 Shell 命名空間的基底，其中可以包含或排除特定範圍，而且通常是可列舉的通訊協定中最高層級的容器。 它不會指定應該或不應該編制索引的這個存放區的哪些部分;它只會指出內容存放區存在，且與已註冊的通訊協定處理常式相關聯。 識別搜尋根 URL 的語法包含通訊協定、存放區或使用者的安全識別碼、路徑，以及選擇性的特定專案 (例如檔案) 。 下列範例示範兩種形式的搜尋根目錄語法。


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



<protocol>區段後面必須接著兩個 (2) 正斜線 ( '/' ) ，除非它是 file： protocol， (file:///) 需要三個斜線。 <site or SID>如果搜尋根目錄必須是使用者特定的，則區段代表內容存放區或使用者安全識別碼。 <path>區段是一組容器，例如目錄或資料夾，而且可以包含萬用字元 ' \* '。 此 <item> 區段是選擇性的，也可以包含萬用字元 ' \* '。 如果您未包含專案，請務必使用斜線完成路徑區段，否則索引子會假設最後一個 subcontainer 是專案。

例如，假設您已執行通訊協定處理常式 (myPH) 來處理 \* 自訂應用程式的 myext 檔案。 所有這些檔案都位於 \\ 本機電腦上的 WorkteamA ProjectFiles 資料夾中。 的搜尋根可能看起來像這樣：

-   myPH:///C： \\ WorkteamA \\ ProjectFiles\\

假設您打算在索引中包含所有的 myext 檔案，但不包含任何其他容器。 的搜尋根可能看起來像這樣：

-   myPH:///C： \\ WorkteamA \\ ProjectFiles \\ \* . myext。

萬用字元模式會使用萬用字元 ' ' 定義 Url， \* 並將其視為模式而非 URL，但術語通常會交替使用。 例如，file:///C： \\ ProjectA \\ \* \\ 資料 \\ 會符合下列 url：

-   C： \\ ProjectA \\ **version1** \\ 資料\\
-   C： \\ ProjectA \\ **version2** \\ 資料\\

但該模式不符合這個 URL：

-   C： \\ ProjectA \\ **version1 \\ temp** \\ 資料\\

您應該針對尚未在索引子的編目範圍中的容器建立新的搜尋根。 如果路徑 C： \\ ParentScope 已包含在編目範圍中， \\ \\ 除非您知道先前已排除子範圍，否則不需要為 C： ParentScope ChildScope 新增搜尋根目錄。

設定 Windows Search 選項的使用者介面會向使用者顯示搜尋根，讓他們可以精簡搜尋的範圍規則。 在您的自訂通訊協定處理常式、容器及/或應用程式的安裝過程中，您可以使用包含和排除規則來定義預設編目範圍。 這些規則會呈現給終端使用者作為位置。 使用者可以在預先定義之搜尋根目錄的子目錄中流覽，然後選取要包含在搜尋中的專案，或清除要排除的專案。

 

## <a name="before-you-begin"></a>開始之前

您必須執行下列必要條件步驟，才能使用任何編目範圍管理員 (CSM) 介面：

1.  建立 **CrawlSearchManager** 物件，並取得其 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 介面。
2.  針對 "SystemIndex" 呼叫 [**ISearchManager：： GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) ，以取得 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 介面的實例。
3.  呼叫 [**ISearchCatalogManager：： GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) 來取得 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面的實例。

對編目範圍管理員 (CSM) 進行任何變更之後，您必須呼叫 [**ISearchCrawlScopeManager：： SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall)。 這個方法不接受任何參數，且 \_ 成功時傳回 S OK。

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7：新的編目範圍管理員 API

在 **Windows 7 和更新版本** 中， [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) 擴充了 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面的功能。 [**ISearchCrawlScopeManager2：： GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion)方法會取得編目範圍管理員 (csm) 版本，這會在 csm 的狀態變更時通知用戶端。 **ISearchCrawlScopeManager2：： GetVersion** 不會產生跨進程呼叫。 如果函式成功，則傳回的指標會維持有效，直到用戶端在指標上呼叫 **UnmapViewOfFile** ，然後在傳回的控制碼上 **CloseHandle** 。

 

## <a name="adding-roots-to-the-crawl-scope"></a>將根目錄新增至編目範圍

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)會告知搜尋引擎有關要編目及/或監看的容器，以及要包含或排除的容器底下的專案。 若要加入新的搜尋根目錄，請將 [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) 物件具現化、設定根屬性，然後呼叫 [**ISearchCrawlScopeManager：： AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) ，然後將指標傳遞至您的 **ISearchRoot** 物件。 搜尋根目錄 URL 會採用與先前所述搜尋根目錄相同的形式。

下表描述 [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)的相關 put 方法;Windows Search 目前不使用介面的其他 put 方法。 建議您將使用者的安全識別碼包含在所有根目錄 (Sid) ，以獲得更好的安全性。 每個使用者的根目錄比較安全，因為查詢是在每個使用者進程中執行，以確保某一位使用者看不到從另一個使用者的收件匣編制索引的專案。



| 方法                     | 描述                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | 如果通訊協定處理常式或其他應用程式將會通知搜尋引擎有關搜尋根目錄下的 Url 變更，則設定為 **TRUE** 。 通知會指出 Url 需要重新編制索引。 |
| put \_ RootURL               | 設定目前搜尋的根 URL。 URL 會採用稍早所述的搜尋根表單。                                                                                                      |



 

 

依預設，當您新增搜尋根時，索引子不會將範圍編目。 您也必須為根目錄新增包含規則。 如果您想要為應用程式新增使用者專屬的根目錄，則應用程式會在應用程式啟動時，為新的使用者新增適當的根。

若要為新使用者新增適當的根目錄：

1.  取得使用者的 SID。
2.  列舉所有根目錄，以檢查此 SID 是否有一個。
3.  如有必要，請使用 SID 新增根。

 

## <a name="removing-roots-from-the-crawl-scope"></a>從編目範圍中移除根目錄

當您不再想要將該 URL 編制索引時，可以使用 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 從編目範圍中移除根。 移除根也會刪除該 URL 的所有範圍規則。 例如，假設您想要從系統卸載內容存放區和/或其通訊協定處理常式。 您可以卸載應用程式、移除所有資料，然後從編目範圍中移除搜尋根，而編目範圍管理員將會移除根目錄以及與根目錄相關聯的所有範圍規則。

若要移除現有的搜尋根目錄，請使用您想要移除的搜尋根來呼叫 [**ISearchCrawlScopeManager：： RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) 。 搜尋根目錄 URL 會採用與先前所述搜尋根目錄相同的形式。 如果找不到 \_ 根目錄，這個方法會傳回 FALSE，如果移除找到的根目錄時發生錯誤，則傳回錯誤碼。

移除搜尋根也會從使用者介面移除 Windows Search 選項的 URL，因此使用者可能無法使用使用者介面重新新增該容器或位置。 您也可以移除搜尋根目錄的所有使用者設定覆寫，並還原為原始搜尋根目錄和範圍規則。 如需詳細資訊，請參閱 [管理領域規則](-search-3x-wds-extidx-csm-scoperules.md)。

> [!Note]  
> 在 Windows Vista 中，如果使用者是透過主控台中的使用者設定檔移除，則 CSM 會移除所有規則和根目錄及其 SID，並從目錄中移除其索引項目目。 在 Windows XP 上，您需要手動移除使用者的根和規則。

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>列舉編目範圍中的根

CSM 會使用標準的 COM 樣式列舉值介面 [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)來列舉搜尋根。 您可以使用此介面來列舉搜尋根的一些用途。 例如，您可能想要在使用者介面中顯示整個編目範圍，或探索特定根或根項目是否已在編目範圍中。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**概念**
</dt> <dt>

[使用編目範圍管理員](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[管理範圍規則](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



