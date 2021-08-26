---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋使用者系統上特定位置中的檔案。
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: 搜尋特定位置中的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b131708e5f9ff37474864aa5d6ef13abcab8f0d162563ca810c7e31fe2c41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041148"
---
# <a name="searching-for-a-file-in-a-specific-location"></a>搜尋特定位置中的檔案

**搜尋使用者系統上特定位置的檔案**

1.  列出 [簽名表](signature-table.md)中的檔案簽章和名稱。 此記錄中的其餘欄位可以是 null，以搜尋任何版本的 MyApp.exe。

    [簽名表](signature-table.md)

    

    | 簽名          | 檔案名稱            |
    |--------------------|----------------------|
    | AppFile<br/> | MyApp.exe<br/> |

    

     

2.  如果已安裝 MyApp.exe，請輸入安裝程式要設定的屬性。

    [AppSearch 資料表](appsearch-table.md) (部分) 

    

    | 屬性         | 簽名          |
    |------------------|--------------------|
    | MYAPP<br/> | AppFile<br/> |

    

     

3.  使用 [DrLocator 資料表](drlocator-table.md)。 在 [路徑] 欄位中，輸入使用者系統上檔案的完整路徑。 在 [深度] 資料行中輸入0值，以搜尋 bin 資料夾。

    [DrLocator 資料表](drlocator-table.md)

    

    | 簽名          | 父代 | 路徑                                                    | 深度        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | AppFile<br/> |        | C： \\ Program Files \\ MyProducts \\ Projects \\ bin<br/> | 0<br/> |

    

     

4.  在動作順序中包含 AppSearch 動作。 如果 MyApp.exe 安裝在 C： \\ Program Files \\ MyProducts \\ Projects Bin 中 \\ ，安裝程式會將屬性 MYAPP 設定為檔案的位置。

 

 




