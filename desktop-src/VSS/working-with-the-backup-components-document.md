---
description: 要求者會在執行備份的開始時建立備份元件檔。
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: 使用備份元件檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973850"
---
# <a name="working-with-the-backup-components-document"></a>使用備份元件檔

要求者會在執行備份的開始時建立備份元件檔。 檔一開始只包含備份操作狀態的描述。 在還原期間，檔應該提供有關要求者如何繼續將檔案複製回磁片的指示。 在還原作業的過程中，會修改備份元件檔，並且包含該作業的狀態。

不同于寫入器元資料檔案（唯讀），有一個視窗可讓要求者和寫入器修改備份元件檔。 您可以更新檔，直到在備份作業期間產生 [*BackupComplete*](vssgloss-b.md) 或 [*BackupShutdown*](vssgloss-b.md) 事件，到還原期間的 [*PostRestore*](vssgloss-p.md) 事件為止。

若要使用要求者的備份元件檔，必須瞭解下列主題：

-   [備份元件檔生命週期](backup-components-document-life-cycle.md)
-   [備份元件檔內容](backup-components-document-contents.md)

 

 



