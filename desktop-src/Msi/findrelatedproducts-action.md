---
description: FindRelatedProducts 動作會依序執行每個升級資料表的記錄，並將每個資料列中的升級程式碼、產品版本和語言，與系統上安裝的產品進行比較。
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: FindRelatedProducts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8201a2e86f9dec09931b17cd4dd594c45e4bf78de32ba438b8824a6f540563fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142877"
---
# <a name="findrelatedproducts-action"></a>FindRelatedProducts 動作

FindRelatedProducts 動作會依序執行每個 [升級資料表](upgrade-table.md) 的記錄，並將每個資料列中的升級程式碼、產品版本和語言，與系統上安裝的產品進行比較。 當 FindRelatedProducts 偵測到升級資訊與已安裝產品之間的對應時，會將產品程式碼附加至 UpgradeTable 的 ActionProperty 資料行中指定的屬性。

只有在第一次安裝產品時，才會執行 FindRelatedProducts 動作。 FindRelatedProducts 動作不會在維護模式或卸載期間執行。

## <a name="database-tables-queried"></a>查詢的資料庫資料表

此動作會查詢下表：

[升級資料表](upgrade-table.md)

## <a name="properties-used"></a>使用的屬性

FindRelatedProducts 動作會使用 [**UpgradeCode**](upgradecode.md) 屬性以及撰寫到升級資料表中的版本和語言資訊，來偵測受擱置升級影響的已安裝產品。 它會將偵測到之產品的產品代碼附加至 UpgradeTable 的 ActionProperty 資料行中的屬性。

FindRelatedProducts 只會辨識已使用 Windows Installer 安裝的現有產品，且 .msi 會定義 [**UpgradeCode**](upgradecode.md)屬性、 [**ProductVersion**](productversion.md)屬性和 [**ProductLanguage**](productlanguage.md)屬性的值，這是 [[**範本摘要**](template-summary.md)] 屬性中所列的其中一種語言。

請注意，FindRelatedProducts 會使用 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)所傳回的語言。 若要讓 FindRelatedProducts 正常運作，封裝作者必須確定 [屬性工作表](property-table.md)中的 [**ProductLanguage**](productlanguage.md)屬性已設定為也列在 [[**範本摘要**](template-summary.md)] 屬性中的語言。 請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。

## <a name="sequence-restrictions"></a>順序限制

FindRelatedProducts 應該撰寫在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence](installexecutesequence-table.md) 資料表中。 如果動作已在 InstallUISequence 中執行，則安裝程式會防止 FindRelated 產品在 InstallExecuteSequence 中執行。 FindRelatedProducts 動作必須位於 [MigrateFeatureStates 動作](migratefeaturestates-action.md) 和 [RemoveExistingProducts 動作](removeexistingproducts-action.md)之前。

## <a name="actiondata-messages"></a>ActionData 訊息

FindRelatedProducts 會傳送其在系統上偵測到的每個相關產品的動作資料訊息。

 

 



