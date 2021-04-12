---
description: 合併模組的資料庫包含模組的所有安裝屬性和安裝程式邏輯。
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: 合併模組資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319839"
---
# <a name="merge-module-database"></a><span data-ttu-id="58551-103">合併模組資料庫</span><span class="sxs-lookup"><span data-stu-id="58551-103">Merge Module Database</span></span>

<span data-ttu-id="58551-104">合併模組的資料庫包含模組的所有安裝屬性和安裝程式邏輯。</span><span class="sxs-lookup"><span data-stu-id="58551-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="58551-105">基本上是簡化的 [安裝程式資料庫](installer-database.md) 或 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="58551-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="58551-106">標準合併模組資料庫檔案是以 .msm 副檔名表示。</span><span class="sxs-lookup"><span data-stu-id="58551-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="58551-107">如需可以存在於合併模組中的所有資料庫資料表清單，請參閱 [合併模組資料庫資料表](merge-module-database-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="58551-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="58551-108">每個 .msm 檔案的資料庫中都需要有下列資料表：</span><span class="sxs-lookup"><span data-stu-id="58551-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="58551-109">元件</span><span class="sxs-lookup"><span data-stu-id="58551-109">Component</span></span>](component-table.md)

[<span data-ttu-id="58551-110">目錄</span><span class="sxs-lookup"><span data-stu-id="58551-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="58551-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="58551-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="58551-112">檔案</span><span class="sxs-lookup"><span data-stu-id="58551-112">File</span></span>](file-table.md)

[<span data-ttu-id="58551-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="58551-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="58551-114">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="58551-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="58551-115">請注意，元件、目錄、FeatureComponents 和檔案資料表也都存在於所有 .msi 檔案中。</span><span class="sxs-lookup"><span data-stu-id="58551-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="58551-116">合併模組資料庫不包含 [功能資料表](feature-table.md) ，因此無法單獨安裝 .msm 檔。</span><span class="sxs-lookup"><span data-stu-id="58551-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="58551-117">若要安裝合併模組，您必須先使用合併工具將其合併至 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="58551-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="58551-118">[ModuleSignature 資料表](modulesignature-table.md)只存在於已與至少一個 .msm 檔案合併的 .msi 檔案中。</span><span class="sxs-lookup"><span data-stu-id="58551-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="58551-119">如果這個資料表出現在 .msi 檔案中，它會針對先前合併到安裝資料庫中的每個合併模組包含一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="58551-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="58551-120">合併模組可能包含選擇性的 MergeModule 順序資料表。</span><span class="sxs-lookup"><span data-stu-id="58551-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="58551-121">這些資料表只會出現在 .msm 檔案中。</span><span class="sxs-lookup"><span data-stu-id="58551-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="58551-122">當 .msm 檔案合併至 .msi 檔案時，這些資料表會修改 .msi 檔案的動作 [*順序資料表*](s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="58551-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="58551-123">合併模組可能包含自訂資料表。</span><span class="sxs-lookup"><span data-stu-id="58551-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="58551-124">這些資料表是由合併模組中定義的 [自訂動作](custom-actions.md) 所使用。</span><span class="sxs-lookup"><span data-stu-id="58551-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="58551-125">合併模組很少需要使用者介面資料表。</span><span class="sxs-lookup"><span data-stu-id="58551-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="58551-126">只有在一般情況下，當合併模組在安裝期間需要使用者輸入時，才需要顯示這些資料表。</span><span class="sxs-lookup"><span data-stu-id="58551-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="58551-127">如需詳細資訊，請參閱 [在合併模組中撰寫使用者介面](authoring-user-interfaces-in-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="58551-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 



