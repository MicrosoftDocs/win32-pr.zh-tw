---
description: 執行中系統上的檔案還原可能會有問題。  (寫入器執行應用程式時，請務必) 指出還原期間發生問題時該怎麼做，例如，如果正在還原的檔案目前正在使用中。
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: VSS 還原設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113177"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="0ca67-104">VSS 還原設定</span><span class="sxs-lookup"><span data-stu-id="0ca67-104">VSS Restore Configurations</span></span>

<span data-ttu-id="0ca67-105">執行中系統上的檔案還原可能會有問題。</span><span class="sxs-lookup"><span data-stu-id="0ca67-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="0ca67-106"> (寫入器執行應用程式時，請務必) 指出還原期間發生問題時該怎麼做，例如，如果正在還原的檔案目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="0ca67-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="0ca67-107">在 VSS 下，寫入器有兩種互補的方式可管理還原：[*還原方法*](vssgloss-r.md) 和 [*還原目標*](vssgloss-r.md)。</span><span class="sxs-lookup"><span data-stu-id="0ca67-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="0ca67-108">此外，要求者可以選擇將檔案還原至先前未指定的位置，並通知寫入器 (參閱 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)) 。</span><span class="sxs-lookup"><span data-stu-id="0ca67-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="0ca67-109">Restore 方法 (也會呼叫原始還原目標) 是由寫入器在備份時間指定的，並且會設定要用來還原未來所有元件之方法的全寫入器定義。</span><span class="sxs-lookup"><span data-stu-id="0ca67-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="0ca67-110">寫入器管理的所有檔案和元件都會共用相同的還原方法。</span><span class="sxs-lookup"><span data-stu-id="0ca67-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="0ca67-111">還原目標可讓寫入器變更在還原時還原特定元件的方式。</span><span class="sxs-lookup"><span data-stu-id="0ca67-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="0ca67-112">不同于 restore 方法，會為元件集定義還原目標。</span><span class="sxs-lookup"><span data-stu-id="0ca67-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="0ca67-113">您可以在下列主題中找到有關還原方法和還原目標使用方式的詳細討論：</span><span class="sxs-lookup"><span data-stu-id="0ca67-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="0ca67-114">VSS 還原狀態</span><span class="sxs-lookup"><span data-stu-id="0ca67-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="0ca67-115">設定 VSS 還原方法</span><span class="sxs-lookup"><span data-stu-id="0ca67-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="0ca67-116">設定 VSS 還原目標</span><span class="sxs-lookup"><span data-stu-id="0ca67-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="0ca67-117">設定 VSS 還原選項</span><span class="sxs-lookup"><span data-stu-id="0ca67-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="0ca67-118"> (如需未使用這些機制之還原的相關資訊，請參閱不 [含寫入器參與的還原](restores-without-writer-participation.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="0ca67-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



