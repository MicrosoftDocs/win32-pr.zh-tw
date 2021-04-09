---
description: Windows Installer 可以優化修補程式，以減少將修補程式套用至已安裝應用程式所需的時間。
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: 修補程式優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848771"
---
# <a name="patch-optimization"></a>修補程式優化

Windows Installer 可以優化修補程式，以減少將修補程式套用至已安裝應用程式所需的時間。

**Windows Installer 2.0：** 不支援。 針對 Windows Installer 3.0 之前發行的 Windows Installer 版本，修補會執行應用程式的完整修複安裝，這可能需要花費更多時間。

**Windows Installer 3.0 和更新版本：** 修補程式只會變更修補程式修改過的應用程式部分。

**Windows Installer 3.1 和更新版本：** 從 Windows Installer 3.1 開始，修補程式優化要求交易中的所有修補程式都會將 OptimizedInstallMode 屬性設定為1， ([MsiPatchMetadata 資料表](msipatchmetadata-table.md)中的一個) 。

如果 patch 只修改了下表，則 Windows Installer 3.0 或更新版本會略過與其他所有資料表相關聯的動作，即使這些動作列在原始應用程式安裝套件的順序資料表中， ( .msi 檔案) 。

-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [檔案](file-table.md)
-   [FileSFPCatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [媒體](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [MsiDigitalCertificate](msidigitalcertificate-table.md)
-   [MsiDigitalSignature](msidigitalsignature-table.md)
-   [MsiFileHash](msifilehash-table.md)
-   [MsiPatchHeaders](msipatchheaders-table.md)
-   [修補](patch-table.md)
-   [PatchPackage](patchpackage-table.md)
-   [屬性](property-table.md)
-   [登錄](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [類型](typelib-table.md)
-   [\_資料行](-columns-table.md)
-   [\_存儲](-storages-table.md)
-   [\_串流](-streams-table.md)
-   [\_Tables](-tables-table.md)
-   [\_TransformView 資料表](-transformview-table.md)
-   [\_驗證](-validation-table.md)

若要關閉修補程式優化選項，請使用 [DisableFlyWeightPatching](disableflyweightpatching.md) 原則。

 

 



