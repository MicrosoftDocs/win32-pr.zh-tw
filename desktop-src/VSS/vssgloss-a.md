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
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="49a49-103"> (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="49a49-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="49a49-104">[B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="49a49-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="49a49-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**中止事件**</span><span class="sxs-lookup"><span data-stu-id="49a49-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-106">由磁碟區陰影複製服務發出的 VSS 事件，表示已中止符合規範的備份或還原作業。</span><span class="sxs-lookup"><span data-stu-id="49a49-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="49a49-107">事件處理常式是 **CVssWriter：： OnAbort**。</span><span class="sxs-lookup"><span data-stu-id="49a49-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="49a49-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="49a49-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-109">Active Directory 服務 (ADSI) 是一種以 COM 為基礎的服務，它提供了一種機制來尋找、識別及存取分散式運算環境系統中可用的使用者和資源。</span><span class="sxs-lookup"><span data-stu-id="49a49-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="49a49-110">尤其是，Active Directory 服務是用來管理企業目錄資訊，以供 Windows 網域伺服器散發。</span><span class="sxs-lookup"><span data-stu-id="49a49-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="49a49-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**替代位置對應**</span><span class="sxs-lookup"><span data-stu-id="49a49-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-112">在特定情況下，檔案可能還原的路徑，而不是檔案的原始路徑。</span><span class="sxs-lookup"><span data-stu-id="49a49-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="49a49-113">一般而言，不會針對單一定義完善的檔案定義替代位置對應，而是針對路徑/檔案規格組定義，而且可能是遞迴的。</span><span class="sxs-lookup"><span data-stu-id="49a49-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="49a49-114">替代位置對應只會在還原作業期間使用，不應該與替代路徑混淆，後者只會在備份作業期間使用。</span><span class="sxs-lookup"><span data-stu-id="49a49-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="49a49-115">另請參閱 *替代路徑*。</span><span class="sxs-lookup"><span data-stu-id="49a49-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="49a49-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**替代路徑**</span><span class="sxs-lookup"><span data-stu-id="49a49-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-117">在備份作業期間， **IVssWMFiledesc** 介面的實例所處理的路徑/檔案規格組 () 在其檔案描述項 (如 **IVssWMFiledesc：： GetAlternateLocation**) 所傳回的非 Null 時，則稱為具有替代路徑。</span><span class="sxs-lookup"><span data-stu-id="49a49-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="49a49-118">這是來自此路徑，而不是預設的指定路徑，而是在備份磁片區時複製該檔案。</span><span class="sxs-lookup"><span data-stu-id="49a49-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="49a49-119">替代路徑只會在備份作業期間使用，不應與替代位置對應混淆。</span><span class="sxs-lookup"><span data-stu-id="49a49-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="49a49-120">只有在還原作業期間，才會使用替代位置對應。</span><span class="sxs-lookup"><span data-stu-id="49a49-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="49a49-121">另請參閱 *替代位置對應*。</span><span class="sxs-lookup"><span data-stu-id="49a49-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="49a49-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**應用層級**</span><span class="sxs-lookup"><span data-stu-id="49a49-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-123">由 VSS 用來指出建立陰影複製的過程中，寫入器會通知凍結的時間點。</span><span class="sxs-lookup"><span data-stu-id="49a49-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="49a49-124">另請參閱 [*後端層級應用程式*](vssgloss-b.md)、 [*凍結*](vssgloss-f.md)、 [*前端層級應用程式*](vssgloss-f.md)、 [*陰影複製*](vssgloss-s.md)、 [*系統層級應用程式*](vssgloss-s.md)、 [*寫入器*](vssgloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="49a49-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="49a49-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**自動復原陰影複製**</span><span class="sxs-lookup"><span data-stu-id="49a49-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-126">由寫入器進行額外處理，以完全一致的方式進行備份或資料採礦動作的陰影複製 (例如，復原在建立陰影複製時尚未完成的所有交易。 ) 這可由寫入器起始，方法是在 **vss \_ COMPONENTINFO** 結構的 **dwComponentFlags** 成員中指定適當的旗標，或是由要求者藉由將 **vss \_ VOLSNAP \_ ATTR \_ 復原復原 \_** 旗標新增至陰影複製的內容，藉以指定適當的旗 **\_ \_ 標**。</span><span class="sxs-lookup"><span data-stu-id="49a49-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="49a49-127">自動復原允許在唯讀磁片區上使用陰影複製的資料、進行資料採礦、部分還原 (例如資料庫) 中的選取專案，或其他用途。</span><span class="sxs-lookup"><span data-stu-id="49a49-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="49a49-128">另請參閱可 [*轉移的陰影複製*](vssgloss-t.md)。</span><span class="sxs-lookup"><span data-stu-id="49a49-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="49a49-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**自動發行陰影複製**</span><span class="sxs-lookup"><span data-stu-id="49a49-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="49a49-130">當備份作業終止時，將會刪除的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="49a49-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="49a49-131">以程式設計的方式，這表示在釋放 **>ivssbackupcomponents** 介面時，將會刪除陰影複製。</span><span class="sxs-lookup"><span data-stu-id="49a49-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="49a49-132">自動發行陰影複製不可以是持續性。</span><span class="sxs-lookup"><span data-stu-id="49a49-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="49a49-133">依預設，所有陰影複製都會自動釋放。</span><span class="sxs-lookup"><span data-stu-id="49a49-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="49a49-134">另請參閱 [*持續陰影複製*](vssgloss-p.md)、可 [*轉移的陰影複製*](vssgloss-t.md)。</span><span class="sxs-lookup"><span data-stu-id="49a49-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



