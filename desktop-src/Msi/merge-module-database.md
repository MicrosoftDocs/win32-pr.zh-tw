---
description: 合併模組的資料庫包含模組的所有安裝屬性和安裝程式邏輯。
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: 合併模組資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319839"
---
# <a name="merge-module-database"></a>合併模組資料庫

合併模組的資料庫包含模組的所有安裝屬性和安裝程式邏輯。 基本上是簡化的 [安裝程式資料庫](installer-database.md) 或 .msi 檔案。 標準合併模組資料庫檔案是以 .msm 副檔名表示。 如需可以存在於合併模組中的所有資料庫資料表清單，請參閱 [合併模組資料庫資料表](merge-module-database-tables.md)。 每個 .msm 檔案的資料庫中都需要有下列資料表：

[元件](component-table.md)

[目錄](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[檔案](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

請注意，元件、目錄、FeatureComponents 和檔案資料表也都存在於所有 .msi 檔案中。 合併模組資料庫不包含 [功能資料表](feature-table.md) ，因此無法單獨安裝 .msm 檔。 若要安裝合併模組，您必須先使用合併工具將其合併至 .msi 檔案。

[ModuleSignature 資料表](modulesignature-table.md)只存在於已與至少一個 .msm 檔案合併的 .msi 檔案中。 如果這個資料表出現在 .msi 檔案中，它會針對先前合併到安裝資料庫中的每個合併模組包含一筆記錄。

合併模組可能包含選擇性的 MergeModule 順序資料表。 這些資料表只會出現在 .msm 檔案中。 當 .msm 檔案合併至 .msi 檔案時，這些資料表會修改 .msi 檔案的動作 [*順序資料表*](s-gly.md) 。

合併模組可能包含自訂資料表。 這些資料表是由合併模組中定義的 [自訂動作](custom-actions.md) 所使用。

合併模組很少需要使用者介面資料表。 只有在一般情況下，當合併模組在安裝期間需要使用者輸入時，才需要顯示這些資料表。 如需詳細資訊，請參閱 [在合併模組中撰寫使用者介面](authoring-user-interfaces-in-merge-modules.md)。

 

 



