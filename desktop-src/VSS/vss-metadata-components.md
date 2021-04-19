---
description: 重要的是，若要組織要備份或還原的寫入器檔案，就是元件的概念。
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: VSS 中繼資料元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973471"
---
# <a name="vss-metadata-components"></a>VSS 中繼資料元件

重要的是，若要組織要備份或還原的寫入器檔案，就是 [*元件*](vssgloss-c.md)的概念。

元件可讓寫入器向備份引擎指出其檔案的組織方式、檔案之間的相依性，以及這些檔案可以包含的資料類型。 這可讓備份引擎決定儲存檔案以取得最高效率。

此外，以 VSS 為基礎的應用程式會使用元件做為其中繼資料的建立區塊，以及寫入器/要求者通訊的媒體。

寫入器和要求者會分別在寫入器元資料檔案和備份元件檔中儲存有關元件的資訊，而且每個標記法中的資訊都不同。

寫入器元資料檔案中的元件資訊包括下列各項：

-   每份檔中只有一個寫入器的資訊
-   所有的寫入器元件，不論它們是否可以 [*明確包含*](vssgloss-e.md) 或必須 [*隱含地包含*](vssgloss-i.md) 在備份或還原作業中
-   [*邏輯路徑*](vssgloss-l.md) 資訊，用來將可選取的備份元件與備份元件的特定其建立關聯，進而形成元件集
-   針對每個元件所管理的 [*檔集*](vssgloss-f.md) 資訊（路徑、檔案規格和遞迴旗標）

寫入器元資料檔案也包含寫入器層級的中繼資料資訊，例如還原的還原方法和替代位置對應。 寫入器元資料檔案是唯讀的。 檢查這項資訊的介面 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)。

備份元件檔中的元件資訊包括下列各項：

-   僅限明確包含元件的資訊
-   寫入器層級的中繼資料資訊，例如替代位置對應和還原
-   描述備份或還原作業的狀態資訊

備份元件檔不包含元件檔案 [*集*](vssgloss-f.md)的資訊。 備份元件檔不是唯讀的，而且可以由寫入器修改。 存取此資訊的介面 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)。

元件的兩個運算式之間的生命週期和關聯性可理解如下：

-   寫入器負責元件的初始定義。
-   要求者會檢查所有寫入器及其元件的中繼資料。
-   在元件的 selectability 和邏輯路徑資訊中，要求者會決定必須明確包含哪些元件，而這些元件可能會明確包含在內，這些元件會定義元件集合，而這些元件是元件集的成員。
-   要求者會新增需要明確包含的元件，並隱含地在 [*元件集中*](/windows) 包含子元件， (其資訊不在備份元件檔) 中。
-   處理事件時，寫入器和要求者可以修改和檢查儲存在備份元件檔中的元件資訊，以協調其活動。

寫入器和要求者版本的元件資訊都需要適當地執行備份和還原作業，而且兩者都必須與任何已備份的資料一起儲存：

-   [元件類型](component-types.md)
-   [作者的元件定義](definition-of-components-by-writers.md)
-   [要求者使用元件](use-of-components-by-the-requestor.md)

 

 
