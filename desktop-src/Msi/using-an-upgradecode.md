---
description: UpgradeCode 主要是用來支援主要升級，雖然小型和次要升級修補程式可能會使用 UpgradeCode 進行產品驗證。
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: 使用 UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482bdaa228bc57432ab730e59f265fc50352c3a63ed29f75ee0a63c65c201ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039088"
---
# <a name="using-an-upgradecode"></a>使用 UpgradeCode

[**UpgradeCode**](upgradecode.md)主要是用來支援主要升級，雖然小型和次要升級修補程式可能會使用 **UpgradeCode** 進行產品驗證。 在主要升級期間， [FindRelatedProducts](findrelatedproducts-action.md)、 [MigrateFeatureStates](migratefeaturestates-action.md)和 [RemoveExistingProducts](removeexistingproducts-action.md) 動作會偵測、遷移和移除產品的先前版本。 FindRelatedProducts 動作會根據 **UpgradeCode**、 [**ProductLanguage**](productlanguage.md)和 [**ProductVersion**](productversion.md)，使用準則來搜尋產品。 這些準則是在 [升級](upgrade-table.md) 資料表中指定的。

根據 [FindRelatedProducts](findrelatedproducts-action.md) 動作所使用的準則，單一產品的不同語言和版本的 [**UpgradeCode**](upgradecode.md) 可能相同。 這是因為 [升級](upgrade-table.md) 資料表可讓您在產品版本和語言行之間進行區別。

在相同產品的不同版本中，您可能永遠不需要變更 [**UpgradeCode**](upgradecode.md)。 每個獨立產品都應該有自己的 **UpgradeCode**。 產品套件應該也有自己的 **UpgradeCode**。 這麼做可讓套件使用 [升級資料表](upgrade-table.md)中的多個資料列，升級舊版的套件或獨立產品。

下列兩個案例說明 [**UpgradeCode**](upgradecode.md)的使用。

-   產品 A 和產品 B 隨附于相同的 [**ProductLanguage**](productlanguage.md)、 [**ProductVersion**](productversion.md)和 [**UpgradeCode**](upgradecode.md)。 產品 A 和產品 B 有不同的 [**ProductCodes**](productcode.md)。 因為產品已獲指派相同的 **UpgradeCode**，所以無法撰寫 [升級](upgrade-table.md) 資料表來區分舊版產品 a 與較舊版本產品 B 的較舊版本。在此情況下，您將無法安裝產品 A 的升級，而忽略產品 B。因為這些是不同的產品，所以應該將不同的 **UpgradeCode** 指派給每個產品。
-   產品 A 的英文和法文版本是隨附于相同的 [**ProductVersion**](productversion.md) 和 [**UpgradeCode**](upgradecode.md)。 英文和法文版本的產品 A 具有不同的 [**ProductLanguages**](productlanguage.md) 和 [**ProductCodes**](productcode.md)。 雖然英文和法文語言版本都共用相同的 **UpgradeCode**，但是您可以撰寫 [升級](upgrade-table.md) 資料表，使其只會偵測及升級舊版的英文語言，而且會忽略較舊的法文版本。 產品的不同語言版本可使用相同的 **UpgradeCode**。

 

 



