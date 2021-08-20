---
description: 可能的話，為目錄指定目標位置的最佳方式，就是在安裝套件中撰寫目錄表格，以提供正確的位置。 如需詳細資訊，請參閱使用目錄資料表。
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: 變更目錄的目標位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27adf952faeb4d37d5edb08a04bf25cc640d41e5d87732b30c80d25bba729705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145681"
---
# <a name="changing-the-target-location-for-a-directory"></a>變更目錄的目標位置

可能的話，為目錄指定目標位置的最佳方式，就是在安裝套件中撰寫 [目錄表格](directory-table.md) ，以提供正確的位置。 如需詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。

如果您需要在安裝時變更目錄位置，您有下列選項：

-   藉由在命令列上設定 [公用屬性](public-properties.md) 的值，指定目錄的位置。 在 [CostFinalize 動作](costfinalize-action.md)期間，安裝程式所使用的內部目錄路徑會更新為 [目錄資料表](directory-table.md)中列為索引鍵的屬性值。 如需詳細資訊，請參閱在命令列上 [使用屬性](using-properties.md) 和 [設定公用屬性值](setting-public-property-values-on-the-command-line.md)。
-   使用自訂動作來指定目錄的位置。 如果在 [CostFinalize 動作](costfinalize-action.md)之前執行自訂動作，您可以使用 [自訂動作類型 51](custom-action-type-51.md) ，從格式化的文字字串設定屬性的值。 如果在 [CostFinalize 動作](costfinalize-action.md)之後執行自訂動作，您可以使用 [自訂動作類型 35](custom-action-type-35.md) ，從格式化的文字字串設定目錄路徑的值。 變更其中一個 [系統資料夾屬性](property-reference.md) 的自訂動作，應該包含在執行順序資料表中 ([InstallExecuteSequence 資料表](installexecutesequence-table.md) 或 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)) ，而使用者介面順序資料表 ([InstallUISequence 資料表](installuisequence-table.md) 和 [AdminUISequence 資料表](adminuisequence-table.md)) ，如此一來，在 [*完全 ui*](f-gly.md) 和 [*基本 ui*](b-gly.md) 安裝期間，資料夾就會變更。
-   如果安裝正在執行完整的 [*UI*](f-gly.md)，您可以使用 [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) 或 [SetTargetPath ControlEvent](settargetpath-controlevent.md) 來設定目錄路徑。 檢查 [**ProductState**](productstate.md) 屬性，以判斷是否已安裝包含此元件的產品，然後再呼叫 **MsiSetTargetPath** 或 SetTargetPath ControlEvent。 如果已為目前使用者或不同的使用者安裝了某些使用該路徑的元件，請不要嘗試變更目標目錄路徑。

下列限制適用于上述所有選項：

-   如果已為目前使用者或不同的使用者安裝了某些使用路徑的元件，請不要嘗試變更目標目錄路徑。
-   在 [維護安裝](maintenance-installation.md)期間，請勿嘗試變更目標目錄路徑。

 

 



