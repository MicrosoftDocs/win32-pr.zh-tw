---
description: Windows如果使用者已安裝較新的版本，則可以撰寫安裝程式升級套件，以不安裝主要升級。
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: 防止舊套件安裝在較新的版本上
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e992cc1e32d2b25e5af587c00ca4f8ee28e4b09fd3100cb12b382ae90f8c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145381"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>防止舊套件安裝在較新的版本上

Windows如果使用者已安裝較新的版本，則可以撰寫安裝程式升級套件，以不安裝主要升級。 本主題中的程式僅能防止可能因為執行主要升級封裝而造成的降級。 此程式依賴 [FindRelatedProducts 動作](findrelatedproducts-action.md)，此動作只會在第一次安裝期間執行，而且無法在維護模式下執行 (重新安裝) 。 因為次要升級是使用重新安裝來執行，所以此程式無法用來判斷次要升級套件是否正在嘗試降級應用程式。 如需詳細資訊，請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。

**防止舊套件安裝在較新的版本上**

1.  輸入可能符合 [升級資料表](upgrade-table.md)的 UpgradeCode 資料行之相關產品群組的 [ [**UpgradeCode**](upgradecode.md) ] 屬性。
2.  在 [[升級] 資料表](upgrade-table.md)的 [屬性] 資料行中，輸入 **msidbUpgradeAttributesOnlyDetect** 位旗標。
3.  在 [ [升級] 資料表](upgrade-table.md)的 [VersionMin] 資料行中，輸入此封裝所提供的升級版本。 將 VersionMax 資料行保留空白。
4.  在 [[升級] 資料表](upgrade-table.md)的 [ActionProperty] 資料行中，輸入[FindRelatedProducts 動作](findrelatedproducts-action.md)要設定之屬性的名稱。
5.  將 [**SecureCustomProperties**](securecustomproperties.md) 屬性和 [升級資料表](upgrade-table.md) 的 ActionProperty 資料行中所指定的屬性加入至 [屬性資料表](property-table.md)。
6.  在[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的 FindRelatedProducts 動作之後，加入[自訂動作類型 19](custom-action-type-19.md) 。 在 [CustomAction 資料表](customaction-table.md) 中包含此動作的記錄，然後輸入要在目標資料行中顯示的文字。 類型19自訂動作內建于安裝程式中，因此沒有可寫入的程式碼。
7.  在 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中，于包含 [自訂動作類型 19](custom-action-type-19.md)的 [記錄] 的 [條件] 資料行中，輸入 ActionProperty 的名稱。 這種情況下，只有當 [升級資料表](upgrade-table.md) 偵測到已安裝較新版本時，才會執行自訂動作。

    例如，將相關產品群組升級至3.0 版的 Windows Installer 封裝，可能會在其[Upgrade](upgrade-table.md)、 [CustomAction](customaction-table.md)、 [InstallExecuteSequence](installexecutesequence-table.md)和[Property](property-table.md)資料表中包含下列記錄。 群組中的所有相關產品都有相同的 UpgradeCode，但是如果電腦上已安裝3.0 以後的版本，安裝程式就不會安裝此升級套件。 在此情況下，安裝程式會顯示錯誤訊息，且安裝會失敗。 3.0 版升級套件會安裝在1.0 和2.0 版。

    [升級資料表](upgrade-table.md)

    

    | UpgradeCode                            | VersionMin | VersionMax | 語言 | 屬性                                | 移除 | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [CustomAction 資料表](customaction-table.md)

    

    | 動作 | 類型 | 來源 | 目標                                 |
    |--------|------|--------|----------------------------------------|
    | CA1    | 19   |        | 已安裝較高的升級。 |

    

     

    [InstallExecuteSequence 資料表](installexecutesequence-table.md)

    

    | 動作              | 條件       | 順序 |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | CA1                 | NEWPRODUCTFOUND | 201      |

    

     

    [屬性工作表](property-table.md)

    

    | 屬性                                                 | 值                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND;UPGRADEFOUND |

    

     

 

 



