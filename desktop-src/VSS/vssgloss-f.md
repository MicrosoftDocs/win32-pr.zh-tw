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
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="82225-103">F (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="82225-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="82225-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="82225-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="82225-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**檔案群組元件**</span><span class="sxs-lookup"><span data-stu-id="82225-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="82225-106">一組檔案，而非做為資料庫的檔案，並由寫入器定義，以在備份和還原作業期間以一個單位來處理。</span><span class="sxs-lookup"><span data-stu-id="82225-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="82225-107">另請參閱 [*元件*](vssgloss-c.md)、 [*資料庫元件*](vssgloss-d.md)。</span><span class="sxs-lookup"><span data-stu-id="82225-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="82225-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**檔案集**</span><span class="sxs-lookup"><span data-stu-id="82225-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="82225-109">描述檔案或檔案群組之一的路徑、檔案規格和遞迴旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="82225-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="82225-110">例如，檔案會新增至檔集中的元件。</span><span class="sxs-lookup"><span data-stu-id="82225-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="82225-111">除非另有指示，否則檔案集的路徑是標準 Windows 路徑，而且可以包含環境變數 (例如% SystemRoot% ) ，但不能包含萬用字元。</span><span class="sxs-lookup"><span data-stu-id="82225-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="82225-112">路徑結尾不需要使用反斜線 ( " \\ " ) 。</span><span class="sxs-lookup"><span data-stu-id="82225-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="82225-113">它是由取得此資訊的應用程式所組成，以進行檢查。</span><span class="sxs-lookup"><span data-stu-id="82225-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="82225-114">檔案組中包含的檔案規格會指出檔案的名稱或包含的檔案名。</span><span class="sxs-lookup"><span data-stu-id="82225-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="82225-115">此檔案規格不能包含目錄規格 (例如，沒有反斜線) ，但可以包含？</span><span class="sxs-lookup"><span data-stu-id="82225-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="82225-116">和 \* 萬用字元。</span><span class="sxs-lookup"><span data-stu-id="82225-116">and \* wildcard characters.</span></span>

<span data-ttu-id="82225-117">遞迴標記是一個布林值，用來指定是否應將檔案集的路徑視為只有單一目錄，或者是否表示要以遞迴方式進行的目錄階層。</span><span class="sxs-lookup"><span data-stu-id="82225-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="82225-118">如果路徑被視為要以遞迴方式進行往返的目錄階層，則布林值為 **true** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="82225-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="82225-119">檔案集的相關資訊會透過 **IVssWMFiledesc** 介面的實例傳回，而且可以包含其他資訊，包括替代路徑、替代位置對應和檔案層級架構支援設定。</span><span class="sxs-lookup"><span data-stu-id="82225-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="82225-120">另請參閱 [*替代路徑*](vssgloss-a.md)、 [*替代位置對應*](vssgloss-a.md)、 [*元件*](vssgloss-c.md)、檔案 *規格*。</span><span class="sxs-lookup"><span data-stu-id="82225-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="82225-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**檔案規格**</span><span class="sxs-lookup"><span data-stu-id="82225-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="82225-122">用來比對目錄內的檔案，並定義檔案集。</span><span class="sxs-lookup"><span data-stu-id="82225-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="82225-123">它不能包含目錄規格 (例如，沒有反斜線) ，但它可以包含？</span><span class="sxs-lookup"><span data-stu-id="82225-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="82225-124">和 \* 萬用字元。</span><span class="sxs-lookup"><span data-stu-id="82225-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="82225-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**檔案複寫服務**</span><span class="sxs-lookup"><span data-stu-id="82225-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="82225-126">用來在多餘的系統磁碟區 (SysVol) 目錄中複寫系統檔案，以支援檔案系統的存留能力，特別是針對分散式檔案系統。</span><span class="sxs-lookup"><span data-stu-id="82225-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="82225-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**凍結**</span><span class="sxs-lookup"><span data-stu-id="82225-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="82225-128">當所有寫入器已將其寫入排清至磁片區，但未起始額外寫入時，陰影複製建立程式期間的一段時間。</span><span class="sxs-lookup"><span data-stu-id="82225-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="82225-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**凍結事件**</span><span class="sxs-lookup"><span data-stu-id="82225-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="82225-130">VSS 事件，指出陰影複製凍結正在進行中。</span><span class="sxs-lookup"><span data-stu-id="82225-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="82225-131">另請參閱 *凍結*、 [*陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="82225-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="82225-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**前端層級應用程式**</span><span class="sxs-lookup"><span data-stu-id="82225-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="82225-133">指示寫入器收到 VSS 凍結的通知點。</span><span class="sxs-lookup"><span data-stu-id="82225-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="82225-134">初始化為前端層級應用程式的寫入器會在寫入器初始化為後端層級應用程式或系統層級應用程式之前收到通知。</span><span class="sxs-lookup"><span data-stu-id="82225-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="82225-135">另請參閱 [*應用層級*](vssgloss-a.md)、 [*後端層級應用程式*](vssgloss-b.md)、 [*系統層級應用程式*](vssgloss-s.md)、 [*寫入器*](vssgloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="82225-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



