---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: '我 (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a672a8cd25792dedb6e32e0916e85ddf50634824b00491733e19bab2c30ece4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056168"
---
# <a name="i-volume-shadow-copy-service"></a>我 (磁碟區陰影複製服務) 

[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**識別事件**
</dt> <dd>

VSS 事件，指出寫入器或要求者需要查詢目前的寫入器。 它是用來建立目前寫入器的中繼資料資訊。 [*另請*](vssgloss-r.md)參閱要求者、[*寫入器*](vssgloss-w.md)。

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**隱含元件包含**
</dt> <dd>

當它參與備份或還原作業時，不會將元件的資訊新增至要求者的備份元件檔。

具有可選取上階的其元件只有在包含其上階時，才會隱含包含。

如果包含上階，則可以隱含地包含可選取的上階，或可能明確地包含上階。

其元件若沒有任何可選取的祖系，則不會隱含地包含在備份或還原作業中; 如果有任何寫入器元件參與，則所有這類元件都必須明確地新增至備份元件檔。

在作業中，不能以隱含方式包含要求者所選擇的可選取元件，而要求者參與備份或還原，但必須明確地將其新增至備份元件檔。

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**增量備份作業**
</dt> <dd>

備份或還原作業只會在儲存最後一個完整、增量或差異備份之後所建立或變更的檔案上執行。 另請參閱 [*差異備份作業*](vssgloss-d.md)。

</dd> </dl>

 

 



