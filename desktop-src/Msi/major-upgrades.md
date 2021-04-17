---
description: 重大升級是需要變更 [ProductCode] 屬性之產品的完整更新。
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: 主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512016"
---
# <a name="major-upgrades"></a>主要升級

重大升級是需要變更 [ [**ProductCode**](productcode.md) ] 屬性之產品的完整更新。

一般的主要升級會移除舊版的應用程式，並安裝新的版本。 主要升級可以重新組織功能元件樹狀結構。 如需詳細資訊，請參閱 [ [**ProductCode**](productcode.md) ] 和 [[變更產品代碼](changing-the-product-code.md)]。

在使用 Windows Installer 進行主要升級期間，安裝程式會在使用者電腦上搜尋與擱置升級相關的應用程式，並在偵測到使用者電腦時，從系統登錄抓取已安裝應用程式的版本。 然後，安裝程式會使用升級資料庫中的資訊來判斷是否要升級已安裝的應用程式。

若要啟用安裝程式升級功能，每個封裝都應該有 [**UpgradeCode**](upgradecode.md) 屬性和 [升級資料表](upgrade-table.md)。 每個獨立產品或產品套件都應該有自己的 **UpgradeCode**。 如需使用 **UpgradeCode** 的詳細資訊，請參閱 [使用 UpgradeCode](using-an-upgradecode.md)一節。 升級資料表中的每一筆記錄都會提供升級程式碼、產品版本和語言資訊的組合，用來識別一組受升級影響的產品。 當 [FindRelatedProducts 動作](findrelatedproducts-action.md) 偵測到系統上已安裝受影響的產品時，它會將產品程式碼附加至升級資料表之 ActionProperty 資料行中的屬性。 [RemoveExistingProducts 動作](removeexistingproducts-action.md)和[MigrateFeatureStates 動作](migratefeaturestates-action.md)會移除或遷移 ActionProperty 清單中列出的產品。 套件作者也可以遵循主題中所述的程式： [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。

您可以撰寫 Windows Installer 升級套件，如果使用者已安裝較新版本的應用程式，則不會安裝主要升級。 如需如何撰寫不會透過較新版本安裝之套件的詳細資訊，請參閱 [防止舊套件安裝在較新版本上](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows Installer 只會使用產品版本的前三個欄位。 如需這些欄位的說明，請參閱 [**ProductVersion**](productversion.md) 屬性。 如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。

 

建議的方法是安裝更新產品的完整套件，以套用主要升級。 如需有關如何藉由安裝產品來套用主要升級的詳細資訊，請參閱 [安裝產品](applying-major-upgrades-by-installing-the-product.md)以套用主要升級。

套用為產品 [修補套件](patch-packages.md) 的主要升級，不能與其他更新一起排序，也不是 [可卸載修補程式](uninstallable-patches.md)。 如需如何將主要升級修補封裝套用至 Windows Installer 套件的詳細資訊，請參閱 [修補產品的本機安裝以套用主要升級](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)。 不建議使用修補套件進行主要升級的應用程式，而是安裝完整產品以套用主要升級。

> [!Note]  
> 如果應用程式安裝在每個使用者的 [安裝內容](installation-context.md)中，則任何主要的應用程式升級也都必須使用每個使用者的內容來執行。 如果應用程式安裝在每部電腦的安裝內容中，則任何主要的應用程式升級也都必須使用每一電腦的內容來執行。 Windows Installer 不會在安裝內容之間安裝主要升級。

 

您可以使用 [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)屬性，條件在 [InstallValidate](installvalidate-action.md)之後排序的自訂動作，以處理主要升級：

-   如果您想要在卸載產品期間執行自訂動作，而不是在主要升級移除產品期間執行，請使用此狀況。

    REMOVE = "ALL" 而非 [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   如果您只想要在主要升級期間執行自訂動作，請使用此條件。

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



