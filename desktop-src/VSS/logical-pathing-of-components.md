---
description: 邏輯路徑可用來將寫入器管理的元件組織成定義完善的群組。
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: 元件的邏輯路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a591f3eec0e00257740dbbd24ab7c609c53c27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989347"
---
# <a name="logical-pathing-of-components"></a>元件的邏輯路徑

[*邏輯路徑*](vssgloss-l.md) 可用來將寫入器管理的元件組織成定義完善的群組。

邏輯路徑類似于傳統檔案路徑的結構，使用反斜線 " \\ " 來分隔路徑中的元素。 與檔案路徑不同的是，邏輯路徑的根目錄是 **Null**，而不是 " \\ "。

邏輯路徑會以以 **Null** 結尾的字串表示，而且路徑可以包含的字元沒有其他限制。

邏輯路徑的最重要用途是定義 [*元件集*](vssgloss-c.md)，其中一個可選取元件的備份或還原作業中所 [*包含的明確元件*](vssgloss-e.md) ，需要包含一些其他元件， ([*子*](vssgloss-s.md) 元件) 。 元件集之定義元件的邏輯路徑是其子元件邏輯路徑的父系，以及：

-   子元件必須以根路徑的形式共用，可選取元件的邏輯路徑，以定義元件集。
-   **Null** 的根路徑有效。
-   定義可選取元件的名稱必須是元件集之每個其子元件的根路徑之後的第一個邏輯路徑元素。
-   元件集可以嵌套。
-   邏輯路徑和元件名稱的組合在 [*寫入器類別*](vssgloss-w.md)的所有實例中必須是唯一的。

以下定義的邏輯路徑結構之寫入器 *MyWriter* 的假設範例說明邏輯路徑。



| 元件名稱 | 邏輯路徑            | 可選取以進行備份 |
|----------------|-------------------------|-----------------------|
| 執行  | ""                      | N                     |
| "ConfigFiles"  | 執行           | N                     |
| "LicenseInfo"  | ""                      | Y                     |
| "Security"     | ""                      | Y                     |
| 使用者     | "Security"              | N                     |
| 數位憑證 | "Security"              | N                     |
| "writerData"   | ""                      | Y                     |
| Set1         | "writerData"            | N                     |
| Jan          | "writerData \\ Set1"      | N                     |
| 年          | "writerData \\ Set1"      | N                     |
| Set2         | "writerData"            | N                     |
| Jan          | \\"writerData      | N                     |
| 年          | \\"writerData      | N                     |
| 查詢        | "writerData \\ QueryLogs" | N                     |
| 用法        | "writerData"            | Y                     |
| Jan          | "writerData \\ Usage"     | N                     |
| 年          | "writerData \\ Usage"     | N                     |



 

請注意，「可執行檔」和「中」元件有父子式關聯性，但兩者都是其。 因此，它們不會形成元件集。 每當備份或還原寫入器 *MyWriter* 時，這兩個元件就必須 [*明確包含*](vssgloss-e.md) 在作業中。

元件 "LicenseInfo" 可供選擇，而不是上階或子系。 在備份或還原作業中，可以明確地將它包含在備份或還原作業中。

元件「安全性」會定義簡單元件集，其中不包含任何元件集。

元件 "writerData" 會定義元件集，其中包含一個複雜的元件集合，其中包含幾個定義完善的邏輯路徑階層。

一個子元件（「使用量」）是可選取的，而且會定義元件集。

有幾個元件具有相同的名稱，並依其邏輯路徑來區分。 其元件 "Dec" 和 "Jan" 的實例存在於元件其元件 "Set1" 和 ""，以及在可選取的子元件 "Usage" 下。

如果在備份或還原中明確包含元件 "writerData"，則其所有子元件（即使是以 "Usage" 定義之嵌套元件集中的子元件）都會 [*隱含*](vssgloss-e.md)[*地包含在作業*](vssgloss-i.md) 中。

如果 "writerData" 定義的元件集未明確包含在備份或還原中，則 "Set1"、"QueryLogs" 和 "" 元件 (以及其子元件 "Dec" 和 "Jan" ) 的實例將不會以隱含方式包含在備份或還原作業中。

但是，即使作業中沒有包含 "writerData"，元件「使用方式」仍可供選擇，而且仍可明確地包含在備份或還原作業中。 如果是，則會隱含包含其子元件 "Jan" 和 "Dec"。

值得注意的其他幾點：

-   可選取的元件 "LicenseInfo" 和 "writerData" 和其元件「可執行檔」全都位於 *MyWriter* 邏輯路徑階層中的相同層級：全部都具有相同的邏輯路徑 **Null** 或 ""，也就是根邏輯路徑。
-   如果可選取的父系 ( "writerData" ) 已明確包含在備份或還原作業中，則不應明確地將可選取的元件包含在備份中。
-   定義元件集的元件可能只是為了組織的原因而存在。 例如，"writerData" 或 "Usage" 元件，或兩者都是空的;也就是說，使用 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)， [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)方法不會將任何檔案 [*集*](vssgloss-f.md)加入至其中。 元件仍會定義元件集。

 

 



