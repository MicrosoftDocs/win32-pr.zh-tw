---
description: 在 Windows Search 中查詢進程
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: 在 Windows Search 中查詢進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffec01c7b85b54d56e4e1092004be7e18e318b736cb591a10db0973153471cd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680249"
---
# <a name="querying-process-in-windows-search"></a>在 Windows Search 中查詢進程

本主題的組織方式如下：

-   [關於查詢 Windows Search](#about-querying-in-windows-search)
    -   [本機和遠端查詢](#local-and-remote-queries)
    -   [結構化查詢 API 總覽](#structured-query-api-overview)
-   [查詢案例](#querying-scenarios)
    -   [條件提取和查詢剖析](#condition-extraction-and-query-parsing)
    -   [查詢索引](#querying-the-index)
-   [相關主題](#related-topics)

## <a name="about-querying-in-windows-search"></a>關於查詢 Windows Search

Windows Search 中的查詢是以下列四種方法為基礎：

-   [Advanced Query 語法](-search-3x-advancedquerysyntax.md) (AQS) 
-   NQS) 的自然查詢語法 (
-   結構化查詢語言 (SQL) (Structured Query Language (SQL))
-   結構化查詢介面

AQS 是 Windows Search 用來查詢索引，以及精簡和縮小搜尋參數的預設查詢語法。 AQS 主要是使用者面向的，可供使用者用來建立 AQS 查詢，但開發人員也可以使用它來以程式設計方式建立查詢。 在 Windows 7 中引進標準 AQS，且必須用來以程式設計方式產生 AQS 查詢。 在 Windows 7 和更新版本中，可以根據是否符合 AQS 條件來使用快捷方式功能表選項。 如需詳細資訊，請參閱 [建立快捷方式功能表處理常式](../shell/context-menu-handlers.md)中的「使用 Advanced Query 語法取得靜態動詞的動態行為」。 AQS 查詢可以限制為特定類型的檔案，也就是所謂的檔案類型。 如需詳細資訊，請參閱 [檔案類型和關聯](../shell/fa-intro.md)。 如需相關屬性的參考 [檔，請參閱](../properties/props-system-kind.md) [KindText](../properties/props-system-kindtext.md)。

NQS 是比 AQS 更寬鬆的查詢語法，類似于人類語言。 如果選取 NQS，而不是預設的 AQS，Windows Search 可以使用 NQS 來查詢索引。

SQL 是定義查詢的文字語言。 SQL 在許多不同的資料庫技術中都很常見。 Windows搜尋會使用 SQL、執行它的子集，並藉由將專案新增至語言來加以擴充。 Windows搜尋 SQL 擴充標準的 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強其實用性。 Windows Search SQL 的所有功能都與 Windows XP 和 Windows Server 2003 及更新版本上的 Windows Search 相容。 如需 Windows Search SQL 的詳細資訊，請參閱[使用 Windows Search SQL 語法來查詢索引](-search-sql-windowssearch-entry.md)，以及[Windows Search 語法的總覽](-search-sql-ovwofsearchquery.md)。

本主題稍後會描述結構化查詢 Api。 如需結構化查詢 Api 的參考檔，請參閱 [查詢介面](-search-querying-interfaces-entry-page.md)。 介面（例如 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ）有助於從一組輸入值 SQL 字串。 這個介面會將 AQS 的使用者查詢轉換成 Windows Search SQL 並指定可在 SQL 中表示的查詢限制，而不能在 AQS 中表示。 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)也會取得連接到 Windows Search 資料庫 OLE DB 連接字串。

### <a name="local-and-remote-queries"></a>本機和遠端查詢

您可以在本機或遠端執行查詢。 下列範例顯示使用 [FROM 子句](-search-sql-from.md) 的本機查詢。 本機查詢只會查詢本機 SystemIndex 目錄。


```
FROM SystemIndex
```



下列範例顯示使用 [FROM 子句](-search-sql-from.md) 的遠端查詢。 加入 ComputerName 會將前一個範例轉換為遠端查詢。


```
FROM [<ComputerName>.]SystemIndex
```



依預設，Windows XP 和 Windows Server 2003 未安裝 Windows Search。 只有 Windows Search 4 (WS4) 提供遠端查詢支援。 舊版的 Windows Desktop 搜尋 (WDS) （例如3.01 和更早版本）不支援遠端查詢。 您可以使用 Windows 檔案總管來查詢遠端電腦的本機索引，以尋找 "file：" 通訊協定) 所處理的檔案系統專案 (專案。

若要透過遠端查詢取得專案，專案必須符合下列需求：

-   可透過通用命名慣例 (UNC) 路徑來存取。
-   存在於用戶端可存取的遠端電腦上。
-   將其安全性設定為允許用戶端擁有讀取權限。

WindowsExplorer 有共用專案的功能，包括網路和共用中心中的「公用」共用 (\\ \\ 電腦 \\ \\ ) ，以及「使用者」共用 (\\ \\ 電腦 \\ 使用者 \\ ... ) 透過共用嚮導共用的專案。 在您共用 (s) 的資料夾之後，您可以在 FROM 子句中指定遠端電腦的電腦名稱稱，並在範圍子句中的遠端電腦上指定 UNC 路徑，藉以查詢本機索引。 下列範例顯示使用 FROM 和 SCOPE 子句的遠端查詢。


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



此處提供的範例會使用 SQL。

### <a name="structured-query-api-overview"></a>結構化查詢 API 總覽

結構化查詢可讓您依個別屬性的查詢布林值組合來搜尋資訊。 在本主題中，我們將概述最重要的結構化查詢 Api 和方法的功能。 如需結構化查詢 Api 的參考檔，請參閱 [查詢介面](-search-querying-interfaces-entry-page.md)。

### <a name="iqueryparser"></a>IQueryParser

[**IQueryParser：:P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse)方法會剖析使用者輸入字串，並以 [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)的形式產生轉譯。 如果該方法的 *pCustomProperties* 參數不是 null，則它是 [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) 物件的列舉， (每一個可辨識的自訂屬性) 。 其他 [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) 方法可讓應用程式設定數個選項，例如地區設定、架構、斷詞工具，以及各種命名實體類型的處理常式。 [**IQueryParser：： GetSchemaProvider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) 會傳回 [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) 介面，以流覽已載入的架構。

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution : IConditionFactory

[**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)介面提供有關剖析輸入字串之結果的所有資訊。 由於 **IQuerySolution** 也是 [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) 介面，因此可以建立額外的條件樹狀節點。 [**IQuerySolution：： GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery)方法會產生轉譯的條件樹狀結構。 **IQuerySolution：： GetQuery** 也會傳回語義型別。

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) 會建立條件樹狀節點。 如果 [**IConditionFactory：： MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot)的 *簡化* 參數為 **VARIANT \_ TRUE**，則產生的 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)會簡化，而且不需要是負的節點。 如果 [**IConditionFactory：： MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor)的 *pSubConditions* 參數不是 null，則該參數應為 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)物件的列舉，並且成為子樹。[**IConditionFactory：： MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf)會使用指定的屬性名稱、作業和值來建立分葉節點。 *PValueType* 參數中的字串應該是架構中的語義型別名稱。 如果 *expand* 參數為 **VARIANT \_ TRUE** 且屬性為 virtual，則產生的條件樹狀結構通常是將屬性展開為其定義的子系所產生的分離結果。 如果不是 null， *pPropertyNameTerm*、 *pOperatorTerm* 和 *pValueTerm* 參數應該識別指出屬性、作業和值的詞彙。

### <a name="icondition--ipersiststream"></a>ICondition： IPersistStream

[**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)介面是條件樹狀結構中的單一節點。 節點可以是否定節點、節點、節點或分葉節點。 非分葉節點的 [**ICondition：： GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) 會傳回子樹的列舉。 若為分葉節點，下列 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) 方法會傳回下列值：

-   [**GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) 會傳回屬性名稱、運算和值。
-   [**GetValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype)會傳回值的語義型別，這個值是在 [**IConditionFactory：： MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf)的 *pszValueType* 參數中 specificied 的。
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) 會傳回值的字串形式。  (如果值已是字串，此表單就會根據大小寫、重音等進行正規化。 ) 
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) 會傳回輸入句子中哪些部分產生屬性名稱、作業和值的相關資訊。
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) 會傳回條件樹狀結構的深層複本。

