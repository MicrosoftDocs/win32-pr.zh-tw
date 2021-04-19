---
description: 備份組是要備份的所有檔案、其位置，以及備份方式的清單。
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: 正在產生備份組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d9ecb90ac376aa9818b61e8dab65550ff8c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988745"
---
# <a name="generating-a-backup-set"></a><span data-ttu-id="467ea-103">正在產生備份組</span><span class="sxs-lookup"><span data-stu-id="467ea-103">Generating A Backup Set</span></span>

<span data-ttu-id="467ea-104">備份組是要備份的所有檔案、其位置，以及備份方式的清單。</span><span class="sxs-lookup"><span data-stu-id="467ea-104">A backup set is a list of all files to be backed up, their locations, and how to back them up.</span></span>

<span data-ttu-id="467ea-105">在 >ivssbackupcomponents 之後，要求者必須使用陰影複製磁片區上包含的檔案 [**：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 成功傳回，以產生要備份之檔案的完整清單。</span><span class="sxs-lookup"><span data-stu-id="467ea-105">A requester must make use of the files contained on the shadow-copied volumes after the [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) returns successfully to generate the full list of files to be backed up.</span></span>

<span data-ttu-id="467ea-106">此外，要求者必須處理某些檔案具有 [*替代路徑*](vssgloss-a.md) ，且已排除某些檔案的可能性。</span><span class="sxs-lookup"><span data-stu-id="467ea-106">In addition, a requester must deal with the possibility that some files have [*alternate paths*](vssgloss-a.md) and that some files have been excluded.</span></span>

<span data-ttu-id="467ea-107">用來選取要備份之檔案的演算法應該依照寫入 [*器實例*](vssgloss-w.md) 、個別元件的方式 (，如同還原期間的情況一樣：請參閱 [產生還原集](generating-a-restore-set.md)) ，並可執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="467ea-107">An algorithm for selecting files to back up should go on a [*writer instance*](vssgloss-w.md) by writer instance, component-by-component basis (as will be the case during restore; see [Generating a Restore Set](generating-a-restore-set.md)) and might proceed by doing the following:</span></span>

1.  <span data-ttu-id="467ea-108">判斷包含寫入器檔案和對應裝置物件的磁片區</span><span class="sxs-lookup"><span data-stu-id="467ea-108">Determining the volumes that contain the writer's files and the corresponding device objects</span></span>
2.  <span data-ttu-id="467ea-109">使用 [**IVssExamineWriterMetadata：：) GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)所傳回 [**之 IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)物件中所包含的檔案 [*集*](vssgloss-f.md)資訊 (，以建立明確排除的檔案清單（如有必要使用 **FindFileFirst**、 **FindFileFirstEx** 和 **FindNextFile**）。</span><span class="sxs-lookup"><span data-stu-id="467ea-109">Using the [*file set*](vssgloss-f.md) information (contained in [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) objects returned by [**IVssExamineWriterMetadata::GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)) to create a list of the explicitly excluded files, if necessary using **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>
3.  <span data-ttu-id="467ea-110">使用 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)逐一查看寫入器的所有元件。</span><span class="sxs-lookup"><span data-stu-id="467ea-110">Iterating over all of a writer's components, using [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).</span></span> <span data-ttu-id="467ea-111">如果選取了可選取的元件，請使用 [*邏輯路徑*](vssgloss-l.md) 來取得元件集內與其相關聯的其元件。</span><span class="sxs-lookup"><span data-stu-id="467ea-111">If a selectable component is selected, use [*logical path*](vssgloss-l.md) to obtain those nonselectable components associated with it in a component set.</span></span> <span data-ttu-id="467ea-112"> (，請參閱 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="467ea-112">(See [Working with Selectability and Logical Paths](working-with-selectability-and-logical-paths.md).)</span></span>
4.  <span data-ttu-id="467ea-113">使用 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)介面（對應至它所包含的每個元件）取得每個選取元件中包含的檔案 [*集*](vssgloss-f.md)。</span><span class="sxs-lookup"><span data-stu-id="467ea-113">Obtaining the [*file sets*](vssgloss-f.md) contained in each selected component by using the [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) interface corresponding to each component it contains.</span></span>
5.  <span data-ttu-id="467ea-114">從規格產生檔案清單（如有必要，請使用 **FindFileFirst**、 **FindFileFirstEx** 和 **FindNextFile**）。</span><span class="sxs-lookup"><span data-stu-id="467ea-114">Generating a list of files from the specifications—if necessary using **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>
6.  <span data-ttu-id="467ea-115">從元件資訊所產生清單中的每個檔案，針對上述產生的排除檔案清單進行檢查。</span><span class="sxs-lookup"><span data-stu-id="467ea-115">Checking each file in the list generated from component information against the list of excluded files generated above.</span></span> <span data-ttu-id="467ea-116">這應該使用 [**IVssWMFiledesc：：) GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) 所傳回之檔案 (的預設路徑，而不是 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) 所傳回的替代路徑。</span><span class="sxs-lookup"><span data-stu-id="467ea-116">This should be done using the default path for the file (returned by [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), not by the alternate path returned by [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)).</span></span> <span data-ttu-id="467ea-117">如果檔案符合排除的清單，將不會備份。</span><span class="sxs-lookup"><span data-stu-id="467ea-117">If the file matches the excluded list, it will not be backed up.</span></span>
7.  <span data-ttu-id="467ea-118">選擇要用來備份 (的實際位置（若已設定）) </span><span class="sxs-lookup"><span data-stu-id="467ea-118">Choosing the actual location from which to back up (using the alternate path if it was set)</span></span>
8.  <span data-ttu-id="467ea-119">此時，可以使用完整的檔案及其位置清單，而且可以開始備份。</span><span class="sxs-lookup"><span data-stu-id="467ea-119">At this point, a full list of files and their locations is available and a backup can begin.</span></span>

