---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: 'S (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92843e9277709a1138bc51b403089c932387e1b282e349c7907fc4cde88e9de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124478"
---
# <a name="s-volume-shadow-copy-service"></a>S (磁碟區陰影複製服務) 

[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**適用于備份的 selectability**
</dt> <dd>

如果在備份作業中明確包含的元件是選擇性的，則會將元件視為可供選擇進行備份。 如果 [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)結構的 **bSelectable** 成員值為 **true**，就會啟用 Selectability for backup。 元件的 selectability 沒有預設值可進行備份;寫入器一律必須明確設定此值。

寫入器也會使用 selectability 進行還原，以組織其元件參與還原作業。

另請參閱可 *選取的元件*、 *還原 selectability*、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**用於還原的 selectability**
</dt> <dd>

如果元件可以隱含地備份為元件集的一部分，則會被視為可選取的元件，然後在未設定其餘元件的情況下個別進行還原。 如果 [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)結構的 **bSelectableForRestore** 成員值為 **true**，就會啟用 Selectability for restore。 根據預設，元件的還原 selectability 為 **false**。 只有當元件尚未新增至備份檔案時，Selectability for restore 才有意義。

另請參閱可 *選取的元件*、 *selectability 以進行備份*、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**可選取的元件**
</dt> <dd>

如果在備份或還原作業中明確包含的元件是選擇性的，則會將其視為可選取。

Selectability for backup 和 Selectability for restore 彼此獨立，因此可以針對這兩項作業、還原和不備份，或備份和不還原來選取元件。

寫入器也會使用 selectability 將其元件組織成群組：

-   如果要備份或還原寫入器，則在邏輯路徑中沒有可選取之祖系的其元件，一律必須明確包含。
-   如果至少包含一個可選取的上階，其具有可選取之祖系的元件只會包含在備份或還原中。
-   沒有可選取之祖系的可選取元件只能在備份或還原作業中明確包含。
-   具有可選取上階的可選取元件可以明確地包含在備份或還原作業中，或者如果包含其中一個可選取的祖系，則可以隱含地包含這些元件。

另請參閱 [*元件*](vssgloss-c.md)、 *selectability for backup*、 *selectability for restore*、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**陰影複製**
</dt> <dd>

原始磁片區內容的唯讀時間點複本。 每個陰影複製是以持續性 GUID 為索引鍵。 也稱為磁片區陰影複製。 另請參閱 *陰影複製集*。

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**共用資料夾陰影複製**
</dt> <dd>

Windows 的功能，可使用 VSS 建立磁片區的輕量線上備份複本。 用戶端可以透過 Windows shell 存取這些備份，以查看舊版檔案和復原錯誤，而不需要完整還原。 另請參閱 [*用戶端可存取陰影複製*](vssgloss-c.md)。

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**陰影複製集**
</dt> <dd>

同時建立的磁片區陰影複製集合，並以一般的陰影複製集識別碼識別 (持續性 GUID) 值。 這是用來允許跨磁片區管理陰影複製作業的機制。 另請參閱 *陰影複製*。

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**軟體提供者**
</dt> <dd>

在檔案系統與磁片區管理員之間的軟體層級攔截 i/o 要求的提供者。 另請參閱 [*硬體提供者*](vssgloss-h.md)和 [*提供者*](vssgloss-p.md)。

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**子元件**
</dt> <dd>

任何具有邏輯路徑的元件，其中包含備份或還原) 父元件的可選取 (。 子元件必須有格式 {元件 \_ 名稱} \\ {子元件名稱} 的邏輯路徑 \_ 。 如果備份或還原) 上階的子元件可選取 (明確包含在備份或還原中，則子元件會隱含地包含在作業中。 隱含包含子群組件不會將其資料包含在備份元件檔中，而不論是否可針對 restore 或 Backup) 選擇 (。 另請參閱 [*元件*](vssgloss-c.md)、 [*邏輯路徑*](vssgloss-l.md)。

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**呈現的陰影複製**
</dt> <dd>

系統的 Mount Manager 命名空間可以看到陰影複製的磁片區，這表示 **FindFirstVolume** 和 **FindNextVolume** 可以找到它，並產生磁片區抵達和起飛通知。 所有公開的陰影複製也會呈現陰影複製。 但是，不需要公開所呈現的陰影複製。 如果陰影複製是可轉移的，則無法呈現。 另請參閱 [*公開陰影複製*](vssgloss-e.md)、可 [*轉移的陰影複製*](vssgloss-t.md)。

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**系統檔案保護**
</dt> <dd>

請參閱 [*Windows 檔案保護*](vssgloss-w.md)。

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**系統層級應用程式**
</dt> <dd>

指出 VSS 通知寫入器的時間點。 初始化為系統層級應用程式的寫入器會在寫入器初始化為前端層級應用程式或後端層級應用程式之後收到通知。 另請參閱 [*應用層級*](vssgloss-a.md)、 [*後端層級*](vssgloss-b.md)應用程式、 [*前端層級應用*](vssgloss-f.md)程式。

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**系統提供者**
</dt> <dd>

Windows 中提供的預設預先安裝提供者。

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**系統磁碟區資料夾**
</dt> <dd>

共用的目錄，儲存網域公用檔案的共用複本，也就是在網域中的所有網域控制站之間複寫的檔案。

</dd> </dl>

 

 