### <a name="irichchunk"></a>IRichChunk

每個 [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) 物件都會識別一個 token 範圍和一個字串。 **IRichChunk** 是公用程式介面，代表範圍的相關資訊， (通常是以起始位置和長度識別的權杖範圍) 。 此範圍資訊包括字串和/或 **變異**。

### <a name="iconditiongenerator"></a>IConditionGenerator

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)介面是由應用程式提供，用來處理命名實體類型的辨識和條件樹狀結構產生。 條件產生器會透過 [**IQueryParser：： SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption)提供給 [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) 。 [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)會使用目前載入之架構的 [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider)來呼叫 [**IConditionGenerator：： Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) 。 這麼做可讓 [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) 取得所需的任何架構資訊。 剖析輸入字串時， **IQueryParser** 會呼叫每個 [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)的 [**IConditionGenerator：： RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities)方法，如此一來，就可以報告在輸入字串中可辨識的已命名實體的出現次數。 **IQueryParser** 可以使用目前的地區設定，而且應該使用輸入的 token 化，因為它需要報告任何命名實體的權杖範圍。

當 [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) 即將發出分葉節點，而且值的語義型別符合 [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)的命名實體型別時， **IQueryParser** 會使用要產生之節點的資訊來呼叫 [**IConditionGenerator：： GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) 。 如果 [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) 傳回「 \_ 確定」，則應該傳回不需要是分葉節點的條件樹狀結構 () ，並通知 **IQueryParser** 是否要隱藏通常會產生的替代字串解釋以做為預防措施。

