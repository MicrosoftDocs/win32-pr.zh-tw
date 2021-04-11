---
description: 使用者介面序列會匯入到範例資料庫中。
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: 匯入 InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193681"
---
# <a name="importing-the-installuisequence"></a>匯入 InstallUISequence

[InstallUISequence 資料表](installuisequence-table.md)會列出執行最上層[安裝動作](install-action.md)時所執行的動作，以及將內部使用者介面層級設定為完整 ui 或縮減 ui 的動作。 如果使用者介面層級設定為基本 UI 或無 UI，則安裝程式會略過此資料表中的動作。 請參閱 [消費者介面](user-interface.md) 和 [消費者介面層級](user-interface-levels.md)。 請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。

如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。 撰寫「記事本」安裝套件時，不需要變更這些順序。

使用您的資料庫編輯器開啟 MNP2000.msi，並在 InstallUISequence 資料表中輸入下列資料。

[InstallUISequence 資料表](installuisequence-table.md)



| 動作                | 條件                                    | 順序 |
|-----------------------|----------------------------------------------|----------|
| AppSearch             |                                              | 400      |
| CCPSearch             | 未安裝                                | 500      |
| CostFinalize          |                                              | 1000     |
| CostInitialize        |                                              | 800      |
| ExecuteAction         |                                              | 1300     |
| ExitDlg               |                                              | -1       |
| FatalErrorDlg         |                                              | -3       |
| FileCost              |                                              | 900      |
| LaunchConditions      |                                              | 100      |
| MaintenanceWelcomeDlg | 已安裝且不會繼續，且未預先選取 | 1250     |
| PrepareDlg            |                                              | 140      |
| ProgressDlg           |                                              | 1280     |
| ResumeDlg             | 已安裝並 (繼續或預先選取)         | 1240     |
| RMCCPSearch           | 未安裝                                | 600      |
| UserExitDlg           |                                              | -2       |
| WelcomeDlg            | 未安裝                                | 1230     |
| MigrateFeatureStates  |                                              | 1200     |
| FindRelatedProducts   |                                              | 200      |



 

[繼續](importing-the-adminexecutesequence.md)

 

 



