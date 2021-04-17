---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: 'W (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511505"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="d1623-103">W (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="d1623-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="d1623-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) W X [](vssgloss-v.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="d1623-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d1623-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows 檔案保護**</span><span class="sxs-lookup"><span data-stu-id="d1623-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="d1623-106">保護特殊作業系統檔案的系統服務。</span><span class="sxs-lookup"><span data-stu-id="d1623-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="d1623-107">如果刪除或覆寫這些檔案的其中一個，Windows 檔案保護會以原始檔取代其快取中的檔案。</span><span class="sxs-lookup"><span data-stu-id="d1623-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="d1623-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**作家**</span><span class="sxs-lookup"><span data-stu-id="d1623-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="d1623-109">此應用程式會使用與 VSS 陰影複製和陰影複製相關的作業（例如備份和還原）來協調其 i/o 作業 (例如備份和還原) ，如此一來，陰影複製的磁片區上所含的資料就會處於一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="d1623-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="d1623-110">為了支援此協調，寫入器必須執行衍生自抽象基類 **CVssWriter** 的類別實例，以與 VSS 基礎結構進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d1623-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="d1623-111">另請參閱 [*陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="d1623-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1623-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**寫入器類別**</span><span class="sxs-lookup"><span data-stu-id="d1623-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="d1623-113">全域唯一識別碼 (GUID) 在初始化期間由寫入器提供，表示它屬於指定的寫入器類型。</span><span class="sxs-lookup"><span data-stu-id="d1623-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="d1623-114">例如，多個寫入器的執行可以共用相同的寫入器類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1623-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="d1623-115">相同類別的寫入器可能會由其寫入器實例來區分。</span><span class="sxs-lookup"><span data-stu-id="d1623-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="d1623-116">應用程式開發人員可以指定寫入器類別。</span><span class="sxs-lookup"><span data-stu-id="d1623-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="d1623-117">另請參閱 *寫入器實例*。</span><span class="sxs-lookup"><span data-stu-id="d1623-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="d1623-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**寫入器實例**</span><span class="sxs-lookup"><span data-stu-id="d1623-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="d1623-119">全域唯一識別碼 (GUID) 為系統上執行的每個寫入器處理常式提供。</span><span class="sxs-lookup"><span data-stu-id="d1623-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="d1623-120">每次寫入器啟動時，就會產生寫入器實例的唯一值。</span><span class="sxs-lookup"><span data-stu-id="d1623-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="d1623-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**寫入器元資料檔案**</span><span class="sxs-lookup"><span data-stu-id="d1623-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="d1623-122">寫入器所建立的 XML 檔 (使用 **IVssCreateWriterMetadata** 介面) 包含寫入器的狀態和元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d1623-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="d1623-123">要求者可以在執行還原或備份作業時，使用 **IVssExamineWriterMetadata** 介面) 來查詢寫入器元資料檔案 (。</span><span class="sxs-lookup"><span data-stu-id="d1623-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="d1623-124">寫入器元資料檔案包含所有寫入器元件的清單，其中任何一項都可能參與備份。</span><span class="sxs-lookup"><span data-stu-id="d1623-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="d1623-125">這與要求者的備份元件檔不同，其中只包含針對備份或還原作業明確包含的元件。</span><span class="sxs-lookup"><span data-stu-id="d1623-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="d1623-126">一旦建立之後，就應該將寫入器元資料檔案視為唯讀物件。</span><span class="sxs-lookup"><span data-stu-id="d1623-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="d1623-127">您可以將它儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="d1623-127">It can be saved to disk.</span></span> <span data-ttu-id="d1623-128">另請參閱 [*備份元件檔*](vssgloss-b.md)、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。</span><span class="sxs-lookup"><span data-stu-id="d1623-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



