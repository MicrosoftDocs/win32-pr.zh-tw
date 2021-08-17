---
description: InstallExecute 動作會執行包含動作順序中所有作業的腳本，自安裝開始或上次 InstallExecute 動作或 InstallExecuteAgain 動作起。
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: InstallExecute 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249a83f283b3abee97fbddf99d755b158678726fbb36c066791e3f87ae718f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946126"
---
# <a name="installexecute-action"></a>InstallExecute 動作

InstallExecute 動作會執行包含動作順序中所有作業的腳本，自安裝開始或上次 InstallExecute 動作或 [InstallExecuteAgain 動作](installexecuteagain-action.md)起。 InstallExecute 動作會更新系統而不結束交易。

## <a name="sequence-restrictions"></a>順序限制

InstallExecute 動作位於 [InstallInitialize 動作](installinitialize-action.md) 和 [InstallFinalize 動作](installfinalize-action.md)之間。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

[InstallExecuteAgain 動作](installexecuteagain-action.md)執行的動作與 InstallExecute 動作相同。 由於順序資料表只有一個主鍵，因此動作資料行不能在特定順序資料表中重複執行相同的動作。 有兩個動作會執行相同的動作（InstallExecute 和 InstallExecuteAgain），以便在 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中有兩次需要 InstallExecute 的功能。 如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

 

 



