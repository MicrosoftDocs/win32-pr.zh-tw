---
description: AdvtExecuteSequence 資料表會列出安裝程式在執行最上層通告動作時所呼叫的動作。 請參閱安裝程式資料表群組、使用順序資料表，以及順序資料表詳細的範例。
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: 匯入 AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693852"
---
# <a name="importing-the-advtexecutesequence"></a>匯入 AdvtExecuteSequence

[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)會列出安裝程式在執行最上層[通告動作](advertise-action.md)時所呼叫的動作。 請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。

如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。 撰寫「記事本」範例安裝套件時，不需要變更這些順序。

使用您的資料庫編輯器開啟 MNP2000.msi，並在 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中輸入下列資料。

[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)



| 動作                | 條件 | 順序 |
|-----------------------|-----------|----------|
| CostFinalize          |           | 1000     |
| CostInitialize        |           | 800      |
| CreateShortcuts       |           | 4500     |
| InstallFinalize       |           | 6600     |
| InstallInitialize     |           | 1500     |
| InstallValidate       |           | 1400     |
| PublishComponents     |           | 6200     |
| PublishFeatures       |           | 6300     |
| PublishProduct        |           | 6400     |
| RegisterClassInfo     |           | 4600     |
| RegisterExtensionInfo |           | 4700     |
| RegisterMIMEInfo      |           | 4900     |
| RegisterProgIdInfo    |           | 4800     |



 

安裝程式不會使用 [AdvtUISequence 資料表](advtuisequence-table.md) 。 在安裝資料庫中，此資料表不應存在或保持空白。

[繼續](adding-summary-information.md)

 

 