### <a name="itokencollection"></a>ITokenCollection

[**ITokenCollection：： NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens)方法會傳回權杖數目。[**ITokenCollection：： GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken)會傳回關於我的第 *i* 個權杖的資訊。 開頭和長度是輸入字串中的字元位置。 只有當有文字覆寫輸入字串中的字元時，傳回的文字才會是 null。 例如，這是用來覆寫輸入字串中的虛線，而不是在應該將該虛線視為負的內容中。

### <a name="inamedentitycollector"></a>INamedEntityCollector

針對每個已辨識的實體， [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)會呼叫 [**INamedEntityCollector：： Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) 。 範圍是權杖範圍。 它一定是 *beginSpan* 的情況？ *beginActual*  < *endActual* 嗎？ *endSpan*。 *beginSpan* 和 *endSpan* 可能會與 *beginActual* 和 *endActual* 不同，如果命名實體的開頭和/或結尾是以語義來說不重要的標記，例如引號 (，但已命名實體) 所涵蓋的標記。 值必須以字串表示，之後會出現在 [**IConditionGenerator：： GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf)的呼叫中。

### <a name="ischemaprovider"></a>ISchemaProvider

[**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider)介面可以用來流覽 (類型) 和關聯 (屬性) 的已載入架構。 以下是其個別方法的用途：

-   [**實體**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) 會傳回架構中每個實體 ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) 的列舉。
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) 會傳回架構的根實體。 針對一般架構，會傳回每個 [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) 的主要類型。
-   [**GetEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) 會依名稱尋找實體， \_ 如果架構中沒有這類實體，就會傳回 FALSE。
-   [**中繼資料**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) 會傳回 [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) 介面的列舉。

### <a name="ientity"></a>IEntity

[**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)介面是一個架構實體，代表具有名稱的類型、有一些與其他類型的已命名關聯性 (屬性) ，並且衍生自基底實體。 以下是其個別方法的用途：

