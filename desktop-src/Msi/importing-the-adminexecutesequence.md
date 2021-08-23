---
description: AdminExecuteSequence 資料表會列出安裝程式在呼叫最上層系統管理員動作時所執行的動作。 請參閱安裝程式資料表群組、使用順序資料表，以及順序資料表詳細的範例。
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: 匯入 AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de646049fed05f881b61c4b635af3bc9d2caed09512a1ec89853066b0ba99c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787378"
---
# <a name="importing-the-adminexecutesequence"></a>匯入 AdminExecuteSequence

[AdminExecuteSequence 資料表](adminexecutesequence-table.md)會列出安裝程式在呼叫最上層系統[管理員動作](admin-action.md)時所執行的動作。 請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。

如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的[空白資料庫](importing-a-blank-database.md)，則 MNP2000.msi 副本中的順序資料表已包含[使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。 撰寫記事本範例安裝套件時，不需要變更這些序列。

使用您的資料庫編輯器開啟 MNP2000.msi，並在 AdminExecuteSequence 資料表中輸入下列資料。

[AdminExecuteSequence 資料表](adminexecutesequence-table.md)



| 動作              | 條件 | 順序 |
|---------------------|-----------|----------|
| CostFinalize        |           | 1000     |
| CostInitialize      |           | 800      |
| FileCost            |           | 900      |
| InstallAdminPackage |           | 3900     |
| InstallFiles        |           | 4000     |
| InstallFinalize     |           | 6600     |
| InstallInitialize   |           | 1500     |
| InstallValidate     |           | 1400     |



 

[繼續](importing-the-adminuisequence.md)

 

 



