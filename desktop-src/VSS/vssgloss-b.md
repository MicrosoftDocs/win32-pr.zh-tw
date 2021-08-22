---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: 'B (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f20bbe9f858066d7fca09a3f263aa618c79c4174664b9a4e0994c900fb81c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998048"
---
# <a name="b-volume-shadow-copy-service"></a>B (磁碟區陰影複製服務) 

[B](vssgloss-a.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**後端層級應用程式**
</dt> <dd>

指示寫入器收到 VSS 凍結的通知點。 初始化為後端層級應用程式的寫入器會在寫入器初始化為前端層級應用程式之後，以及初始化為系統層級應用程式的之前收到通知。 另請參閱 [*應用層級*](vssgloss-a.md)、 [*前端層級應用程式*](vssgloss-f.md)、 [*系統層級應用程式*](vssgloss-s.md)、 [*寫入器*](vssgloss-w.md)。

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete 事件**
</dt> <dd>

表示 VSS 備份已完成的 VSS 事件。 在正常作業下，此事件後面應該接著 BackupShutdown 事件。 另請參閱 *BackupShutdown 事件*。

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**備份元件檔**
</dt> <dd>

要求者所建立的 XML 檔 (在設定還原或備份作業的過程中，) 使用 **>ivssbackupcomponents** 介面。 備份元件文件包含從參與備份或還原作業的一或多個寫入器明確加入的元件清單。 不包含隱含加入的元件資訊。 相反地，寫入器中繼資料文件只會包含可能參與備份的寫入器元件。

您可以將備份元件檔儲存到磁片。 另請參閱 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件*](vssgloss-i.md)包含。

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**備份組**
</dt> <dd>

要備份的檔案。 它包含元件中所選取的檔案，這些檔案包含在元件中（由寫入器層級的 include 語句所表示），而不是已明確包含的檔案。

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown 事件**
</dt> <dd>

VSS 事件，指出符合規範的備份應用程式已關閉。 一般來說，這會在 BackupComplete 事件之前。 但是，如果備份非預期地終止，則不需要先前的 BackupComplete 事件就可以產生此事件。 另請參閱 *BackupComplete 事件*。

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**備份戳記**
</dt> <dd>

字串，其中包含發生備份時的資訊。 除了智慧型至指定類別的所有寫入器實例之外，VSS 對此字串的格式沒有任何限制。 它可能包含時間和日期資訊、邏輯序號或任何其他資訊，這些資訊將允許相同類別的寫入器判斷上次備份的發生時間。

</dd> </dl>

 

 



