---
description: 在 VSS 下處理備份時，要求者和寫入器會一起運作，以產生穩定的系統映射來備份資料，而這需要協調和建立目前系統的陰影複製。
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: 在 VSS 下處理還原的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985637"
---
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="7fdb4-103">在 VSS 下處理還原的總覽</span><span class="sxs-lookup"><span data-stu-id="7fdb4-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="7fdb4-104">在 VSS 下處理備份時，要求者和寫入器會一起運作，以產生穩定的系統映射來備份資料，而這需要協調和建立目前系統的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="7fdb4-105">相較于 VSS 備份，要求者和寫入器的目的是要產生穩定的系統映射，以從中複製資料，以 VSS 為基礎的還原目標是將檔案以最實用的方式傳回磁片，以對目前在系統上執行的應用程式)  (的寫入器。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="7fdb4-106">這不需要穩定的系統映射，因此不需要陰影複製。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="7fdb4-107">相反地，注意的重點是要避免寫入器活動中斷、防止在磁片上建立不一致的資料集，並允許寫入器在必要時評估及合併資料所需的範圍。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="7fdb4-108">如同備份作業，VSS 還原需要存取備份元件檔和寫入元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="7fdb4-109">這些檔通常不會藉由查詢執行中的應用程式取得，而是從備份媒體上儲存為 XML 檔的版本中取出。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="7fdb4-110">就像備份作業期間一樣，寫入器元資料檔案仍會保留唯讀物件，且 (取出之後) 備份元件檔仍可進行修改。</span><span class="sxs-lookup"><span data-stu-id="7fdb4-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="7fdb4-111">修改備份元件檔可讓寫入器和要求者進行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7fdb4-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="7fdb4-112">使用 [*還原目標*](vssgloss-r.md)覆寫 [*restore 方法*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="7fdb4-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="7fdb4-113">使用 [*替代位置* 對應](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="7fdb4-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="7fdb4-114">將檔案還原至磁片上的新位置</span><span class="sxs-lookup"><span data-stu-id="7fdb4-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="7fdb4-115">在備份期間使用不同的選取規則</span><span class="sxs-lookup"><span data-stu-id="7fdb4-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="7fdb4-116">為了更充分了解執行還原所牽涉到的基本工作，將此概觀細分成下列主題會很有用：</span><span class="sxs-lookup"><span data-stu-id="7fdb4-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="7fdb4-117">還原初始化的總覽</span><span class="sxs-lookup"><span data-stu-id="7fdb4-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="7fdb4-118">準備還原的總覽</span><span class="sxs-lookup"><span data-stu-id="7fdb4-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="7fdb4-119">實際檔案還原的總覽</span><span class="sxs-lookup"><span data-stu-id="7fdb4-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="7fdb4-120">還原清除和終止的總覽</span><span class="sxs-lookup"><span data-stu-id="7fdb4-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



