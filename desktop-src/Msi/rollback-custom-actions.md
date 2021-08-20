---
description: 當安裝程式處理安裝腳本時，它會同時產生 rollback 腳本。
ms.assetid: 5b9bfc5a-6a78-4b0e-aed8-f25aba089af1
title: 復原自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f2b0522c8cf22f36398b3e4cb76e3576ea28e74fee9fbf140bccce2d2eaedd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990239"
---
# <a name="rollback-custom-actions"></a>復原自訂動作

當安裝程式處理安裝腳本時，它會同時產生 rollback 腳本。 除了 rollback 腳本，安裝程式還會在安裝期間儲存其所刪除之每個檔案的複本。 這些檔案會保存在隱藏的系統目錄中。 安裝完成之後，就會刪除復原腳本和儲存的檔案。 如果安裝失敗，安裝程式會嘗試復原在安裝期間所做的變更，並還原電腦的原始狀態。

雖然藉由將資料列插入資料庫資料表來排程系統作業的自訂動作會反轉安裝的復原、直接變更系統的自訂動作，或對其他系統服務發出的命令，不能一律由回復反轉。 復原自訂動作是指安裝程式只在安裝復原期間執行的動作，而它的目的是反轉已對系統進行變更的自訂動作。

復原自訂動作是一種 [順延強制自訂動作](deferred-execution-custom-actions.md)，因為它在安裝順序期間叫用時，會順延強制。 它與一般延後的自訂動作不同，因為它只會在復原期間執行。 復原自訂動作必須一律在動作順序中回復的延遲自訂動作之前。 復原自訂動作也應該處理延遲的自訂動作在執行中途中斷的情況。 例如，如果使用者在執行自訂動作時按下 [取消] 按鈕。

請注意，復原自訂動作無法以非同步方式執行。 查看 [同步和非同步自訂動作](synchronous-and-asynchronous-custom-actions.md)。

復原自訂動作的補充項是 [commit 自訂動作](commit-custom-actions.md)。 安裝程式會在安裝順序期間執行認可自訂動作、將自訂動作複製到復原腳本，但不會在復原期間執行動作。

請注意，復原自訂動作可能無法移除認可自訂動作所做的所有變更。 雖然安裝程式會將 rollback 和 commit 自訂動作寫入至復原腳本，但 commit 自訂動作只會在安裝程式成功處理安裝腳本之後執行。 Commit 自訂動作是要在復原腳本中執行的第一個動作。 如果 commit 自訂動作失敗，安裝程式就會起始復原，但只能復原已寫入至復原腳本的作業。 這表示，視 commit 自訂動作而定，回復可能無法復原動作所做的變更。 您可以藉由撰寫自訂動作來忽略傳回碼，來忽略認可自訂動作中的失敗。

當安裝程式執行復原自訂動作時，唯一會設定的模式參數是 MSIRUNMODE \_ 復原。 如需執行模式參數的說明，請參閱 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 。

您可以藉由將選項旗標加入至 [CustomAction 資料表](customaction-table.md)的 [類型] 欄位，來指定復原自訂動作。 請參閱指定復原自訂動作之選項旗標的 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md) 。

停用回復時，不會執行 rollback 和 commit 自訂動作。 如果封裝作者要求這些自訂動作類型進行適當的安裝，則在停用回復時，就應該在防止安裝繼續的情況下使用 [**RollbackDisabled**](rollbackdisabled.md) 屬性。 如需有關如何停用回復的詳細資訊，請參閱[復原安裝 (Windows Installer) ](rollback-installation.md)。

 

 



