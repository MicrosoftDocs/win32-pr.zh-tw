---
title: 使用 DirSync 控制項輪詢變更
description: Active Directory 目錄同步作業 (DirSync) control 是一種 LDAP 伺服器延伸，可讓應用程式在目錄磁碟分割中搜尋自從先前狀態以來已變更的物件。
ms.assetid: f77caeb3-bfc9-4ae6-8d1d-73f4ee554336
ms.tgt_platform: multiple
keywords:
- 使用 DirSync Control AD 輪詢變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b95e9fed93a962ef95e8cdbe08c202bd8e46df21959d9e1fcabe8eac033b6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185405"
---
# <a name="polling-for-changes-using-the-dirsync-control"></a>使用 DirSync 控制項輪詢變更

Active Directory 目錄同步作業 (DirSync) control 是一種 LDAP 伺服器延伸，可讓應用程式在目錄磁碟分割中搜尋自從先前狀態以來已變更的物件。

使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)時，藉由指定 **ADS \_ SEARCHPREF \_ dirsync** 搜尋喜好設定，在 ADSI 中使用 dirsync 控制項。 如需詳細資訊和程式碼範例，請參閱 [使用 ADS \_ SEARCHPREF \_ DIRSYNC 的範例程式碼](example-code-using-ads-searchpref-dirsync.md)。 您也可以使用 LDAP API 來執行 DirSync 搜尋。 以下描述 ADSI 的執行，其中大部分也適用于直接使用 LDAP，但本主題結尾所討論的除外。

當您執行 DirSync 搜尋時，會將提供者特定的資料元素傳入 (cookie) ，以識別先前的 DirSync 搜尋時的目錄狀態。 在第一次搜尋時，您會傳入 null cookie，且搜尋會傳回符合篩選準則的所有物件。 搜尋也會傳回有效的 cookie。 將 cookie 儲存在與 Active Directory 伺服器同步處理的相同儲存體中。 在後續的搜尋中，從儲存體取得 cookie，並將其傳遞至搜尋要求。 搜尋結果現在只會包含在 cookie 所識別的先前狀態之後變更的物件和屬性。 搜尋也會傳回新的 cookie 來儲存，以供下一個搜尋之用。

下表列出用戶端搜尋要求可以指定的搜尋參數。



| 參數          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 搜尋的基底 | DirSync 搜尋的基底必須是目錄分割的根目錄（可以是網域磁碟分割、設定磁碟分割或架構磁碟分割）。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 範圍              | DirSync 搜尋的範圍必須是 **ADS \_ 範圍 \_ 子樹**，也就是資料分割的整個子樹。 請注意，若要搜尋網域分割區，子樹包含設定和架構分割區的標頭，但不包含內容。 若要輪詢較小範圍中的變更，請使用 **USNChanged** 技術，而不是 DirSync。                                                                                                                                                                                                                                                                                                                                                                                 |
| 篩選             | 您可以指定任何有效的搜尋篩選準則。 對於具有 null cookie 的初始搜尋，結果會包含符合篩選準則的所有物件。 針對使用有效 cookie 的後續搜尋，搜尋結果只會包含符合篩選準則的物件資料，並在 cookie 所指示的狀態之後變更。 如需搜尋篩選準則的詳細資訊，請參閱 [建立查詢篩選器](creating-a-query-filter.md)。                                                                                                                                                                                                                                                                                                                |
| 屬性         | 您可以指定在發生變更時要傳回的屬性清單。 針對每個物件，初始結果會包含在物件上設定的所有要求屬性。 後續搜尋結果只會包含已變更的指定屬性。 未變更的屬性不會包含在搜尋結果中。 在 ADSI 的執行中，搜尋結果一律包含每個物件的 **objectGUID** 和 **instanceType** 。 此外，指定的屬性清單也可做為額外的篩選：初始搜尋結果只會包含至少有一個指定屬性集的物件。後續的搜尋只會包含一或多個屬性已變更 (值) 新增或刪除的物件。 |



 

此外，請注意：

-   針對漸進式搜尋，最佳做法是系結至先前搜尋中使用的相同網域控制站 (DC) ，也就是產生 cookie 的 DC。 如果無法使用相同的 DC，請等候它，或系結至新的 DC，然後執行完整的同步處理。 使用 cookie 在次要儲存體中儲存 DC 的 DNS 名稱。

    您可以將一個 DC 所產生的 cookie 傳遞給裝載相同目錄分割複本的不同 DC。 用戶端不可能會在另一個 DC 上使用某個 DC 的 cookie 來遺漏變更。 不過，來自新 DC 的搜尋結果可能會包含舊 DC 所報告的變更;在某些情況下，新的 DC 可能會傳回所有物件和屬性，就像完整的同步處理一樣。 用戶端應該只讓其資料庫與針對任何指定 DirSync 呼叫所報告的搜尋結果保持一致，也就是處理所有增量結果，就好像它們是最新的狀態一樣。 無論您是否已經看到先前的變更，或甚至回到先前的狀態，因為重複的累加式同步處理將會一致。

