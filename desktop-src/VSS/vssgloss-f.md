---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: 'F (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690448"
---
# <a name="f-volume-shadow-copy-service"></a>F (磁碟區陰影複製服務) 

[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**檔案群組元件**
</dt> <dd>

一組檔案，而非做為資料庫的檔案，並由寫入器定義，以在備份和還原作業期間以一個單位來處理。 另請參閱 [*元件*](vssgloss-c.md)、 [*資料庫元件*](vssgloss-d.md)。

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**檔案集**
</dt> <dd>

描述檔案或檔案群組之一的路徑、檔案規格和遞迴旗標的組合。 例如，檔案會新增至檔集中的元件。

除非另有指示，否則檔案集的路徑是標準 Windows 路徑，而且可以包含環境變數 (例如% SystemRoot% ) ，但不能包含萬用字元。 路徑結尾不需要使用反斜線 ( " \\ " ) 。 它是由取得此資訊的應用程式所組成，以進行檢查。

檔案組中包含的檔案規格會指出檔案的名稱或包含的檔案名。 此檔案規格不能包含目錄規格 (例如，沒有反斜線) ，但可以包含？ 和 \* 萬用字元。

遞迴標記是一個布林值，用來指定是否應將檔案集的路徑視為只有單一目錄，或者是否表示要以遞迴方式進行的目錄階層。 如果路徑被視為要以遞迴方式進行往返的目錄階層，則布林值為 **true** ，否則為 **false** 。

檔案集的相關資訊會透過 **IVssWMFiledesc** 介面的實例傳回，而且可以包含其他資訊，包括替代路徑、替代位置對應和檔案層級架構支援設定。

另請參閱 [*替代路徑*](vssgloss-a.md)、 [*替代位置對應*](vssgloss-a.md)、 [*元件*](vssgloss-c.md)、檔案 *規格*。

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**檔案規格**
</dt> <dd>

用來比對目錄內的檔案，並定義檔案集。 它不能包含目錄規格 (例如，沒有反斜線) ，但它可以包含？ 和 \* 萬用字元。

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**檔案複寫服務**
</dt> <dd>

用來在多餘的系統磁碟區 (SysVol) 目錄中複寫系統檔案，以支援檔案系統的存留能力，特別是針對分散式檔案系統。

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**凍結**
</dt> <dd>

當所有寫入器已將其寫入排清至磁片區，但未起始額外寫入時，陰影複製建立程式期間的一段時間。

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**凍結事件**
</dt> <dd>

VSS 事件，指出陰影複製凍結正在進行中。 另請參閱 *凍結*、 [*陰影複製*](vssgloss-s.md)。

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**前端層級應用程式**
</dt> <dd>

指示寫入器收到 VSS 凍結的通知點。 初始化為前端層級應用程式的寫入器會在寫入器初始化為後端層級應用程式或系統層級應用程式之前收到通知。 另請參閱 [*應用層級*](vssgloss-a.md)、 [*後端層級應用程式*](vssgloss-b.md)、 [*系統層級應用程式*](vssgloss-s.md)、 [*寫入器*](vssgloss-w.md)。

</dd> </dl>

 

 



