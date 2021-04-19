---
description: 還原選項可讓要求者將自訂的還原選項傳達給寫入器。
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: 設定 VSS 還原選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980801"
---
# <a name="setting-vss-restore-options"></a><span data-ttu-id="344e0-103">設定 VSS 還原選項</span><span class="sxs-lookup"><span data-stu-id="344e0-103">Setting VSS Restore Options</span></span>

<span data-ttu-id="344e0-104">還原選項可讓要求者將自訂的還原選項傳達給寫入器。</span><span class="sxs-lookup"><span data-stu-id="344e0-104">Restore options allow requesters to communicate customized restore options to writers.</span></span>

## <a name="restore-options"></a><span data-ttu-id="344e0-105">還原選項</span><span class="sxs-lookup"><span data-stu-id="344e0-105">Restore Options</span></span>

<span data-ttu-id="344e0-106">將還原選項的格式標準化，可讓寫入器和要求者處理常見的自訂要求。</span><span class="sxs-lookup"><span data-stu-id="344e0-106">Standardizing the format of the restore options allow writers and requesters to handle common custom requests.</span></span> <span data-ttu-id="344e0-107">在呼叫 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)方法之前，會針對每個選取的備份元件呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)方法，以針對要求者設定還原選項。</span><span class="sxs-lookup"><span data-stu-id="344e0-107">Restore options are set by the requester by calling the [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method up to once per selected-for-backup component before calling the [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) method.</span></span> <span data-ttu-id="344e0-108">在 *wszRestoreOptions* 參數中傳遞給 **SetRestoreOptions** 方法的字串可以包含多個值，如下所述。</span><span class="sxs-lookup"><span data-stu-id="344e0-108">The string passed in the *wszRestoreOptions* parameter to the **SetRestoreOptions** method can contain multiple values, as described below.</span></span>

## <a name="format"></a><span data-ttu-id="344e0-109">格式</span><span class="sxs-lookup"><span data-stu-id="344e0-109">Format</span></span>

<span data-ttu-id="344e0-110">還原選項的格式為一或多個以逗號分隔的名稱/值組，而且名稱會選擇性地加上其所套用的子元件名稱。</span><span class="sxs-lookup"><span data-stu-id="344e0-110">The format of restore options, is one or more comma-separated name/value pairs, and the name is optionally prefixed with the name of the subcomponent to which it applies.</span></span> <span data-ttu-id="344e0-111">元件名稱和選項名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="344e0-111">The component names and option names are case-insensitive.</span></span> <span data-ttu-id="344e0-112">值的區分大小寫取決於寫入器。</span><span class="sxs-lookup"><span data-stu-id="344e0-112">The case-sensitivity of the values is determined by the writer.</span></span> <span data-ttu-id="344e0-113">例如：</span><span class="sxs-lookup"><span data-stu-id="344e0-113">For example:</span></span>

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

<span data-ttu-id="344e0-114">在此範例中，"Option1" 僅適用于 "Child1" 子元件和其子系，"Option2" 適用于所有元件及其下階，而 "Option3" 只適用于 "Child2 \\ Grandchild3" 子元件及其下階。</span><span class="sxs-lookup"><span data-stu-id="344e0-114">In this example, "Option1" only applies to the "Child1" subcomponent and its descendants, "Option2" applies to all components and their descendants, and "Option3" applies only to the "Child2\\Grandchild3" subcomponents and its descendants.</span></span>

<span data-ttu-id="344e0-115">[**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)方法只能在可選取要進行備份的元件上呼叫，而子節點可能無法針對備份進行選取，它們可能可供還原。</span><span class="sxs-lookup"><span data-stu-id="344e0-115">The [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) method can only be called on components that are selectable for backup, while descendant nodes may not be selectable for backup, they may be selectable for restore.</span></span>

## <a name="common-restore-options"></a><span data-ttu-id="344e0-116">一般還原選項</span><span class="sxs-lookup"><span data-stu-id="344e0-116">Common Restore Options</span></span>

<span data-ttu-id="344e0-117">這些常見的還原選項已定義為增加寫入器與要求者之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="344e0-117">These common restore options have been defined to increase interoperability between writers and requesters.</span></span>

-   <span data-ttu-id="344e0-118">權威</span><span class="sxs-lookup"><span data-stu-id="344e0-118">Authoritative</span></span>

    <span data-ttu-id="344e0-119">「授權」選項支援多個「專案」值，但只能有一個「全部」值。</span><span class="sxs-lookup"><span data-stu-id="344e0-119">The "Authoritative" option supports multiple "Item" values, but only one "All" value.</span></span>

    <span data-ttu-id="344e0-120">整個元件都具有授權。</span><span class="sxs-lookup"><span data-stu-id="344e0-120">This entire component is authoritative.</span></span>

    ``` syntax
    "Authoritative"="All"
    ```

    <span data-ttu-id="344e0-121">只有指定的專案具有授權。</span><span class="sxs-lookup"><span data-stu-id="344e0-121">Only the specified item is authoritative.</span></span> <span data-ttu-id="344e0-122">命名專案的格式是由寫入器定義。</span><span class="sxs-lookup"><span data-stu-id="344e0-122">The format of the named item is defined by the writer.</span></span> <span data-ttu-id="344e0-123">常見的指定是 " \* " 表示所有檔案，"..."表示指定元件的所有檔案和子目錄。</span><span class="sxs-lookup"><span data-stu-id="344e0-123">Common designations are "\*" to indicate all files, "..." to indicate all files and subdirectories of the specified component.</span></span>

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   <span data-ttu-id="344e0-124">向前復原</span><span class="sxs-lookup"><span data-stu-id="344e0-124">Roll Forward</span></span>

    <span data-ttu-id="344e0-125">還原資料庫之後，寫入器通常會透過記錄向前復原，讓資料庫保持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="344e0-125">After a database is restored, writers usually roll forward through logs to bring the database up to date.</span></span> <span data-ttu-id="344e0-126">在增量或差異還原的情況下，要求者會使用 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) 方法來部分控制記錄處理行為，此還原選項可讓您更細微地控制。</span><span class="sxs-lookup"><span data-stu-id="344e0-126">In the case of incremental or differential restores, the requester uses the [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) method to partially control the log-handling behavior - this restore option allows more granular control.</span></span>

    <span data-ttu-id="344e0-127">請勿變換記錄。</span><span class="sxs-lookup"><span data-stu-id="344e0-127">Do not roll through logs.</span></span>

    ``` syntax
    "Roll Forward"="None"
    ```

    <span data-ttu-id="344e0-128">滾動所有記錄。</span><span class="sxs-lookup"><span data-stu-id="344e0-128">Roll through all logs.</span></span>

    ``` syntax
    "Roll Forward"="All"
    ```

    <span data-ttu-id="344e0-129">向前復原記錄到指定的時間點。</span><span class="sxs-lookup"><span data-stu-id="344e0-129">Roll through logs up to specified point.</span></span> <span data-ttu-id="344e0-130">指定點的格式是由寫入器定義。</span><span class="sxs-lookup"><span data-stu-id="344e0-130">The format of the specified point is defined by the writer.</span></span>

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   <span data-ttu-id="344e0-131">新元件名稱</span><span class="sxs-lookup"><span data-stu-id="344e0-131">New Component Name</span></span>

    <span data-ttu-id="344e0-132">寫入器可能會想要將元件還原至新的名稱。</span><span class="sxs-lookup"><span data-stu-id="344e0-132">A writer may want to restore a component to a new name.</span></span> <span data-ttu-id="344e0-133">例如，將資料庫還原至不同的名稱來還原個別專案;還原為相同的名稱會讓所有資料都建議寫入器接受有效的邏輯路徑和元件名稱做為此選項的值。</span><span class="sxs-lookup"><span data-stu-id="344e0-133">For example, restoring a database to a different name to restore an individual item; restoring to the same name would please all data We recommend that writers accept a valid logical path and component name as this options' value.</span></span> <span data-ttu-id="344e0-134">這通常會與 [*導向的目標*](vssgloss-d.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="344e0-134">This will often be used with a [*directed target*](vssgloss-d.md).</span></span>

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



