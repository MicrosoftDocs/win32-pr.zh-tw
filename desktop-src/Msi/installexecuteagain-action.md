---
description: InstallExecuteAgain 動作會執行包含動作順序中所有作業的腳本，自安裝開始或最後一個 InstallExecuteAgain 動作或最後一個 InstallExecute 動作起。
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: InstallExecuteAgain 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943348"
---
# <a name="installexecuteagain-action"></a>InstallExecuteAgain 動作

InstallExecuteAgain 動作會執行包含動作順序中所有作業的腳本，自安裝開始或最後一個 InstallExecuteAgain 動作或最後一個 [InstallExecute 動作](installexecute-action.md)起。 InstallExecute 動作會更新系統而不結束交易。 InstallExecuteAgain 與 [InstallExecute 動作](installexecute-action.md) 執行相同的作業，但只應在 InstallExecute 之後使用。

應該一律設定 InstallExecuteAgain，使其不會在移除期間執行。 如需詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。

## <a name="sequence-restrictions"></a>順序限制

InstallExecute 動作位於 [InstallInitialize 動作](installinitialize-action.md) 和 [InstallFinalize 動作](installfinalize-action.md)之間。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

InstallExecuteAgain 動作執行的動作與 [InstallExecute 動作](installexecute-action.md)相同。 由於順序資料表只有一個主鍵，因此動作資料行不能在特定順序資料表中重複執行相同的動作。 有兩個動作會執行相同的動作（InstallExecute 和 InstallExecuteAgain），以便在 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中有兩次需要 InstallExecute 的功能。 如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

 

 



