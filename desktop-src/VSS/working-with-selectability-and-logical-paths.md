---
description: 寫入器參與備份或還原作業，以及儲存的資料是哪一種，取決於哪個元件會明確包含在要求者的備份元件檔中，以及這些元件與寫入器元資料檔案中其他元件的邏輯路徑之間的關聯性。
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: 使用 Selectability 和邏輯路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973066"
---
# <a name="working-with-selectability-and-logical-paths"></a>使用 Selectability 和邏輯路徑

寫入器參與備份或還原作業，以及儲存的資料是哪一種，取決於哪個元件會 [*明確包含*](vssgloss-e.md) 在要求者的備份元件檔中，以及這些元件與寫入器元資料檔案中其他元件的邏輯路徑之間的關聯性。

在 [*PrepareForBackup*](vssgloss-p.md) 事件產生之前，沒有任何元件的寫入器會新增至要求者的備份元件檔 (在進行備份作業) 或 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (事件的情況下，) 在還原作業的情況下不會收到任何事件，且不會參與備份或還原作業。

不過，要求者可以自由地在備份或還原中包含或排除任何指定的元件，如下所示：

-   由寫入器管理並以 [*邏輯路徑* 表示的元件之間存在的任何階層](vssgloss-l.md)
-   元件是否已指定為可 [*選取以進行備份*](vssgloss-s.md)
-   是否要將它指定為可 [*供還原*](vssgloss-s.md)
-   給定寫入器中的指定元件與其他寫入器中的其他元件之間是否有明確的相依性

有關這些問題的詳細資訊，請按下列主題：

-   [元件的邏輯路徑](logical-pathing-of-components.md)
-   [使用 Selectability 進行備份](working-with-selectability-for-backup.md)
-   [使用 Selectability 進行還原和子元件](working-with-selectability-for-restore-and-subcomponents.md)
-   [Selectability 和使用元件屬性](selectability-and-working-with-component-properties.md)
-   [不同寫入器所管理元件之間的相依性](dependencies-between-components-managed-by-different-writers.md)

 

 



