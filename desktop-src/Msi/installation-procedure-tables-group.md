---
description: 安裝程式群組中的資料表會控制在安裝期間依標準動作和自訂動作所執行的工作。
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: 安裝程式資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320879"
---
# <a name="installation-procedure-tables-group"></a>安裝程式資料表群組

安裝程式群組中的資料表會控制在安裝期間依 [標準動作](standard-actions.md) 和 [自訂動作](custom-actions.md)所執行的工作。

此群組中的部分資料表會藉由提供一系列動作來控制高階動作。 下列每一個順序資料表都會控制高階動作的一部分。

-   [InstallUISequence 資料表](installuisequence-table.md)
-   [InstallExecuteSequence 資料表](installexecutesequence-table.md)
-   [AdminUISequence 資料表](adminuisequence-table.md)
-   [AdminExecuteSequence 資料表](adminexecutesequence-table.md)
-   [AdvtUISequence 資料表](advtuisequence-table.md)
-   [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)

在某些情況下，安裝必須使用 [標準動作](standard-actions.md)來執行某些動作。 為了提供最大的彈性，安裝程式會讓安裝程式作者能夠建立自己的自訂動作。 如果您有任何自訂動作，您應該填入 CustomAction 資料表來向安裝程式註冊它們。

[CustomAction 資料表](customaction-table.md)提供將自訂程式碼和資料整合至安裝程式的方法。 執行的程式碼可以是包含在資料庫內的資料流程、最近安裝的檔案，或現有的可執行檔。

下表將在安裝期間擴充安裝程式的功能，以操作檔案和資料夾。

-   [RemoveFile 資料表](removefile-table.md)包含在安裝期間移除的檔案清單。
-   [RemoveIniFile 資料表](removeinifile-table.md)包含應用程式需要從 .ini 檔案移除的資訊。
-   [RemoveRegistry 資料表](removeregistry-table.md)包含已選取要安裝的對應元件時，從系統登錄刪除的資訊。
-   [CreateFolder 資料表](createfolder-table.md)會列出在安裝期間必須建立的資料夾。 雖然安裝程式會在需要時建立資料夾，但它們會在空白時立即移除。 在卸載元件之前，不會刪除 CreateFolder 資料表中的資料夾清單。
-   [MoveFile 資料表](movefile-table.md)包含要從使用者電腦上指定的來原始目錄移動或複製到目的地目錄的檔案清單。 您不需要使用 MoveFile 資料表來描述與您要安裝之元件相關聯的檔案。

若要設定必須符合才能起始安裝的必要條件，請填入 LaunchCondition 資料表。

[LaunchCondition 資料表](launchcondition-table.md)包含條件清單，必須滿足這些條件，動作才會成功。

 

 



