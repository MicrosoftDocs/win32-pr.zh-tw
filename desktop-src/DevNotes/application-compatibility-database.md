---
description: 相容性基礎結構會使用資料庫來識別應用程式相容性問題及其解決方案。
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: 應用程式相容性資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787e8dbc9aa07bc8d466dae766c3fed406692dbd32e128123c4b37d9a7a5618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956157"
---
# <a name="application-compatibility-database"></a>應用程式相容性資料庫

相容性基礎結構會使用資料庫來識別應用程式相容性問題及其解決方案。 此資料庫是具有 sdb 副檔名的索引二進位檔案。 相容性基礎結構提供用來存取資料庫的程式設計介面。

您可以在執行時間依應用程式來解決相容性問題。 資料庫中指定的每個應用程式都包含一或多個需要解決方案的元件。 元件是一般使用其檔案屬性描述的可執行檔 (例如，總和檢查碼) 。

資料庫查閱和決定每個應用程式之解決方案的程式，都稱為 *符合*。 檔案屬性以及包含 .exe 檔案的資料夾或子資料夾中有相關聯的檔案，可以用來建立唯一的相符項。 相關聯的檔案稱為 *相符* 的檔案。

*標記* 是資料庫中專案和屬性的唯一識別碼。 *標記類型* 表示與 [**標記**](tag.md)相關聯的資料格式。 例如， **標記 \_ 名稱** 的類型為 **tag \_ 類型 \_ STRINGREF**; 標籤 **\_ 名稱** 的資料是名稱字串。 *TAGID* 是特定資料庫中專案的指標。 *TAGREF* 是可跨多個資料庫使用之專案的指標。

*檔案屬性* 是與磁片上的檔案相關聯的中繼資料。 這些屬性包括檔案名、檔案大小、總和檢查碼、版本和日期。 這些屬性是用來判斷系統載入的檔案是否符合資料庫專案。 因此，這些檔案屬性也稱為 *相符的屬性*。

## <a name="solutions"></a>方案

套用至應用程式元件的最常見方案是 Apphelp 和 Appfix。

使用 Apphelp 時，會顯示自訂當地語系化訊息通知，通常是在安裝或啟動應用程式時。 其中包含簡短的文字，說明相容性問題，並提供可讓您繼續執行應用程式的選項。 不過，有些應用程式會大幅失敗，而無法執行;Apphelp 不會提供使用者繼續執行這些應用程式的選項。

使用 Appfix 時，會為應用程式的元件所呼叫的 Api 安裝勾點。 這些勾點指向可以呼叫的存根函式，而不是系統函數 (也稱為 *填充碼銜接*) 。 存根函式會執行必要的作業，讓應用程式能夠在安裝的 Windows 版本上執行。 每個存根函式在完成其工作之後，可以選擇性地呼叫系統函數。 *相容性層* 或 *模式* 包含一或多個填充碼和旗標。

## <a name="in-this-section"></a>本節內容

-   [**APPHELP \_ 資料**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**尋找 \_ 資訊**](find-info.md)
-   [**INDEXID**](indexid.md)
-   [**路徑 \_ 類型**](path-type.md)
-   [**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
-   [**SdbCloseDatabase**](sdbclosedatabase.md)
-   [**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
-   [**SdbCommitIndexes**](sdbcommitindexes.md)
-   [**SdbCreateDatabase**](sdbcreatedatabase.md)
-   [**SdbDeclareIndex**](sdbdeclareindex.md)
-   [**SdbEndWriteListTag**](sdbendwritelisttag.md)
-   [**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
-   [**SdbFindFirstTag**](sdbfindfirsttag.md)
-   [**SdbFindNextTag**](sdbfindnexttag.md)
-   [**SdbFormatAttribute**](sdbformatattribute.md)
-   [**SdbFreeFileAttributes**](sdbfreefileattributes.md)
-   [**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
-   [**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
-   [**SdbGetFileAttributes**](sdbgetfileattributes.md)
-   [**SdbGetFirstChild**](sdbgetfirstchild.md)
-   [**SdbGetIndex**](sdbgetindex.md)
-   [**SdbGetMatchingExe**](sdbgetmatchingexe.md)
-   [**SdbGetNextChild**](sdbgetnextchild.md)
-   [**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
-   [**SdbGetTagFromTagID**](sdbgettagfromtagid.md)
-   [**SdbInitDatabase**](sdbinitdatabase.md)
-   [**SdbIsStandardDatabase**](sdbisstandarddatabase.md)
-   [**SdbMakeIndexKeyFromString**](sdbmakeindexkeyfromstring.md)
-   [**SdbOpenApphelpDetailsDatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**SdbOpenApphelpResourceFile**](sdbopenapphelpresourcefile.md)
-   [**SdbOpenDatabase**](sdbopendatabase.md)
-   [**SdbQueryDataExTagID**](sdbquerydataextagid.md)
-   [**SDBQUERYRESULT**](sdbqueryresult.md)
-   [**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
-   [**SdbReadBinaryTag**](sdbreadbinarytag.md)
-   [**SdbReadDWORDTag**](sdbreaddwordtag.md)
-   [**SdbReadQWORDTag**](sdbreadqwordtag.md)
-   [**SdbReadStringTag**](sdbreadstringtag.md)
-   [**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
-   [**SdbReleaseDatabase**](sdbreleasedatabase.md)
-   [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
-   [**SdbStartIndexing**](sdbstartindexing.md)
-   [**SdbStopIndexing**](sdbstopindexing.md)
-   [**SdbTagRefToTagID**](sdbtagreftotagid.md)
-   [**SdbTagToString**](sdbtagtostring.md)
-   [**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
-   [**SdbWriteBinaryTag**](sdbwritebinarytag.md)
-   [**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
-   [**SdbWriteDWORDTag**](sdbwritedwordtag.md)
-   [**SdbWriteNullTag**](sdbwritenulltag.md)
-   [**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
-   [**SdbWriteStringTag**](sdbwritestringtag.md)
-   [**SdbWriteWORDTag**](sdbwritewordtag.md)
-   [**填充碼資料庫類型**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**標記**](tag.md)
-   [**標記類型**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



