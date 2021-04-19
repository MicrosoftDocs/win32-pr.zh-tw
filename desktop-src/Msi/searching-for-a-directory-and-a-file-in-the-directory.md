---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋目錄和該目錄中的檔案。
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: 搜尋目錄和目錄中的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978000"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a>搜尋目錄和目錄中的檔案

**搜尋目錄和該目錄中的檔案**

1.  先搜尋目錄。

    AppDir 必須定義為目錄的有效簽章。 如果 AppDir 未定義為有效的簽章，AppSearch 就不會有尋找檔案的位置，例如，如果搜尋是針對 c： \\ MyDir \\MyApp.exe，則 AppDir 應定義為 c： \\ MyDir。 AppDir 可能是藉由在 [DrLocator 資料表](drlocator-table.md)中包含記錄，或由其他方法來定義。 目錄搜尋的簽章 [資料表](signature-table.md) 中不會包含任何記錄。 針對檔案搜尋，列出簽章和簽章資料表中的名稱。 此記錄中的其餘欄位可以是 null，以搜尋任何版本的 MyApp.exe。

    [簽名表](signature-table.md) (部分) 

    

    | 簽名          | 檔案名稱            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  使用 [AppSearch 資料表](appsearch-table.md)。

    如果已安裝 AppDir 簽章的目錄，請輸入安裝程式要設定的屬性。 如果安裝程式發現已安裝此目錄，它會將 MYDIR 設定為目錄路徑。 如果已安裝 MyApp.exe，請輸入安裝程式要設定的屬性。

    [AppSearch 資料表](appsearch-table.md) (部分) 

    

    | 屬性         | 簽名          |
    |------------------|--------------------|
    | MYDIR<br/> | AppDir<br/>  |
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  使用 [DrLocator 資料表](drlocator-table.md)。

    在父資料行中，輸入定義為目錄路徑的 AppDir 簽章。 在 [深度] 資料行中指定要在此目錄中搜尋的子目錄層級數目。 AppDir 必須定義為目錄簽章。 AppDir 可透過如下所示的記錄來定義，或由其他方法來定義。

    [DrLocator 資料表](drlocator-table.md)

    

    | 簽名 | 父代 | 路徑      | 深度 |
    |-----------|--------|-----------|-------|
    | AppDir    |        | C： \\ MyDir | 0     |
    | AppFile   | AppDir |           | 0     |

    

     

4.  在動作順序中包含 AppSearch 動作。

    如果在 AppDir 中找到要安裝的 MyApp.exe，安裝程式會將屬性 MYAPP 設定為檔案的位置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