-   [**IEntity：：關聯**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) 性會傳回 [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) 物件的列舉，此類型的每個外寄關聯都有一個列舉。 實體的每個外寄關聯都有一個名稱。
-   [**IEntity：： GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) 會依名稱尋找關聯性， \_ 如果這個實體沒有這類關聯性，就會傳回 FALSE。
-   [**IEntity：： MetaData**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) 會傳回 [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) 介面的列舉，此實體的每個中繼資料配對都有一個列舉。
-   [**IEntity：:D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) 會傳回預設片語，以協助產生條件樹狀結構的 AQS 或 NQS 重述。

### <a name="irelationship"></a>IRelationship

[**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship)介面代表兩個實體之間的關聯性：來源和目的地。 以下是其個別方法的用途：

-   [**IRelationship：： IsReal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) 報告關聯性是否為真實的。 例如，如果實體 A 衍生自實體 B，並繼承名稱為 R 的關聯性，則可能仍有它自己的關聯性名稱 R。不過，關聯性 beween A 和 R 必須具有與 B 相同的目的地類型，而且它要存在的唯一原因是儲存 B 專屬的中繼資料。B 的關聯性雖不是真正的關聯性。
-   [**IRelationship：： Medadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) 會傳回 [**IMetaData**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) 介面的列舉，此實體的每個中繼資料配對都有一個列舉。
-   [**IRelationship：:D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) 會傳回在重述中用於此關聯性的預設片語。 每個關聯性都有一個預設片語，表示它有助於產生條件樹狀結構的 AQS 或 NQS 重述。

### <a name="imetadata"></a>IMetaData

中繼資料是成對的索引鍵/值組，每個都與實體、關聯性或整個架構相關聯。 因為索引鍵不一定是唯一的，所以可將中繼資料的集合視為多對應。 呼叫 [**IMetaData：：**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata)中繼資料，以取出組的索引鍵和值。

## <a name="querying-scenarios"></a>查詢案例

下列案例說明一般查詢案例中 Windows Search 的結構化查詢 api 用法，例如建立條件樹狀結構和查詢索引。

### <a name="condition-extraction-and-query-parsing"></a>條件提取和查詢剖析

建立查詢時，會藉由告訴系統要搜尋的位置來定義其範圍。 這會限制搜尋結果。 定義範圍之後，會套用篩選，並傳回篩選器集合。 藉由建立具有分葉節點的條件樹狀結構（類似于圖表）來限制搜尋結果。 然後會將這些條件解壓縮。 條件樹狀結構是一個布林值組合 (AND、OR、NOT) 的分葉條件，每個條件都會將某個屬性（property）與值產生關聯。 分葉節點代表透過某些作業對單一屬性進行值的限制。

篩選準則限制需要描述限制的邏輯運算式。 定義此運算式的開頭是 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) 介面，此介面是用來在條件樹狀結構中建立單一節點。 因為在下列範例中只有一個條件，所以樹狀結構不會變更。


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



如果有一個以上的篩選準則，則和和其他布林運算子會用來達成單一樹狀結構。 和-樹狀結構或樹狀結構代表其子樹的結合和 disjunctions。 非樹狀結構代表其單一子樹的否定。 AQS 提供使用布林運算子來達成邏輯運算式的文字方法，通常較為簡單。

在下一個範例中，我們會將條件樹狀結構 ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) 轉換成視覺化形式。 使用 [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) 介面的查詢剖析器會將 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) 轉換成格式化 (rtf) 查詢字串格式的 rtf 格式文字。 [**IQueryParser：： RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring)方法會傳回查詢文字，而 [**IQueryParser：:P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse)方法會產生 [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)介面。 下列範例示範如何執行所有動作。


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



