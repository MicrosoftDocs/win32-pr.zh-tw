---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋檔案，並建立包含檔案路徑的屬性。
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: 搜尋檔案並建立保存檔案路徑的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d1315616c6d2ea24052ddad85c005d53716f8b130f4aa2d23d69754c946416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041138"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a>搜尋檔案並建立保存檔案路徑的屬性

**搜尋檔案並建立保存該檔案路徑的屬性**

1.  首先，請在簽章 [資料表](signature-table.md)中列出檔案簽章和名稱，以搜尋檔案。

    此記錄的其餘欄位可以保留空白，以指定搜尋任何版本的 MyApp.exe。

    [簽名表](signature-table.md) (部分) 

    

    | 簽名          | 檔案名稱            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  接下來，指定要在 [DrLocator 資料表](drlocator-table.md)中搜尋之檔案的路徑。

    因為 AppFolder 不會列在簽章 [資料表](signature-table.md)中，所以安裝程式會判斷 AppFolder 是資料夾而非檔案。

    [DrLocator 資料表](drlocator-table.md)

    

    | 簽名            | 父代             | 路徑 | 深度 |
    |----------------------|--------------------|------|-------|
    | AppFile<br/>   |                    |      |       |
    | AppFolder<br/> | AppFile<br/> |      |       |

    

     

3.  最後，填入 [AppSearch 資料表](appsearch-table.md) ，讓 [AppSearch 動作](appsearch-action.md) 傳回 AppFolder 的路徑。

    在安裝程式執行 AppSearch 動作之後，MYFOLDER 的值是 AppFolder 的完整路徑。

    [AppSearch 資料表](appsearch-table.md) (部分) 

    

    | 屬性            | 簽名            |
    |---------------------|----------------------|
    | MYFOLDER<br/> | AppFolder<br/> |

    

     

 

 




