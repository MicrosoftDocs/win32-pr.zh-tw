---
description: 成功完成安裝腳本時，會執行 Commit 自訂動作。
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: 認可自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a126468df400e23c8eb59885b6e5a66c96d740c0c0e0959320697da293d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380303"
---
# <a name="commit-custom-actions"></a>認可自訂動作

成功完成安裝腳本時，會執行 Commit 自訂動作。 如果 [InstallFinalize 動作](installfinalize-action.md) 成功，安裝程式就會執行任何現有的 Commit 自訂動作。 在此案例中，安裝程式所設定的唯一模式參數是 MSIRUNMODE \_ COMMIT。 如需執行模式參數的說明，請參閱 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 。

您可以藉由將選項旗標加入至 [CustomAction 資料表](customaction-table.md)的 [類型] 欄位，來指定 commit 自訂動作。 請參閱指定認可自訂動作之選項旗標的 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md) 。

Commit 自訂動作是 [rollback 自訂動作](rollback-custom-actions.md) 的補充，可與 rollback 自訂動作搭配使用，以反轉直接對系統進行變更的自訂動作。

請注意，復原自訂動作可能無法移除認可自訂動作所做的所有變更。 雖然安裝程式會將 rollback 和 commit 自訂動作寫入至復原腳本，但 commit 自訂動作只會在安裝程式成功處理安裝腳本之後執行。 Commit 自訂動作是要在復原腳本中執行的第一個動作。 如果 commit 自訂動作失敗，安裝程式就會起始復原，但只能復原已寫入至復原腳本的作業。 這表示，視 commit 自訂動作而定，回復可能無法復原動作所做的變更。 您可以藉由撰寫自訂動作來忽略傳回碼，來忽略認可自訂動作中的失敗。

停用回復時，不會執行 rollback 和 commit 自訂動作。 如果封裝作者要求這些自訂動作類型進行適當的安裝，則在停用回復時，就應該在防止安裝繼續的情況下使用 [**RollbackDisabled**](rollbackdisabled.md) 屬性。

 

 



