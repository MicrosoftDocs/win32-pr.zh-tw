---
description: Windows Server 2003 版的 VSS 已不再支援下列各項：
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: 從 Windows Server 2003 移除的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986875"
---
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="988f9-103">從 Windows Server 2003 移除的功能</span><span class="sxs-lookup"><span data-stu-id="988f9-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="988f9-104">Windows Server 2003 版的 VSS 已不再支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="988f9-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="988f9-105">寫入器無法在還原作業)  ([*新的目標位置*](vssgloss-n.md) ，指定新的檔案還原目的地。</span><span class="sxs-lookup"><span data-stu-id="988f9-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="988f9-106">不再支援將公開的陰影複製重新掛接為可寫入的磁片區。</span><span class="sxs-lookup"><span data-stu-id="988f9-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="988f9-107">**>ivssbackupcomponents：： RemountReadWrite** 方法已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="988f9-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="988f9-108">寫入器無法 (使用 [**IVssCreateWriterMetadata：： AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)) 指定明確包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="988f9-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="988f9-109">您只能使用 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)，將檔案加入至元件中。</span><span class="sxs-lookup"><span data-stu-id="988f9-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="988f9-110">您仍可使用 [**IVssCreateWriterMetadata：： AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)，以明確地從元件中排除檔案。</span><span class="sxs-lookup"><span data-stu-id="988f9-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



