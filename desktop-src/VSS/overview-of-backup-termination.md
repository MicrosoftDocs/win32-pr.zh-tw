---
description: 下表顯示要終止備份作業所需的動作和事件順序。 如需詳細資訊，請參閱在 VSS 下處理備份的總覽。
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: 備份終止的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fd57822a62cf3fa39cee2b17d79ae2545afa07bd722d26cacda68cba3b6695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937966"
---
# <a name="overview-of-backup-termination"></a>備份終止的總覽

下表顯示要終止備份作業所需的動作和事件順序。 如需詳細資訊，請參閱 [在 VSS 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md)。



| 要求者動作                                                                                                                                                                                                              | 事件                                                                 | 寫入器動作                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 要求者藉由釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面或呼叫 [**>ivssbackupcomponents：:D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots)來終止陰影複製。 | 無                                                                  | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 藉由呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)來釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 。                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | 寫入器會使用 [**CVssWriter：： OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)來處理事件，讓它能夠清除與陰影複製集相關的任何狀態。 如果備份作業失敗，也就是未產生 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) 事件，寫入器可能也必須執行錯誤處理。 如需詳細資訊，請參閱 [處理 BackupShutdown 事件](handling-backupshutdown-events.md) 。 |



 

由於 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面無法重複使用，且介面的函式會終止陰影複製，因此通常沒有理由呼叫 [**>ivssbackupcomponents：:D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots)。 此方法的設計目的是要與錯誤處理和中止備份搭配使用 (查看) [中止 VSS 作業](aborting-vss-operations.md) 。

 

 
