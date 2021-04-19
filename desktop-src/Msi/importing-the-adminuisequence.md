---
description: AdminUISequence 資料表會列出安裝程式在執行最上層系統管理員動作時所呼叫的動作，而且內部使用者介面層級會設定為完整 UI 或縮減的 UI。
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: 匯入 AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978038"
---
# <a name="importing-the-adminuisequence"></a>匯入 AdminUISequence

[AdminUISequence 資料表](adminuisequence-table.md)會列出安裝程式在執行最上層系統[管理員動作](admin-action.md)時所呼叫的動作，而且內部使用者介面層級會設定為完整 UI 或縮減的 ui。 如果使用者介面層級設定為基本 UI 或沒有 UI，則安裝程式會略過此資料表中的動作。 請參閱 [消費者介面](user-interface.md) 和 [消費者介面層級](user-interface-levels.md)。 請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。

如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。 安裝「記事本」範例時，不需要變更這些順序。

使用您的資料庫編輯器開啟 MNP2000.msi，並在 AdminExecuteSequence 資料表中輸入下列資料。

[AdminUISequence 資料表](adminuisequence-table.md)



| 動作          | 條件 | 順序 |
|-----------------|-----------|----------|
| AdminWelcomeDlg |           | 1230     |
| CostFinalize    |           | 1000     |
| CostInitialize  |           | 800      |
| ExecuteAction   |           | 1300     |
| ExitDlg         |           | -1       |
| FatalErrorDlg   |           | -3       |
| FileCost        |           | 900      |
| PrepareDlg      |           | 140      |
| ProgressDlg     |           | 1280     |
| UserExitDlg     |           | -2       |



 

[繼續](importing-the-advtexecutesequence.md)

 

 



