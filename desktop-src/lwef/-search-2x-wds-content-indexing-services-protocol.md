---
title: 內容索引服務通訊協定
description: 本檔是內容索引服務通訊協定的規格。
ms.assetid: b91c8038-5ace-441d-8523-60f849ff1458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14573dac5a7a6818234c086d05b52e5b81c2a1c1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119733"
---
# <a name="content-indexing-services-protocol"></a>內容索引服務通訊協定

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

通訊協定規格，版本0.12

-   [1簡介](#1-introduction)
    -   [1.1 詞彙](#11-glossary)
    -   [1.2 參考](#12-references)
    -   [1.3 通訊協定總覽 (概要) ](#13-protocol-overview-synopsis)
    -   [1.4 與通訊協定的關聯性](#14-relationship-to-other-protocols)
    -   [1.5 必要條件和前置條件](#15-prerequisites-and-preconditions)
    -   [1.6 適用性陳述](#16-applicability-statement)
    -   [1.7 版本設定和功能交涉](#17-versioning-and-capability-negotiation)
    -   [1.8 廠商可延伸欄位](#18-vendor-extensible-fields)
    -   [1.9 標準指派](#19-standards-assignments)
-   [2 訊息](#2-messages)
    -   [2.1 傳輸](#21-transport)
    -   [2.2 訊息語法](#22-message-syntax)
-   [3 通訊協定詳細資料](#3-protocol-details)
    -   [3.1 伺服器詳細資料](#31-server-details)
    -   [3.2 用戶端詳細資料](#32-client-details)
-   [4 通訊協定範例](#4-protocol-examples)
    -   [4.1 範例1](#41-example-1)
    -   [4.2 範例2](#42-example-2)
-   [5 安全性](#5-security)
    -   [5.1 實作者的安全性考量](#51-security-considerations-for-implementers)
    -   [5.2 安全性參數的索引](#52-index-of-security-parameters)
-   [6個版本特定行為的索引](#6-index-of-version-specific-behavior)

本檔是內容索引服務通訊協定的規格。

工作組伺服器通訊協定程式 (WSPP) 檔集適用于搭配公用標準檔、網路程式設計藝術以及 Windows 工作組分散式系統概念，並假設讀者已熟悉上述的材質或立即存取它。

WSPP 通訊協定規格不需要使用 Microsoft 程式設計工具或程式設計環境，才能讓授權者開發執行。 擁有 Microsoft 程式設計工具和環境存取權的授權人可自由利用這些工具。

## <a name="1-introduction"></a>1 簡介

-   [1.1 詞彙](#11-glossary)
-   [1.2 參考](#12-references)
-   [1.3 通訊協定總覽 (概要) ](#13-protocol-overview-synopsis)
-   [1.4 與通訊協定的關聯性](#14-relationship-to-other-protocols)
-   [1.5 必要條件和前置條件](#15-prerequisites-and-preconditions)
-   [1.6 適用性陳述](#16-applicability-statement)
-   [1.7 版本設定和功能交涉](#17-versioning-and-capability-negotiation)
-   [1.8 廠商可延伸欄位](#18-vendor-extensible-fields)
-   [1.9 標準指派](#19-standards-assignments)

### <a name="11-glossary"></a>1.1 詞彙

> [!Note]  
> 下列詞彙定義于 MS-SYS 的詞彙區段中 \[ \] ：
>
> -   GUID
> -   位元組由小到小
> -   具名管道
> -   路徑

 

**Binding**：在傳回的資料 **列** 集中包含特定資料 **行** 的要求。 系結會指定要包含在搜尋結果 **中的屬性** 。

**書簽**：在一組資料列中唯一識別資料列的標記。

**目錄**：索引服務中最高層級的組織單位。 它代表一組已編制索引的檔，可讓您使用「內容索引服務」通訊協定來執行查詢。

**Category**：階層式資料列群組。 例如，包含 author 和 title 資料行的查詢結果可以根據作者分類。 每一組包含相同作者值的資料列都會構成一個類別目錄。

**章節**：一組 **資料列內** 的資料 **列** 範圍。

資料 **行**：資料 **列** 中單一類型資訊的容器。 資料行會對應至屬性名稱，並指定搜尋查詢的 **命令****樹** 元素所使用的屬性。

**命令樹**：為搜尋查詢指定的 **限制** 、 **類別** 和 **排序次序** 的組合。

資料 **指標**：一個實體，用來做為在結果集中傳回的一組資料中，一次處理一個資料 **列** 或小型資料 **列** 區塊的機制。 資料 **指標** 位於結果集內的單一資料 **列** 。 將資料 **指標** 置於資料列之後，就可以在該資料 **列** 或從該位置開始的資料 **列** 區塊上執行作業。

**控制碼**：可以用來識別及存取資料 **指標** 、 **章節** 和 **書簽** 的權杖。

**Index**：持續性結構，包含 **索引服務** 所提取的文字內容。 這包含單字清單，這些字組會與包含的檔案名、單字位置和 **地區** 設定一起儲存。

**索引**：從檔案中解壓縮文字和屬性，以及將解壓縮的值儲存到文字) 的 **索引** (，以及) 屬性的 **屬性** 快取 (的程式。

**索引服務**：為檔案系統的內容和屬性建立索引 **目錄** 的服務。 應用程式可以在目錄中搜尋已編制索引之檔案系統上的檔案資訊。

**地區** 設定：以 GPSI 附錄 A 指定的識別碼，可 \[ \] 指定與語言相關的喜好設定。 這些喜好設定會指出如何格式化日期和時間、依字母順序排序專案、要比較的字串等等。

**自然語言查詢**：使用人類語言而非查詢語法所建立的查詢。

非搜尋 **字**：索引服務在針對搜尋查詢所指定的 **限制** 中出現時，會忽略該單字，因為它的歧視性值很小。 英文範例包括「a」、「和」和「」。

**屬性** 快取： **索引服務** 所解壓縮檔案屬性的快取。

**屬性編制索引**：建立檔之實 **數值型別屬性****索引** 的程式，包括作者、主旨、類型、字數統計、列印的頁面計數，以及任何其他屬性。

**限制**：檔案必須符合才能包含在 **索引服務** 所傳回之搜尋結果中的一組條件，以回應搜尋查詢。 **限制** 可縮小搜尋查詢的焦點，將 **索引服務** 只會包含在搜尋結果中的檔案，限制為符合條件的檔案。

**Row**：資料行的 **集合，其中** 包含的屬性值會描述一組檔案中的單一檔案，這些檔案會與提交給 **索引服務** 的搜尋查詢中所指定的 **限制** 相符。

資料列 **集**：在搜尋結果中傳回的一組資料 **列**。

**排序次序**：搜尋查詢中定義搜尋結果中資料列順序的規則集。 每個規則都包含一個屬性 (名稱、大小等等 ) 以及排序 (遞增或遞減) 的方向。 順序套用多個規則

**文字類型屬性**：描述檔內容的屬性，而且只有未格式化的文字與其名稱相關聯。

**數值型別屬性**：描述整份檔之單一屬性的屬性。 實數值型別屬性具有資料類型識別碼，以及與其名稱相關聯之資料類型的值。

**虛擬根目錄**：資料夾的替代路徑。 實體資料夾可以有零或多個虛擬根目錄。 以虛擬根目錄開頭的路徑稱為虛擬路徑。 例如，/server/vanityroot 可能是 C： \\ IIS web folder1 的虛擬根目錄 \\ \\ 。 然後 file C： \\ IIS \\ web \\ folder1 \\default.htm 會有/server/vanityroot/default.htm 的虛擬路徑。

「不得」、「**不得**」、「不得」、「不得」：這些詞彙 (在所有 caps) 中，如 RFC2119 中所述 \[ \] 。 選擇性行為的所有陳述均使用「可能」、「應該」或「不應」。

### <a name="12-references"></a>1.2 參考

### <a name="121-normative-references"></a>1.2.1 標準參考

\[IEEE754 \] 協會的電子和電子工程師「標準的二進位 Floating-Point 算術標準」、IEEE 754-1985、1985年10月 https://standards.ieee.org/standard/754-1985.html

\[MS DCOM \] Microsoft Corporation，「分散式元件物件模型遠端通訊協定」，2006年6月。

\[GPSI Microsoft Corporation 「 \] 群組原則軟體安裝延伸模組」，2006年6月。

\[MS SMB \] Microsoft Corporation 「Microsoft Server Message Block (SMB) 通訊協定和延伸模組」，可能是2006。

\[MS SYS \] Microsoft Corporation "System 總覽 v4"，2006年7月。

\[SALTON \] SALTON，G.，"自動文字處理：依電腦的轉換剖析和抓取資訊"，1988，ISBN 0-201-2227-8。

\[Unicode \] 協會： "Unicode Standard，Version 2.0"，1996， https://www.unicode.org

### <a name="122-informative-references"></a>1.2.2 資訊參考

\[MSDN-OLEDB \] Microsoft Corporation，OLE DB https://msdn.microsoft.com/library/default.asp?url=/library/oledb/htm/dasdkoledboverview.asp 。

\[MSDN-QUERYERR \] Microsoft Corporation、Query-Execution 值、 https://msdn.microsoft.com/library/default.asp?url=/library/indexsrv/html/ixreferr\_5df7.asp

### <a name="13-protocol-overview-synopsis"></a>1.3 通訊協定總覽 (概要) 

內容 **編制索引服務** 有助於有效率地組織檔集合的已解壓縮功能。 內容編制索引服務通訊協定 (CISP) 可讓用戶端與裝載索引服務的伺服器進行通訊，以發出查詢並允許系統管理員管理索引伺服器。

處理檔案時，索引服務會分析一組檔，並重新組織其內容，如此一來，這些檔的 **屬性** 就可以有效率地傳回以回應查詢。 可以查詢的檔集合包含 **目錄** 。 目錄可以包含 **索引** (，以快速參考文字) 和 **屬性** 快取 (來快速抓取屬性值) 。

就概念而言，目錄是由具有文字或值的屬性邏輯「資料表」，以及儲存在資料表資料 **行** 中的對應地區設定所組成。 資料表的每個「資料列」會對應至目錄範圍中的個別檔，而資料表的每個「資料行」會對應至屬性。

CISP 執行的特定工作分為兩個功能區域：

-   索引服務目錄的遠端系統管理
-   遠端查詢索引服務目錄。

### <a name="131-remote-administration-tasks"></a>1.3.1 遠端系統管理工作

CISP 可讓用戶端進行下列索引編制服務類別目錄管理工作：

-   查詢伺服器上索引服務類別目錄的目前狀態。
-   更新索引服務類別目錄的狀態。
-   啟動一組特定檔案的編制索引程式。
-   起始索引的優化，以便改善查詢效能。

所有遠端系統管理工作都遵循簡單的要求/回應模型。 用戶端不會在任何系統管理呼叫中維護任何狀態，而且系統會以任何順序進行管理呼叫。

### <a name="132-remote-querying"></a>1.3.2 遠端查詢

CISP 可讓用戶端對裝載索引服務的遠端伺服器執行搜尋查詢。

傳送搜尋查詢是由用戶端所起始的多步驟處理常式。 步驟如下：

1.  用戶端要求連接到裝載索引服務的伺服器。
2.  用戶端會傳送搜尋查詢的參數，包括：
    -   指定要在搜尋結果中包含及/或排除哪些檔的 **限制** 。
    -   傳回搜尋結果的順序。
    -   要在結果集中傳回的資料行。
    -   應針對查詢傳回的最大資料 **列** 數。
    -   查詢執行的最長時間。

        一旦伺服器已確認用戶端起始查詢的要求，用戶端就可以要求有關查詢的狀態資訊，但這不是必要的步驟。

3.  用戶端接著會指定伺服器應包含在搜尋結果中的屬性。
4.  用戶端會向伺服器要求結果集，而伺服器會透過傳送用戶端搜尋查詢結果中所包含之檔案的屬性值來回應。 如果屬性值太大而無法放入單一回應緩衝區中，伺服器將不會傳送屬性，而是會將屬性狀態設定為 [已延後]。 然後，用戶端會使用一系列的連續值區塊來個別要求屬性值，然後再繼續要求其他值。
5.  一旦用戶端使用搜尋查詢完成，且不再需要額外的結果，用戶端會與伺服器聯繫以釋出查詢。
6.  一旦伺服器釋出查詢之後，用戶端可能會傳送要求，以便中斷與伺服器的連線。 然後連接會關閉。 或者，用戶端可能會發出另一個查詢，並重複步驟2中的順序。

Windows 行為：此通訊協定是在 Windows 2000、Windows XP、Windows Server 2003 和 Windows Vista 上執行。

### <a name="14-relationship-to-other-protocols"></a>1.4 與通訊協定的關聯性

CISP 依賴 SMB \[ MS smb \] 通訊協定來傳輸訊息。 沒有其他通訊協定直接相依于內容編制索引服務通訊協定。

*Windows 行為：應用程式通常會與 OLE DB 介面包裝函 \[ 式 MSDN-OLEDB \] (，例如通訊協定用戶端) ，而不是直接與通訊協定互動。*

### <a name="15-prerequisites-and-preconditions"></a>1.5 必要條件和前置條件

假設用戶端在叫用此通訊協定之前，已取得伺服器的名稱和目錄名稱。 用戶端如何進行這項規格的範圍之外。

也假設用戶端和伺服器具有可與具名管道 MS SMB 搭配使用的安全性關聯 \[ \] 。

### <a name="16-applicability-statement"></a>1.6 適用性陳述

CISP 是設計用來從用戶端查詢及管理遠端伺服器上的目錄。 CISP 已在 Windows Vista 上淘汰。

### <a name="17-versioning-and-capability-negotiation"></a>1.7 版本設定和功能交涉

此通訊協定沒有任何版本控制或功能協商機制。

### <a name="18-vendor-extensible-fields"></a>1.8 廠商可延伸欄位

此通訊協定會使用可延伸廠商的 Hresult。 您可以針對此欄位自由選擇自己的值，只要 C 位 (0x20000000) 設定為在 MS-SYS 的區段4.1.1 中指定 \[ \] ，表示它是客戶程式碼。

此通訊協定也會使用取自在 Ms-chap 中定義之 NTSTATUS 網際空間的 NTSTATUS 值 \[ \] 。 廠商應以其指定的意義重複使用這些值。 選擇任何其他值，就會在未來發生衝突的風險。

*Windows 行為： Windows 只會使用4.1.3 的區段中指定的值 \[ \] 。*

### <a name="181-property-ids"></a>1.8.1 屬性識別碼

屬性是由稱為屬性識別碼的識別碼來表示。 每個屬性都必須有全域唯一識別碼。 此識別碼是由 GUID 所組成，此 **GUID** 代表稱為屬性集的屬性集合，加上字串或32位整數，以識別集合中的屬性。 如果使用整數形式的識別碼，則會將0x00000000、0xFFFFFFFF 和0xFFFFFFFE 值視為無效。

廠商可以將屬性放在其本身的 GUID 所定義的屬性集中，以保證其屬性是唯一的定義。

### <a name="19-standards-assignments"></a>1.9 標準指派

此通訊協定不會指派標準，而只會使用其他通訊協定中指定的配置程式來進行 Microsoft 所做的私用指派。

Microsoft 已將此通訊協定配置給以 MS SMB 指定的具名管道 \[ \] 。 指派為：



| 參數 | 值             | 參考  |
|-----------|-------------------|------------|
| 管道名稱 | \\管道 \\ CI \_ SKADS | \[MS-SMB\] |



 

## <a name="2-messages"></a>2 訊息

-   [2.1 傳輸](#21-transport)
-   [2.2 訊息語法](#22-message-syntax)

### <a name="21-transport"></a>2.1 傳輸

所有訊息都必須使用具名管道來傳輸（如 MS SMB 中所指定） \[ \] 。 使用的管道名稱如下：

-   \\管道 \\ CI \_ SKADS

此通訊協定會使用基礎 SMB 具名管道通訊協定，來抓取進行連接的呼叫端身分識別，如 MS-SMB 的區段2.2.8 中所指定 \[ \] ; 用戶端必須將安全性 \_ 識別設定為要求中的 ImpersonationLevel，才能開啟具名管道。

### <a name="22-message-syntax"></a>2.2 訊息語法

下列各節中的數個結構和訊息是指章節或書簽控制碼。 控制碼是可唯一識別章節或書簽的32位長透明結構。 一般而言，用戶端應用程式會透過方法呼叫來接收控制碼值;不過，有幾個已知的值不需要從伺服器取得，其意義如下表所示：



| 值                         | 意義                                                                      |
|-------------------------------|------------------------------------------------------------------------------|
| DB \_ Null \_ HCHAPTER 0x00000000 | Unchaptered 資料列集的章節控制碼，其中包含所有查詢結果。    |
| DBBMK \_ FIRST 0x00000001       | 書簽的書簽控制碼，這個書簽會識別資料列集中的第一個資料列。 |
| DBBMK \_ 最後的0x00000002        | 書簽的書簽控制碼，這個書簽會識別資料列集中的最後一個資料列。  |



 

### <a name="221-structures"></a>2.2.1 結構

本節詳細說明 CISP 所定義和使用的資料結構。

下列結構中的所有2、4和8位元組的帶正負號和不帶正負號的整數都必須以位元組由小到大的順序傳送。

下表摘要說明此區段中定義的資料結構。



| 結構                    | 描述                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| CBaseStorageVariant          | 包含針對 CPropertyRestriction 結構中所指定之屬性執行比對作業的值。 |
| SAFEARRAY、SAFEARRAY2        | 包含多維陣列。                                                                                     |
| SAFEARRAYBOUND               | 表示 SAFEARRAY 結構中所指定之陣列維度的界限。                                  |
| CFullPropSpec                | 包含屬性規格。                                                                                     |
| CContentRestriction          | 包含屬性（property）快取中的屬性值所要比對的字串。                                                 |
| CKey                         | 包含屬性值。                                                                                             |
| CInternalPropertyRestriction | 包含要與作業相符的屬性值。                                                                  |
| CNatLanguageRestriction      | 包含屬性的自然語言查詢相符項。                                                                |
| CNodeRestriction             | 包含指定查詢限制的命令樹節點陣列。                                       |
| COccRestriction              | 包含單字在片語中的位置。                                                                           |
| CPropertyRestriction         | 包含要與作業相符的屬性值。                                                                  |
| CRangeRestriction            | 包含值範圍的限制。                                                                           |
| CScopeRestriction            | 包含要搜尋之檔案的限制。                                                                    |
| CSort                        | 識別要排序的資料行。                                                                                           |
| CSynRestriction              | 包含查詢片語的單字或其同義字。                                                                    |
| CVectorRestriction           | 包含命令樹節點上的加權或運算。                                                               |
| CWordRestriction             | 包含查詢片語的單字。                                                                                    |
| CRestriction                 | 包含查詢命令樹的節點。                                                                               |
| CColumnSet                   | 指出要傳回的資料行數目。                                                                             |
| CCategorizationSet           | 包含一組查詢結果群組的相關資訊。                                                     |
| CCategorizationSpec          | 包含分類的定義，查詢結果將分類至其中。                                      |
| CDbColId                     | 包含資料行。                                                                                                     |
| CDbProp                      | 包含屬性。                                                                                                   |
| CDbPropSet                   | 包含一組屬性。                                                                                          |
| CPidMapper                   | 包含屬性識別碼的陣列，可指定要在資料列集中傳回的屬性。                                     |
| CRowSeekAt                   | 包含要在 CPMGetRowsIn 訊息中取得資料列的位移                                                |
| CRowSeekAtRatio              | 識別開始抓取 CPMGetRowsIn 訊息的起點。                                           |
| CRowSeekByBookmark           | 識別要從中取出 CPMGetRowsIn 訊息之資料列的書簽。                                       |
| CRowSeekNext                 | 包含要在 CPMGetRowsIn 訊息中略過的資料列數目。                                                         |
| CRowsetProperties            | 包含查詢的設定資訊。                                                                    |
| CSortSet                     | 包含查詢的排序次序。                                                                                   |
| CTableColumn                 | 包含 CPMSetBindings 訊息的資料行。                                                                      |
| SERIALIZEDPROPERTYVALUE      | 包含序列化值。                                                                                           |



 

### <a name="2211-cbasestoragevariant"></a>2.2.1.1 CBaseStorageVariant

CBaseStorageVariant 結構包含針對 CPropertyRestriction 結構中所指定之屬性執行比對作業的值。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

vData1

vData2

vValue (變數) 



 

**vType**：類型指標，表示 vValue 的類型。 它必須是下表中指定的其中一個 VARENUM 值。



| 值                 | 意義                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ 空白 (0x0000)     | vValue 不存在。                                                                                                               |
| VT \_ Null (0x0001)      | vValue 不存在。                                                                                                               |
| VT \_ I1 (0x0010)        | 1 位元帶正負號的整數。                                                                                                             |
| VT \_ UI1 (0x0011)       | 1 位元組不帶正負號的整數。                                                                                                           |
| VT \_ I2 (0x0002)        | 2 位元帶正負號的整數。                                                                                                             |
| VT \_ UI2 (0x0012)       | 2 位元組不帶正負號的整數。                                                                                                           |
| VT \_ BOOL (0x000B)      | 布林值;雙位元組整數，其中包含 0x0000 (FALSE) 或 0xFFFF (TRUE) 。                                                        |
| VT \_ I4 (0x0003)        | 4 位元帶正負號的整數。                                                                                                             |
| VT \_ UI4 (0x0013)       | 4 位元組不帶正負號的整數。                                                                                                           |
| VT \_ R4 (0x0004)        | IEEE 32 位浮點數，如 IEEE754 中所定義 \[ \] 。                                                                     |
| VT \_ INT (0x0016)       | 4 位元帶正負號的整數。                                                                                                             |
| VT \_ UINT (0x0017)      | 4 位元組不帶正負號的整數。                                                                                                           |
| VT \_ 錯誤 (0x000A)     | 包含 HRESULT 的4位元組不帶正負號的整數，如 Ms-chap 中所指定 \[ \] 。                                                         |
| VT \_ I8 (0x0014)        | 8位元組帶正負號的整數。                                                                                                            |
| VT \_ UI8 (0x0015)       | 8 位元不帶正負號的整數。                                                                                                          |
| VT \_ R8 (0x0005)        | IEEE754 中定義的 IEEE 64 位浮點數 \[ \] 。                                                                      |
| VT \_ CY (0x0006)        | 8個位元組的補數整數 (由 10000) 調整。                                                                               |
| VT \_ DATE (0x0007)      | 64位浮點數，代表自00:00:00 年12月31日起算的天數（1899 (國際標準時間) 。     |
| VT \_ FILETIME (0x0040)  | 64位整數，表示自年1月 1 1601 日起00:00:00 的100秒間隔數， (國際標準時間) 。 |
| VT \_ DECIMAL (0x000E)   | 2.2.1.1.1.1 一節中所指定的十進位結構。                                                                             |
| VT \_ CLSID (0x0048)     | 包含 GUID 的16位元組二進位值。                                                                                            |
| VT \_ BLOB (0x0041)      | Blob 中4位元組不帶正負號的整數的位元組計數，後面接著該資料的多個位元組。                                           |
| VT \_ BSTR (0x0008)      | 字串中4位元組不帶正負號的整數的位元組計數，後面接著字串，如以下所示 vValue 下所指定。                       |
| VT \_ LPSTR (0x001E)     | 以 null 結束的 ANSI 字串。                                                                                                       |
| VT \_ LPWSTR (0x001F)    | 以 null 結尾的 Unicode \[ \] 字串。                                                                                        |
| VT \_ 變異 (0x000C)   | CBaseStorageVariant. 必須與 VT \_ 陣列或 vt 向量的類型修飾詞結合 \_ 。                                               |



 

下表指定 vType 的類型修飾詞。 類型修飾詞可以是具有 vType 的二進位 Or 運算，用以變更 vValue 的意義，表示它是兩個可能陣列類型的其中一個。



| 值               | 意義                                                                                                                                                                                                                                                                                                                                                            |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ 向量 (0x1000)  | 如果類型指標是 \_ 使用 OR 運算子與 VT 向量結合，則 vValue 是所指定類型之值的計數陣列。 如需詳細資訊，請參閱2.2.1.1.1.2 一節。 <br/> 此類型修飾詞不能與下列類型結合： VT \_ INT、VT \_ UINT、vt \_ DECIMAL、VT \_ blob、vt \_ blob \_ 物件。<br/>                                    |
| VT \_ 陣列 (0x2000)   | 如果類型指標是 \_ 由 OR 運算子與 VT 陣列結合，則此值為 SAFEARRAY (，如區段 2.2.1.1.1.3) 中所指定，其中包含指定之類型的值。 <br/> 此類型修飾詞不能與下列類型結合： VT \_ I8、vt \_ UI8、vt \_ FILETIME、VT \_ CLSID、vt \_ blob、vt \_ BLOB \_ 物件、vt \_ LPSTR、vt \_ LPWSTR。 <br/> |



 

**vData1**：當 VTYPE 是 VT \_ DECIMAL 時，此欄位的值會指定為區段2.2.1.1.1.1 中的 [小數位數] 欄位。 若為所有其他 vTypes，此值必須設定為0x00。

**vData2**：當 VTYPE 是 VT \_ DECIMAL 時，此欄位的值會指定為區段2.2.1.1.1.1 中的 Sign 欄位。 若為所有其他 vTypes，此值必須設定為0x00。

**vValue**：相符運算的值。 語法必須如 vType 欄位所示。

下表摘要說明 vValue 欄位的大小，其相依于固定長度資料類型的 vType 欄位。 大小是以位元組為單位。



| vType                                                   | 大小 |
|---------------------------------------------------------|------|
| VT \_ I1、vt、 \_ UI1                                        | 1    |
| VT \_ I2，vt \_ UI2，vt \_ BOOL                               | 2    |
| VT \_ I4，vt \_ UI4，vt \_ R4，VT \_ INT，vt \_ UINT，VT \_ 錯誤   | 4    |
| VT \_ I8、vt \_ UI8、vt \_ R8、VT \_ CY、vt \_ DATE、vt \_ FILETIME | 8    |
| VT \_ DECIMAL、VT \_ CLSID                                  | 16   |



 

如果 vType 設定為 VT \_ BLOB、vt \_ BSTR 或 vt LPSTR，則 \_ vValue 的結構會在下圖中指定：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbSize

blobData (變數，選擇性) 



 

**cbSize**：不帶正負號的32位整數，表示 blobData 欄位的大小（以位元組為單位）。 如果 vType 設定為 VT \_ BSTR 或 vt \_ LPSTR，則當表示的字串為空字串時，cbSize 必須設定為0x00000000。

**blobData**：必須是 cbSize 的長度（以位元組為單位）。

針對設定為 VT blob 的 vType \_ ，此欄位是不透明的二進位 blob 資料。

針對設定為 VT BSTR 的 vType \_ ，此欄位是 OEM 所選取字元集中的一組字元。 用戶端和伺服器必須設定為具有可交互操作的字元集， (頻外的通訊協定) 。 不需要以 null 終止。

若 vType 設為 VT \_ LPSTR，此欄位是 OEM 所選取字元集中以 null 結束的字元字串。 用戶端和伺服器必須設定為具有可交互操作的字元集， (頻外的通訊協定) 。

如果 vType 設定為 VT LPWSTR，則 \_ vValue 的結構會在下圖中指定：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

ccLen

字串 (變數，選擇性) 



 

**ccLen**：不帶正負號的32位整數，表示字串欄位的大小（以 Unicode 字元表示）。 若為空字串，則必須設定為0x00000000。

**字串**：以 Null 結束的 Unicode 字串。

### <a name="22111-cbasestoragevariant-structures"></a>2.2.1.1.1 CBaseStorageVariant 結構

下列結構會在 CBaseStorageVariant 結構中使用。

### <a name="221111-decimal"></a>2.2.1.1.1.1 DECIMAL

DECIMAL 用來表示具有固定有效位數和固定小數位數的精確數值。

當 vType 設定為 VT \_ DECIMAL (0x0000E) 時，CBaseStorageVariant 的 vData1 和 vData2 欄位必須解釋如下：

**vData1**：小數點右邊的位數。 必須在0到28的範圍內。

**vData2**：數位值的正負號。 如果是正數，則設定為0x00，如果是負數，則為0x80。

VValue 欄位的格式為：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Hi32

Lo32

Mid32



 

**Hi32**：96位整數的最高32位。

**Lo32**：96位整數的最低32位。

**Mid32**：96位整數的中間32位。

### <a name="221112-vt_vector"></a>2.2.1.1.1.2 VT \_ 向量

VT \_ 向量用來傳遞一維陣列。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vVectorElements

vVectorData



 

**vVectorElements**：不帶正負號的32位整數，指出 vVectorData 欄位中的元素數目。

**vVectorData**：專案的陣列，其中包含已清除0x1000 位之 vType 所指出的型別。 您可以從固定長度的資料類型資料表取得個別固定長度專案的大小，如2.2.1.1 一節中所指定。 這個欄位的長度（以位元組為單位）可以藉由將 vVectorElements 乘以個別專案的大小來計算。

針對可變長度的資料類型，vVectorData 包含一連串連續封送處理的簡單類型，其中的類型是由 vType （已清除0x1000 位）所表示。 這包括以 vType VT ARRAY VT VARIANT 表示的特殊案例 \_ \| \_ (例如 0x100C) 。

VVectorData 欄位中的元素必須以0到3個填補位元組分隔，讓每個專案從包含這個陣列的訊息開頭的4個位元組的倍數開始。 如果有填補位元組存在，它們所包含的值就是任意值。 接收者必須忽略填補位元組的內容。

如果 vType 設定為 VT \_ ARRAY \| vt \_ VARIANT，則此序列中的專案類型為 CBaseStorageVariant。

### <a name="221113-safearray"></a>2.2.1.1.1.3 SAFEARRAY

SAFEARRAY 用來傳遞多維度陣列。 結構包含陣列大小資訊，以及陣列中的資料。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

fFeatures

cbElements

Rgsabound (變數) 

vData (變數) 



 

**cDims**：不帶正負號的16位整數，表示多維陣列的維度數目。

**fFeatures**：16位位。 這些值代表由上層應用程式定義的功能，必須予以忽略。

**cbElements**：32位不帶正負號的整數，指定陣列中每個元素的大小。

**Rgsabound**：包含一個 SAFEARRAYBOUND 結構的陣列，此結構是在 SAFEARRAY 的每個維度的區段2.2.1.1.1.4 中指定的。 這個陣列的第一個是最左邊的維度，最後是最右邊的維度。

**vData**：特定類型之封送處理專案的向量，由包含 CBaseStorageVariant 的 vType 所表示，並已清除位0x2000。

vData 的封送處理方式類似于 VT \_ 向量（如區段2.2.1.1.1.2 中所指定），差別在於專案數不會儲存在向量前方。 而是將 cElements 值乘以 Rgsabound 欄位中提供的所有安全陣列界限，來計算專案數。 專案會以維度的順序儲存在向量中，並以最右邊的維度開始反覆運算。

下圖以視覺方式呈現二維陣列範例。 第一個維度的 cElements 等於 4 (水準表示) ，而 lLbound 等於0，而第二個維度的 cElements 等於 2 (表示垂直) ，lLbound 等於0。

:::row:::
    :::column:::
        0x00000001
    :::column-end:::
    :::column:::
        0x00000002
    :::column-end:::
    :::column:::
        0x00000003
    :::column-end:::
    :::column:::
        0x00000005
    :::column-end:::
:::row-end:::

：： row：：：
    :::column:::
        0x00000007
    :::column-end:::
    :::column:::
        0x00000011
    :::column-end:::
    :::column:::
        0x00000013
    :::column-end:::
    :::column:::
        0x00000017
    :::column-end:::
:::row-end:::

使用上圖，vData 將包含下列順序：0x00000001、0x00000007、0x00000002、0x00000011、0x00000003、0x00000013、0x00000005、0x00000017 (先逐一查看最右邊的維度，然後再遞增下一個維度) 。 上述 Rgsabound (會記錄 cElements 和 Lbound) 為：0x00000004、0x00000000、0x00000002、0x00000000。

### <a name="221114-safearraybound"></a>2.2.1.1.1.4 SAFEARRAYBOUND

SAFEARRAYBOUND 結構代表 SAFEARRAY 或 SAFEARRAY2 之一維度的範圍。 其格式為：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cElements

lLbound



 

**cElements**：32位不帶正負號的整數，指定維度中的元素數目。

**lLbound**：32位不帶正負號的整數，指定維度的下限。

### <a name="221115-safearray2"></a>2.2.1.1.1.5 SAFEARRAY2

SAFEARRAY2 用來傳遞 SERIALIZEDPROPERTYVALUE 中的多維度陣列。 結構包含界限資訊和資料。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cDims

Rgsabound (變數) 

vData (變數) 



 

**cDims**：不帶正負號的32位整數，表示 SAFEARRAY2 的維度數目。

**Rgsabound**：包含一個 SAFEARRAYBOUND 結構的陣列，如 SAFEARRAY2 中每個維度的區段2.2.1.1.1.4 所指定。 這個陣列的第一個是最左邊的維度，最後是最右邊的維度。

**vData**：特定類型之封送處理專案的向量，由包含 SERIALIZEDPROPERTYVALUE 的 dwType 所表示，並已清除位0x2000。 VData 的格式與在區段2.2.1.1.1.3 中針對 SAFEARRAY 的 vData 欄位指定的格式相同。

### <a name="2212-cfullpropspec"></a>2.2.1.2 CFullPropSpec

CFullPropSpec 結構包含屬性集 GUID 和屬性識別碼，可唯一識別屬性。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_guidPropSet

...

...

...

ulKind

PrSpec

屬性名稱 (變數) 



 

**\_ guidPropSet**：屬性所屬之屬性集的 GUID。

**ulKind**：32位不帶正負號的整數。 下列其中一個值，表示 PrSpec 的內容。



| 值                                            | 意義                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------|
| PRSPEC \_ LPWSTR<br/> 0x00000000<br/> | PrSpec 欄位會指定 [屬性名稱] 欄位中的非 Null 字元數目。 |
| PRSPEC \_ PROPID<br/> 0x00000001<br/>  | PrSpec 欄位會指定屬性識別碼 (PROPID) 。                                     |



 

**PrSpec**：具有意義的32位不帶正負號整數，如 ulKind 欄位所示。

**屬性名稱**：如果 ulKind 設為 PRSPEC \_ PROPID，就不能有此欄位。 如果 ulKind 設定為 PRSPEC \_ LPWSTR，則這個欄位必須包含 PRSPEC 非 Null Unicode 字元的不區分大小寫陣列，其中包含屬性的名稱。

### <a name="2213-ccontentrestriction"></a>2.2.1.3 CContentRestriction

CContentRestriction 結構包含要與屬性快取中的屬性相符的字串。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_屬性 (變數) 

...

Padding1 (變數) 

副本

\_pwcsPhrase (變數) 

...

Padding2 (變數) 

lcid

\_ulGenerateMethod



 

**\_ 屬性**： CFullPropSpec 結構，如區段2.2.1.2 中所指定。 這個欄位指出要執行比對作業的屬性。

**Padding1**：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**Cc**：32位不帶正負號的整數，指定 pwcsPhrase 欄位中的字元數 \_ 。

**\_ pwcsPhrase**：以非 Null 結束的 Unicode 字串，表示要比對屬性的單字或片語。 此欄位不得為空白。 Cc 欄位包含字串的長度。

**Padding2**：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**Lcid**：32位不帶正負號的整數，表示 pwcsPhrase 的地區設定 \_ ，如 \[ GPSI 附錄 A 中所指定 \] 。

**\_ ulGenerateMethod**：32位不帶正負號的整數，指定產生替代字表單時要使用的方法



| 值                                                       | 意義                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 產生 \_ 精確的方法 \_<br/> 0x00000000<br/>    | 完全相符。                                                                                                                                                                                                                                                                                      |
| 產生 \_ 方法 \_ 前置詞<br/> 0x00000001 <br/>  | 前置詞相符。                                                                                                                                                                                                                                                                                     |
| 產生 \_ 方法 \_ INFLECT <br/> 0x00000002<br/> | 符合單字的 inflections。 單字的變化是已根據指定語言的語言規則修改過的相同語音部分中的根字組變數。 例如，以英文的動詞「泳道」（inflections）包含「泳道」、「游泳」、「游泳」和「swam」。 |



 

### <a name="2214-ckey"></a>2.2.1.4 CKey

CKey 結構包含屬性值。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PROPID

Cb

buf (變數) 



 

**PROPID**：32位不帶正負號的整數，表示如1.8.1 小節中所討論的屬性識別碼。 已知的值為：



| 值      | 意義                                                 |
|------------|---------------------------------------------------------|
| 0xFFFFFFFF | 代表不正確屬性識別碼，不可使用。 |
| 0xFFFFFFFE | 代表不正確屬性識別碼，不可使用。 |
| 0x00000000 | 表示任何屬性識別碼。                             |



 

**Cb**：32位不帶正負號的整數，其中包含 buf 的長度（以位元組為單位）。

**buf**：代表屬性值的位元組序列。

### <a name="2215-cinternalpropertyrestriction"></a>2.2.1.5 CInternalPropertyRestriction

CInternalPropertyRestriction 結構包含要與作業相符的屬性值。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_relop

\_pid

\_prval (變數) 

restrictionPresent

nextRestriction (變數) 



 

**\_ relop**：32位整數，指定要在屬性上執行的關聯性。 必須是下列其中一個值：



| 值                 | 意義                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | 小於比較。                                                                                           |
| PRLE 0x00000001       | 小於或等於比較。                                                                               |
| PRGT 0x00000002       | 大於比較。                                                                                        |
| PRGE 0x00000003       | 大於或等於比較。                                                                            |
| PREQ 0x00000004       | 相等比較。                                                                                           |
| PRNE 0x00000005       | 不相等的比較。                                                                                           |
| PRRE 0x00000006       | 正則運算式比較。                                                                                  |
| PRAllBits 0x00000007  | 傳回右運算元的位 AND。                                                                     |
| PRSomeBits 0x00000008 | 傳回非零值的位 AND。                                                                       |
| PRAll 0x00000100      | 作業是在資料列集的資料行上執行，而且只有在所有資料列的作業都為 true 時才會是 true。 |
| PRAny 0x00000200      | 作業是在資料列集的資料行上執行，如果任何資料列的作業都是 true，則為 true。       |



 

**\_ pid**：32位不帶正負號的整數，代表屬性識別碼 (請參閱2.2.1.4 一節中的 PROPID) 。

**\_ prval**：包含與屬性相關之值的 CBaseStorageVariant。

**restrictionPresent**：指出 nextRestriction 欄位是否存在的位元組值。 必須設定為0x00 或0x01。 如果設定為0x01，restrictionPresent 會指出 nextRestriction 欄位存在。 如果設定為0x00，restrictionPresent 會指出 nextRestriction 欄位不存在。

**nextRestriction**： CRestriction 結構，如2.2.1.16 一節中所指定，指定進一步的限制。

### <a name="2216-cnatlanguagerestriction"></a>2.2.1.6 CNatLanguageRestriction

CNatLanguageRestriction 結構包含屬性的 **自然語言查詢** 相符項。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_屬性 (變數) 

...

\_填補 \_ cc (變數) 

副本

\_pwcsPhrase (變數) 

...

\_填補 \_ lcid (變數) 

Lcid



 

**\_ 屬性**： CFullPropSpec 結構，如區段2.2.1.3 中所指定。 這個欄位指出要執行比對作業的屬性。

**\_ 填補 \_** 副本：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**Cc**：32位不帶正負號的整數。 PwcsPhrase 欄位中的字元數 \_ 。

**\_ pwcsPhrase**：以非 Null 結束的 Unicode 字串，表示要比對屬性的單字或片語。 不得為空白。 Cc 欄位包含字串的長度。

**\_ 填補 \_ lcid**：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**Lcid**：32位不帶正負號的整數，表示 pwcsPhrase 的地區設定 \_ ，如 \[ GPSI 附錄 A 中所指定 \] 。

### <a name="2217-cnoderestriction"></a>2.2.1.7 CNodeRestriction

CNodeRestriction 結構包含指定查詢限制的 **命令樹** 節點陣列。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cNode

\_paNode (變數) 



 

**\_ cNode**：32位不帶正負號的整數，指定 paNode 欄位中包含的 CRestriction 結構數目 \_ 。

**\_ PaNode**： CRestriction 結構的陣列。 陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是從包含這個陣列的訊息開頭的4個位元組的倍數。 如果有填補位元組存在，它們所包含的值就是任意值。 接收者必須忽略填補位元組的內容。

### <a name="2218-coccrestriction"></a>2.2.1.8 COccRestriction

COccRestriction 結構包含單字在片語中的位置。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Occ

\_cPrevNoiseWords

\_cNextNoiseWords



 

**\_ occ**：32位不帶正負號的整數，指定查詢字串中的單字位移（以單字為單位）。 此規格中使用的單字是具有意義的任何地區設定中的語言單位。

**\_ cPrevNoiseWords**：32位不帶正負號的整數，其中包含此單字與片語中前一個單字之間出現的非搜尋 **字** 數目。

**\_ cNextNoiseWords**：32位不帶正負號的整數，其中包含此單字與片語中下一個單字之間出現的非搜尋字數目。

### <a name="2219-cpropertyrestriction"></a>2.2.1.9 CPropertyRestriction

CPropertyRestriction 結構包含要與作業相符的屬性值。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_relop

\_屬性 (變數) 

\_prval (變數) 



 

**\_ relop**：32位不帶正負號的整數，指定要在屬性上執行的關聯性。 必須是下列其中一個值。



| 值                 | 意義                                                                                                           |
|-----------------------|-------------------------------------------------------------------------------------------------------------------|
| PRLT 0x00000000       | 小於比較。                                                                                           |
| PRLE 0x00000001       | 小於或等於比較。                                                                               |
| PRGT 0x00000002       | 大於比較。                                                                                        |
| PRGE 0x00000003       | 大於或等於比較。                                                                            |
| PREQ 0x00000004       | 相等比較。                                                                                           |
| PRNE 0x00000005       | 不相等的比較。                                                                                           |
| PRRE 0x00000006       | 正則運算式比較。                                                                                  |
| PRAllBits 0x00000007  | 傳回右運算元的位 AND。                                                                     |
| PRSomeBits 0x00000008 | 傳回非零值的位 AND。                                                                       |
| PRAll 0x00000100      | 作業是在資料列集的資料行上執行，而且只有在所有資料列的作業都為 true 時才會是 true。 |
| PRAny 0x00000200      | 作業是在資料列集的資料行上執行，如果任何資料列的作業都是 true，則為 true。       |



 

**\_ 屬性**： CFullPropSpec 結構（如區段2.2.1.2 中所指定），表示要執行比對作業的屬性。

**\_ prval**：在區段2.2.1.1 中指定的 CBaseStorageVariant 結構，其中包含與屬性相關的值。

### <a name="22110-crangerestriction"></a>2.2.1.10 CRangeRestriction

CRangeRestriction 結構包含值範圍的限制。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_keyStart (變數) 

\_keyEnd (變數) 



 

**\_ keyStart**：2.2.1.4 區段中指定的 CKey 結構，其中包含範圍的開頭。

**\_ keyEnd**：包含範圍結尾的 CKey 結構。

### <a name="22111-cscoperestriction"></a>2.2.1.11 CScopeRestriction

CScopeRestriction 結構包含要搜尋之檔案的限制



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CcLowerPath

\_lowerPath (變數) 

...

\_填補 ( 變數) 

\_長度

\_fRecursive

\_fVirtual



 

**CcLowerPath**：32位不帶正負號的整數，其中包含 lowerPath 欄位中的 Unicode 字元數 \_ 。

**\_ lowerPath**：非以 Null 終止的 Unicode 字串，表示應限制查詢的 **路徑**。 CcLowerPath 欄位包含字串的長度。

**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**\_ 長度**：32位不帶正負號的整數，其中包含 lowerPath 的長度 \_ （以 Unicode 字元為單位）。 這必須與 CcLowerPath 的值相同。

**\_ fRecursive**：32位不帶正負號的整數。 必須設定為0x00000001 或0x00000000。 如果設定為0x00000001，伺服器就會以遞迴方式檢查路徑的所有子目錄。 如果設定為0x00000000，則伺服器不會檢查任何子目錄。

**\_ fVirtual**：32位不帶正負號的整數。 必須設定為0x00000001 或0x00000000。 如果設定為0x00000001， \_ lowerPath 就是 (統一資源定位器 (URL) 的虛擬路徑，與網站檔案系統) 上的實體目錄相關聯。 如果設定為0x00000000， \_ lowerPath 就是檔案系統路徑。

### <a name="22112-csort"></a>2.2.1.12 CSort

CSort 結構會識別要排序的資料行。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

pidColumn

dwOrder

locale



 

**pidColumn**：32位不帶正負號的整數。 排序依據的資料行編號。

**dwOrder**：32位不帶正負號的整數。 必須是下列其中一個值，指定如何根據資料行排序。



| 值                        | 意義                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------|
| 查詢 \_ SORTASCEND 0x00000000 | 資料列會根據指定之資料行中的值，以遞增順序排序。  |
| 查詢下降 \_ 0x00000001    | 資料列會根據指定之資料行中的值，以遞減順序排序。 |



 

**地區** 設定：32位不帶正負號的整數，指出資料行的地區設定（如 \[ GPSI \] 附錄 A 所指定）。

### <a name="22113-csynrestriction"></a>2.2.1.13 CSynRestriction

CSynRestriction 結構包含查詢片語的單字或其同義字。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

限制

...

...

cKey

\_keyArray (變數) 

\_isRange



 

**限制**：指定單字位置的 COccRestriction 結構。

**cKey**：32位不帶正負號的整數，指定 keyArray 陣列中的元素數目 \_ 。

**\_ keyArray**：指定單字及其同義字的 CKey 結構陣列。

**\_ isRange**：如果設定為0x01，索引鍵會是要比對的首碼。 如果設定為0x00，索引鍵會是要比對的精確值。 \_isRange 不得設定為任何其他值。

### <a name="22114-cvectorrestriction"></a>2.2.1.14 CVectorRestriction

CVectorRestriction 結構包含命令樹節點上的加權或運算。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_按 (變數) 

...

\_填補 (變數) 

\_ulRankMethod



 

**\_ 按**：要執行排名或運算的 CNodeRestriction 命令樹。

**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**\_ ulRankMethod**：指定排名演算法的32位不帶正負號的整數。 必須設定為下列其中一個值。



| 值                            | 意義                                       |
|----------------------------------|-----------------------------------------------|
| 向量 \_ 排名 \_ 最小0x00000000     | 使用最小演算法 \[ SALTON \] 。             |
| 向量順 \_ 位 \_ 最大值0x00000001     | 使用最大演算法 \[ SALTON \] 。             |
| 向量 \_ 排名 \_ 內部0x00000002   | 使用內部產品演算法 \[ SALTON \] 。       |
| 向量順 \_ 位 \_ 骰子0x00000003    | 使用骰子係數演算法 \[ SALTON \] 。    |
| 向量順 \_ 位 \_ JACCARD 0x00000004 | 使用 Jaccard 係數演算法 \[ SALTON \] 。 |



 

### <a name="22115-cwordrestriction"></a>2.2.1.15 CWordRestriction

CWordRestriction 結構包含查詢片語的單字。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

限制

...

...

\_key (變數) 

\_isRange



 

**限制**：指定單字位置的 COccRestriction 結構。

**\_ key**：指定單字的 CKey 結構。

**\_ isRange**：如果設定為0x01，則索引鍵是要比對的前置詞。 如果設定為0x00，則索引鍵是要比對的精確值。 \_isRange 不得設定為任何其他值。

### <a name="22116-crestriction"></a>2.2.1.16 CRestriction

CRestriction 結構包含查詢命令樹的節點。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ulType

Weight

限制



 

**\_ ulType**：32位不帶正負號的整數，表示用於命令樹節點的限制類型。 必須設定為下列其中一個值。



| 值                    | 意義                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------|
| RTNone 0x00000000        | 節點代表向量查詢中的非搜尋字。                                         |
| RTAnd 0x00000001         | 節點包含要在其上執行邏輯 AND 運算的 CNodeRestriction。 |
| RTOr 0x00000002          | 節點包含要在其上執行邏輯 OR 運算的 CNodeRestriction。  |
| RTNot 0x00000003         | 節點包含不會執行任何作業的 CRestriction。             |
| RTContent 0x00000004     | 節點包含 CContentRestriction。                                                    |
| RTProperty 0x00000005    | 節點包含 CPropertyRestriction。                                                   |
| RTProximity 0x00000006   | 節點包含要執行鄰近排名的 CNodeRestriction，     |
| RTVector 0x00000007      | 節點包含 CVectorRestriction。                                                     |
| RTNatLanguage 0x00000008 | 節點包含 CNatLanguageRestriction。                                                |
| RTScope 0x00000009       | 節點包含 CScopeRestriction。                                                      |
| PRAny 0xFFFFFFFA         | 節點包含 CInternalPropertyRestriction。                                           |
| RTRange 0xFFFFFFFC       | 節點包含 CRangeRestriction。                                                      |
| RTPhrase 0xFFFFFFFD      | 節點包含要執行片語相符的 CNodeRestriction。          |
| RTSynonym 0xFFFFFFFE     | 節點包含 CSynRestriction。                                                        |
| RTWord 0xFFFFFFFF        | 節點包含 CWordRestriction。                                                       |



 

**權數**：代表節點權數的32位不帶正負號整數。 權數表示相對於查詢命令樹中其他節點的節點重要性。 較高的權數值更重要。

**限制**：命令樹節點的限制類型。 語法必須如 \_ ulType 欄位所示。

### <a name="22117-ccolumnset"></a>2.2.1.17 CColumnSet

CColumnSet 結構會指定要傳回的資料行編號。 此結構一律用於參考特定的 CPidMapper 結構， (區段 2.2.1.23) 。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

計數

 (變數的索引) 



 

**計數**：指定索引陣列中元素數目的32位不帶正負號的整數。

**索引**：4位元組不帶正負號的整數的陣列，代表對應 CPidMapper 結構中 aPropSpec 陣列的以零為基底的索引。

### <a name="22118-ccategorizationset"></a>2.2.1.18 CCategorizationSet

CCategorizationSet 結構包含有關查詢結果集群組的資訊。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

計數

類別 (變數) 



 

**計數**：32位不帶正負號的整數，其中包含分類陣列中的元素數目。

**類別**：指定查詢群組的 CCategorizationSpec 結構陣列。

### <a name="22119-ccategorizationspec"></a>2.2.1.19 CCategorizationSpec

CCategorizationSpec 結構包含查詢結果集的群組。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_csColumns (變數) 

\_ulCategType



 

**\_ CsColumns**： CColumnSet 結構，指出用來將查詢分組的資料行。

**\_ ulCategType**：32位不帶正負號的整數。 必須設定為0x00000000。

### <a name="22120-cdbcolid"></a>2.2.1.20 CDbColId

CDbColId 結構包含資料行。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

eKind

GUID

...

...

...

ulId

vString (變數) 



 

**eKind**：必須設定為下列其中一個值，以指出 GUID 和 vValue 的內容。



| 值                            | 意義                                                                                                         |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| DBKIND \_ GUID \_ 名稱0x00000000    | vString 包含屬性名稱。                                                                               |
| DBKIND \_ GUID \_ PROPID 0x00000001  | ulId 包含4個位元組的整數，表示屬性識別碼。                                                      |
| DBKIND \_ PGUID \_ NAME 0x00000003   | vString 包含屬性名稱。 必須將此值視為與 DBKIND \_ GUID 名稱相同 \_ 。                    |
| DBKIND \_ PGUID \_ PROPID 0x00000004 | ulId 包含4個位元組的整數，表示屬性識別碼。 此值必須與 DBKIND \_ GUID \_ PROPID 相同。 |



 

**Guid**：屬性 guid。

**ulId**：如果 EKIND 為 DBKIND \_ GUID \_ PROPID 或 DBKIND \_ PGUID \_ PROPID，則此欄位包含不帶正負號的整數，並指定屬性識別碼。 如果 eKind 為 DBKIND \_ GUID \_ NAME 或 DBKIND \_ PGUID \_ NAME，則此欄位包含一個不帶正負號的整數，指定 vString 欄位中包含的 Unicode 字元數。

**vString**：表示屬性名稱的非 Null 終止 Unicode 字串。 除非 eKind 欄位設定為 DBKIND \_ GUID \_ NAME 或 DBKIND \_ PGUID NAME，否則必須省略它 \_ 。

### <a name="22121-cdbprop"></a>2.2.1.21 CDbProp

CDbProp 結構包含屬性。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

DBPROPID

DBPROPOPTIONS

DBPROPSTATUS

colid (變數) 

vValue (變數) 



 

**DBPROPID**：32位不帶正負號的整數，表示屬性識別碼。

**DBPROPOPTIONS** ：必須設定為0x00000000。

**DBPROPSTATUS**：必須設定為0x00000000。

**colid**： CDbColId 結構（如區段2.2.1.20 所指定），表示要套用屬性的資料行。

**vValue**：包含屬性值的 CBaseStorageVariant。

### <a name="221211-properties"></a>2.2.1.21.1 屬性

本節將詳細說明 CISP 所使用的屬性。 這些屬性會分成三個屬性集，也就是 CDbPropSet 結構的 guidPropertySet 欄位中的 ident 2.2.1.21.1 ified， (區段 2.2.1.22) 。

下表列出屬於 DBPROPSET \_ FSCIFRMWRK \_ EXT 屬性集一部分的屬性。



| 值                                  | 意義                                                                                                                                            |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ CI \_ 目錄 \_ 名稱0x00000002   | 指定要查詢的目錄或目錄名稱。 值必須是 VT \_ LPWSTR 或 vt \_ 向量 \| vt \_ LPWSTR                                   |
| DBPROP \_ CI \_ 包括 \_ 範圍0x00000003 | 指定要包含在查詢中的一或多個路徑。 值必須是 VT \_ LPWSTR 或 vt \_ 向量 \| vt \_ LPWSTR。                                 |
| DBPROP \_ CI \_ 範圍 \_ 旗標0x00000004    | 指定 \_ 要如何處理 DBPROP CI \_ 包含範圍屬性所指定的路徑 \_ 。 值必須是 VT \_ I4 或 vt \_ 向量 \| vt \_ I4。 |
| DBPROP \_ CI \_ 查詢 \_ 類型0x00000007     | 指定查詢的類型。 CDbColId 必須設定為資料庫 \_ NullID。                                                                               |



 

下表列出 DBPROP \_ CI \_ 範圍 \_ 旗標屬性的旗標：



| 值                     | 意義                                                                                                                                                                                                                 |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 查詢 \_ 深度0x01          | 如果設定，表示範圍目錄和所有子目錄中的檔案都會包含在結果中。 如果清除，只有範圍目錄中的檔案才會包含在結果中。 不得與查詢 \_ 深度合併。 |
| 查詢 \_ 虛擬 \_ 路徑0x02 | 如果設定，則表示範圍是虛擬路徑。 如果清除，表示範圍是實體目錄。                                                                                                         |



 

下表列出 [DBPROP \_ CI \_ 查詢類型] 屬性的查詢類型 \_ ：



| 值                     | 意義                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| CiNormal 0x00000000       | 一般查詢。                                                                                                   |
| CiVirtualRoots 0x00000001 | 查詢正在要求目錄的虛擬根目錄清單。 此值需要系統管理許可權。 |
| CiProperties 0x00000003   | 查詢正在要求索引服務所支援的所有屬性清單。                            |
| CiAdminOp 0x00000004      | 查詢是系統管理作業。 此值需要系統管理許可權。                           |



 

下表列出屬於 DBPROPSET \_ QUERYEXT 屬性集一部分的屬性。



| 值                                      | 意義                                                                                                                                                                                                                          |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ USECONTENTINDEX 0x00000002         | 指定索引服務處理緩慢查詢的方式。 值必須是 VT \_ BOOL。 若為 TRUE，則允許伺服器讓這些查詢失敗。                                                                                    |
| DBPROP \_ DEFERNONINDEXEDTRIMMING 0x00000003 | 指出索引服務是否要執行結果修剪。 若為 TRUE，則伺服器會考慮以將回應時間優化至用戶端的方式來執行結果修剪。 值必須是 VT \_ BOOL。             |
| DBPROP \_ USEEXTENDEDDBTYPES 0x00000004      | 指出用戶端是否支援 VT \_ 向量資料類型。 若為 TRUE，則表示用戶端支援 VT \_ 向量; 如果為 FALSE，則伺服器會將 VT \_ 向量資料類型轉換成 vt \_ 陣列資料類型。  值必須是 VT \_ BOOL。 |
| DBPROP \_ FIRSTROWS 0x00000007               | 表示要傳回的資料列相符專案。 若為 TRUE，則伺服器會傳回一組相符的資料列。 如果為 FALSE，則應該傳回最符合的資料列。 值必須是 VT \_ BOOL。                                             |



 

下表列出屬於 DBPROPSET \_ CIFRMWRKCORE \_ EXT 屬性集一部分的屬性。



| Value/DBPROPID                 | 意義                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| DBPROP \_ 機器0x00000002       | 指定要處理查詢 (s) 電腦的名稱。 值必須是 VT \_ bstr 或 vt \_ 陣列 \| VT \_ BSTR。 |
| DBPROP \_ 用戶端 \_ CLSID 0x00000003 | 指定索引服務的連接常數。 此值必須是 \_ 包含0x2A4880706FD911D0A80800A0C906241A 的 VT CLSID。  |



 

### <a name="22122-cdbpropset"></a>2.2.1.22 CDbPropSet

CDbPropSet 結構包含一組屬性。 請注意，第一個欄位是固定大小，但可能無法對齊包含此結構之訊息開頭的4位元組倍數的位移。 不過，cProperties 欄位會對齊，因此格式如下所示：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

guidPropertySet

...

...

...

...

\_填補 (變數) 

cProperties

aProps (變數) 



 

**guidPropertySet**：識別屬性集的 GUID。 必須設定為對應到下列其中一個值的二進位格式 (以字串表示表單) 顯示，識別 aProps 欄位中包含之屬性的屬性集。



| 值/GUID                                                                              | Name                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| DBPROPSET \_ FSCIFRMWRK \_ EXT<br/> {A9BD1526-6A80-11D0-8C9D-0020AF1D740E}<br/>   | 檔案系統內容索引架構屬性集 |
| DBPROPSET \_ QUERYEXT<br/> {A7AC77ED-F8D7-11CE-A798-0020F8008025}<br/>          | 查詢延伸模組屬性集                     |
| DBPROPSET \_ CIFRMWRKCORE \_ EXT<br/> {AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D}<br/> | 內容索引架構核心屬性集        |



 

**\_ 填補**：此欄位的長度必須介於0到3個位元組之間。 這個欄位的長度必須是下欄欄位的起始位置：從包含此結構之訊息開頭的4個位元組的倍數開始。 如果這個欄位存在 (亦即，長度非零) ，它所包含的值是任意的。 接收者必須忽略此欄位的內容。

**cProperties**：32位不帶正負號的整數，其中包含 aProps 陣列中的元素數目。

**aProps**： CDbProp 結構的陣列，如區段0中所指定，包含屬性。 陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是從包含這個陣列的訊息開頭的4個位元組的倍數。 如果有填補位元組存在，它們所包含的值就是任意值。 接收者必須忽略填補位元組的內容。

### <a name="22123-cpidmapper"></a>2.2.1.23 CPidMapper

CPidMapper 結構包含屬性識別碼的陣列，可指定要在資料列集中傳回的屬性。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

計數

aPropSpec

... (變數) 



 

**count**：包含 aPropSpec 陣列中元素數目的32位不帶正負號的整數。

**aPropSpec**： CFullPropSpec 結構的陣列，表示要傳回的屬性。 陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。 這類填補位元組可以是任意值，而且必須在收到時忽略。

### <a name="22124-crowseekat"></a>2.2.1.24 CRowSeekAt

CRowSeekAt 結構包含在 CPMGetRowsIn 訊息中取得資料列的位移。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cskip

\_bmkOffset



 

**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。

**\_ cskip**：32位不帶正負號的整數，其中包含要在資料列集中略過的資料列數目。

**\_ bmkOffset**：代表 **書簽** 控制碼的32位值，表示在開始抓取之前，要從中略過 cskip 中指定之資料列數的起始位置 \_ 。

### <a name="22125-crowseekatratio"></a>2.2.1.25 CRowSeekAtRatio

CRowSeekAtRatio 結構會識別開始抓取 CPMGetRowsIn 訊息的起點。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_ulNumerator

\_ulDenominator



 

**CiTblChapt**：32位不帶正負號的整數，表示要從中取出資料列的資料列集章節。

**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。

**\_ ulNumerator**：不帶正負號的32位整數，代表要開始抓取之章節中資料列比例的分子。

**\_ ulDenominator**：不帶正負號的32位整數，代表要開始抓取之章節中資料列比例的分母。 必須大於零。

### <a name="22126-crowseekbybookmark"></a>2.2.1.26 CRowSeekByBookmark

CRowSeekByBookmark 結構會識別要從中開始抓取 CPMGetRowsIn 訊息之資料列的書簽。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hRegion

\_cBookmarks

\_maxRet

\_cValidRet

\_aBookmarks (變數) 

\_ascRet (變數) 



 

**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。

**\_ cBookmarks**：不帶正負號的32位整數，代表 aBookmarks 陣列中的元素數目 \_ 。

**\_ maxRet**：不帶正負號的32位整數，代表 ascRet 陣列中的元素數目 \_ 。

**\_ cValidRet**：不帶正負號的32位整數，代表 ascRet 陣列中有效的元素數目 \_ 。 陣列中已定義有效的元素，但不正確元素未定義。

**\_ aBookmarks**：書簽的陣列 (每個) 以4個位元組表示，如同從 CPMGetRowsOut 訊息取得的。

**\_ ASCRET**： HRESULT 值的陣列。 將 CRowSeekByBookMark 當作 CPMGetRowsIn 要求的一部分傳送時，陣列中的專案數目必須等於 \_ cBookMarks。 當用戶端傳送時，值必須設定為零，而且伺服器必須忽略陣列的內容。 當伺服器 (傳送) CPMGetRowsOut 訊息的一部分時，陣列中的值會指出每個資料列抓取的結果狀態。

### <a name="22127-crowseeknext"></a>2.2.1.27 CRowSeekNext

CRowSeekNext 結構包含要在 CPMGetRowsIn 訊息中略過的資料列數目。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

CiTblChapt

\_hRegion

\_cskip



 

**CiTblChapt**：不帶正負號的32位整數，指定要從中取得資料列的資料列集章節。

**\_ hRegion**：必須設定為0X00000000，而且必須加以忽略。

**\_ cskip**：不帶正負號的32位整數，代表要在資料列集中略過的資料列數目。

### <a name="22128-crowsetproperties"></a>2.2.1.28 CRowsetProperties

CRowsetProperties 結構包含查詢的設定資訊。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_uBooleanOptions

\_ulMaxOpenRows

\_ulMemoryUsage

\_cMaxResults

\_cCmdTimeout



 

**\_ uBooleanOptions**：此欄位最小的3位必須包含下列三個值的其中一個：



| 值                  | 意義                                                             |
|------------------------|---------------------------------------------------------------------|
| eSequential 0x00000001 | 資料指標只能向前移動。                              |
| eLocatable 0x00000003  | 資料指標可移至任何位置。                            |
| eScrollable 0x00000007 | 您可以將游標移至任何位置，並以任何方向提取。 |



 

其餘的位可能是明確的，或設定為邏輯或的任何下列值組合：



| 值                     | 意義                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------|
| eAsynchronous 0x00000008  | 用戶端不會等待執行完成。                                                          |
| eFirstRows 0x00000080     | 傳回所遇到的第一個資料列，而不是最符合的專案。                                                    |
| eHoldRows 0x00000200      | 在使用查詢完成用戶端之前，伺服器不能捨棄資料列。                                     |
| eChaptered 0x00000800     | 資料列集支援章節。                                                                               |
| eUseCI 0x00001000         | 請只從索引（而不是檔案系統）回答查詢。                                                  |
| eDeferTrimming 0x00002000 | 索引服務是在執行移除結果時，考慮將回應時間優化到用戶端。 |



 

**\_ ulMaxOpenRows**：不帶正負號的32位整數。 必須設定為0x00000000。 未使用且必須加以忽略。

**\_ ulMemoryUsage**：不帶正負號的32位整數。 必須設定為0x00000000。 未使用且必須加以忽略。

**\_ cMaxResults**：32位不帶正負號的整數，指定要針對查詢傳回的最大資料列數。

**\_ cCmdTimeout**：32位不帶正負號的整數，指定查詢開始時間和自動終止的秒數，從查詢在伺服器上開始執行的時間算起。 值為0x00000000 表示查詢不會超時。

### <a name="22129-crowvariant"></a>2.2.1.29 CRowVariant

CRowVariant 結構包含儲存在 CPMGetRowsOut 訊息中之可變長度資料類型的固定大小部分。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

vType

reserved1

reserved2

 (選擇性) 位移



 

**vType**：類型指標，表示 vValue 的類型。 它必須是2.2.1.1 區段中所指定的其中一個 VARENUM 值。

**reserved1**：未使用。 值可以設定為任何任意值，而且必須在收到時忽略。

**reserved2**：未使用。 值可以設定為任何任意值，而且必須在收到時忽略。

**Offset**：變數長度資料的位移 (例如字串) 。  這必須是32位值 (4 個位元組長) 如果32位位移是使用於區段 2.2.3.16) 中的規則 (，或64位元組的值 (8 個位元組長) 如果使用的是64位位移。

### <a name="22130-csortset"></a>2.2.1.30 CSortSet

CSortSet 結構包含查詢的排序次序。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

Count

sortArray (變數) 



 

**計數**：指定 sortArray 中元素數目的32位不帶正負號的整數。

**sortArray**： CSort 結構的陣列，描述排序查詢結果的順序。 陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。 這類填補位元組可以是任意值，而且必須在收到時忽略。

### <a name="22131-ctablecolumn"></a>2.2.1.31 CTableColumn

CTableColumn 結構包含 CPMSetBindingsIn 訊息的資料行



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

PropSpec

... (變數) 

vType

ValueUsed

\_padding1 (選用) 

ValueOffset (選用) 

ValueSize (選用) 

StatusUsed

\_padding2 (選用) 

StatusOffset (選用) 

LengthUsed

\_padding3 (選用) 

LengthOffset (選用) 



 

**PropSpec**：在區段2.2.1.3 中指定的 CFullPropSpec 結構。

**vType**：指定包含在資料行中的資料數值型別。 如需此欄位的值清單，請參閱2.2.1.1 一節中的 vType 欄位。

**ValueUsed**：必須設定為0x01 或0x00 的一個位元組欄位。 如果設定為0x01，資料行會在固定大小的資料列內傳輸。 如果設定為0x00，則資料行的值會在緩衝區結尾的可變長度區段中傳輸。

**\_ padding1**：一個位元組欄位必須在 ValueOffset 之前插入，如果沒有，則 ValueOffset 不會從訊息開頭的平均位移開始。 此位元組的值是任意的，且必須加以忽略。 如果 ValueUsed 設定為0x00，就不能有此欄位。

**ValueOffset**：不帶正負號的2位元組整數，指定資料列中資料行值的位移。 如果 ValueUsed 設定為0x00，就不能有此欄位。

**ValueSize**：不帶正負號的2位元組整數，指定資料行值的大小（以位元組為單位）。 如果 ValueUsed 設定為0x00，就不能有此欄位。

**StatusUsed**：必須設定為0x01 或0x00 的一個位元組欄位。 如果設定為0x01，資料行的狀態就會在資料列中傳輸。 若為0x00，則資料行的狀態不會在資料列中傳輸。

**\_ padding2**：一個位元組欄位必須在 StatusOffset 之前插入，如果沒有此欄位，StatusOffset 欄位就不會從訊息開頭的平均位移開始。 此位元組的值是任意的，且必須加以忽略。 如果 StatusUsed 設定為0x00，就不能有此欄位。

**StatusOffset**：不帶正負號的2位元組整數，指定資料列中資料行狀態的位移。 如果 StatusUsed 設定為0x00，就不能有此欄位。

**LengthUsed**：必須設定為0x01 或0x00 的一個位元組欄位。 如果設定為0x01，資料行的長度會在資料列中傳輸。 如果0x00，則資料行的長度不能在資料列內傳輸。

**\_ padding3**：一個位元組欄位必須在 LengthOffset 之前插入，如果沒有，則 LengthOffset 不會從訊息開頭的平均位移開始。 此位元組的值是任意的，且必須加以忽略。 如果 LengthUsed 設定為0x00，就不能有此欄位。

**LengthOffset**：不帶正負號的2位元組整數，指定資料列中資料行長度的位移。 如果 LengthUsed 設定為0x00，就不能有此欄位。

### <a name="22132-serializedpropertyvalue"></a>2.2.1.32 SERIALIZEDPROPERTYVALUE

SERIALIZEDPROPERTYVALUE 結構包含序列化值。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

dwType

rgb (變數) 



 

**dwType**：在 section 2.2.1.1 中定義的其中一個 variant 類型，可以與 variant 類型修飾詞結合。 針對所有 variant 類型，除了與 VT 陣列結合的類型之外， \_ SERIALIZEDPROPERTYVALUE 具有與 CBaseStorageVariant 相同的版面配置，如2.2.1.1 一節中所指定。 如果 variant 類型與 VT \_ 陣列類型修飾詞結合，則會使用 SAFEARRAY2 （在2.2.1.2.1.1 區段中指定），而不是 CBaseStorageVariant 的 vValue 欄位中的 SAFEARRAY。

**rgb**：序列化值。 請參閱2.2.1.1 中 vValue 的序列化詳細資料。

### <a name="222-message-headers"></a>2.2.2 訊息標頭

所有內容索引服務通訊協定訊息都有16位元組的標頭。

以下是顯示內容索引服務通訊協定訊息標頭格式的圖表。



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_msg

\_地位

\_ulChecksum

\_ulReserved2



 

\_**msg**：識別標頭後面之訊息類型的32位整數。 下表列出內容索引服務的通訊協定訊息，以及為每個訊息指定的整數值。 如下表所示，某些值會識別資料表中的2個訊息。 在這些情況下，可透過訊息流程的方向識別標頭後面的訊息。 如果方向是 [用戶端至伺服器]，則會指出訊息名稱後面附加有 "In" 的訊息。 如果方向為 [伺服器至用戶端]，則會指出訊息名稱後面附加有 "Out" 的訊息。



| 值      | 意義                                                     |
|------------|-------------------------------------------------------------|
| 0x000000C8 | CPMConnectIn 或 CPMConnectOut                               |
| 0x000000C9 | CPMDisconnect                                               |
| 0x000000CA | CPMCreateQueryIn 或 CPMCreateQueryOut                       |
| 0x000000CB | CPMFreeCursorIn 或 CPMFreeCursorOut                         |
| 0x000000CC | CPMGetRowsIn 或 CPMGetRowsOut                               |
| 0x000000CD | CPMRatioFinishedIn 或 CPMRatioFinishedOut                   |
| 0x000000CE | CPMCompareBmkIn 或 CPMCompareBmkOut                         |
| 0x000000CF | CPMGetApproximatePositionIn 或 CPMGetApproximatePositionOut |
| 0x000000D0 | CPMSetBindingsIn                                            |
| 0x000000D1 | CPMGetNotify                                                |
| 0x000000D2 | CPMSendNotifyOut                                            |
| 0x000000D7 | CPMGetQueryStatusIn 或 CPMGetQueryStatusOut                 |
| 0x000000D9 | CPMCiStateInOut                                             |
| 0x000000E1 | CPMForceMergeIn                                             |
| 0x000000E4 | CPMFetchValueIn 或 CPMFetchValueOut                         |
| 0x000000E6 | CPMUpdateDocumentsIn                                        |
| 0x000000E7 | CPMGetQueryStatusExIn 或 PMGetQueryStatusExOut              |
| 0x000000E8 | CPMRestartPositionIn                                        |
| 0x000000E9 | CPMStopAsynchIn                                             |
| 0x000000EC | CPMSetCatStateIn 或 CPMSetCatStateOut                       |



 

\_**狀態**： HRESULT \[ ms-chap \] ，指出要求之作業的狀態。

\* *

*Windows 行為：用戶端一律將 \_ status 欄位設定為0x00000000。*

**\_ ulChecksum**： \_ ULCHECKSUM 的計算方式必須如下列訊息的區段3.2.4 所指定：

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMSetBindingsIn
-   CPMGetRowsIn
-   CPMFetchValueIn

若為所有其他訊息， \_ ULCHECKSUM 必須設定為0x00000000。 用戶端必須忽略 \_ ulChecksum 欄位。

**\_ ulReserved2**：必須設定為0，而且接收者會忽略它。

### <a name="223-messages"></a>2.2.3 訊息

### <a name="2231-cpmcistateinout"></a>2.2.3.1 CPMCiStateInOut

CPMCiStateInOut 訊息包含索引服務狀態的相關資訊。 標頭後面的 CPMCiStateInOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

cbStruct

cWordList

cPersistentIndex

cQueries

cDocuments

cFreshTest

dwMergeProgress

eState

cFilteredDocuments

cTotalDocuments

cPendingScans

dwIndexSize

cUniqueKeys

cSecQDocuments

dwPropCacheSize



 

**cbStruct**：32位不帶正負號的整數。 此訊息的大小（以位元組為單位） (不包括通用標頭) 。 必須設為0x0000003C。

**cWordList**：32位不帶正負號的整數，表示為最近編制索引的檔所建立的初始索引計數。

**cPersistentIndex**：32位不帶正負號的整數，表示持續性索引的計數。

**cQueries**：32位不帶正負號的整數，表示正在執行的查詢數目。

**cDocuments**：32位不帶正負號的整數，指出等候編制索引的檔總數。

**cFreshTest**：32位不帶正負號的整數，指出未針對效能進行完整優化的唯一檔數目，以及索引中的資訊。

**dwMergeProgress**：不帶正負號的32位整數，指定目前的索引完整優化的完成百分比（如果目前正在進行優化）。 必須小於或等於100。

**資產**：依 \_ \_ \* 下表所定義的一或多個 CI 狀態常數所提供的內容編制索引狀態。



| 值                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CI \_ 狀態 \_ 陰影 \_ 合併0x00000001           | 索引服務正在優化某些索引，以降低記憶體使用量並提升查詢效能。                                                                                                                                                                                                                                                                                                                                                                |
| CI \_ 狀態 \_ 主要 \_ 合併0x00000002           | 索引服務正在進行所有索引的完整優化處理。                                                                                                                                                                                                                                                                                                                                                                                                                  |
| CI \_ 狀態 \_ 內容 \_ 掃描 \_ 所需的0x00000004 | 索引中的某些檔已變更，而索引服務需要判斷已新增、變更或刪除的檔。                                                                                                                                                                                                                                                                                                                                                              |
| CI \_ 狀態 \_ 鍛煉 \_ 合併0x00000008        | 索引服務正在將索引優化，以降低記憶體使用量並提升查詢效能。 此程式比 CI 狀態陰影合併值所識別的程式更完整 \_ \_ \_ ，但不像 ci \_ 狀態 \_ 主要合併值所指定的完整 \_ 。 這類優化是實作為特定的，因為它們相依于內部儲存資料的方式;優化不會以回應時間以外的任何方式影響通訊協定。 |
| CI \_ 狀態 \_ 掃描0x00000010                | 索引服務正在檢查目錄或一組目錄，以查看自上次索引目錄之後，是否已新增、刪除或更新任何檔案。                                                                                                                                                                                                                                                                                                                 |
| CI \_ 狀態 \_ 復原0x00000020              | 服務從上次儲存的狀態開始，而且正在復原。                                                                                                                                                                                                                                                                                                                                                                                                        |
| CI \_ 狀態 \_ 低 \_ 記憶體0x00000080             | 伺服器的大部分虛擬記憶體正在使用中。                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CI \_ 狀態 \_ 高 \_ IO 0x00000100                | 伺服器上的輸入/輸出 (i/o) 活動的層級相對較高。                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CI \_ 狀態 \_ 主要 \_ 合併已 \_ 暫停0x00000200   | 所有進行中之索引的完整優化程式都已暫停。 這僅供提供資訊之用，並不會影響 CISP。                                                                                                                                                                                                                                                                                                                                  |
| CI \_ 狀態 \_ 唯讀 \_ 0x00000400              | 將新檔挑選至索引的索引服務部分已暫停。 這僅供提供資訊之用，並不會影響 CISP。                                                                                                                                                                                                                                                                                                                               |
| CI \_ 狀態 \_ 電池 \_ 電力0x00000800          | 將新檔挑選至索引的索引服務部分已暫停，以節省電池存留期，但仍會回復查詢。 這僅供提供資訊之用，並不會影響 CISP。                                                                                                                                                                                                                                                                 |
| CI \_ 狀態 \_ 使用者使用中 \_ 0x00001000            | 將新檔挑選至索引的索引服務部分，因為使用者 (鍵盤或滑鼠) 的高度活動，但仍在回復查詢，所以已暫停。 這僅供提供資訊之用，並不會影響 CISP。                                                                                                                                                                                                                                         |
| CI \_ 狀態 \_ 開始0x00002000                | 服務正在啟動。 您可以執行查詢，但尚未啟用掃描和通知。 這僅供提供資訊之用，並不會影響 CISP。                                                                                                                                                                                                                                                                                                                   |
| \_ \_ 讀取 \_ USN 0x00004000 的 CI 狀態           | 服務未讀取檔案系統所保留的記錄檔，以追蹤磁片區中檔案或目錄的變更，因此索引可能不是最新狀態。                                                                                                                                                                                                                                                                                                                                  |



 

**cFilteredDocuments**：32位不帶正負號整數，指出自開始編制內容索引之後編制索引的檔數目。

**cTotalDocuments**：32位不帶正負號的整數，表示系統中的檔總數。

**cPendingScans**：32位不帶正負號的整數，表示暫止高階索引編制作業的數目。 此值的意義是提供者專屬的，但預期會有較大的數位，以表示保留更多索引。

*Windows 行為*：此值通常是零，但在開始編制索引之後，或在通知佇列溢出之後立即發生。

**dwIndexSize**：32位不帶正負號的整數，表示索引的大小（以 mb 為單位） (不包括屬性快取) 。

**cUniqueKeys**：32位不帶正負號的整數，表示目錄中唯一索引鍵的大約數目。

**cSecQDocuments**：32位不帶正負號的整數，指出索引服務將重新嘗試編制索引的檔數目，因為初始索引嘗試期間發生失敗。

**dwPropCacheSize**：32位不帶正負號的整數，表示屬性快取的大小（以 mb 為單位）。

### <a name="2232-cpmsetcatstatein"></a>2.2.3.2 CPMSetCatStateIn

CPMSetCatStateIn 訊息會設定目錄的狀態。 標頭後面的 CPMSetCatStateIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID

\_dwNewState

\_CatName (變數，選擇性) 



 

**\_ partID**：必須設定為0x00000001。

**\_ dwNewState**：必須設定為下列其中一個值，表示目錄的新狀態。



| 值                         | 意義                                                                                                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CICAT \_ 停止的0x00000001     | 目錄已停止。 此狀態表示不會編制任何新檔案的索引，也不會處理任何搜尋查詢。                                                     |
| CICAT \_ READONLY 0x00000002    | 目錄是唯讀的。 不會為任何新檔案編制索引。                                                                                                               |
| CICAT \_ 可寫入的0x00000004    | 目錄是可寫入的。 您可以建立新檔案的索引，並處理搜尋查詢。                                                                              |
| CICAT \_ 沒有 \_ 查詢0x00000008   | 目錄無法供查詢。                                                                                                                              |
| CICAT \_ 取得 \_ 狀態0x00000010  | 目錄的狀態不會變更，只會進行取出。                                                                                                          |
| CICAT \_ 所有 \_ 開啟的0x00000020 | 查看是否已啟動所有目錄的檢查。 若是如此， \_ 在 CPMSetCatStateOut 回復中傳送給此訊息的 dwOldState 欄位將會報告為非零。 |



 

**\_ CatName**：要修改其狀態的目錄名稱。 名稱必須是以 null 結束的 Unicode 字串。 如果 \_ dwNewState 設定為 CICAT 全部開啟，則必須省略此欄位 \_ \_ 。

### <a name="2233-cpmsetcatstateout"></a>2.2.3.3 CPMSetCatStateOut

CPMSetCatStateOut 訊息是具有類別目錄舊狀態的 CPMSetCatStateIn 訊息回復。 標頭後面的 CPMSetCatStateOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwOldState



 

**\_ dwOldState**：下列其中一個值，表示目錄的舊狀態。



| 值                       | 意義                                    |
|-----------------------------|--------------------------------------------|
| CICAT \_ 停止的0x00000001   | 目錄已停止。                    |
| CICAT \_ READONLY 0x00000002  | 目錄是唯讀的。                  |
| CICAT \_ 可寫入的0x00000004  | 目錄是可寫入的。                   |
| CICAT \_ 沒有 \_ 查詢0x00000008 | 目錄無法供查詢。 |



 

### <a name="2234-cpmupdatedocumentsin"></a>2.2.3.4 CPMUpdateDocumentsIn

CPMUpdateDocumentsIn 訊息會指示伺服器為指定的路徑編制索引。

伺服器將會使用 CPMUpdateDocumentsOut 訊息的訊息標頭來回複，並將要求的結果包含在 \_ 訊息標頭的 [狀態] 欄位中。

標頭後面的 CPMUpdateDocumentsIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ (選擇性的旗標) 

\_fRootPath (選用) 

RootPath (變數，選擇性) 



 

**\_ 旗** 標：要執行的更新類型。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。 此欄位必須設定為下列其中一個值：



| 值                  | 意義                                   |
|------------------------|-------------------------------------------|
| UPD \_ INCREM 0x00000000 | 要執行累加式更新。 |
| UPD \_ FULL 0x00000001   | 要執行完整更新。         |
| UPD \_ INIT 0x00000002   | 要執行新的初始化。  |



 

**\_ fRootPath**：布林值，指出 RootPath 欄位是否指定要執行更新的路徑。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。 此欄位必須設定為0x00000001 或0x00000000。 如果設定為0x00000001，則 RootPath 中會包含要執行更新的路徑。 如果設定為0x00000000，則會在所有已編制索引的路徑上執行更新。

**RootPath**：要更新的路徑名稱。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。 名稱必須是以 null 結束的 Unicode 字串。 如果 fRootPath 設定為0x00000000，則必須省略此欄位 \_ 。

### <a name="2235-cpmforcemergein"></a>2.2.3.5 CPMForceMergeIn

CPMForceMergeIn 訊息要求伺服器執行任何必要的維護，以改善查詢效能。 伺服器將會使用 CPMForceMergeIn 訊息的訊息標頭來回複，並在 [狀態] 欄位中包含要求的結果 \_ 。

標頭後面的 CPMForceMergeIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_partID (選用) 



 

**\_ partID**：當用戶端傳送訊息時，此欄位必須存在，而且當伺服器傳送訊息時必須不存在。 當這個欄位存在時，必須設定為0x00000001。

### <a name="2236-cpmconnectin"></a>2.2.3.6 CPMConnectIn

CPMConnectIn 訊息會開始用戶端與伺服器之間的會話。

標頭後面的 CPMConnectIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_iClientVersion

\_fClientIsRemote

\_cbBlob1

\_cbBlob2

\_填充

...

...

MachineName

... (變數) 

使用者名稱

... (變數) 

\_paddingcPropSets (選擇性、變數) 

cPropSets

PropertySet1 (變數) 

PropertySet2 (變數) 

\_paddingExtPropset (選擇性、變數) 

cExtPropSet

aPropertySets (變數) 



 

**\_ iClientVersion**：32位整數，指出伺服器是否要驗證訊息標頭的 ulChecksum 欄位中所指定的總和檢查碼值是否 \_ 為用戶端所傳送的訊息。 如果 \_ iClientVersion 欄位設定為0x00000008 或更高，則伺服器必須驗證 \_ 下列訊息的 ulChecksum 域值：

-   CPMConnectIn
-   CPMCreateQueryIn
-   CPMFetchValueIn
-   CPMGetRowsIn
-   CPMSetBindingsIn

如需有關伺服器如何針對上方所列訊息的 ulChecksum 欄位驗證用戶端所指定值的詳細資訊，請參閱3.2.5 一節。

如果值大於0x00000008，則會假設用戶端能夠處理 CPMGetRowsOut 訊息中的64位位移。 如需詳細資訊，請參閱2.2.3.16 一節。

*Windows 行為：在 windows 用戶端上，iClientVersion 的設定* 如下：



| 值      | 意義                                                              |
|------------|----------------------------------------------------------------------|
| 0x00000005 | 用戶端作業系統是 Windows 2000。                                           |
| 0x00000008 | 用戶端作業系統可能是32位的 Windows XP 或32位 Windows Server 2003。 |
| 0x00010008 | 用戶端作業系統可能是64位的 Windows XP 或64位 Windows Server 2003。 |



 

\_**fClientIsRemote**：布林值，指出用戶端是否正在與伺服器不同的電腦上執行。 必須設定為0x00000001。

\_**cbBlob1**：32位不帶正負號的整數，表示 CPropSet、PropertySet1 和 PropertySet2 欄位的大小（以位元組為單位）。

\_**cbBlob2**：32位不帶正負號的整數，表示 CExPropSet 和 aPropertySet 欄位的大小（以位元組為單位），結合起來。

\_**填補**：可以包含任意值的12個位元組填補，而且必須予以忽略。

**MachineName**：用戶端的電腦名稱稱。 名稱字串必須是小於512個 Unicode 字元的 null 終止陣列，包括 Null 結束字元。

**UserName**：代表正在執行叫用此通訊協定之應用程式之人員的使用者名稱的字串。 當與 MachineName 串連時，名稱字串必須是小於512的 Unicode 字元之以 null 結束的陣列。

**\_ paddingcPropSets**：此欄位的長度必須介於0到7個位元組之間。 位元組數必須是將 cPropSets 欄位的位元組位移從包含此結構的訊息開頭的位元組位移，變成8的倍數。 位元組的值可以是任意值，而且接收者必須忽略此值。

**cPropSets**：32位不帶正負號的整數，指出遵循此欄位的 CDbPropSet 結構數目。 此值必須設為0x0000002。

**PropertySet1**：具有 GuidPropertySet 的 CDbPropSet 結構，其中包含 DBPROPSET \_ FSCIFRMWRK \_ EXT (請參閱 2.2.1.22) 一節。

**PropertySet2**：具有 GuidPropertySet 的 CDbPropSet 結構，其中包含 DBPROPSET \_ CIFRMWRKCORE \_ EXT (請參閱 2.2.1.22) 一節。

\_**PaddingExtPropset**：此欄位的長度必須介於0到7個位元組之間。 位元組數必須是將 cExtPropSets 欄位的位元組位移從包含此結構的訊息開頭的位元組位移，變成8的倍數。 位元組的值可以是任意值，而且接收者必須忽略此值。

**cExtPropSet**：32位不帶正負號的整數，指出遵循此欄位的 CDbPropSet 結構數目。

**aPropertySets**：指定其他屬性之 CDbPropSet 結構的陣列。 此陣列中的元素數目必須等於 cExtPropSet。

### <a name="2237-cpmconnectout"></a>2.2.3.7 CPMConnectOut

CPMConnectOut 訊息包含 CPMConnectIn 訊息的回應。

標頭後面的 CPMConnectOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_serverVersion

\_保留的 (變數) 



 

**\_ serverVersion**：

32位整數，表示伺服器是否可支援64位位移 *。* 如需詳細資訊，請參閱2.2.3.16 一節。



| 值      | 意義                                 |
|------------|-----------------------------------------|
| 0x00000007 | 伺服器只能傳送32位的位移。 |
| 0x00010007 | 伺服器可以傳送32或64位位移。   |



 

**\_ reserved**： reserved。 伺服器可能會傳送任意數目的任意值，而且用戶端必須忽略這些值（如果有的話）。

### <a name="2238-cpmcreatequeryin"></a>2.2.3.8 CPMCreateQueryIn

CPMCreateQueryIn 訊息會建立新的查詢。 標頭後面的 CPMCreateQueryIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

大小

CColumnSetPresent

ColumnSet (選用) 

... (變數) 

CRestrictionPresent.

限制 (選擇性) 

... (變數) 

CSortSetPresent

SortSet (選用) 

... (變數) 

CCategorizationSetPresent

CategorizationSet (選用) 

... (變數) 

RowSetProperties

...

...

...

...

PidMapper (變數) 



 

**大小**：32位不帶正負號的整數，表示從這個欄位開頭到訊息結尾的位元組數目。

**CColumnSetPresent**：指出 ColumnSet 欄位是否存在的位元組欄位。 此欄位必須設定為0x01 或0x00。 如果設定為0x01，則必須有 CColumnSet 欄位。 如果設定為0x00，則必須不存在。

**ColumnSet**： CColumnSet 結構，其中包含要傳回 CPidMapper 屬性的資料行編號。

**CRestrictionPresent**：一個位元組欄位，指出限制欄位是否存在。 如果設定為任何非零值，則限制欄位必須存在。 如果設定為0x00，則限制必須不存在。

**限制**： CRestriction 結構，其中包含查詢的命令樹。

**CSortSetPresent**：指出 SortSet 欄位是否存在的位元組欄位。 如果設定為任何非零值，則必須有 SortSet 欄位。 如果設定為0x00，則 SortSet 必須不存在。

**SortSet**： CSortSet 結構，指出查詢的排序次序。

**CCategorizationSetPresent**：指出 CCategorizationSet 欄位是否存在的位元組欄位。 如果設定為任何非零值，則必須有 CCategorizationSet 欄位。 如果設定為0x00，則 CCategorizationSet 必須不存在。

**CCategorizationSet**：包含查詢群組的 CCategorizationSet 結構。

**RowSetProperties**：提供查詢設定資訊的 CRowsetProperties 結構。

**PidMapper**： CPidMapper 結構，其中包含要在資料列集中傳回的屬性。

### <a name="2239-cpmcreatequeryout"></a>2.2.3.9 CPMCreateQueryOut

CPMCreateQueryOut 訊息包含 CPMCreateQueryIn 訊息的回應。

標頭後面的 CPMCreateQueryOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_fTrueSequential

\_fWorkIdUnique

aCursors



 

**\_ fTrueSequential**：資訊性布林值，指出查詢是否可預期更快提供結果。 當針對 CPMCreateQueryIn 中提供的查詢設定為0x00000001 時，伺服器可以使用索引，因為這樣可能會更快傳遞查詢結果。 當設定為0x00000000 時，傳遞查詢結果會有較大的延遲。 不得設定為任何其他值。

**\_ fWorkIdUnique**：布林值，指出資料指標所指向的檔識別碼在查詢結果中是否是唯一的。 如果設定為0x00000001，則識別碼是唯一的。 如果設定為0x00000000，則只有在整個資料列集中是唯一的。

**aCursors**：32位不帶正負號整數的陣列，代表資料指標的控制碼，其中專案數等於 CPMCreateQueryIn 訊息的 CategorizationSet 欄位中的類別目錄數目。

### <a name="22310-cpmgetquerystatusin"></a>2.2.3.10 CPMGetQueryStatusIn

CPMGetQueryStatusIn 訊息會要求查詢的狀態。 標頭後面的 CPMGetQueryStatusIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor**：32位不帶正負號的整數，代表 CPMCreateQueryOut 訊息中的控制碼，該控制碼會識別要取得其狀態資訊的查詢。

### <a name="22311-cpmgetquerystatusout"></a>2.2.3.11 CPMGetQueryStatusOut

CPMGetQueryStatusOut 訊息會以查詢的狀態回復 CPMGetQueryStatusIn 訊息。 標頭後面的 CPMGetQueryStatusOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_狀態



 

**\_ 狀態**：下表中定義的值位元遮罩，可描述查詢。

下表列出透過 \_ \* 0x00000007 對狀態執行位 and 運算所取得的 STAT 值 \_ 。 結果必須是下列其中一項：



| 常數                 | 意義                                                                           |
|--------------------------|-----------------------------------------------------------------------------------|
| STAT \_ 忙碌0x00000000    | 非同步查詢仍在執行中。                                          |
| STAT \_ 錯誤0x00000001   | 查詢處於錯誤狀態。                                                   |
| STAT \_ 完成0x00000002    | 查詢已完成。                                                            |
| STAT \_ REFRESH 0x00000003 | 查詢已完成，但更新會導致額外的查詢計算。 |



 

下表列出 \_ \* 可以獨立設定的其他 STAT 位。



| 常數                                    | 意義                                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| STAT 非搜尋 \_ \_ 字0x00000010               | 在內容查詢中，以萬用字元取代非搜尋字。                                                              |
| \_新的 STAT 內容已 \_ 過期 \_ \_     | 查詢的結果可能不正確，因為涉及修改但未建立索引的檔案。                             |
| STAT 重新整理 \_ \_ 未完成0x00000040        | 查詢的結果可能不正確，因為涉及修改的查詢和重新編制索引的檔案不包含內容。 |
| STAT \_ 內容 \_ 查詢 \_ 未完成0x00000080 | 內容查詢太複雜而無法完成或需要列舉，而不是使用內容索引。                          |
| 已 \_ 超過 STAT 時間 \_ 限制 \_ 0x00000100      | 查詢的結果可能不正確，因為查詢執行時間達到允許的時間上限。                    |



 

### <a name="22312-cpmgetquerystatusexin"></a>2.2.3.12 CPMGetQueryStatusExIn

CPMGetQueryStatusExIn 訊息會要求查詢的狀態和其他資訊，例如已編制索引的檔數目、剩下要編制索引的檔數目等等。 標頭後面的 CPMGetQueryStatusExIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_bmk



 

**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，識別要從中取得狀態資訊的查詢。

**\_ bmk**：代表應抓取其位置之書簽控制碼的32位值。

### <a name="22313-cpmgetquerystatusexout"></a>2.2.3.13 CPMGetQueryStatusExOut

CPMGetQueryStatusExOut 訊息會以查詢的狀態和其他狀態資訊回復 CPMGetQueryStatusExIn 訊息，如下圖所述。 標頭後面的 CPMGetQueryStatusExOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_狀態

\_cFilteredDocuments

\_cDocumentsToFilter

\_dwRatioFinishedDenominator

\_dwRatioFinishedNumerator

\_iRowBmk

\_cRowsTotal



 

**\_ 狀態**：其中一個 STAT \_ \*在區段2.2.3.11 中指定的值。

**\_ cFilteredDocuments**：32位不帶正負號的整數，表示已編制索引的檔數目

**\_ cDocumentsToFilter**：32位不帶正負號的整數，表示仍維持編制索引的檔數目。

**\_ dwRatioFinishedDenominator**：32位不帶正負號的整數，表示查詢已完成處理之檔比例的分母。

**\_ dwRatioFinishedNumerator**：32位不帶正負號的整數，表示查詢完成處理之檔的比率分子。

**\_ iRowBmk**：32位不帶正負號的整數，指出資料列集中書簽的大概位置（以資料列為單位）。

**\_ cRowsTotal**：32位不帶正負號的整數，指定資料列集中的資料列總數。

### <a name="22314-cpmsetbindingsin"></a>2.2.3.14 CPMSetBindingsIn

CPMSetBindingsIn 訊息會要求將資料行系結至資料列集。 伺服器將會使用 CPMBindingsIn 訊息的標頭區段，以及 [狀態] 欄位中包含的要求結果來回複 CPMSetBindingsIn 要求訊息 \_ 。 標頭後面的 CPMSetBindingsIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (選用) 

\_cbRow (選用) 

\_cbBindingDesc (選用) 

\_虛擬 (選擇性) 

cColumns (選用) 

aColumns (變數，選擇性) 



 

**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，可識別要設定系結的資料列。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

**\_ cbRow**：32位不帶正負號的整數，表示資料列的大小（以位元組為單位）。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

**\_ cbBindingDesc**：32位不帶正負號的整數，表示在虛擬欄位之後的欄位長度（以位元組為單位） \_ 。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

**\_ 虛擬**：此欄位未使用，必須予以忽略。 可以設定為任意值。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

**cColumns**：32位不帶正負號的整數，表示 aColumns 陣列中的元素數目。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

**aColumns**： CTableColumn 結構的陣列，描述資料列集中資料列的資料行。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。 陣列中的結構必須以0到3個填補位元組分隔，因此每個結構的開頭都是4個位元組的對齊方式。 這類填補位元組可以是任意值，而且必須在收到時忽略。

### <a name="22315-cpmgetrowsin"></a>2.2.3.15 CPMGetRowsIn

CPMGetRowsIn 訊息會要求查詢中的資料列。 標頭後面的 CPMGetRowsIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_cRowsToTransfer

\_cbRowWidth

\_cbSeek

\_cbReserved

\_cbReadBuffer

\_ulClientBase

\_fBwdFetch

eType

\_chapt

SeekDescription

...

... (變數) 



 

**\_ hCursor**：代表 CPMCreateQueryOut 訊息之控制碼的32位值，識別要從中取得資料列的查詢。

**\_ cRowsToTransfer**：32位不帶正負號的整數，指出用戶端想要接收以回應此訊息的最大資料列數目。

**\_ cbRowWidth**：32位不帶正負號的整數，表示資料列的長度（以位元組為單位）。

**\_ cbSeek**：32位不帶正負號的整數，表示以 eType 開頭的訊息大小。

**\_ cbReserved**：32位不帶正負號的整數，指出 CPMGetRowsOut 訊息的大小（以位元組為單位）， (不含資料列和 SeekDescriptions 欄位) 。 這個欄位中的這個值會加入至 \_ cbSeek 欄位的值，然後用來計算 CPMGetRowsOut 訊息中資料欄欄位的位移。

**\_ cbReadBuffer**：32位不帶正負號的整數，必須設定為 cRowsToTransfer 的值 \_ cbRowWidth 或1000倍的最大值 \_ ，舍入到最接近的512位元組倍數。 此值不得超過0x00004000。

**\_ ulClientBase**：32位不帶正負號的整數，表示要用於資料列緩衝區中指標計算的基底值。 如果使用的是64位位移，則會使用訊息標頭的 reserved2 欄位作為上層32位，並使用 \_ ulClientBase 作為64位值的低32位。 如需詳細資訊，請參閱2.2.3.16 一節。

**\_ fBwdFetch**：32位不帶正負號的整數，表示提取資料列的順序。 如果設定為0x00000001，則會以反向順序提取資料列。 如果設定為0x00000000，則會以正向順序提取資料列。 不得設定為任何其他值。

**eType**：32位不帶正負號的整數，其中包含下列其中一個值，表示要執行的作業類型。



| 值                         | 意義                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowSeekNext 0x00000001       | SeekDescription 包含 CRowSeekNext 結構。       |
| eRowSeekAt 0x00000002         | SeekDescription 包含 CRowSeekAt 結構。         |
| eRowSeekAtRatio 0x00000003    | SeekDescription 包含 CRowSeekAtRatio 結構。    |
| eRowSeekByBookmark 0x00000004 | SeekDescription 包含 CRowSeekByBookmark 結構。 |



 

**\_ chapt**：代表資料列集章節之控制碼的32位值。

**SeekDescription**：這個欄位必須包含 eType 值所指定之類型的結構。

### <a name="22316-cpmgetrowsout"></a>2.2.3.16 CPMGetRowsOut

CPMGetRowsOut 訊息會以查詢的資料列回復 CPMGetRowsIn 訊息。 伺服器必須在 [資料列] 欄位中將位移格式化為可變長度資料類型，如下所示：

-   用戶端表示它是32位系統 (0x00000008 或更少在 CPMConnectIn) 的 iClientVersion 欄位中：位移是32位整數。
-   用戶端表示它是64位的系統 (\_ iClientVersion >) CPMConnectIn 中的0x00000008，而伺服器表示它是32位系統 (\_ serverVersion 設定為0x00000007 中的 CPMConnectOut) ：位移是32位整數
-   用戶端表示它是64位的系統 (\_ iClientVersion >) CPMConnectIn 中的0x00000008，而伺服器表示它是64位系統 (\_ serverVersion 設定為0x00010007 中的 CPMConnectOut) ：位移是64位整數

標頭後面的 CPMGetRowsOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cRowsReturned

eType

\_chapt

SeekDescription (選擇性、變數) 

...

...

paddingRows (選擇性、變數) 

資料列



 

**\_ cRowsReturned**：32位不帶正負號的整數，指出資料列中傳回的資料列數目。

**eType**：32位不帶正負號的整數，其中包含下列其中一個值，以指出要執行的 rowseek 作業類型



| 值                         | 意義                                                  |
|-------------------------------|----------------------------------------------------------|
| eRowsSeekNone 0x00000000      | 無 SeekDescription，忽略 SeekDescription 欄位。        |
| eRowSeekNext 0x00000001       | SeekDescription 包含 CRowSeekNext 結構。       |
| eRowSeekAt 0x00000002         | SeekDescription 包含 CRowSeekAt 結構。         |
| eRowSeekAtRatio 0x00000003    | SeekDescription 包含 CRowSeekAtRatio 結構。    |
| eRowSeekByBookmark 0x00000004 | SeekDescription 包含 CRowSeekByBookmark 結構。 |



 

**\_ chapt**：代表資料列集章節之控制碼的32位值。

**SeekDescription**：此欄位必須包含 eType 欄位所表示之類型的結構。

**paddingRows**：此欄位必須有足夠的長度 (0 到 \_ cbReserved-1 個位元組) 為了將資料欄欄位填補至 \_ 從訊息開頭 cbReserved 的位移，其中 \_ cbReserved 是 CPMGetRowsIn 訊息中的值。 此欄位中使用的填補位元組可以是任意值。 接收者必須忽略此欄位。

資料列：資料列資料的格式設定為最近 CPMSetBindingsIn 訊息中的 **資料行資訊**。 資料列必須以轉寄順序儲存 (例如，資料列2之前的資料列 1) 。

固定大小的資料行必須儲存在最新 CPMSetBindingsIn 訊息所指定的位移上。

可變大小的資料行 (例如，字串) 必須依照下列方式儲存：

-   變數資料本身 (例如，字串) 會以遞減 (順序儲存在緩衝區結尾，例如，資料列1的所有變數資料的集合在結尾、第2列最接近的位置，) 依此類推。
-   在資料列緩衝區開頭的固定大社區域 (，) 必須包含每個資料行的 CRowVariant，這些資料行會儲存在最新 CPMSetBindingsIn 訊息中指定的位移。 vType 必須包含資料類型 (例如： VT \_ LPWSTR) 。 若為，則在使用32位位移時，CRowVariant 中的位移欄位必須包含32位值，這是從 CPMGetRowsOut 訊息的開頭算起的變數資料位移，加上 \_ 最新 CPMGetRowsIn 訊息中指定的 ulClientBase 的值。 如果使用的是64位位移，則 CRowVariant 中的位移欄位必須包含64位值，該值是 CPMGetRowsOut 訊息開頭的位移，並新增至使用 \_ ulClientBase 做為低32位和 \_ ulReserved2 為高32位所組成的64位值。

例如，如果 CPMSetBindingsIn 訊息指定了兩個數據行大小 (VT \_ I4) 和 Title (vt \_ LPWSTR) -and \_ ulClientBase from CPMGetRowsIn was 0x10000，則兩個數據列會如下所示。 以灰色標示的區段是緩衝區的固定長度部分。

![cpmsetbindingsin 訊息範例](images/cpmgetrowsout.gif)

### <a name="22317-cpmratiofinishedin"></a>2.2.3.17 CPMRatioFinishedIn

CPMRatioFinishedIn 訊息會要求查詢的完成百分比。 標頭後面的 CPMRatioFinishedIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_fQuick



 

**\_ HCursor**： CPMCreateQueryOut 訊息的控制碼，識別要要求完成資訊的查詢。

**\_ fQuick**：必須設定為0x00000001。 如果未使用，則伺服器必須加以忽略。

### <a name="22318-cpmratiofinishedout"></a>2.2.3.18 CPMRatioFinishedOut

CPMRatioFinishedOut 訊息會以查詢的完成率回復 CPMRatioFinishedIn 訊息。 標頭後面的 CPMRatioFinishedOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_ ulNumerator

\_ulDenominator

\_烏鴉

\_fNewRows



 

**\_ ulNumerator**：32位不帶正負號的整數，指出完成比率的分子（以資料列數為單位）。

**\_ ulDenominator**：32位不帶正負號整數，指出完成比率的分母（以資料列為單位）。 必須大於零。

**\_ >crows**：32位不帶正負號的整數，指出查詢的資料列總數。

**\_ fNewRows**：布林值，指出是否有新的資料列可用。 值為0x00000001 表示資料列集內有新的資料列可用。 值為0x00000000 表示資料列集不包含任何新的資料列。 這個欄位不得設定為任何其他值。

### <a name="22319-cpmfetchvaluein"></a>2.2.3.19 CPMFetchValueIn

CPMFetchValueIn 訊息要求的屬性值太大而無法在資料列集中傳回。 如3.2.4.2.5 一節中所指定，此訊息會重複傳送以抓取屬性的所有位元組，並為 \_ 每個位元組更新 cbSoFar，直到 \_ CPMFetchValueOut 訊息的 fMoreExists 欄位設定為 **FALSE**。

標頭後面的 CPMFetchValueIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_Wid

\_cbSoFar

\_cbPropSpec

\_cbChunk

PropSpec (變數) 

...

\_填補 (變數) 



 

**\_ wid**：32位不帶正負號的整數，其中包含可識別應提取屬性之檔識別碼的相關資訊。

**\_ cbSoFar**：32位不帶正負號的整數，其中包含先前針對此屬性傳送的位元組數目。 在第一則訊息中必須設定為0x00000000。

**\_ cbPropSpec**：32位不帶正負號的整數，其中包含 PropSpec 欄位的大小（以位元組為單位）。

**\_ cbChunk**：32位不帶正負號的整數，其中包含傳送者可在 CPMFetchValueOut 訊息中接受的位元組數目上限。

*Windows 行為：此欄位會設定為所有 Windows 版本的0x00004000。*

**PropSpec**：指定要取得之屬性的 CFullPropSpec 結構。

**\_ 填補**：此欄位必須是必要的長度 (0 至3個位元組) 將訊息填補至4個位元組的長度。 填補位元組的值可以是任意值。 接收者必須忽略此欄位。

### <a name="22320-cpmfetchvalueout"></a>2.2.3.20 CPMFetchValueOut

CPMFetchValueOut 訊息會使用前一個查詢的屬性值回復 CPMFetchValueIn 訊息。 如3.1.5.2.8 一節中所指定，此訊息會在每個 CPMFetchValueIn 訊息之後傳送，直到屬性的所有位元組都經過傳送為止。

標頭後面的 CPMFetchValueOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cbValue

\_fMoreExists

\_fValueExists

vType

vValue (變數) 



 

**\_ cbValue**：32位不帶正負號的整數，其中包含總大小（以位元組為單位） vValue。

**\_ fMoreExists**：布林值，指出是否有其他可用的 CPMFetchValueOut 訊息。 如果設定為0x00000001，則會有額外的 CPMFetchValueOut 訊息。 如果設定為0x00000000，則沒有其他可用的 CPMFetchValueOut 訊息。

**\_ fValueExists**：布林值，指出屬性是否有值。 如果設定為0x00000001，屬性的值就會存在。 如果設定為0x00000000，則屬性的值不存在。

**vType**: A value from the VARENUM enumeration, see Section 2.2.1.1 for details, describing the type of the property.

**vValue**：位元組陣列的一部分，其中包含2.2.1.32 區段中指定的 SERIALIZEDPROPERTYVALUE 結構，其中部分開頭的位移是 \_ CPMFetchValueIn 中 cbSoFar 的值。 \_如果 fMoreExists 設定為0x00000001，部分的長度（以 cbValue 欄位表示）必須等於 \_ CPMFetchValueIn 中 cbChunk 的值， \_ 否則必須小於或等於 cbChunk 的值 \_ 。

### <a name="22321-cpmgetnotify"></a>2.2.3.21 CPMGetNotify

CPMGetNotify 訊息會要求用戶端想要收到資料列集變更的通知。

訊息不得包含主體;只會傳送在2.2.2 節中指定的訊息標頭。

### <a name="22322-cpmsendnotifyout"></a>2.2.3.22 CPMSendNotifyOut

CPMSendNotifyOut 訊息會通知用戶端查詢結果的變更。

只有在發生變更時，才會傳送此訊息。 標頭後面的 CPMSendNotifyOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_watchNotify



 

**\_ watchNotify**：對查詢的變更。 它必須是下列值之一：



| 值                                     | 意義                                             |
|-------------------------------------------|-----------------------------------------------------|
| DBWATCHNOTIFY \_ ROWSCHANGED 0x00000001     | 查詢資料列集中的資料列數目已變更。 |
| DBWATCHNOTIFY \_ QUERYDONE 0x00000002       | 查詢已完成。                            |
| DBWATCHNOTIFY \_ QUERYREEXECUTED 0x00000003 | 已重新執行查詢。                     |



 

### <a name="22323-cpmgetapproximatepositionin"></a>2.2.3.23 CPMGetApproximatePositionIn

CPMGetApproximatePositionIn 訊息會要求某一章中書簽的大概位置。 標頭後面的 CPMGetApproximatePositionIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmk



 

**\_ hCursor**：代表從 CPMCreateQueryOut 針對包含書簽的資料列集取得之查詢資料指標的32位值。

**\_ chapt**：代表包含書簽之章節控制碼的32位值。

**\_ bmk**：代表要取得其近似位置之書簽控制碼的32位值。

### <a name="22324-cpmgetapproximatepositionout"></a>2.2.3.24 CPMGetApproximatePositionOut

CPMGetApproximatePositionOut 訊息會回復 CPMGetApproximatePositionIn 訊息，其中描述章節中書簽的大概位置。 標頭後面的 CPMGetApproximatePositionOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_分子

\_denominator



 

**\_ 分子**：32位不帶正負號的整數，其中包含資料列集中書簽的資料列編號。 如果沒有任何資料列，則此欄位必須設定為0x00000000。

**\_ 分母**：32位不帶正負號的整數，其中包含資料列集中的資料列數目。

### <a name="22325-cpmcomparebmkin"></a>2.2.3.25 CPMCompareBmkIn

CPMCompareBmkIn 訊息會要求一章中兩個書簽的比較。

標頭後面的 CPMCompareBmkIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor

\_chapt

\_bmkFirst

\_bmkSecond



 

\_**hCursor**：代表包含書簽之資料列集之 CPMCreateQueryOut 訊息控制碼的32位值。

\_**chapt**：代表章節之控制碼的32位值，其中包含要比較的書簽。

\_**bmkFirst**：代表要比較之第一個書簽控制碼的32位值。

\_**bmkSecond**：代表要比較之第二個書簽控制碼的32位值。

### <a name="22326-cpmcomparebmkout"></a>2.2.3.26 CPMCompareBmkOut

CPMCompareBmkOut 訊息會使用一章中兩個書簽的比較來回複 CPMCompareBmkIn 訊息。 標頭後面的 CPMCompareBmkOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_dwComparison



 

\_**dwComparison**：下列其中一個值，表示章節中兩個書簽的相對位置。



| 值                               | 意義                                                           |
|-------------------------------------|-------------------------------------------------------------------|
| DBCOMPARE \_ LT 0x00000000            | 第一個書簽位於第二個。               |
| DBCOMPARE \_ EQ 0x00000001            | 第一個書簽的位置與第二個相同。           |
| DBCOMPARE \_ GT 0x00000002            | 第一個書簽的位置是在第二個。                |
| DBCOMPARE \_ NE 0x00000003            | 第一個書簽的位置與第二個不同。 |
| DBCOMPARE \_ NOTCOMPARABLE 0x00000004 | 第一個書簽無法與第二個書簽比較。               |



 

### <a name="22327-cpmrestartpositionin"></a>2.2.3.27 CPMRestartPositionIn

CPMRestartPositionIn 訊息會將資料指標的提取位置移至章節的開頭。 如3.1.5.2.12 一節中所指定，伺服器將使用相同的訊息來回複，並將要求的結果包含在 \_ CISP 標頭的 status 欄位中。

標頭後面的 CPMRestartPositionIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor (選用) 

\_chapt (選用) 



 

**\_ hCursor**：代表從 CPMCreateQueryOut 訊息取得之控制碼的32位值，識別要重新開機位置的查詢。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

**\_ chapt**：代表從中取出資料列之章節控制碼的32位值。 當用戶端傳送訊息時，這個欄位必須存在，而且當伺服器傳送訊息時，必須不存在這個欄位。

### <a name="22328-cpmfreecursorin"></a>2.2.3.28 CPMFreeCursorIn

CPMFreeCursorIn 訊息會要求資料指標的版本。 標頭後面的 CPMFreeCursorIn 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_hCursor



 

**\_ hCursor**：代表要釋放之 CPMCreateQueryOut 訊息中資料指標控制碼的32位值。

### <a name="22329-cpmfreecursorout"></a>2.2.3.29 CPMFreeCursorOut

CPMFreeCursorOut 訊息會回復 CPMFreeCursorIn 訊息，其中包含釋出資料指標的結果。 標頭後面的 CPMFreeCursorOut 訊息格式如下：



0

1

2

3

4

5

6

7

8

9

1<br/> 0<br/>

1

2

3

4

5

6

7

8

9

2<br/> 0<br/>

1

2

3

4

5

6

7

8

9

3<br/> 0<br/>

1

\_cCursorsRemaining



 

**\_ cCursorsRemaining**：32位不帶正負號的整數，表示仍在查詢中使用的資料指標數目。

### <a name="22330-cpmdisconnect"></a>2.2.3.30 CPMDisconnect

CPMDisconnect 訊息會結束與伺服器的連接

訊息不得包含主體;只會傳送在2.2.2 節中指定的訊息標頭。

### <a name="224-errors"></a>2.2.4 錯誤

所有內容索引服務通訊協定訊息都必須在成功時傳回 0x00000000;否則，它們會傳回32位非零的錯誤碼，此錯誤碼可以是 HRESULT 或 NTSTATUS 值 (請參閱 1.8) 一節。 如果緩衝區太小而無法符合結果，就必須傳回狀態為 [ \_ 資源不足] (0xC0000009A) 的狀態碼， \_ 而且應該以較大的緩衝區重試失敗的作業。

所有其他錯誤值都必須視為相同。

 (請注意，除非具有相同意義的值，否則目前的 HRESULT 和 NTSTATUS 編號空間不會重迭，但即使它們在未來會發生衝突，也不會造成任何通訊協定問題，只要狀態不足的資源值仍維持唯一的值，就不會造成任何通訊協定問題 \_ \_ ，因為所有其他錯誤值的處理方式都相同。 ) 

## <a name="3-protocol-details"></a>3 通訊協定詳細資料

-   [3.1 伺服器詳細資料](#31-server-details)
-   [3.2 用戶端詳細資料](#32-client-details)

從遠端查詢索引服務目錄的 CISP 訊息要求不需要任何特定的順序。 建議您將較高的層級導向至有意義的訊息順序，不過，就像是從這個序列或使用不正確資料收到的訊息一樣，伺服器將會以錯誤回應。 某些訊息也會相依于更高的層級，以提供在序列稍早的訊息中收到的有效資料。

下圖說明從用戶端到遠端電腦的簡單查詢的一般訊息順序。

![簡單查詢的訊息順序](images/protocoldetails.jpg)

上圖所示的訊息代表用來查詢遠端索引服務類別目錄的所有 CISP 訊息子集。

### <a name="31-server-details"></a>3.1 伺服器詳細資料

### <a name="311-abstract-data-model"></a>3.1.1 抽象資料模型

下一節指定 CISP 伺服器所維護的資料和狀態。 此處提供的資料可協助說明通訊協定的運作方式。 本節不會強制執行此模型，只要其外部行為與本檔中所述的一致。

執行 CISP 的索引服務必須維護下列抽象資料元素：

-   連線到伺服器的用戶端清單
-   每個用戶端的相關資訊，包括：
-   -   用戶端的版本 (，如區段2.2.3.6 中指定的 CPMConnectIn 訊息所示) 
    -   CPMConnectIn 訊息 (與用戶端相關聯的目錄) 
    -   2.2.1.21.1 一節中所指定的其他用戶端屬性。
    -   用戶端的搜尋查詢
    -   查詢的資料指標控制碼清單以及每個控制碼的結果集中的位置。
    -   目前的系結集合
    -   查詢的目前狀態，其中包含每個資料指標) 的 (：
    -   -   查詢結果中的資料列數目
        -   查詢完成的分子和分母
        -   最後一個資料列數目，由這個資料指標的最新 CPMRatioFinishedOut 訊息所報告
        -   無論查詢是否由伺服器監視查詢結果的變更，以及它是否受到監視，查詢結果中的變更會在查詢結果中變更，因為它上次回報給用戶端的 CPMSendNotifyOut
        -   此查詢對用戶端提供的章節控制碼清單。
        -   此查詢對用戶端提供之每個資料指標的書簽控制碼清單。

-   索引服務目前的狀態，可能是「未初始化」、「執行中」或「正在關機」。 請注意，大部分的時間伺服器處於「正在執行」狀態。 以下是伺服器的狀態機器圖表：

    ![索引服務伺服器的狀態機器圖表](images/abstractdatamodel.jpg)

-   每個目錄資訊：已編制索引的檔數目、索引的大小、唯一索引鍵的數目等 (請參閱 < 完整清單 () 的2.2.3.1 一節，其中對應至區段 2.2.3.2) 中 dwNewState 的值。
-   針對每個支援的語言，如2.2.1.3 一節中所討論的單字變化資料庫。

### <a name="312-timers"></a>3.1.2 計時器

不需要任何通訊協定計時器。

### <a name="313-initialization"></a>3.1.3 初始化

初始化時，伺服器必須將其狀態設定為 [未初始化]，並開始接聽區段1.9 中指定之具名管道上的訊息。 進行任何其他內部初始化之後，它必須轉換成「正在執行」狀態。

### <a name="314-higher-layer-triggered-events"></a>3.1.4 較高層級觸發事件

無。

### <a name="315-message-processing-and-sequencing-rules"></a>3.1.5 訊息處理和排序規則

當處理用戶端傳送的訊息期間發生錯誤時，伺服器必須向用戶端報告錯誤，如下所示：

-   停止處理用戶端傳送的訊息
-   以訊息標頭回應 (只有用戶端傳送的訊息) ，讓 \_ msg 欄位保持不變。
-   將 [ \_ 狀態] 欄位設定為錯誤碼值。

當訊息抵達時，伺服器必須檢查 \_ msg 域值，以查看它是否為已知的類型 (請參閱第2.2.2 節) 。 如果類型未知，則必須報告狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。

\_如果訊息類型是下列其中一項，則伺服器必須驗證 ulChecksum 域值：

-   CPMConnectIn (0x000000C8) 
-   CPMCreateQueryIn (0x000000CA) 
-   CPMSetBindingsIn (0x000000D0) 
-   CPMGetRowsIn (0x000000CC) 
-   CPMFetchValueIn (0x000000E4) 

若要驗證 \_ ulChecksum 域值，伺服器必須檢查用戶端在 CPMConnectIn 訊息的 iClientVersion 欄位中指定的值 \_ 。

如果 [ \_ iClientVersion] 欄位未設定為 [0x00000008]，且 [ \_ ulChecksum] 欄位未設定為0x00000000，則伺服器必須回報狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。 伺服器不能驗證 \_ 用戶端的 ulChecksum 欄位將 \_ iClientVersion 欄位設定為小於0x00000008 的值。

如果 \_ iClientVersionfield 域值為0x00000008 或更大，則伺服器必須驗證 \_ ulChecksum 欄位的計算方式是在 [3.2.4] 區段中指定。 如果 \_ ulChecksum 值無效，伺服器必須報告狀態不正確參數， \_ \_ (0xC000000D) 錯誤。

接著，伺服器會檢查其中的狀態。 如果其狀態為 [未初始化]，伺服器必須報告 CI \_ E \_ 未 \_ 初始化 (0x8004180B) 錯誤。 如果狀態為「關閉」，伺服器必須報告 CI \_ E \_ SHUTDOWN (0x80041812) 錯誤。

一旦將標頭判斷為有效且伺服器處於「執行中」狀態之後，就必須依照下列各節所指定的方式來執行進一步的訊息特定處理。

### <a name="3151-remote-indexing-service-catalog-management"></a>3.1.5.1 遠端索引服務目錄管理

### <a name="31511-receiving-a-cpmcistateinout-request"></a>3.1.5.1.1 接收 CPMCiStateInOut 要求

當伺服器收到來自用戶端的 CPMCIStateInOut 訊息要求時，伺服器必須先檢查用戶端是否在已連線的用戶端清單中。 如果用戶端不在清單中，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。 否則，它必須以 CPMCIStateInOut 訊息回應用戶端，並使用與2.2.3.1 小節中所指定的用戶端相關聯的目錄相關資訊來填入。

### <a name="31512-receiving-a-cpmsetcatstatein-request"></a>3.1.5.1.2 接收 CPMSetCatStateIn 要求

當伺服器收到來自用戶端的 CPMSetCatStateIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否具有系統管理存取權。 如果用戶端沒有系統管理存取權，則伺服器必須回報狀態 \_ 拒絕存取 \_ (0xC0000022) 錯誤。
-   如果 \_ dwNewState 不等於 CICAT ALL 會 \_ \_ 開啟，則變更 CatName 欄位中指定的目錄狀態，如 \_ dwNewState 欄位所指定。 如需詳細資訊，請參閱2.2.3.2 一節。 如果伺服器未在 CatName 欄位中找到具有指定名稱的目錄，伺服器必須傳回狀態 \_ 不正確 \_ 參數， (0xC000000D) 錯誤。
-   以 CPMSetCatStateOut 訊息回應用戶端，其中 \_ DWOLDSTATE 必須設定為目錄的先前狀態。 如果 \_ dwNewState 等於 CICAT， \_ 則所有 \_ 開啟的伺服器都必須檢查所有目錄的狀態，如果全部都已啟動，就必須將 \_ dwOldState 設定為0x00000001，否則請將 \_ dwOldState 設定為0x00000000。

### <a name="31513-receiving-a-cpmupdatedocumentsin-request"></a>3.1.5.1.3 接收 CPMUpdateDocumentsIn 要求

當伺服器收到 CPMUpdateDocumentsIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否位於已連線的用戶端清單中， (具有) 相關聯的目錄。 如果用戶端不在清單中，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查用戶端是否具有系統管理存取權。 如果用戶端沒有伺服器的系統管理存取權，則伺服器必須回報狀態 \_ \_ 拒絕存取 (0xC0000022) 錯誤。
-   根據 CPMUpdateDocumentsIn 訊息中的旗標欄位，開始建立用戶端所指定路徑的索引編制程式、執行完整或增量掃描 \_ 。 如果路徑先前未建立索引，則必須將它加入至索引位置的集合，並執行完整掃描。 如果指定了不合法的 \_ 旗標欄位值，伺服器必須 \_ 將旗標設為 UPD \_ INIT 並執行完整掃描。 這項作業必須在與用戶端相關聯的目錄中執行。
-   使用 CPMUpdateDocumentsIn 的訊息標頭回應用戶端，並將 [狀態] \_ 欄位設定為要求的結果。

### <a name="31514-receiving-a-cpmforcemergein-request"></a>3.1.5.1.4 接收 CPMForceMergeIn 要求

當伺服器收到 CPMForceMergeIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否位於已連線的用戶端清單中， (具有) 相關聯的目錄。 如果用戶端不在清單中，伺服器必須報告狀態 \_ 不正確 \_ 參數 (0xC000000D) 錯誤。
-   檢查用戶端是否具有系統管理存取權。 如果用戶端沒有系統管理存取權，則伺服器必須回報狀態 \_ 拒絕存取 \_ (0xC0000022) 錯誤。
-   開始在與用戶端相關聯的目錄上改善查詢效能所需的維護流程。
-   使用 CPMForceMergeIn 的訊息標頭回應用戶端，並將 [狀態] \_ 欄位設定為要求的結果。

請注意，維護程式是非同步，而且可以在用戶端收到回應訊息之後繼續進行。 此程式不會直接影響通訊協定， (回應時間) 以外的任何方式。

### <a name="3152-remote-indexing-service-querying"></a>3.1.5.2 遠端索引服務查詢

### <a name="31521-receiving-a-cpmconnectin-request"></a>3.1.5.2.1 接收 CPMConnectIn 要求

當伺服器收到來自用戶端的 CPMConnectIn 要求時，伺服器必須執行下列動作：

-   檢查用戶端是否在已連線用戶端清單中。 如果是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查指定的目錄是否存在，而不是處於已停止狀態。 如果不是這種情況，伺服器就必須要有報表 CI \_ E \_ NO \_ CATALOG (0x8004181D) 錯誤。
-   將用戶端新增至已連線的用戶端清單。
-   將目錄與用戶端產生關聯。
-   將 CPMConnectIn 訊息中傳遞的資訊儲存 (例如目錄名稱、用戶端版本等 ) 處於用戶端狀態。
-   以 CPMConnectOut 訊息回應用戶端。

### <a name="31522-receiving-a-cpmcreatequeryin-request"></a>3.1.5.2.2 接收 CPMCreateQueryIn 要求

當伺服器收到來自用戶端的 CPMCreateQueryIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否在已連線用戶端清單中。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查用戶端是否已經有與其相關聯的查詢。 如果是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查與用戶端相關聯的目錄是否處於狀態，以允許處理查詢 (CICAT \_ READONLY 或 CICAT \_ 可寫入) 。 如果不是這種情況，伺服器就必須回報查詢 \_ S 查詢 \_ \_ (0x8004160C) 錯誤。
-   剖析查詢中指定的限制集、排序次序和群組。 如果伺服器發生錯誤，則必須報告適當的錯誤。 如果此步驟因為任何其他原因而失敗，則伺服器必須報告所遇到的錯誤。 如需索引服務查詢錯誤的詳細資訊，請參閱 \[ MSDN-QUERYERR \] 。
-   將搜尋查詢儲存為用戶端的狀態。
-   根據 CPMCreateQueryIn 訊息) 中傳遞的資訊，進行將資料列提供給用戶端所需的準備工作，並將查詢與適當的資料指標控制碼產生關聯 (。
-   將這些控制碼新增至用戶端的資料指標控制碼清單，然後初始化章節控制碼和書簽的清單。
-   將此查詢中每個資料指標的章節控制碼清單初始化為 DB \_ Null \_ HCHAPTER
-   將此查詢中每個資料指標的書簽控制碼清單，初始化為一組 DBBMK \_ FIRST 和 DBBMK \_ LAST。
-   將查詢標示為未監視變更。
-   將資料列的數目初始化為目前計算的資料列數目 (如果查詢無法開始執行，則可以是0，如果查詢是在執行) 的進程中，則為某個數位，然後初始化查詢完成的分子和分母。
-   以 CPMCreateQueryOut 訊息回應用戶端。

### <a name="31523-receiving-a-cpmgetquerystatusin-request"></a>3.1.5.2.3 接收 CPMGetQueryStatusIn 要求

當伺服器收到來自用戶端的 CPMGetQueryStatusIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查游標控制碼是否位於用戶端的資料指標控制碼清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   準備 CPMGetQueryStatusOut 訊息。 伺服器必須抓取目前的查詢狀態，並在 [QStatus] 欄位中設定它 (如需 \_ 可能的值) ，請參閱2.2.3.11。 如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。
-   以 CPMGetQueryStatusOut 訊息回應用戶端。

### <a name="31524-receiving-a-cpmgetquerystatusexin-request"></a>3.1.5.2.4 接收 CPMGetQueryStatusExIn 要求

當伺服器收到來自用戶端的 CPMGetQueryStatusExIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查傳遞的資料指標控制碼是否位於用戶端的資料指標控制碼清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   準備 CPMGetQueryStatusExOut 訊息。 伺服器必須抓取目前的查詢狀態和查詢進度，並設定 QStatus (如需可能的值，請分別參閱 2.2.3.11) 、 \_ dwRatioFinishedDenominator 和 \_ dwRatioFinishedNumerator。 然後，它必須將查詢結果中的資料列數目設定為 \_ cRowsTotal。 如果此步驟因為任何原因而失敗，伺服器必須回報發生錯誤。
-   取得用戶端類別目錄的相關資訊，並填寫 \_ cFilteredDocuments 和 \_ cDocumentsToFilter。 如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。
-   取出 bmk 欄位中的控制碼所指定之書簽的位置 \_ ，然後在 CPMGetQueryStatusExOut 訊息中填滿其餘的 \_ iRowBmk 欄位。 如果此步驟因為任何原因而失敗，伺服器必須回報發生錯誤。
-   以 CPMGetQueryStatusExOut 訊息回應用戶端。

### <a name="31525-receiving-a-cpmratiofinishedin-request"></a>3.1.5.2.5 接收 CPMRatioFinishedIn 要求

當伺服器收到來自用戶端的 CPMRatioFinishedIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   準備 CPMRatioFinishedOut 訊息。 伺服器必須抓取用戶端的查詢狀態，並填寫 \_ ulNumerator、 \_ ulDenominator 和 \_ >crows 欄位。 如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。
-   如果 \_ >crows 等於此查詢最後報告的資料列數目，請將 \_ fNewRows 設定為0x00000000，否則請將其設定為0x00000001。
-   將此查詢最後報告的資料列數更新為 >crows 的值 \_ 。
-   以 CPMRatioFinishedOut 訊息回應用戶端。

### <a name="31526-receiving-a-cpmsetbindingsin-request"></a>3.1.5.2.6 接收 CPMSetBindingsIn 要求

當伺服器收到來自用戶端的 CPMSetBindingsIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   確認系結資訊有效 (亦即，資料行至少指定要傳回的值、長度或狀態;值、長度或狀態的系結中沒有重迭以及符合指定之資料列大小的值、長度和狀態) 以及如果未報告 DB \_ E \_ BADBINDINFO (0x80040E08) 錯誤。
-   儲存與 aColumns 欄位中指定之資料行相關聯的系結資訊。 如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。
-   使用訊息標頭來回應用戶端 (只) \_ 將 msg 設定為 CPMSetBindingsIn，並 \_ 將狀態設定為指定之系結的結果。

### <a name="31527-receiving-a-cpmgetrowsin-request"></a>3.1.5.2.7 接收 CPMGetRowsIn 要求

當伺服器收到來自用戶端的 CPMGetRowsIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查傳遞的資料指標控制碼是否在用戶端資料指標控制碼的 athelist 中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   檢查用戶端是否有一組目前的系結。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   準備 CPMGetRowsOut 訊息。 伺服器必須將游標放在查詢結果中，如搜尋描述所指示。 如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。
-   提取最適合緩衝區的資料列數目，其大小會以 \_ cbReadBuffer 表示，但不能超過 cRowsToTransfer 的指示 \_ 。 提取資料列時，伺服器必須將每個選取的資料行的屬性值類型，與用戶端目前的系結集合中指定的型別進行比較 (區段 3.1.1) 。 如果系結中的型別不是 VT \_ 變異，伺服器必須嘗試將資料行的屬性值轉換為該型別。 否則，如果在 \_ 用戶端的 DBPROPSET QUERYEXT 屬性集中設定 DBPROP USEEXTENDEDDBTYPES 旗標 \_ ，或如果資料行的屬性值不是 VT \_ 向量類型，則必須以其一般型別傳回屬性值。 如果這兩種情況都沒有 (也就是伺服器有 VT \_ 向量類型，而用戶端不支援 vt \_ 向量) ，則伺服器必須嘗試將它轉換成 vt 陣列類型，如下所示 \_ ： VT \_ I8、vt \_ UI8、vt \_ FILETIME 和 vt \_ CLSID 陣列元素無法轉換，而是無法轉換;VT \_ LPSTR 和 vt \_ LPWSTR 陣列元素必須轉換成 vt \_ BSTR; 所有其他類型的陣列元素都必須保持不變。 最後，如果資料列資料行包含章節控制碼或書簽控點，則伺服器必須更新對應的清單。 如果此步驟因為任何原因而失敗，則伺服器必須報告發生錯誤。
-   儲存 cRowsReturned 中提取的實際資料列數 \_ 。
-   將 [搜尋描述] 和 [章節] 欄位從 CPMGetRowsIn 複製到要傳送的 CPMGetRowsOut 訊息。
-   在 [資料列] 欄位中儲存提取的資料列 (請參閱下方的 [狀態位元組] 和 [資料列的結構] 欄位) 的 [2.2.3.16] 區段。
-   以 CPMGetRowsOut 訊息回應用戶端。

[狀態位元組] 欄位上的附注：

如果資料行的 CPMSetBindingIn 訊息 CTableColumn 中的 StatusUsed 設定為0x01，則伺服器必須將從這個資料行的資料列開頭) 的狀態位元組 (設定為下列其中一個值：



| 值 | 意義        |
|-------|----------------|
| 0x00  | StatusOK       |
| 0x01  | StatusDeferred |
| 0x02  | StatusNull     |



 

如果此資料列的屬性值不存在，伺服器必須將狀態位元組設定為 StatusNull。 如果值太大而無法在 CPMGetRowsOut 訊息中傳送，伺服器必須將狀態位元組設定為 StatusDeferred。 否則伺服器必須將狀態位元組設為 StatusOK。

### <a name="31528-receiving-a-cpmfetchvaluein-request"></a>3.1.5.2.8 接收 CPMFetchValueIn 要求

當伺服器收到來自用戶端的 CPMFetchValueIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   準備 CPMFetchValueOut 訊息。 如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。
-   尋找 wid 欄位所指出的檔 \_ ，並檢查此檔的屬性識別碼 (稍後稱為「屬性值」，此用戶端可以使用 PropSpec 結構所指出的「屬性值」 ) 。 如果無法使用此值，伺服器必須將 \_ fValueExists 設定為0x00000000，否則請將 \_ fValueExists 設定為0x00000001。 如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。
-   如果 \_ fValueExists 等於0x00000001，伺服器必須執行下列動作：
-   -   將屬性值序列化為 SERIALIZEDPROPERTYVALUE 結構，並從 cbSoFar 位移開始複製（ \_ 最多 \_ cbChunk 個位元組） (但不超過序列化屬性) 到 vValue 欄位的結尾。 如果此步驟因為任何原因而失敗，伺服器必須報告錯誤。
    -   將 \_ cbValue 設定為上一個步驟中複製的位元組數目。
    -   將 vType 設定為屬性值的屬性類型。
    -   如果序列化屬性的長度大於 \_ cbSoFar 新增至 \_ cbValue，則將 \_ fMoreExists 設定為0x00000001，否則請將其設定為0x00000000。

-   以 CPMFetchValueOut 訊息回應用戶端

### <a name="31529-receiving-a-cpmgetnotify-request"></a>3.1.5.2.9 接收 CPMGetNotify 要求

當伺服器收到來自用戶端的 CPMGetNotify 訊息時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   如果自這個用戶端的最後一個 CPMSendNotifyOut 訊息之後，查詢結果集內沒有任何變更，或者查詢目前未監視結果集內的變更，則伺服器必須回應 CPMGetNotify 訊息，並開始監視查詢結果集的變更。 如果稍後在查詢結果集中有變更，伺服器必須只傳送一個 CPMSendNotifyOut 訊息給用戶端，而且必須在 [watchNotify] 欄位中指定變更 \_ 。
-   如果自上次 CPMSendNotifyOut 訊息之後，查詢結果集的變更，伺服器必須以 CPMSendNotifyOut 回復，而且必須在 [watchNotify] 欄位中指定變更 \_ 。 請注意，在查詢結果的許多變更時，DBWATCHNOTIFY \_ ROWSCHANGED 會採用優先權 (也就是，如果查詢已完成、重新執行，然後變更資料列的數目，然後再次執行查詢，則回報的事件會是 DBWATCHNOTIFY \_ ROWSCHANGED) 。

### <a name="315210-receiving-a-cpmgetapproximatepositionin-request"></a>3.1.5.2.10 接收 CPMGetApproximatePositionIn 要求

當伺服器收到來自用戶端的 CPMGetApproximatePositionIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查游標控制碼、章節控制碼和傳遞的書簽控制碼是否在對應的清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   在查詢結果中尋找與書簽控制碼相關聯的資料列，並估計資料列集中的資料列位置（由章節控點參考），並決定該位置的分子和分母。 請注意，當章節控制碼是 DB \_ Null \_ HCHAPTER 時，對應的章節是查詢的主要資料列集。 如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。
-   以 CPMFetchValueOut 訊息回應用戶端。

### <a name="315211-receiving-a-cpmcomparebmkin-request"></a>3.1.5.2.11 接收 CPMCompareBmkIn 要求

當伺服器收到來自用戶端的 CPMCompareBmkIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查游標控制碼、章節控制碼和傳遞的書簽控制碼是否在對應的清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   準備 CPMCompareBmkOut 訊息。
-   如果書簽控制碼相等，則 \_ DWCOMPARISON 必須設定為 DBCOMPARE \_ EQ。
-   否則，如果其中一個書簽控制碼是 DBBMK \_ FIRST 或 DBBMK \_ LAST，則 \_ dwComparison 必須設定為 DBCOMPARE \_ NE。
-   否則伺服器必須執行下列動作：
-   -   尋找查詢結果中每個書簽控制碼所參考的資料列
    -   如果有任何一個資料列不在 CPMCompareBmkIn 的章節控制碼所指示的章節中，則 \_ DWCOMPARISON 必須設定為 DBCOMPARE \_ NOTCOMPARABLE。
    -   否則，當兩個數據列都位於相同的章節時，伺服器必須近似于本章節的控制碼所參考的資料列集中的資料列位置。 然後，如果第一個資料列的位置小於第二個數據列的位置，則它必須比較位置值，並將 \_ dwComparison 設定為 DBCOMPARE \_ LT; 否則 \_ dwComparison 必須設定為 DBCOMPARE \_ GT。

-   使用已填滿的 CPMCompareBmkOut 訊息來回應用戶端。

### <a name="315212-receiving-a-cpmrestartpositionin-request"></a>3.1.5.2.12 接收 CPMRestartPositionIn 要求

當伺服器收到來自用戶端的 CPMRestartPositionIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查游標控制碼和傳遞的章節控制碼是否在對應的清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   將游標移至章節的開頭，以章節控點來識別。 請注意，當章節控制碼是 DB \_ Null \_ HCHAPTER 時，對應的章節是查詢的主要資料列集。 如果此步驟因為任何原因而失敗，則伺服器必須報告錯誤。
-   以 CPMRestartPositionIn 訊息回應用戶端。

### <a name="315213-receiving-a-cpmfreecursorin-request"></a>3.1.5.2.13 接收 CPMFreeCursorIn 要求

當伺服器收到來自用戶端的 CPMFreeCursorIn 訊息要求時，伺服器必須執行下列動作：

-   檢查用戶端是否有相關聯的查詢。 如果不是這種情況，伺服器必須報告狀態不正確 \_ \_ 參數 (0xC000000D) 錯誤。
-   檢查傳遞的資料指標控制碼是否位於用戶端資料指標控制碼的清單中。 如果不是這種情況，伺服器就必須回報電子 \_ (0x80004005) 錯誤的失敗。
-   釋出資料指標和相關聯的資源 (如需此資料指標控制碼的完整清單) ，請參閱3.1.1 一節。
-   從該用戶端的資料指標清單中移除資料指標。
-   以 CPMFreeCursorOut 訊息回應， \_ 並以剩餘的資料指標數目設定 cCursorsRemaining 欄位。 在此用戶端清單中。
-   如果此用戶端沒有其他資料指標，則伺服器必須釋放查詢和相關聯的資源 (請參閱 3.1.1) 一節。

### <a name="315214-receiving-a-cpmdisconnect-request"></a>3.1.5.2.14 接收 CPMDisconnect 要求

當伺服器收到來自用戶端的 CPMDisconnect 訊息要求時，伺服器必須從連線的用戶端清單中移除用戶端，並釋放與用戶端相關聯的所有資源。

### <a name="316-timer-events"></a>3.1.6 計時器事件

無。

### <a name="317-other-local-events"></a>3.1.7 其他本機事件

當伺服器停止時，它必須先轉換成「正在關機」狀態。 然後，它必須停止接聽管道、執行任何其他執行特定的關機工作，然後轉換成「已停止」狀態。

### <a name="32-client-details"></a>3.2 用戶端詳細資料

### <a name="321-abstract-data-model"></a>3.2.1 抽象資料模型

下一節會指定內容索引服務通訊協定用戶端所維護的資料和狀態。 提供的資料是為了促進通訊協定運作方式的說明。 本節不會強制執行此模型，只要其外部行為與本檔中所述的一致。

用戶端具有下列抽象狀態：

-   **最後傳送的訊息**：最後傳送至伺服器的訊息複本。
-   **目前的屬性值**：「已延後」屬性的部分值，此為正在抓取的進程中。
-   **目前接收的位元組** 數：目前為止針對目前屬性值所接收的位元組數目。
-   **具名管道連接狀態**：與伺服器的連接

### <a name="322-timers"></a>3.2.2 計時器

不需要任何通訊協定計時器。

### <a name="323-initialization"></a>3.2.3 初始化

在收到較高層級的要求之前，不會採取任何動作。

### <a name="324-higher-layer-triggered-events"></a>3.2.4 Higher-Layer 觸發的事件

從較高的層收到要求時，用戶端必須使用2.1 節中指定的詳細資料，建立與伺服器的具名管道連接。 如果無法這麼做，則更高的層級要求必須失敗。 亦即，如果連線失敗，則需要較高層級的責任才能重試。

標頭必須預先暫止，並設定為從2.2.2 節中指定的欄位。

如果是指定為需要非零總和檢查碼的訊息，則 \_ 必須計算 ulChecksum 值，如下所示：

1.  訊息 \_ 標頭中的 ulReserved2 欄位之後的訊息內容必須解釋為32位整數的序列。 用戶端必須計算這些整數所指定之數值的總和。
2.  使用0x59533959 計算此值的位 XOR。
3.  \_從位 XOR 產生的值減去 msg 提供的值。

### <a name="3241-remote-indexing-service-catalog-management"></a>3.2.4.1 遠端索引服務目錄管理

每個訊息都是由較高層的要求所觸發。 用戶端不會針對遠端系統管理目錄的 CISP 訊息要求強制執行訊息順序，但是 (除了 CPMSetCatStateIn) 訊息之外，伺服器只會在用戶端先前透過 CPMConnectIn 訊息連接時才回復成功。

### <a name="32411-sending-a-cpmcistateinout-request"></a>3.2.4.1.1 傳送 CPMCiStateInOut 要求

一般而言，較高的層級會要求通訊協定用戶端在需要伺服器上索引服務的相關資訊時，傳送 CPMCiStateInOut 訊息。

當要求傳送此訊息時，用戶端必須執行下列動作：

-   將區段2.2.3.1 中指定的 CPMCiStateInOut 訊息傳送至伺服器。
-   等候接收來自伺服器的 CPMCiStateInOut 訊息，以無訊息方式捨棄所有其他訊息。
-   報告回應的 [狀態] 欄位的值 \_ ，如果成功，則會將資訊結構傳回至較高的層級。

### <a name="32412-sending-a-cpmsetcatstatein-request"></a>3.2.4.1.2 傳送 CPMSetCatStateIn 要求

一般而言，較高的層級會要求通訊協定用戶端在需要類別目錄或所有目錄的資訊時傳送 CPMSetCatStateIn 訊息。 在此訊息中，較高層必須為通訊協定用戶端提供 dwNewState 的值， \_ 並視需要提供類別目錄的名稱。

當要求傳送此訊息時，用戶端必須執行下列動作：

-   將2.2.3.2 中所指定的 CPMSetCatStateIn 訊息傳送至伺服器。
-   等候接收來自伺服器的 CPMSetCatStateOut 訊息，以無訊息方式捨棄所有其他訊息。
-   報告回應的 [狀態] 欄位的值 \_ ，如果成功，則 \_ dwOldState 回較高的圖層。

### <a name="32413-sending-a-cpmupdatedocumentsin-request"></a>3.2.4.1.3 傳送 CPMUpdateDocumentsIn 要求

如果需要在現有的路徑中更新檔，或將新的檔案路徑加入至索引，則較高的層通常會要求傳送此訊息。 因此，較高的層級是提供掃描的路徑和類型，其指定方式是在2.2.3.4 的區段中指定，其中增量或完整更新適用于現有的路徑，而新的初始化則適用于新的路徑。

為了提供更高的層級要求，用戶端必須執行下列動作：

-   將區段2.2.3.4 中指定的 CPMUpdateDocumentsIn 訊息傳送至伺服器。
-   等候接收來自伺服器的 CPMUpdateDocumentsIn 訊息，以無訊息方式捨棄所有其他訊息。
-   將回應的 [狀態] 欄位值報告 \_ 回較高的圖層。

### <a name="32414-sending-a-cpmforcemergein-request"></a>3.2.4.1.4 傳送 CPMForceMergeIn 要求

一般來說，如果需要改善查詢效能，或是已排程的索引服務維護，則傳送此訊息的層級要求越高。

為了提供更高層級的服務，用戶端必須執行下列動作：

-   依區段2.2.3.5 的指定將 CPMForceMergeIn 訊息傳送至伺服器。
-   等候接收來自伺服器的 CPMUpdateDocumentsIn 訊息，以無訊息方式捨棄所有其他訊息。
-   將回應的 [狀態] 欄位值報告 \_ 回較高的圖層。

### <a name="3242-remote-indexing-service-catalog-query-messages"></a>3.2.4.2 遠端索引服務目錄查詢訊息

除了 CPMGetRowsIn/CPMGetRowsOut、CPMFetchValueIn/CPMFetchValueOut，CISP 訊息和更高層級的要求之間有一對一的關聯性。 針對上述兩個例外狀況，用戶端可能會產生多個訊息來滿足大小需求，或取得完整的屬性。 較高層級通常會追蹤所有查詢特定的資訊 (例如開啟的資料指標控制碼、書簽和章節控制碼的合法值、延遲屬性值的 wid 值等等 ) ，也會追蹤用戶端是否處於連接狀態，但不會由用戶端以任何方式強制執行。

為了方便說明，第3節中的圖表用戶端部分會說明這種簡單的索引服務查詢順序。

### <a name="32421-sending-a-cpmconnectin-request"></a>3.2.4.2.1 傳送 CPMConnectIn 要求

這則訊息通常是較高層級的第一個要求 (如同用戶端未連線一樣，伺服器將會失敗大部分的訊息，但 CPMSetCatStateIn) 除外。 較高層級會為通訊協定用戶端提供連接所需的資訊。

為了提供更高的層級，用戶端必須執行下列動作：

-   填寫訊息，使用更高層級用戶端所提供的資訊 (請參閱 \_ iClientVersion、MachineName、UserName、PropertySet1、PropertySet2 和 aPropertySet 中的 2.2.3.6) 一節。
-   設定 \_ fClientIsRemote、 \_ cbBlob、 \_ cbBlob2、cPropSet 和 cExtPropSet，如2.2.3.6 中所指定。
-   在 [ulChecksum] 欄位中設定總和檢查碼 \_ 。
-   將 CPMConnectIn 訊息傳送至伺服器。
-   等候接收來自伺服器的 CPMConnectOut 訊息，以無訊息方式捨棄所有其他訊息。
-   報告回應的 [狀態] 欄位的值 \_ ，如果成功，則 \_ serverVersion 回較高的圖層。

基於資訊的目的，較高層級通常會在連接成功時執行下列動作，但 CISP 用戶端不會強制執行這些動作：

-   使用遠端索引服務目錄管理訊息進行系統管理工作
-   使用 CPMCreateQueryIn 要求建立搜尋查詢，其目的是要從目錄中抓取結果。

### <a name="32422-sending-a-cpmcreatequeryin-request"></a>3.2.4.2.2 傳送 CPMCreateQueryIn 要求

當通訊協定用戶端連線之後，較高層級通常會提供查詢建立的資訊。 較高的層級會為用戶端提供限制設定、資料行集、排序次序規則和分類集 (可以省略) 、資料列集屬性和屬性識別碼對應程式結構。

從較高的層接收此要求時，用戶端必須執行下列動作：

-   準備 CPMCreateQueryOut，如下所示。
-   -   如果有資料行集存在，請將 CColumnsSetPreset 設定為0x01 並填滿 ColumnsSet 欄位。
    -   如果有限制，請將 CRestrictionPresent 設定為0x01 並填滿限制欄位。
    -   如果有排序集存在，請填入 SortSet 欄位。
    -   如果有分類集存在，請將 CSortSetPresent 設定為0x01 並填滿 CategorizationSet 欄位。
    -   設定2.2.3.8 中指定的剩餘欄位

-   計算 \_ 標頭中的 ulCheckSum 欄位。
-   將 CPMCreateQueryIn 訊息傳送至伺服器。
-   等候接收 CPMCreateQueryOut 訊息 (請參閱3.2.5.1.1 一節中的詳細資料) ，以無訊息方式捨棄所有其他訊息。
-   報告回應的 [狀態] 欄位的值， \_ 如果成功，則會將資料指標控制碼的陣列和資訊性布林值 (指定在 2.2.3.9) 回到較高的層級。

### <a name="32423-sending-a-cpmsetbindingsin-request"></a>3.2.4.2.3 傳送 CPMSetBindingsIn 要求

一般來說， (當資料列已成功接收 CPMCreateQueryOut 之後，資料列中的每個資料行的系結將會被傳回，請參閱 3.2.5.1.1) 一節。 較高的預期會提供 CTableColumn 結構的陣列，如2.2.4.31 中所指定的 aColumns 欄位和有效的資料指標控制碼。

從較高的層接收此要求時，用戶端必須執行下列動作：

-   計算 aColumns 陣列中的 CTableColumn 結構數目，並將 cColumns 欄位設定為此值。
-   計算 cColumns 和 aColumns 欄位的總大小（以位元組為單位），並將 \_ cbBindingDesc 欄位設定為此值。
-   在 CPMSetBindingsIn 訊息中，將指定的欄位設定為較高的應用層所提供的值。 將 [ \_ ulChecksum] 欄位設定為 [3.2.5] 區段中所指定的計算值。
-   將已完成的 CPMSetBindignsIn 訊息傳送至伺服器。
-   等候接收來自伺服器的 CPMSetBindingsIn 訊息，並捨棄其他訊息。
-   從回應的 [狀態] 欄位中，指出 \_ 對較高層的狀態。

基於資訊的目的，較高層級通常會要求用戶端傳送 CPMGetRowsIn 訊息，但不會由內容編制索引服務通訊協定強制執行。

### <a name="32424-sending-a-cpmgetrowsin-request"></a>3.2.4.2.4 傳送 CPMGetRowsIn 要求

當較高的層級即將接收資料列資訊時，它會提供具有有效資料指標和章節控制碼的通訊協定用戶端，並提供適當的搜尋描述。 一般來說，當它有有效的資料指標和/或章節控制碼，且系結已設定了 CPMSetBindingsIn 訊息時，就會需要較高層級的層級。 若要存取章節中的資料列集，較高的層級是在先前的 CPMGetRowsOut 訊息中使用從伺服器收到的章節控制碼。

從較高的層接收此要求時，用戶端必須執行下列動作：

-   判斷要為 cbReadBuffer 欄位指定的不帶正負號的整數值 \_ 。 若要判斷此值，用戶端必須採用下列值的最大值：
-   -   C RowsToTransfer 欄位值的1000倍 \_ 。
    -   CbRowWidth 的值 \_ ，進位至最接近的512位元組倍數。
    -   將這兩個值的較高，最多可達16K 限制。
    -   在單一資料列大於16K 的情況下，伺服器無法將結果傳回此查詢。

在 ulClientBase 欄位的用戶端位址空間中，為可變大小的資料列資料指定用戶端基底 \_ 。

*Windows 行為：對於與32位伺服器通訊的32位用戶端，或與64位伺服器通訊的64位用戶端，此值會設定為應用程式進程中接收緩衝區的記憶體位址。這允許在用戶端應用程式進程中，以 CPMGetRowsOut 的資料欄欄位中收到的指標為正確的記憶體指標。否則，它會設定為0x00000000。*

-   計算 [搜尋描述] 的大小，並在 [cbSeek] 欄位中進行設定 \_ 。
-   設定 cbReserved (的值，此值會作為資料列的位移開始) \_ cbSeek plus 0x14 的值。
-   將2.2.3.15 中所指定的 CPMConnectIn 訊息傳送至伺服器。

### <a name="32425-sending-a-cpmfetchvaluein-request"></a>3.2.4.2.5 傳送 CPMFetchValueIn 要求

如果用戶端收到來自伺服器的 CPMGetRowsOut 回應，且資料行的 Status 欄位設定為 StatusDeferred (0x01) 這表示屬性值未包含在 CPMGetRowsOut 訊息的 Rows 欄位中。 在此情況下，較高層級通常會要求通訊協定用戶端透過 CPMFetchValueIn 訊息來取得值，並提供延遲屬性的 PropSpec 和 \_ wid 值（通訊協定用戶端必須在第一個 CPMFetchValueIn 訊息中使用）。

如果這是用戶端傳送的第一個 CPMFetchValueIn 訊息，要求指定的屬性，用戶端必須執行下列動作：

-   設定訊息中的所有欄位，如2.2.3.19 一節中所指定。
-   將 \_ cbSoFar 設定為0x00000000。
-   將接收的目前位元組設定為0。
-   將 CPMFetchValueIn 訊息傳送至伺服器。

### <a name="32426-sending-a-cpmfreecursorin-request"></a>3.2.4.2.6 傳送 CPMFreeCursorIn 要求

一旦較高層級不再使用搜尋查詢，它就可以要求用戶端傳送 CPMFreeCursorIn 訊息，以釋放伺服器上的資源。

收到此要求時，用戶端必須將2.2.3.28 中所指定的 CPMFreeCursorIn 訊息傳送至伺服器，其中包含上層所指定的控制碼。

### <a name="32427-sending-a-cpmdisconnect-message"></a>3.2.4.2.7 傳送 CPMDisconnect 訊息

如果較高層級的索引服務沒有其他查詢，則若要釋出更多伺服器資源，應用程式可能會要求用戶端將 CPMDisconnect 訊息傳送至伺服器。 收到此查詢時，用戶端必須直接以要求的方式傳送訊息。 伺服器不會回應此訊息。

### <a name="325-message-processing-and-sequencing-rules"></a>3.2.5 訊息處理和排序規則

當用戶端收到來自伺服器的訊息回應時，用戶端必須使用最後傳送的訊息，判斷從伺服器接收的訊息是否為用戶端所預期的訊息。 與 \_ [msg] 欄位不同的所有訊息都必須被忽略。

### <a name="3251-receiving-a-cpmcreatequeryout-response"></a>3.2.5.1 接收 CPMCreateQueryOut 回應

當用戶端收到來自伺服器的 CPMCreateQueryOut 訊息回應時，用戶端必須 \_ 傳回狀態 (，而且如果狀態成功) 資料指標控制碼值傳回至較高的層級，用戶端就必須傳回狀態。 任何進一步的動作都是最高的層級。

因為較高的層級知道查詢結構，所以一定會在 CPMCreateOueryOut 訊息中傳回正確的資料指標控制碼數目。 資料指標控制碼會以下列順序傳回：第一個控制碼是 unchaptered 資料列集，第二個控制碼是第一個章節的資料列集 (這是根據 CPMCreateQueryIn 訊息的 CategorizationSet 欄位中指定的第一個類別的結果群組。 ) 

基於資訊的目的，較高層級必須執行下列動作，但 CISP 用戶端並不會強制執行這些動作：

-   使用 CPMSetBindingsIn 來設定個別資料行的系結，並對查詢路徑執行任何後續的動作
-   使用 CPMGetQueryStatusIn 來檢查查詢的執行進度。
-   使用 CPMRatioFinishedIn 來要求查詢的完成百分比。

### <a name="3252-receiving-a-cpmgetrowsout-response"></a>3.2.5.2 接收 CPMGetRowsOut 回應

當用戶端收到來自伺服器的 CPMGetRowsOut 訊息回應時，用戶端必須執行下列動作：

-   檢查 \_ 標頭中的 [狀態] 欄位是否表示成功或失敗。
-   如果 \_ status 值為 status \_ 緩衝區 \_ 太 \_ 小 (0xC0000023) ，用戶端必須檢查最後一個訊息傳送狀態。 如果未包含 CPMGetRowsIn 訊息，則必須以無訊息方式忽略接收的訊息。 否則，用戶端必須將新的 CPMGetRowsIn 訊息傳送至伺服器，其中所有欄位都與儲存的欄位相同，不同之處在于 \_ CBREADBUFFER 必須增加 512 (但不能大於 0x4000) 。 如果 \_ 狀態 \_ 緩衝區 \_ 太 \_ 小 (0XC0000023) ，而且最後傳送的訊息已 \_ cbReadBuffer 等於0X4000 用戶端，則必須將錯誤回報到較高的層級。
-   如果 \_ 狀態值為任何其他錯誤值，用戶端必須指出最高層級的失敗。
-   如果 \_ 狀態值表示成功，則結果必須指出最高的層級要求資訊，而進一步的動作則是最高的層級。

基於資訊的目的，較高層級通常會執行下列動作，但內容索引服務通訊協定用戶端不會強制執行這些動作：

-   如果資料列中的值代表檔識別碼、章節或書簽控點，則較高層通常會儲存它們，以便在牽涉到有效檔識別碼、章節或書簽控制碼的後續作業中使用。
-   較高的圖層通常會儲存或顯示資料，或以其他方式使用資料行值。
-   針對標示為 [延後] 較高層的值，將會使用 CPMFetchValueIn 訊息來提取值。
-   搜尋描述也會傳回至較高的層級，而且可以由較高的圖層重複使用或檢查。

基於資訊的目的，如果較高層要求的控制碼是在資料列中收到的章節和書簽，則可能會執行下列動作：

-   使用 CPMGetQueryStatusExIn 來檢查查詢的執行進度，以及其他狀態資訊，例如已篩選的檔數目、要篩選的檔、查詢所處理的檔比例、查詢中的資料列總數，以及書簽在資料列集中的位置。
-   使用 CPMGetNotify 來要求伺服器通知資料列集變更的用戶端。
-   使用 CPMGetApproximatePositionIn，在章節中要求書簽的大概位置。
-   使用 CPMCompareBmkIn 來要求一章中兩個書簽的比較。
-   使用 CPMRestartPositionIn 將資料指標的位置變更為資料列集的開頭。

### <a name="3253-receiving-a-cpmfetchvalueout-response"></a>3.2.5.3 接收 CPMFetchValueOut 回應

當用戶端收到來自伺服器的 CPMGetRowsOut 訊息回應時，用戶端必須執行下列動作：

-   檢查 \_ 標頭中的 [狀態] 欄位是否表示成功或失敗。 在失敗案例中，請通知較高的層級。 否則，請繼續下一節。
-   檢查 \_ fValueExist，如果設定為0x00000000，則會通知較高的圖層，指出找不到此值。
-   否則 \_ ，請將 cbValue 的位元組從 vValue 附加至目前的屬性值。
-   如果 \_ \_ fMoreExists 設定為0x00000001，然後將 \_ cbValue 所接收的目前位元組遞增， \_ 並將 CPMFetchValueIn 訊息傳送至伺服器，請將 \_ cbSoFar 設定為目前接收的位元組值， \_ cbPropSpec 為零，而 \_ cbChunk 為較高層所需的緩衝區大小。
-   如果 \_ fMoreExists 設定為0x00000000，則會將目前屬性值的屬性值指定為較高的層級。

### <a name="3254-receiving-a-cpmfreecursorout-response"></a>3.2.5.4 接收 CPMFreeCursorOut 回應

當用戶端從伺服器收到成功的 CPMFreeCursorOut 訊息回應時，用戶端必須將 \_ cCursorsRemaining 值傳回至較高的層級。

下列資訊僅供參考之用，不會由 CISP 用戶端強制執行。 較高的層級預期會追蹤資料指標控制碼，而不是使用已釋放的資料指標。 一旦 cCursorsRemaining 的數目 \_ 等於0x00000000，較高的層級就可以使用此連接來指定另一個查詢 (使用 CPMCreateQueryIn 訊息) 。

### <a name="326-timer-events"></a>3.2.6 計時器事件

無。

### <a name="327-other-local-events"></a>3.2.7 其他本機事件

無。

## <a name="4-protocol-examples"></a>4 通訊協定範例

-   [4.1 範例1](#41-example-1)
-   [4.2 範例2](#42-example-2)

### <a name="41-example-1"></a>4.1 範例1

在下列範例中，我們假設電腦 A 上的使用者 JOHN 想要從儲存在伺服器 X 上的檔集的目錄系統中，取得包含 "Microsoft" 這個字的檔案大小。 讓我們假設電腦 A 正在執行32位的 Windows XP 作業系統，而電腦 X 正在執行32位的 Windows Server 2003 作業系統。

1.  使用者啟動搜尋應用程式，並輸入搜尋查詢。 接著，應用程式會將搜尋查詢傳遞給通訊協定用戶端。
2.  通訊協定用戶端建立與索引伺服器 X 的連接。通訊協定用戶端使用具名管道 \\ 管道 \\ CI \_ SKADS，透過 SMB 連線到伺服器 X。
3.  然後，通訊協定用戶端會使用下列值來準備 CPMConnectIn 訊息：

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000C8，表示這是 CPMConnectIn 訊息。
    -   **\_ 狀態** 設定為0x00000000。
    -   **\_ ulChecksum** 包含總和檢查碼，依3.2.4 區段中的指定進行計算。
    -   **\_ ulReserved2** 設定為0x00000000。

    訊息本文的填入方式如下：

    -   **\_ iClientVersion** 設定為0x00000008，表示伺服器要驗證總和檢查碼欄位。
    -   **\_ fClientIsRemote** 設定為0x00000001，表示伺服器是遠端伺服器。
    -   **\_ cbBlob1** 會設定為結合 cPropSet、PropertySet1 和 PropertySet2 欄位的大小（以位元組為單位）。
    -   **\_ cbBlob2** 設定為 0x00000004 (表示沒有任何額外的屬性集) 。
    -   **MachineName** 設定為。
    -   **UserName** 設定為 JOHN。
    -   **cPropSets** 設定為0x00000002。
    -   **PropertySet1** 欄位的類型為 CDbPropSet。 組成 PropertySet1 欄位的 CDbPropSet 結構會填入如下：
        -   **GuidPropSet** 欄位設定為 A9BD1526-6A80-11D0-8C9D-0020AF1D740E (DBPROPSET \_ FSCIFRMWRK \_ EXT) 。
        -   **cProperties** 欄位設定為0x00000004。
        -   **aProps** 欄位是 CDbProp 結構的陣列。

            針對 **aProps \[ 0 \]** 元素：

            -   **PropId** 會設定為 0X00000002 (DBPROP \_ CI \_ 類別目錄 \_ 名稱) 。
            -   **DBPROPOPTIONS** 設定為0x0000000。
            -   **DBPROPSTATUS** 設定為0x00000000。
            -   針對 **ColId** 元素：
                -   **eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 
                -   **GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。
                -   **ulID** 設定為0x00000000。
            -   針對 **vValue** 元素：
                -   **vType** 設定為 0X001F (VT \_ LPWSTR) 。
                -   **vValue** 會設定為 "SYSTEM"，也就是所需的目錄名稱。

            針對 **aProps \[ 1 \]** 元素：

            -   **PropId** 設定為 0X00000007 (DBPROP \_ CI \_ 查詢 \_ 類型) 
            -   **DBPROPOPTIONS** 設定為0x0000000。
            -   **DBPROPSTATUS** 是設定為 to0x00000000。
            -   針對 **ColId** 元素：
                -   **eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。
                -   **GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。
                -   **ulID** 設定為0x00000000。
            -   針對 **vValue** 元素：
                -   **vType** 設定為 0X0003 (VT \_ I4) 。
                -   **vValue** 會設定為 0X00000000 (CiNormal) ，這表示它是一般查詢。

            針對 **aProps \[ 2 \]** 元素：

            -   **PropId** 會設定為 0X00000004 (DBPROP \_ CI \_ 範圍 \_ 旗標) 。
            -   **DBPROPOPTIONS** 設定為0x0000000。
            -   **DBPROPSTATUS** 設定為0x00000000。
            -   針對 **ColId** 元素：
                -   **eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。
                -   **GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。
                -   **ulID** 設定為0x00000000。
            -   針對 **vValue** 元素：
                -   **vType**： 0X1003 (VT \_ 向量 \| VT \_ I4) 
                -   **vValue**： 0x00000001/0x00000001 (一個具有值 1) 的元素，這表示搜尋子資料夾

            針對 **aProps \[ 3 \]** 元素：

            -   **PropId**： 0X00000003 (DBPROP \_ CI \_ 包含 \_ 範圍) 
            -   **DBPROPOPTIONS**：0x0000000
            -   **DBPROPSTATUS**：0x00000000
            -   針對 **ColId** 元素：
                -   **eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) 。
                -   **GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。
                -   **ulID** 設定為0x00000000
            -   針對 **vValue** 元素：
                -   **vType** 設定為 0X101F (VT \_ VECTOR \| vt \_ LPWSTR) 。
                -   **vValue** 設定為 0x00000001/0x00000002/" \\ " (一個元素，其中有2個字元的 null 終止字串) ，亦即根範圍。

    -   **PropertySet2** 欄位的類型為 CDbPropSet。

        組成 PropertySet1 欄位的 CDbPropSet 結構會填入如下：

        -   **GuidPropSet** 設定為 AFAFACA5-B5D1-11D0-8C62-00C04FC2DB8D (DBPROPSET \_ CIFRMWRKCORE \_ EXT) 。
        -   **cProperties** 欄位設定為0x00000001。
        -   **AProps** 欄位是 CDbProp 結構的陣列。

            針對 **aProps \[ 0 \]** 元素：

            -   **PropId** 會設定為 0X00000002 (DBPROP \_ 機) 。
            -   **DBPROPOPTIONS** 設定為0x0000000。
            -   **DBPROPSTATUS** 設定為0x00000000。
            -   針對 **ColId** 元素：
                -   **eKind** 設定為 0X00000001 (DBKIND \_ GUID \_ PROPID) ，
                -   **GUID** 為 null (所有零) ，這表示此值會套用至查詢，而不只是單一資料行。
                -   **ulID** 設定為0x00000000。
            -   針對 **vValue** 元素：
                -   **vType**： 0X0008 (VT \_ BSTR) 
                -   **vValue**： 0x04/"X" (4 個位元組/以 null 結束的 Unicode 字串) ，表示 "X"-伺服器的名稱。

    -   **cExtPropSet** 欄位設定為0x00000000。
    -   **aPropertySets** 陣列不存在。
    -   視需要填入各種填補欄位。 訊息會傳送至伺服器。

4.  伺服器會驗證 **\_ ulChecksum** 是否正確、確認使用者已獲授權提出此要求，並以 CPMConnectOut 訊息回應。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000C8，表示這是 CPMConnectOut 訊息。
    -   **\_ 狀態** 會設為0X0000000，表示成功。
    -   **\_ ulChecksum** 設定為0。
    -   **\_ ulReserved2** 設定為0x00000000。

    訊息本文的填入方式如下：

    -   **\_ serverVersion** 欄位設定為 0x00000007 (32 位 windows XP 或32位 windows Server 2003) 。
    -   **\_ 保留** 的欄位會填入任意資料。

5.  用戶端會準備 CPMCreateQueryIn 訊息。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000CA，表示這是 CPMCreateQueryIn 訊息。
    -   **\_ 狀態** 設定為0x00000000。
    -   **\_ ulChecksum** 包含總和檢查碼，根據3.2.5 計算。
    -   **\_ ulReserved2** 設定為0x00000000。

    訊息本文的填入方式如下：

    -   [**大小**] 欄位設定為訊息其餘部分的大小。
    -   **CColumnSetPresent** 欄位設定為0x01。
    -   **ColumnSet** 欄位的類型為 CColumnSet。 組成此欄位的 CColumnSet 結構設定如下：
        -   **\_ count** 欄位設定為0x00000001，表示傳回一個資料行。
        -   **索引** 陣列是0x00000000，表示 aPropSpec 中的第一個專案 \_ 。
    -   **CRestrictionPresent** 欄位設定為0x01，表示 **限制** 欄位存在。
    -   **限制** 欄位的類型為 CRestriction，且設定為：
        -   **\_ ulType** 設定為 0x00000004 (RTContent) 。
        -   **\_ 權數** 設定為0x00000000。
    -   欄位的其餘部分包含 CContentRestriction 結構：
        -   PRSPEC 的屬性設定為 GUID B725F130-47EF-101A-A5F1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13，代表檔主體。
        -   **\_ Cc** 設為0x00000009。
        -   **\_ pwcsphrase** 會設定為字串 "Microsoft"。
        -   針對英文) ， **\_ lcid** 設定為 0x409 (。
        -   **\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。
    -   **CSortPresent** 設定為0x00。
    -   **CCategorizationSetPresent** 設定為0x00。
    -   **RowSetProperties** 的設定如下：
        -   **\_ uBooleanOptions** 會設定為 0x00000001 (順序) 。
        -   **\_ ulMaxOpenRows** 設定為0x00000000。
        -   **\_ ulMemoryUsage** 設定為0x00000000。
        -   \_**cMaxResults** 設定為 0x00000100 (最多傳回256個數據列) 。
        -   **\_ cCmdTimeOut** 設定為 0x00000000 (不會) 超時。
    -   **PidMapper** 設定為：
        -   **\_ count** 設定為0x00000001。
        -   **\_ aPropSpec** 設定為 02608C9EEBAC \_ 的 GUID B725F130-47EF-101A-A5-F1-PRSPEC/0x00000001 (PROPID) /0x0000000c，代表 Windows 檔案大小屬性。

6.  伺服器會處理它，並以 CPMCreateQueryOut 訊息回應。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000CA，表示這是 CPMCreateQueryOut 訊息。
    -   **\_ 狀態** 設定為 [成功]。
    -   **\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。
    -   **\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。

    訊息本文的填入方式如下：

    -   **\_ fTrueSeqeuntial** 設定為0x00000000，表示查詢可以使用索引。
    -   **\_ fWorkIdUnique** 設定為0x00000001。
    -   **ACursors** 陣列只包含一個元素，代表這個查詢的資料指標控制碼。 此值取決於伺服器的狀態。 讓我們假設傳回的值為0xAAAAAAAA。

7.  用戶端發出 CPMSetBindingsIn 要求訊息來定義資料列的格式。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000D0，表示這是 CPMSetBindingsIn 訊息。
    -   **\_ 狀態** 設定為 [成功]。
    -   **\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。
    -   **\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。

    訊息本文的填入方式如下：

    -   **\_ hCursor** 設定為0xAAAAAAAA。
    -   **\_ cbRow** 設定為 0x10 (夠大，足以容納) 的資料行。
    -   **\_ cbBindingDesc** 會設定為結合的 **\_ cColumns** 和 **\_ aColumns** 欄位大小。
    -   **\_ cColumns** 設定為0x00000001。
    -   **\_ aColumns** 陣列設定為包含一個 CTableColumn 結構，其中包含：
    -   -   **\_ PropSpec** 設定為 02608c9eebac \_ 的 GUID b725f130-47ef-101a-a5-f1-PRSPEC/0x00000001 (PROPID) /0x0000000c，代表 Windows 檔案大小屬性。
        -   **\_ vType** 設定為 0x0015 (VT \_UI8) 。
        -   **\_ ValueUsed** 會設定為在資料列) 中傳輸的 0x01 (資料行。
        -   **\_ ValueOffset** 會在資料列) 的開頭設定為 0x0002 (。
        -   **\_ ValueSize** 設定為 0x08 (VT \_ 的大小UI8) 。
        -   **\_ StatusUsed** 設定為0x01。
        -   **\_ StatusOffset** 設定為0x0A。
        -   **\_ LengthUsed** 設定為0x00。

8.  伺服器會處理它，並以 CPMSetBindingsIn 訊息回應。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000D0。
    -   **\_ 狀態** 設定為 [成功]。
    -   **\_ ulChecksum** 設定為 0x00000000 (或任何其他任意值) 。
    -   **\_ ulReserved2** 設定為 0x00000000 (或任何其他任意值) 。

9.  用戶端發出 CPMGetRowsIn 要求訊息。 讓我們假設用戶端已準備好接受100個數據列，而且想要以遞增的順序進行。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000CC，表示這是 CPMGetRowsIn 訊息。
    -   **\_ 狀態** 設定為0x00000000
    -   **\_ ulChecksum** 包含總和檢查碼，依區段0計算。
    -   **\_ ulReserved2** 設定為0x00000000。

    訊息本文的填入方式如下：

    -   **\_ hCursor** 設定為0xAAAAAAAA。
    -   **\_ cRowsToTransfer** 設定為0x00000064。
    -   從) 的系結中， **\_ cRowWidth** 設為 0x00000010 (。
    -   **\_ cbSeek** 會設定為0x14，也就是結合 eType、 \_ chapt 和 CRowSeekNext 欄位的大小。
    -   **\_ cbReserved** 設定為 0x18 (0x14 plus \_ cbSeek) 。
    -   **\_ cbReadBuffer** 設定為 0x800 (0x64 \* 0x10 進位到下一個 0x200) 的倍數。
    -   **\_ ulClientBase** 設定為0x00000000。
    -   **\_ fBwdfetch** 設定為0x00000000，表示資料列會以正向順序提取。
    -   **eType** 設定為0x0000001，表示用戶端需要下一個資料列。
    -   **\_ chapt** 設定為 0 (不是) 的章節化結果。
    -   **SeekDescription** 設定為 CRowSeekNext。 CRowSeekNext 結構包含下列值：
        -   **CiTblChapt** 設定為0x00000000。
        -   **\_ hRegion** 設定為0x00000000。
        -   **\_ cSkip** 設定為0，表示用戶端不想略過資料列。

10. 伺服器會處理它，並以 CPMGetRowsOut 訊息回應。 讓我們假設伺服器找到的100檔中包含 "Microsoft" 這個字。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000CC，表示這是 CPMGetRowsOut 訊息。
    -   **\_ 狀態** 設定為 [成功]。
    -   **\_ ulChecksum** 設定為0x00000000。
    -   **\_ ulReserved2** 設定為0x00000000。

    訊息本文的填入方式如下：

    -   **\_ CRowsReturned** 設定為0x00000064。
    -   **eType** 設定為0x00000001。
    -   **\_ chapt** 設定為 0x00000000 (不是) 的章節化結果。
    -   **SeekDescription** 包含 CRowSeekNext 結構，如下所示：
        -   **CiTblChapt** 設定為0x00000000。
        -   **\_ hRegion** 設定為0x00000000。
        -   **\_ cSkip** 設定為0，表示用戶端不想略過資料列。
    -   資料 **列** 包含100檔的大小，其中包含 "Microsoft" 這個字。 由於這是固定大小的資料，因此它只會以100、8位元組不帶正負號的整數的清單結構化。

11. 用戶端會傳送 CPMDisconnect 訊息來結束連接。

    訊息標頭的填入方式如下：

    -   **\_ msg** 設定為0x000000C9，表示這是 CPMDisconnect 訊息。
    -   **\_ 狀態** 設定為0x00000000。
    -   **\_ ulChecksum** 設定為0x00000000。

12. 伺服器會處理訊息，並移除所有的用戶端狀態。

### <a name="42-example-2"></a>4.2 範例2

在上述範例中，查詢相當簡單。 現在讓我們考慮稍微複雜一點的查詢。 讓我們假設使用者想要取出包含下列兩個字的檔案大小： "Microsoft" 和 "Office"。 這是藉由變更在步驟5中傳送的 CPMCreateQueryIn 訊息所包含的限制欄位來指定，如下所示：

**限制** 欄位的類型為 CRestriction，且設定為：

-   -   **\_ ulType** 設定為 0x00000004 (RTAnd) 。
    -   **\_ 權數** 設定為0x00000000。

欄位的其餘部分包含 CNodeRestriction 結構：

-   -   **\_ cNode** 設定為0X00000002，表示 paNode 陣列中有兩個節點。
    -   **\_ PaNode** 欄位是兩個 CRestriction 結構的陣列。

        **\_ paNode \[ 0 \]** 包含：

        -   -   **\_ ulType** 設定為 0x00000004 (RTContent) 。
            -   **\_ 權數** 設定為0x00000000。
            -   欄位的其餘部分包含 CContentRestriction 結構：
                -   PRSPEC 的屬性設定為 GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13。
                -   **\_ Cc** 設為0x00000009。
                -   **\_ pwcsphrase** 會設定為字串 "Microsoft"。
                -   針對英文) ， **\_ lcid** 設定為 0x409 (。
                -   **\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。

        **\_ paNode \[ 1 \]** 包含：

        -   -   **\_ ulType** 設定為 0x00000004 (RTContent) 。
            -   **\_ 權數** 設定為0x00000000。
            -   欄位的其餘部分包含 CContentRestriction 結構：
                -   PRSPEC 的屬性設定為 GUID b725f130-47ef-101a-a5f1-02608c9eebac/0x00000001 (**\_** \_PROPID) /0x13。
                -   **\_ Cc** 設為0x00000006。
                -   **\_ pwcsphrase** 會設定為 "Office" 字串。
                -   針對英文) ， **\_ lcid** 設定為 0x409 (。
                -   **\_ ulGenerateMethod** 設定為 0x00000000 (完全相符) 。

## <a name="5-security"></a>5 安全性

### <a name="51-security-considerations-for-implementers"></a>5.1 實作者的安全性考量

索引安全內容的索引編制可考慮使用 SMB Ms-chap 提供的使用者內容 \[ \] 來修剪搜尋結果，並且只傳回呼叫者可存取的內容。

### <a name="52-index-of-security-parameters"></a>5.2 安全性參數的索引



| 安全性參數  | 區段 |
|---------------------|---------|
| 模擬等級 | 2.1     |



 

## <a name="6-index-of-version-specific-behavior"></a>6個版本特定行為的索引



| 版本特定行為                                                                         | 區段   | Windows 2000 | Windows XP | Windows Server 2003 |
|---------------------------------------------------------------------------------------------------|-----------|--------------|------------|---------------------|
| 此通訊協定是在 Windows 2000、Windows XP、Windows Server 2003 和 Windows Vista 上執行。 | 1.3.2     | X            | X          | X                   |
| 應用程式通常會與 OLE DB 介面包裝函式互動                                  | 1.4       | X            | X          | X                   |
| NTSTATUS 值                                                                                   | 1.8       | X            | X          | X                   |
| 用戶端會 \_ 在每個訊息標頭中設定 [狀態] 欄位。                                        | 2.2.2     | X            | X          | X                   |
| cPendingScans 值通常是零                                                               | 2.2.3.1   | X            | X          | X                   |
| iClientVersion 值                                                                              | 2.2.3.6   | X            | X          | X                   |
| \_cbChunk 值                                                                                   | 2.2.3.19  | X            | X          | X                   |
| 32位和64位的記憶體位址                                                                | 3.2.4.2.4 | X            | X          | X                   |



 

 

 





