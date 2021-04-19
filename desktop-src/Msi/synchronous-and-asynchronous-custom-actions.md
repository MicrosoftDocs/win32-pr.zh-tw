---
description: Windows Installer 會將自訂動作以獨立于主要安裝的執行緒形式處理。
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: 同步和非同步自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976776"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>同步和非同步自訂動作

Windows Installer 會將自訂動作以獨立于主要安裝的執行緒形式處理。 在同步執行自訂動作期間，安裝程式會先等候自訂動作的執行緒完成，再繼續進行主要安裝。 在非同步執行期間，安裝程式會在目前的安裝繼續時同時執行自訂動作。 因此，自訂動作的作者必須留意任何可能在函式呼叫之間變更安裝資料庫的非同步執行緒。

尤其是，非同步自訂動作應避免呼叫 [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) 和 [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) 。 請改用 [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) 來取得目標路徑。 在任何類型的自訂動作中，都應避免大量資料庫作業，例如匯入、匯出和轉換作業。

您可以在 [CustomAction 資料表](customaction-table.md) 的 [類型] 欄位中設定選項旗標，以指定主要和自訂動作執行緒會以同步或非同步方式執行。 請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

安裝程式只能以同步自訂動作的形式執行 [復原自訂動作](rollback-custom-actions.md) 和 [並行安裝](concurrent-installations.md) 動作。

 

 



