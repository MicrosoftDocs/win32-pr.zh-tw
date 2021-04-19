---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: " (磁碟區陰影複製服務) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991729"
---
# <a name="a-volume-shadow-copy-service"></a> (磁碟區陰影複製服務) 

[B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**中止事件**
</dt> <dd>

由磁碟區陰影複製服務發出的 VSS 事件，表示已中止符合規範的備份或還原作業。 事件處理常式是 **CVssWriter：： OnAbort**。

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

Active Directory 服務 (ADSI) 是一種以 COM 為基礎的服務，它提供了一種機制來尋找、識別及存取分散式運算環境系統中可用的使用者和資源。 尤其是，Active Directory 服務是用來管理企業目錄資訊，以供 Windows 網域伺服器散發。

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**替代位置對應**
</dt> <dd>

在特定情況下，檔案可能還原的路徑，而不是檔案的原始路徑。 一般而言，不會針對單一定義完善的檔案定義替代位置對應，而是針對路徑/檔案規格組定義，而且可能是遞迴的。

替代位置對應只會在還原作業期間使用，不應該與替代路徑混淆，後者只會在備份作業期間使用。 另請參閱 *替代路徑*。

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**替代路徑**
</dt> <dd>

在備份作業期間， **IVssWMFiledesc** 介面的實例所處理的路徑/檔案規格組 () 在其檔案描述項 (如 **IVssWMFiledesc：： GetAlternateLocation**) 所傳回的非 Null 時，則稱為具有替代路徑。 這是來自此路徑，而不是預設的指定路徑，而是在備份磁片區時複製該檔案。

替代路徑只會在備份作業期間使用，不應與替代位置對應混淆。 只有在還原作業期間，才會使用替代位置對應。 另請參閱 *替代位置對應*。

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**應用層級**
</dt> <dd>

由 VSS 用來指出建立陰影複製的過程中，寫入器會通知凍結的時間點。 另請參閱 [*後端層級應用程式*](vssgloss-b.md)、 [*凍結*](vssgloss-f.md)、 [*前端層級應用程式*](vssgloss-f.md)、 [*陰影複製*](vssgloss-s.md)、 [*系統層級應用程式*](vssgloss-s.md)、 [*寫入器*](vssgloss-w.md)。

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**自動復原陰影複製**
</dt> <dd>

由寫入器進行額外處理，以完全一致的方式進行備份或資料採礦動作的陰影複製 (例如，復原在建立陰影複製時尚未完成的所有交易。 ) 這可由寫入器起始，方法是在 **vss \_ COMPONENTINFO** 結構的 **dwComponentFlags** 成員中指定適當的旗標，或是由要求者藉由將 **vss \_ VOLSNAP \_ ATTR \_ 復原復原 \_** 旗標新增至陰影複製的內容，藉以指定適當的旗 **\_ \_ 標**。 自動復原允許在唯讀磁片區上使用陰影複製的資料、進行資料採礦、部分還原 (例如資料庫) 中的選取專案，或其他用途。

另請參閱可 [*轉移的陰影複製*](vssgloss-t.md)。

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**自動發行陰影複製**
</dt> <dd>

當備份作業終止時，將會刪除的陰影複製。 以程式設計的方式，這表示在釋放 **>ivssbackupcomponents** 介面時，將會刪除陰影複製。 自動發行陰影複製不可以是持續性。

依預設，所有陰影複製都會自動釋放。 另請參閱 [*持續陰影複製*](vssgloss-p.md)、可 [*轉移的陰影複製*](vssgloss-t.md)。

</dd> </dl>

 

 



