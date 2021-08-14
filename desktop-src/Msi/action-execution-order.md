---
description: 動作執行的順序取決於已撰寫至順序資料表的動作順序，以及安裝程式執行順序資料表的順序。
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: 動作執行順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28244d46ae5556d1b68cc3b7258297c69e11a8d526f3e7ca31a184e64c424e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381838"
---
# <a name="action-execution-order"></a>動作執行順序

動作執行的順序取決於已撰寫至 [*順序資料表*](s-gly.md) 的動作順序，以及安裝程式執行順序資料表的順序。 如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)中的建議動作順序。

安裝程式會執行順序表格，以回應安裝、 [通告](advertisement.md)或系統 [管理安裝](administrative-installation.md)的要求。 例如，回應使用/I、/J 或/A [命令列選項](command-line-options.md)時，不會從動作順序內呼叫 [安裝](install-action.md)、 [公告](advertise-action.md)和系統 [管理](admin-action.md) 動作。 當安裝程式初始化時，這些高階動作會改傳遞給安裝程式。

如果安裝程式已通過安裝動作，且已使用使用者介面撰寫安裝套件，則安裝程式會先在 [InstallUISequence 資料表](installuisequence-table.md) 中執行動作，然後依序執行 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中的動作。 如果封裝沒有使用者介面，則安裝程式會依序執行 InstallExecuteSequence 資料表中的動作。

如果已將系統管理員動作傳遞給安裝程式，而且已使用使用者介面來撰寫安裝套件，則安裝程式會先執行 [AdminUISequence 資料表](adminuisequence-table.md) ，然後執行 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)。 如果封裝沒有使用者介面，則安裝程式會執行 AdminExecute 資料表。

如果將公告動作傳遞給安裝程式，安裝程式就會執行 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表。

> [!Note]  
> 安裝程式不會使用 [AdvtUISequence](advtuisequence-table.md) 資料表。 AdvtUISequence 資料表不應該存在於安裝資料庫中，也不應該保留空白。

 

當安裝程式執行順序資料表時，它會依照 Sequence 資料行中所列序號的順序來執行動作。 動作順序一律為線性，沒有分支或迴圈。 封裝開發人員可以藉由在 [條件] 資料行中撰寫邏輯運算式，有條件地防止執行特定動作。 當條件評估為 False 時，安裝程式會略過動作。 請參閱 [使用順序資料表](using-a-sequence-table.md) 和 [條件陳述式語法](conditional-statement-syntax.md)。

所有順序資料表都有下列資料行。



| Column    | 描述                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 動作    | 資料表的主鍵;動作名稱必須是唯一的。                                                                                                                                                                                |
| 條件 | 用來判斷是否要執行動作的布林運算式。 如果此欄位為空白或包含評估結果為 True 的運算式，則會執行此動作。 如果運算式評估為 False，則不會執行動作。 |
| 順序  | 用來決定執行動作之順序的相對序號。                                                                                                                                                         |



 

 

 