[**IQueryParser：:P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse)的主要輸入是要剖析的使用者輸入字串，但應用程式也可以通知查詢剖析器，其在輸入 (從應用程式特定的語法) 中辨識的任何屬性。 **IQueryParser：:P arse** 的輸出是一種 [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)，可提供與該剖析調用相關的所有資訊。 有一些方法可取得輸入字串、輸入字串的 token 化方式、任何剖析錯誤，以及剖析的查詢 as 條件樹狀結構（以 [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)表示）。 下列範例顯示 .。。


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



在上述範例中， [**IQuerySolution：： GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) 可以取得查詢的相關資訊，包括原始文字、組成文字的權杖或條件樹狀結構。 下表列出可能傳回查詢值的範例。



| 傳回查詢值的範例                        | 描述                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | [**IQueryParser：： RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring)傳回的查詢文字 |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | 標記的細分                                                                                  |
| ![未解決的條件樹狀結構](images/queryvalues1.png) | 未解決的條件樹狀結構                                                                              |



 

傳回的初始條件樹狀結構無法解析。 在無法解析的條件樹狀結構中，日期和時間的參考（例如 `date:yesterday` ）不會轉換為絕對時間。 此外，虛擬屬性不會展開。 虛擬屬性是作為多個屬性匯總的屬性。

例如，查詢會 `kind:email from:reljai` 產生下列未解決和已解決的條件樹狀結構。 無法解析的條件樹狀結構是在左邊，而已解決的條件樹狀結構是右邊。

![未解決和已解決的條件樹狀結構](images/conditiontree.png)

您可以藉由呼叫 [**IConditionFactory：： Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve)來取得已解析的樹狀結構。 不過，傳遞 [**SQRO 不會 \_ \_ 解決 \_ DATETIME**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) ，無法解析日期和時間。 無法解析的條件樹狀結構有一些優點，因為未解決的條件樹狀結構包含查詢的相關資訊。 每個分葉節點都會指向 [**IQuerySolution：： GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata)所傳回的標記，這會在使用 [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) 介面時對應至屬性、運算子和值。 下列範例顯示 .。。


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>查詢索引

有幾種方法可以查詢索引。 有些是以 SQL 為基礎，其他則是以 AQS 為基礎。 您也可以使用查詢[介面](./-search-querying-interfaces-entry-page.md)，以程式設計方式查詢 Windows Search 索引。 查詢索引有三個特定的介面： [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)、 [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)和 [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)。 如需概念性資訊，請參閱以程式設計 [方式查詢索引](-search-3x-wds-qryidx-overview.md)。

您可以使用 [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 介面來開發元件或 helper 類別，以查詢索引。 這個介面會實作為 helper 類別，以 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (和 [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) ，而且是藉由呼叫 [**ISearchCatalogManager：： GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)取得。 如需概念性資訊，請參閱 [使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)。

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) 可讓您：

-   取得連接到 Windows Search 資料庫 OLE DB 連接字串。
-   將 AQS 使用者查詢轉換成 Windows Search SQL。
-   指定可在 SQL 中表示但無法在 AQS 中表示的查詢限制。

Windows 7 和更新版本支援索引優先順序和資料列集事件。 With [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) 有一個優先順序堆疊，可讓用戶端要求特定查詢中所使用的範圍高於一般優先順序。 [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) 會提供資料列集內專案變更的通知，包括新增專案、刪除專案，以及修改專案資料。 使用資料列集事件通知可確保常設查詢的結果盡可能保持最新狀態。 如需概念性資訊，請參閱[Windows 7 中的索引優先順序和資料列集事件](indexing-prioritization-and-rowset-events.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 中的編制索引、查詢和通知](-search-3x-wds-included-in-index.md)
</dt> <dt>

[索引中包含的內容](-search-indexing-process-overview.md)
</dt> <dt>

[Windows Search 中的編制索引進程](-search-indexing-process-overview.md)
</dt> <dt>

[Windows Search 中的通知處理](-search-3x-wds-support.md)
</dt> <dt>

[URL 格式設定需求](url-formatting-requirements.md)
</dt> </dl>

 

 
