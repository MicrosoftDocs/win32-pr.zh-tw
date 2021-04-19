---
description: 重要的是，若要組織要備份或還原的寫入器檔案，就是元件的概念。
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: VSS 中繼資料元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973471"
---
# <a name="vss-metadata-components"></a><span data-ttu-id="5bd9b-103">VSS 中繼資料元件</span><span class="sxs-lookup"><span data-stu-id="5bd9b-103">VSS Metadata Components</span></span>

<span data-ttu-id="5bd9b-104">重要的是，若要組織要備份或還原的寫入器檔案，就是 [*元件*](vssgloss-c.md)的概念。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-104">Critical to organizing which files of which writer are to be backed up or restored is the concept of a [*component*](vssgloss-c.md).</span></span>

<span data-ttu-id="5bd9b-105">元件可讓寫入器向備份引擎指出其檔案的組織方式、檔案之間的相依性，以及這些檔案可以包含的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-105">Components allow a writer to indicate to a backup engine how its files are to be organized, dependencies between files, and what type of data those files can contain.</span></span> <span data-ttu-id="5bd9b-106">這可讓備份引擎決定儲存檔案以取得最高效率。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-106">This allows a backup engine to decide how to store files for maximum efficiency.</span></span>

<span data-ttu-id="5bd9b-107">此外，以 VSS 為基礎的應用程式會使用元件做為其中繼資料的建立區塊，以及寫入器/要求者通訊的媒體。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-107">In addition, VSS-based applications use components as the building blocks for their metadata and the medium for writer/requester communication.</span></span>

<span data-ttu-id="5bd9b-108">寫入器和要求者會分別在寫入器元資料檔案和備份元件檔中儲存有關元件的資訊，而且每個標記法中的資訊都不同。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-108">Writers and requesters store information about components separately—in the Writer Metadata Document and the Backup Components Document, respectively—and the information differs in each representation.</span></span>

<span data-ttu-id="5bd9b-109">寫入器元資料檔案中的元件資訊包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5bd9b-109">Component information in Writer Metadata Documents includes the following:</span></span>

-   <span data-ttu-id="5bd9b-110">每份檔中只有一個寫入器的資訊</span><span class="sxs-lookup"><span data-stu-id="5bd9b-110">Information from only one writer in each document</span></span>
-   <span data-ttu-id="5bd9b-111">所有的寫入器元件，不論它們是否可以 [*明確包含*](vssgloss-e.md) 或必須 [*隱含地包含*](vssgloss-i.md) 在備份或還原作業中</span><span class="sxs-lookup"><span data-stu-id="5bd9b-111">All of that writer's components, whether they can be [*explicitly included*](vssgloss-e.md) or must be [*implicitly included*](vssgloss-i.md) in a backup or restore operation</span></span>
-   <span data-ttu-id="5bd9b-112">[*邏輯路徑*](vssgloss-l.md) 資訊，用來將可選取的備份元件與備份元件的特定其建立關聯，進而形成元件集</span><span class="sxs-lookup"><span data-stu-id="5bd9b-112">[*Logical path*](vssgloss-l.md) information used to associate a selectable for backup component with particular nonselectable for backup components, thus forming a component set</span></span>
-   <span data-ttu-id="5bd9b-113">針對每個元件所管理的 [*檔集*](vssgloss-f.md) 資訊（路徑、檔案規格和遞迴旗標）</span><span class="sxs-lookup"><span data-stu-id="5bd9b-113">The [*file set*](vssgloss-f.md) information—path, file specification, and recursion flag—managed for each component</span></span>

<span data-ttu-id="5bd9b-114">寫入器元資料檔案也包含寫入器層級的中繼資料資訊，例如還原的還原方法和替代位置對應。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-114">Writer Metadata Documents also contain writer-level metadata information, such as restore methods and alternate location mappings for restore.</span></span> <span data-ttu-id="5bd9b-115">寫入器元資料檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-115">Writer Metadata Documents are read-only.</span></span> <span data-ttu-id="5bd9b-116">檢查這項資訊的介面 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-116">The interface for examining this information is [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span></span>

