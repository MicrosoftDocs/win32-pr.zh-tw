---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: 'E (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305a02633e8ed2aca1e372f250d6d91a8560ef1cb7a9f565e64aea6924397ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905128"
---
# <a name="e-volume-shadow-copy-service"></a>E (磁碟區陰影複製服務) 

[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**明確元件包含**
</dt> <dd>

當元件參與備份或還原作業時，將元件的資訊新增至要求者的備份元件檔。 要求者會使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 明確地在備份作業中包含元件，並使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 或 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) 在還原作業中明確包含元件。

如果已備份或還原任何寫入器的元件，則備份或還原作業中必須明確包含所有沒有可選取之祖系的其元件。

在作業中，必須明確包含要求者為參與備份或還原所選擇的可選取元件，而不需要選取的祖系。

具有可選取上階的其元件絕不會明確包含在內。

具有可選取上階的可選取元件可能會明確包含，如果是明確包含上階，則可以隱含地包含。

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**公開陰影複製**
</dt> <dd>

在系統上掛接的磁片區陰影複製，可供管理該磁片區以外的進程使用。 裝入磁碟機號或目錄位置下的陰影複製磁片區稱為「本機公開」。 可透過共用存取的陰影複製磁片區 (除了用戶端可存取的陰影複製之外) 稱為「遠端公開」。 所有公開的陰影複製也會呈現陰影複製。 另請參閱 [*用戶端可存取陰影複製*](vssgloss-c.md)、 [*陰影複製*](vssgloss-s.md)。

</dd> </dl>

 

 



