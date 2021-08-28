---
description: 編目範圍管理員 (CSM) 可讓您定義範圍規則，其中包含或排除來自 Windows Search 編目範圍的 url。
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: 管理範圍規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134e4241e9dcd66e468935ae56a4029a51a96c37
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880212"
---
# <a name="managing-scope-rules"></a>管理範圍規則

編目範圍管理員 (CSM) 可讓您定義範圍規則，其中包含或排除來自 Windows Search 編目範圍的 url。

CSM 可讓您執行下列作業：

-   將新的範圍規則新增至工作規則集
-   移除現有的範圍規則
-   列舉預設範圍規則
-   探索是否要在編目範圍中包含或排除特定的 URL，或具有父系或子範圍規則

 

本主題包含下列主旨：

-   [關於範圍規則](#about-scope-rules)
-   [開始之前](#before-you-begin)
-   [新增範圍規則](#adding-scope-rules)
    -   [使用者規則的注意事項](#notes-on-user-rules)
-   [移除範圍規則](#removing-scope-rules)
-   [還原為預設規則](#reverting-to-default-rules)
-   [列舉範圍規則](#enumerating-scope-rules)
-   [追蹤範圍規則](#tracing-scope-rules)
-   [相關主題](#related-topics)

## <a name="about-scope-rules"></a>關於範圍規則

範圍規則是一種規則，包含或排除搜尋根內的 Url，使其無法進行編目及編制索引。 包含規則會導致索引子將該 URL 包含在 scrawl 範圍內，而排除規則會導致索引子將該 URL 從編目範圍中排除 (與其子系) 。

例如，假設您已安裝新的應用程式，其資料檔案位於 \\ 本機電腦上的 WorkteamA ProjectFiles 資料夾中。 假設您想要將 ProjectFiles 資料夾中的所有專案編制索引，但子資料夾原型中的專案除外。 在這種情況下，您需要 myPH:///C： \\ WorkteamA ProjectFiles 的包含 \\ 規則 \\ ，以及 MyPH:///C： \\ WorkteamA \\ ProjectFiles 原型的排除 \\ 規則 \\ 。

有三種類型的規則，優先順序如下：

1.  群組原則規則是由系統管理員所設定，而且可以覆寫所有其他規則。
2.  使用者規則是由使用者在 Windows Search options 使用者介面中修改範圍而設定。 使用者或其他應用程式可以移除所有的使用者規則，並還原為預設規則。
3.  預設規則通常是由應用程式設定，以定義預設範圍。 例如，當新的通訊協定處理常式或容器新增至系統時，可能會設定預設規則。

這些類型的規則會一起組成編目範圍管理員 (CSM) 產生要編目之 Url 的完整清單的 *工作規則集* 。 雖然群組原則規則和使用者規則可以覆寫預設規則，但它們會保留在自己的預設規則集中，您隨時都可以將其還原。 索引子會從工作規則集編目 Url，並將專案、屬性和內容新增至目錄。

> [!Note]  
> 具有主控台存取權的使用者，可以透過該介面修改規則。 因此，提供範圍管理的應用程式應該一律使用列舉方法，直接從 CSM 取得規則，而不是依賴已儲存的使用者規則複本。

 

排除規則可以使用萬用字元 ' ' 定義模式 Url， \* 例如： file:///C： \\ ProjectA \\ \* \\ 。 使用此模式的排除規則，可防止索引子將 ProjectA 目錄下的任何資料夾編目。 針對較複雜的範例，假設有一個包含 file:///C： ProjectA 的規則 \\ \\ ，以及 file:///C： ProjectA 資料的排除模式 \\ 規則 \\ \* \\ \\ \* 。 在此情況下，索引子會編目中的專案：

-   C： \\ ProjectA\\
-   C： \\ ProjectA \\ **version1** \\ testfiles\\
-   C： \\ ProjectA \\ **version1 \\ temp** \\ 資料\\

但是，索引子不會將中的專案編目：

-   C： \\ ProjectA \\ **version1** \\ 資料\\

 

## <a name="before-you-begin"></a>開始之前

使用任何編目範圍管理員介面之前，您必須執行下列必要條件步驟：

1.  建立 **CSearchManager** 物件，並取得其 **ISearchManager** 介面。
2.  針對 "SystemIndex" 呼叫 **ISearchManager：： GetCatalog** ，以取得 **ISearchCatalogManager** 介面的實例。
3.  呼叫 **ISearchCatalogManager：： GetCrawlScopeManager** 來取得 **ISearchCrawlScopeManager** 介面的實例。

對編目範圍管理員進行任何變更之後，您必須呼叫 [**ISearchCrawlScopeManager：： SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) 方法。 這個方法不接受任何參數，且 \_ 成功時傳回 S OK。

 

## <a name="adding-scope-rules"></a>新增範圍規則

CSM 的工作規則集包括使用者和預設規則，以及群組原則強制執行的任何規則。 使用者規則是由使用者在使用者介面中設定，而預設規則可以由下列任何一項設定：

-   系統管理員所執行的群組原則 (這些不會使用 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面。 ) 
-   應用程式的安裝或更新，例如 Windows Search 或通訊協定處理常式
-   新增資料存放區或容器的安裝應用程式

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)提供兩種方法來加入新的範圍規則，如下表所述。 檔案系統的包含規則路徑結尾必須是反斜線 ' \\ ' (例如，file:///C： \\ files \\) ，而排除規則的路徑結尾必須是星號 (例如 file:///c： \\ files \\ \*) 。 只有排除規則可以包含模式 Url。 此外，我們建議您在路徑中包含使用者的安全識別碼 (Sid) ，以獲得更好的安全性。 每個使用者的路徑更為安全，因為查詢會在每個使用者進程中執行，以確保某一位使用者看不到從另一個使用者的收件匣編制索引的專案。

下表說明用來新增範圍規則之 ISearchCrawlScopeManager 介面的方法。



| 方法                                                                              | 說明                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | 新增 URL 的規則，如同使用者所指定。 這些規則會覆寫預設規則。 如果您已執行使用者介面，讓使用者管理自己的範圍規則和 Url，請使用這個方法。                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | 新增 URL 的規則，如同其他應用程式（例如通訊協定處理常式）所指定。 當您已執行新的通訊協定處理常式，或加入新的資料存放區時，請使用這個方法。 這些規則可以由使用者規則覆寫。 |



 

每個方法都會取得可編制索引位置的 URL，以及決定是否應包含或排除 URL 的旗標。 *FFollowFlags* 參數已保留供日後使用。 當您加入新的範圍規則，且編目範圍管理員根據) 所提供的 URL 或模式來判斷規則已存在 (時，會更新工作規則集，如此一來， (1) 舊規則會被新規則取代， (2) 任何與其衝突的使用者規則都會被移除。

**秘訣：** 雖然 file://根目錄預設包含在編目範圍中，但預設不會編制程式檔案的索引。 因此，將資料儲存至 [Program Files] 目錄的應用程式必須將其位置新增為預設規則。

### <a name="notes-on-user-rules"></a>使用者規則的注意事項

如果新的使用者規則與現有的預設規則相同，則新的使用者規則會覆寫工作規則集中的預設規則。 如果新的使用者規則與現有的使用者規則相同，則會取代舊的使用者規則。

在工作規則集中設定旗標 *fOverrideChildren* 會產生下列結果：

-   **TRUE** 會導致從工作規則集移除所有子規則， (使用者規則和預設規則) 。
-   FALSE 會導致重新新增至工作規則，將所有預設規則設定為新使用者規則的子系。 如果子系預設規則為包含，而新的使用者規則為排除，則預設規則會變更為包含使用者規則。

 

## <a name="removing-scope-rules"></a>移除範圍規則

您可以使用 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 介面，從工作規則集移除範圍規則。 此介面提供下列兩個方法來移除範圍規則。



| 方法                                                                                    | 描述                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | 從工作規則集中移除指定之 URL 的使用者規則。 如果使用者規則是的重複項或覆寫預設規則，則預設規則會保留在工作規則集中。                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | 從工作規則集和預設規則集移除指定 URL 的預設規則。 呼叫這個方法之後，您就無法使用 RevertToDefaultScopes 還原為此預設規則。 |



 

每個方法都會使用 URL 和旗標，指出要移除的規則是包含或排除規則。 如果找不到具有該 URL 和包含/排除旗標的規則，則這些方法會傳回錯誤。

**秘訣：** 如果您想要完全移除編目範圍中的範圍，請使用 [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) 方法，此方法會移除搜尋根目錄和所有相關聯的範圍規則。 例如，在卸載時執行這項操作，被視為最佳做法。

您也可以移除搜尋根目錄的所有使用者設定覆寫，並還原為原始搜尋根目錄和預設範圍規則。 如需詳細資訊，請參閱下一節。

> [!Note]  
> 在 Windows Vista 中，如果使用者在主控台的使用者設定檔中移除，CSM 會移除所有包含其 SID 的規則和根，並從目錄中移除其索引項目目。 在 Windows XP 上，您必須手動移除使用者的根和規則。

 

 

## <a name="reverting-to-default-rules"></a>還原為預設規則

還原為預設規則會移除 URL 或根的所有使用者規則，並將所有預設規則還原至工作規則集。 但是，它並不會移除群組原則所設定的規則。 [**RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes)方法不接受任何參數，如果無法還原為預設規則，則會傳回錯誤碼。

 

## <a name="enumerating-scope-rules"></a>列舉範圍規則

CSM 會使用標準的 COM 樣式列舉值介面 [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) 來列舉範圍規則。 您可以使用此介面來列舉許多用途的範圍規則。 例如，您可能想要在使用者介面中顯示整個工作規則集，或探索規則或規則的子系是否已在編目範圍中。

 

## <a name="tracing-scope-rules"></a>追蹤範圍規則

CSM 也可讓您判斷指定的 URL 是否包含在編目範圍中，以及它是否具有父系或子系範圍規則。 您也可以瞭解在編目範圍中包含或排除 URL 的原因。 這些方法不適合搭配使用模式 Url。

下表說明用來新增範圍規則的 [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) 方法。



| 方法                                                                                      | 說明                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | 取得父包含 URL 的版本識別碼。 您可以使用這個方法來查看父範圍自您上次檢查之後是否已變更。<br/> 範例：如果郵件應用程式使用提供者管理的通知，它可能會在關閉之前取得父範圍版本，並在開啟時再次檢查版本。 然後，應用程式可以判斷它是否需要將一組新的通知推送至索引子。<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | 如果指定的 URL 具有子規則， (套用至其 URL 階層內任何層級之子系的規則，則傳回 **TRUE**) 。 <br/> 範例：如果 URL 為 file:///C： \\ folder \\ ，則如果 CSM 有專門針對 File:///C： folder 子資料夾的範圍規則，則此方法會傳回 **TRUE** \\ \\ \\ 。<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | 如果指定的 URL 具有父規則 (套用至 URL 階層中任何層級之父系的規則，則傳回 **TRUE**) 。<br/> 範例：如果 URL 是 file:///C： \\ folder \\ 子資料夾，則如果 CSM 有專門針對 File:///C： folder 的範圍規則，則這個方法會傳回 **TRUE** \\ \\ 。<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | 如果指定的 URL 包含在編目範圍中，則傳回 **TRUE** 。                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | 傳回 [**CLUSION \_ REASON**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) 列舉中的值，說明 url 包含在編目範圍中或從中排除的原因，如果 url 包含在編目範圍中，則抓取值 **TRUE** 。 此方法可協助您識別工作規則集內的衝突。                                                                                                                                       |



 

 

> [!Note]  
> [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)和 [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)方法會根據 CSM 中的規則，決定是否要將 URL 僅進行編目。 URL 未編目的原因可能有其他原因，例如設定的 FANCI 位 (也就是使用者在資料夾的 [屬性] 對話方塊中，不允許快速編制索引。 ) 

 

如果您認為應該排除檔案路徑，但是它會列為已包含的檔案路徑，請確定排除規則的結尾為「 &lt; 路徑」 &gt; \\ \* 。 如果您認為應該包含檔案或檔案路徑，但是它不是，請務必檢查檔案或路徑的 FANCI 位設定。 若要這樣做，請以滑鼠右鍵按一下檔案或檔案路徑，然後選取 [ **屬性**]，然後確定已選取 [ **快速搜尋]、[允許編制索引服務來為此資料夾編制索引** ] 核取方塊。 如果檔案或檔案路徑未標示為要在這裡進行索引編制，就不會將它編制索引，即使它是在包含規則中也一樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**概念**
</dt> <dt>

[管理搜尋根目錄](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




