---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋檔案的所有固定磁片磁碟機。
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: 搜尋檔案的所有固定磁片磁碟機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983737"
---
# <a name="searching-all-fixed-drives-for-a-file"></a>搜尋檔案的所有固定磁片磁碟機

**搜尋檔案的所有固定磁片磁碟機**

1.  在簽章 [資料表](signature-table.md)中輸入檔案簽章和名稱。 此記錄中的其餘欄位可以是 null，以搜尋任何版本的 MyApp.exe。

    [簽名表](signature-table.md) (部分) 

    

    | 簽名          | 檔案名稱            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  如果已安裝 MyApp.exe，請輸入安裝程式要設定的屬性。

    [AppSearch 資料表](appsearch-table.md)

    

    | 屬性         | 簽名          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  使用 [DrLocator 資料表](drlocator-table.md)。 將 [父系] 和 [路徑] 欄位保留空白，以搜尋使用者系統的所有固定磁片磁碟機。 在 [深度] 資料行中指定要搜尋的子目錄層級數目。 例如，將 Depth 設定為0會偵測到 c： \\MyApp.exe，但不會在深度2偵測到檔案，例如： c： \\ Program Files \\ MyApps \\MyApp.exe。

    [DrLocator 資料表](drlocator-table.md)

    

    | 簽名          | 父代 | 路徑 | 深度        |
    |--------------------|--------|------|--------------|
    | AppFile<br/> |        |      | 3<br/> |

    

     

4.  在動作順序中包含 AppSearch 動作。 如果已安裝 MyApp.exe，安裝程式會將屬性 MYAPP 設定為檔案的位置。 如果已安裝檔案，MYAPP 會在條件運算式中評估為 True。

 

 




