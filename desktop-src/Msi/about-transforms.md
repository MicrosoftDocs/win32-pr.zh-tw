---
description: 轉換是套用至安裝的變更集合。 藉由將轉換套用至基底安裝套件，安裝程式可以新增或取代安裝資料庫中的資料。 安裝程式只能在安裝期間套用轉換。
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: 關於轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192475"
---
# <a name="about-transforms"></a>關於轉換

轉換是套用至安裝的變更集合。 藉由將轉換套用至基底安裝套件，安裝程式可以新增或取代安裝資料庫中的資料。 安裝程式只能在安裝期間套用轉換。

安裝程式會在安裝期間註冊產品所需的轉換清單。 設定或安裝產品時，安裝程式必須將這些轉換套用至產品的安裝套件。 如果列出的轉換無法使用，且轉換來源復原無法還原，則安裝會失敗。

轉換可以修改 [安裝程式資料庫](installer-database.md)中任何持續性資料表內的資訊。 轉換也可以新增或移除安裝程式資料庫中的持續性資料表。 轉換無法修改不在資料庫資料表中之安裝封裝的任何部分，例如 [摘要資訊資料流程](summary-information-stream.md)中的資訊、substorages 中的資訊，或是內嵌封包中的檔案。

轉換具有可包含驗證條件和錯誤條件的摘要資訊串流。 您可以使用 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) 函式，將轉換驗證和錯誤條件新增至摘要資訊。 驗證條件可控制安裝程式是否可以將轉換套用至指定的安裝資料庫。 轉換的驗證可以根據在轉換中指定的 [**UpgradeCode**](upgradecode.md)、 [**ProductCode**](productcode.md)、 [**ProductVersion**](productversion.md) 和 [**ProductLanguage**](productlanguage.md) 屬性值，以及安裝資料庫中的屬性來進行。 轉換錯誤條件可控制套用轉換時要隱藏的錯誤。 轉換中包含的錯誤條件會由使用 [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) 和 [**ApplyTransform**](database-applytransform.md) 方法指定的錯誤條件覆寫。

> [!Note]  
> 一般的自訂轉換不會有驗證條件或針對 [**ProductCode**](productcode.md)進行驗證。 存放在 [修補程式套件](patch-packages.md) 內的轉換通常會有嚴格的驗證條件，以確保將正確的轉換套用至修補程式目標。

 

有三種類型的 Windows Installer 轉換：

-   [內嵌轉換](embedded-transforms.md)
-   [安全的轉換](secured-transforms.md)
-   [不安全的轉換](unsecured-transforms.md)

 

 