<span data-ttu-id="5bd9b-117">備份元件檔中的元件資訊包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5bd9b-117">Component information in Backup Components Documents includes the following:</span></span>

-   <span data-ttu-id="5bd9b-118">僅限明確包含元件的資訊</span><span class="sxs-lookup"><span data-stu-id="5bd9b-118">Only information on explicitly included components</span></span>
-   <span data-ttu-id="5bd9b-119">寫入器層級的中繼資料資訊，例如替代位置對應和還原</span><span class="sxs-lookup"><span data-stu-id="5bd9b-119">Writer-level metadata information, such as alternate location mappings and restore</span></span>
-   <span data-ttu-id="5bd9b-120">描述備份或還原作業的狀態資訊</span><span class="sxs-lookup"><span data-stu-id="5bd9b-120">State information describing a backup or restore operation</span></span>

<span data-ttu-id="5bd9b-121">備份元件檔不包含元件檔案 [*集*](vssgloss-f.md)的資訊。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-121">Backup Component Documents do not contain information on components' [*file sets*](vssgloss-f.md).</span></span> <span data-ttu-id="5bd9b-122">備份元件檔不是唯讀的，而且可以由寫入器修改。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-122">Backup Component Documents are not read-only and can be modified by the writer.</span></span> <span data-ttu-id="5bd9b-123">存取此資訊的介面 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-123">The interface for accessing this information is [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span></span>

<span data-ttu-id="5bd9b-124">元件的兩個運算式之間的生命週期和關聯性可理解如下：</span><span class="sxs-lookup"><span data-stu-id="5bd9b-124">The life cycle and relationship between the two expressions of a component can be understood as follows:</span></span>

-   <span data-ttu-id="5bd9b-125">寫入器負責元件的初始定義。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-125">Writers are responsible for the initial definitions of components.</span></span>
-   <span data-ttu-id="5bd9b-126">要求者會檢查所有寫入器及其元件的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-126">A requester examines the metadata of all writers and their components.</span></span>
-   <span data-ttu-id="5bd9b-127">在元件的 selectability 和邏輯路徑資訊中，要求者會決定必須明確包含哪些元件，而這些元件可能會明確包含在內，這些元件會定義元件集合，而這些元件是元件集的成員。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-127">From components' selectability and logical path information, a requester determines which components must be explicitly included, which may be explicitly included, which define component sets, and which are members of component sets.</span></span>
-   <span data-ttu-id="5bd9b-128">要求者會新增需要明確包含的元件，並隱含地在 [*元件集中*](/windows) 包含子元件， (其資訊不在備份元件檔) 中。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-128">A requester adds those components that require explicit inclusion, and implicitly includes subcomponents in [*component sets*](/windows) (whose information is not in the Backup Components Document).</span></span>
-   <span data-ttu-id="5bd9b-129">處理事件時，寫入器和要求者可以修改和檢查儲存在備份元件檔中的元件資訊，以協調其活動。</span><span class="sxs-lookup"><span data-stu-id="5bd9b-129">When handling events, writers and requesters may modify and examine the component information stored in the Backup Components Document to coordinate their activity.</span></span>

<span data-ttu-id="5bd9b-130">寫入器和要求者版本的元件資訊都需要適當地執行備份和還原作業，而且兩者都必須與任何已備份的資料一起儲存：</span><span class="sxs-lookup"><span data-stu-id="5bd9b-130">Both the writer and the requester versions component information are required to properly execute backup and restore operations, and both must be stored with any backed-up data:</span></span>

-   [<span data-ttu-id="5bd9b-131">元件類型</span><span class="sxs-lookup"><span data-stu-id="5bd9b-131">Component Types</span></span>](component-types.md)
-   [<span data-ttu-id="5bd9b-132">作者的元件定義</span><span class="sxs-lookup"><span data-stu-id="5bd9b-132">Definition of Components by Writers</span></span>](definition-of-components-by-writers.md)
-   [<span data-ttu-id="5bd9b-133">要求者使用元件</span><span class="sxs-lookup"><span data-stu-id="5bd9b-133">Use of Components by the Requester</span></span>](use-of-components-by-the-requestor.md)

 

 
