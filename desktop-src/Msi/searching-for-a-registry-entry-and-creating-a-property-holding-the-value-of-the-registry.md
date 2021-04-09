---
description: 在 Windows Installer 安裝期間，安裝程式可以搜尋登錄專案，並建立保存登錄值的屬性。
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: 搜尋登錄專案，並建立保存登錄值的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847751"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>搜尋登錄專案，並建立保存登錄值的屬性

**搜尋登錄專案並建立保存該檔案值的屬性**

1.  請勿將簽章加入至簽章 [資料表](signature-table.md) 或 [CompLocator 資料表](complocator-table.md)。 如果檔案簽章列在 [AppSearch 資料表](appsearch-table.md) 中，而且未列于 Signature 或 CompLocator 資料表中，安裝程式會在 [RegLocator 資料表](reglocator-table.md)中尋找。

2.  指定要在 [RegLocator 資料表](reglocator-table.md)中搜尋的登錄專案。 如果簽章 [資料表](signature-table.md) 中沒有簽章，而且類型資料行的值是 **msidbLocatorTypeRawValue**，則會假設搜尋是針對 RegLocator 資料表所指向的特定登錄機碼名稱。

    [RegLocator 資料表](reglocator-table.md) (部分) 

    

    | 簽名\_         | Root         | 按鍵                                                           | 名稱                  | 類型                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | AppValue<br/> | 2<br/> | **軟體** \\**Microsoft** \\**MyApp**<br/> <br/> | **Myname**<br/> | **msidbLocatorTypeRawValue**<br/> |

    

     

3.  最後，填入 [AppSearch 資料表](appsearch-table.md) ，讓 [AppSearch 動作](appsearch-action.md) 傳回 AppValue 的值。 在安裝程式執行 AppSearch 動作之後，MYREGVAL 的值就是 AppValue 的值。

    [AppSearch 資料表](appsearch-table.md) (部分) 

    

    | 屬性            | 簽名           |
    |---------------------|---------------------|
    | MYREGVAL<br/> | AppValue<br/> |

    

     

 

 




