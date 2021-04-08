---
description: 如需下圖的詳細資訊，請參閱實體關聯性圖表圖例。
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: 核心資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945140"
---
# <a name="core-tables-group"></a>核心資料表群組

如需下圖的詳細資訊，請參閱 [實體關聯性圖表圖例](entity-relationship-diagram-legend.md)。

![核心資料表群組](images/core.png)

核心群組是由描述應用程式和安裝程式套件之基本功能和元件的表格所組成。 因此，安裝套件的開發人員應該考慮如何先填入這些表格，因為大部分資料庫的組織將會從這個群組的內容中看出。

-   [功能資料表](feature-table.md)會列出屬於應用程式的所有功能。
-   [Condition 資料表](condition-table.md)包含可決定是否要安裝特定功能的條件運算式。
-   [FeatureComponents 資料表](featurecomponents-table.md)會描述哪些元件屬於各項功能。
-   [元件資料表](component-table.md)會列出屬於安裝的所有元件。
-   [目錄資料表](directory-table.md)會列出安裝期間所需的目錄。 因為每個元件都必須與一個或一個目錄相關聯，所以元件資料表與此資料表密切相關，並且具有目錄資料表的外部索引鍵。
-   [PublishComponent 資料表](publishcomponent-table.md)會列出已發佈以供其他應用程式使用的功能和元件。 [元件和功能](components-and-features.md) 有兩種類型的功能公告。
-   [MsiAssembly 資料表](msiassembly-table.md)會指定 .NET Framework common language runtime 元件和 Win32 元件的 Windows Installer 設定。
-   [MsiAssemblyName 資料表](msiassemblyname-table.md)會為 common language Runtime 或 Win32 元件的強式組件快取名稱指定元素的架構。
-   [Complus 資料表](complus-table.md)包含安裝 com + 應用程式所需的資訊。
-   [IsolatedComponent 資料表](isolatedcomponent-table.md)會將 [元件應用程式] 資料 (行中指定的元件 \_ 與 [元件共用] 資料行中指定的元件) 產生關聯， \_ (通常是共用的 DLL) 。
-   [升級資料表](upgrade-table.md)包含[主要升級](major-upgrades.md)期間所需的資訊。

 

 



