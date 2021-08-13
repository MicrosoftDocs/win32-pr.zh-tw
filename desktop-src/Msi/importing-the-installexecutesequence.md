---
description: InstallExecuteSequence 資料表會列出安裝程式執行最上層安裝動作時所執行的動作。 請參閱安裝程式資料表群組、使用順序資料表，以及順序資料表詳細的範例。
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: 匯入 InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586557130c6aa9af197d5d28f6bd750f4de736feb6982f3b7f12ce73ccf41c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430768"
---
# <a name="importing-the-installexecutesequence"></a>匯入 InstallExecuteSequence

[InstallExecuteSequence 資料表](installexecutesequence-table.md)會列出安裝程式執行最上層[安裝動作](install-action.md)時所執行的動作。 請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。

如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的[空白資料庫](importing-a-blank-database.md)，則 MNP2000.msi 副本中的順序資料表已包含[使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。 撰寫記事本安裝套件時，不需要變更這些序列。

使用您的資料庫編輯器開啟 MNP2000.msi，並在 InstallExecuteSequence 資料表中輸入下列資料。

[InstallExecuteSequence 資料表](installexecutesequence-table.md)



| 動作                   | 條件     | 順序 |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | 未安裝 | 1550     |
| AppSearch                |               | 400      |
| BindImage                |               | 4300     |
| CCPSearch                | 未安裝 | 500      |
| CostFinalize             |               | 1000     |
| CostInitialize           |               | 800      |
| CreateFolders            |               | 3700     |
| CreateShortcuts          |               | 4500     |
| DeleteServices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| FileCost                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize          |               | 6600     |
| InstallInitialize        |               | 1500     |
| InstallODBC              |               | 5400     |
| InstallServices          | VersionNT     | 5800     |
| InstallValidate          |               | 1400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| MoveFiles                |               | 3800     |
| PatchFiles               |               | 4090     |
| ProcessComponents        |               | 1600     |
| PublishComponents        |               | 6200     |
| PublishFeatures          |               | 6300     |
| PublishProduct           |               | 6400     |
| RegisterClassInfo        |               | 4600     |
| RegisterComPlus          |               | 5700     |
| RegisterExtensionInfo    |               | 4700     |
| RegisterFonts            |               | 5300     |
| RegisterMIMEInfo         |               | 4900     |
| RegisterProduct          |               | 6100     |
| RegisterProgIdInfo       |               | 4800     |
| RegisterTypeLibraries    |               | 5500     |
| RegisterUser             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| RemoveEnvironmentStrings |               | 3300     |
| RemoveExistingProducts   |               | 6700     |
| RemoveFiles              |               | 3500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| RemoveODBC               |               | 2400     |
| RemoveRegistryValues     |               | 2600     |
| RemoveShortcuts          |               | 3200     |
| RMCCPSearch              | 未安裝 | 600      |
| SelfRegModules           |               | 5600     |
| SelfUnregModules         |               | 2200     |
| SetODBCFolders           |               | 1100     |
| StartServices            | VersionNT     | 5900     |
| StopServices             | VersionNT     | 1900     |
| UnpublishComponents      |               | 1700     |
| UnpublishFeatures        |               | 1800     |
| UnregisterClassInfo      |               | 2700     |
| UnregisterComPlus        |               | 2100     |
| UnregisterExtensionInfo  |               | 2800     |
| UnregisterFonts          |               | 2500     |
| UnregisterMIMEInfo       |               | 3000     |
| UnregisterProgIdInfo     |               | 2900     |
| UnregisterTypeLibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| WriteEnvironmentStrings  |               | 5200     |
| WriteIniValues           |               | 5100     |
| WriteRegistryValues      |               | 5000     |



 

[繼續](importing-the-installuisequence.md)

 

 



