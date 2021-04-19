---
description: Windows Installer 可以在安裝期間搜尋特定的檔案或目錄。 檔案或目錄搜尋可用來判斷使用者是否已安裝應用程式的版本。
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: 搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41d0ebf8943d1fb82b7c0901a62230e6befdcba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986398"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案

Windows Installer 可以在安裝期間搜尋特定的檔案或目錄。 檔案或目錄搜尋可用來判斷使用者是否已安裝應用程式的版本。

[AppSearch 動作](appsearch-action.md) 會在使用者系統中搜尋 [AppSearch 資料表](appsearch-table.md)中指定的檔案簽章。 如果 AppSearch 動作找到具有指定簽章的已安裝檔案或目錄，它會將對應的屬性（也會在 AppSearch 資料表中指定）設定為檔案或目錄的位置。 搜尋檔案時，檔案簽章也必須列在簽章 [資料表](signature-table.md)中。 如果檔案簽章列在 AppSearch 資料表中，而且未列于簽章資料表中，則搜尋會尋找目錄、登錄專案或 .ini 檔案專案。

為了加速搜尋使用者電腦，安裝程式會依所列的順序來查詢下列定位器資料庫資料表，以取得建議的搜尋位置：

-   如果檔案簽章列在 [CompLocator 資料表](complocator-table.md)中，建議的搜尋位置是元件的金鑰路徑。 如果簽章未列在此資料表中，或未安裝在建議的位置，則安裝程式會查詢 [RegLocator 資料表](reglocator-table.md) 中的建議位置。
-   如果檔案簽章列在 [RegLocator 資料表](reglocator-table.md)中，建議的搜尋位置是在使用者登錄中寫入的金鑰路徑。 如果簽章未列在此資料表中，或未安裝在建議的位置，則安裝程式會查詢 [IniLocator 資料表](inilocator-table.md) 中的建議位置。
-   如果檔案簽章列在 [IniLocator 資料表](inilocator-table.md)中，建議的搜尋位置是寫入 .ini 檔案的金鑰路徑，該檔案存在於使用者系統的預設 Windows 目錄中。 如果簽章未列在此資料表中，或未安裝在建議的位置，則安裝程式會查詢 [DrLocator 資料表](drlocator-table.md) 中的建議位置。
-   如果檔案簽章列在 [DrLocator 資料表](drlocator-table.md)中，建議的搜尋位置是使用者目錄樹狀結構中的路徑。 下表也會指定在此位置底下搜尋的子目錄層級深度。

當安裝程式第一次在建議的位置找到檔案簽章時，它會停止搜尋此檔案或目錄，並在 [AppSearch 資料表](appsearch-table.md)中設定對應的屬性。 如需詳細資訊，請參閱下列：

-   [搜尋檔案的所有固定磁片磁碟機](searching-all-fixed-drives-for-a-file.md)
-   [搜尋目錄和目錄中的檔案](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [搜尋檔案並建立保存檔案路徑的屬性](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [搜尋特定位置中的檔案](searching-for-a-file-in-a-specific-location.md)
-   [搜尋登錄專案，並建立保存登錄值的屬性](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