<span data-ttu-id="467ea-120">針對系統上的所有寫入器產生初始備份組之後，要求者接著會檢查下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="467ea-120">After an initial backup set has been generated for all writers that are present on the system, the requester then checks the following registry key:</span></span>

<span data-ttu-id="467ea-121">**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**</span><span class="sxs-lookup"><span data-stu-id="467ea-121">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\FilesNotToBackup**</span></span>

<span data-ttu-id="467ea-122">要求者會使用此機碼下的子機碼，如下所示：</span><span class="sxs-lookup"><span data-stu-id="467ea-122">The requester uses the subkeys under this key as follows:</span></span>

-   <span data-ttu-id="467ea-123">如果系統上有寫入器，且有一個子機碼的名稱符合寫入器的名稱，則必須忽略該子機碼。</span><span class="sxs-lookup"><span data-stu-id="467ea-123">If a writer is present on the system, and there is a subkey whose name matches the writer's name, that subkey must be ignored.</span></span>
-   <span data-ttu-id="467ea-124">如果寫入器存在於系統上，但目前不存在於備份組內，而且有相符的子機碼，就會排除子機碼資料中指定的任何檔案，而且必須從備份組移除。</span><span class="sxs-lookup"><span data-stu-id="467ea-124">If a writer was present on the system but is currently absent from the backup set, and there is a matching subkey, any files specified in the subkey data are excluded and must be removed from the backup set.</span></span>
-   <span data-ttu-id="467ea-125">備份應用程式會建立多個 \_ SZ 值，其中包含不得備份之檔案的檔案規格清單，藉以將檔案新增至子機碼資料。</span><span class="sxs-lookup"><span data-stu-id="467ea-125">The backup application adds files to the subkey data by creating a MULTI\_SZ value containing a list of file specifications for the files that must not be backed up.</span></span> <span data-ttu-id="467ea-126">多個 SZ 值中的每個字串 \_ 都應該包含一個檔案規格。</span><span class="sxs-lookup"><span data-stu-id="467ea-126">Each string in the MULTI\_SZ value should contain one file specification.</span></span>
-   <span data-ttu-id="467ea-127">檔案規格可以包含？</span><span class="sxs-lookup"><span data-stu-id="467ea-127">File specifications can contain the ?</span></span> <span data-ttu-id="467ea-128">和 \* 萬用字元。</span><span class="sxs-lookup"><span data-stu-id="467ea-128">and \* wildcard characters.</span></span> <span data-ttu-id="467ea-129">您可以藉由將/s 附加至結尾，將規格設為遞迴。</span><span class="sxs-lookup"><span data-stu-id="467ea-129">A specification can be made recursive by appending /s to the end.</span></span> <span data-ttu-id="467ea-130">例如，指定 "% TEMP% \\ \* /s" 會導致% temp% 目錄及其所有子目錄中的所有檔案都不會進行備份。</span><span class="sxs-lookup"><span data-stu-id="467ea-130">For example, specifying "%TEMP%\\\* /s" causes all files in the %TEMP% directory and all of its subdirectories not to be backed up.</span></span>

 

 