-   當物件重新命名或移動時，其子物件（如果有的話）不會包含在搜尋結果中，即使子物件的辨別名稱已變更也一樣。 同樣地，當物件安全性描述項中的可繼承 ACE 遭到修改時，該物件的子物件不會包含在搜尋結果中，即使子物件的安全性描述項已經變更也一樣。
-   使用 **objectGUID** 屬性來識別追蹤的物件。 無論在樹系中移動物件的位置為何，每個物件的 **objectGUID** 都會保持不變。
-   請注意，DirSync 搜尋的搜尋結果會指出搜尋時目錄分割複本上的物件狀態。 這表示，如果在其他 Dc 上所做的變更尚未複寫到目標 DC，將不會包含這些變更。 這也表示物件的屬性可能會在先前的 DirSync 搜尋之後變更數次，但是搜尋只會顯示最後的狀態，而不會顯示變更的順序。
-   在 ADSI 的執行中，應用程式必須將 cookie 處理為不透明，而不會對其內部組織或值做出任何假設。
-   請注意，用戶端會將 DC 的 cookie、cookie 長度和 DNS 名稱儲存在包含已同步處理物件資料的相同儲存體中。 這可確保當儲存體從備份還原時，cookie 和其他參數會保持與物件資料同步。
-   若要取出針對 DirSync 控制項所建立的 [**parentGUID**](/windows/desktop/ADSchema/a-parentguid) 屬性，也需要要求 [**name**](/windows/desktop/ADSchema/a-name) 屬性。

若要使用 DirSync 控制項，呼叫端必須在受監視的磁碟分割根目錄上指派「目錄取得變更」許可權。 依預設，此許可權會指派給網域控制站上的系統管理員和 LocalSystem 帳戶。 呼叫端也必須具有「 [**DS-複寫-取得-變更**](/windows/desktop/ADSchema/r-ds-replication-get-changes) 」擴充控制許可權。 如需針對必須在沒有此許可權的帳戶下執行的應用程式，執行變更追蹤機制的詳細資訊，請參閱 [使用 USNChanged 輪詢變更](polling-for-changes-using-usnchanged.md)。 如需有關許可權的詳細資訊，請參閱 [許可權](/windows/desktop/SecAuthZ/privileges)。

## <a name="retrieving-deleted-objects-with-a-dirsync-search"></a>使用 DirSync 搜尋來抓取已刪除的物件

**ADS \_ SEARCHPREF \_ DIRSYNC** 搜尋結果會自動將已刪除的物件包含 (的標記) 符合指定的搜尋篩選準則。 但是，當物件存留時，將符合該物件的搜尋篩選可能不會在物件被刪除後與物件相符。 這是因為只會在原始物件上保留一組存在的屬性子集。 例如，您通常會針對使用者物件使用下列篩選。


```C++
(&(objectClass=user)(objectCategory=person))
```



刪除物件時，會移除 **objectCategory** 屬性，因此上述篩選不會符合任何標記物件。 相反地， **objectClass** 屬性會保留在標記物件上，因此 " (objectclass = user) " 的篩選準則會符合已刪除的使用者物件。

您使用 DirSync 搜尋指定的屬性清單也可做為篩選準則;搜尋結果只會包含一或多個指定的屬性在上一次 DirSync 搜尋之後已經變更的物件。 如果屬性清單未包含任何在標記時保留的屬性，搜尋結果就不會包含標記。 若要處理這個情況，請指定 null 屬性清單來要求所有屬性;或者，您可以要求 **isDeleted** 屬性，在所有的標記上設定為 **TRUE** 。 標記屬性在 **attributeSchema** 定義的 **searchFlags** 屬性中設定了0x8 位。

如需詳細資訊，請參閱 [取出已刪除的物件](retrieving-deleted-objects.md)。

## <a name="ldap-implementation-of-the-dirsync-control"></a>DirSync 控制項的 LDAP 執行

您也可以使用 LDAP API 搭配 [ldap \_ 伺服器 \_ dirsync \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-dirsync-oid) 控制項來執行 DirSync 搜尋。 如果您使用 LDAP API，也請指定 [ldap \_ 伺服器 \_ 擴充 \_ DN \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-extended-dn-oid) ，而 [ldap \_ 伺服器會 \_ 顯示 \_ 已刪除的 \_ OID](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) 控制項。 LDAP \_ 伺服器 \_ 擴充的 \_ DN \_ OID 控制項會使 ldap 搜尋傳回包含安全性主體物件（例如使用者、群組和電腦）之 **objectGUID** 和 **objectSID** 的辨別名稱的擴充形式。 LDAP \_ 伺服器 \_ 顯示 \_ 已刪除的 \_ OID 控制項會導致搜尋結果包含已刪除物件的資料。 請注意，這些控制項會自動包含在 ADSI 的執行中。

 

 