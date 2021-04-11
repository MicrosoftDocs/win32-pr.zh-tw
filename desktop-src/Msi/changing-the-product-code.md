---
description: 產品代碼是 GUID，也就是應用程式或產品的主體識別。 請參閱產品代碼。
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: 變更產品代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026640"
---
# <a name="changing-the-product-code"></a><span data-ttu-id="6b8b1-104">變更產品代碼</span><span class="sxs-lookup"><span data-stu-id="6b8b1-104">Changing the Product Code</span></span>

<span data-ttu-id="6b8b1-105">產品代碼是 GUID，也就是應用程式或產品的主體識別。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-105">The product code is a GUID that is the principal identification of an application or product.</span></span> <span data-ttu-id="6b8b1-106">請參閱 [產品代碼](product-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-106">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="6b8b1-107">符合下列指導方針的更新通常不需要變更產品程式碼，而且可以當作 [小型更新](small-updates.md)來處理，或是在版本變更時，做為 [次要升級](minor-upgrades.md)：</span><span class="sxs-lookup"><span data-stu-id="6b8b1-107">An update that meets the following guidelines generally does not require a change of the product code and can be handled as a [small update](small-updates.md), or if the version is to change, as a [minor upgrade](minor-upgrades.md):</span></span>

-   <span data-ttu-id="6b8b1-108">更新可以放大或縮小功能元件樹狀結構，但不能重新組織 [功能](feature-table.md) 和 [FeatureComponents](featurecomponents-table.md) 資料表所描述的現有功能和元件階層。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-108">The update can enlarge or reduce the feature-component tree but it must not reorganize the existing hierarchy of features and components described by the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables.</span></span> <span data-ttu-id="6b8b1-109">它可以將新功能加入至現有的功能元件樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-109">It can add a new feature to the existing feature-component tree.</span></span> <span data-ttu-id="6b8b1-110">如果移除父功能，它也必須移除已移除功能的所有子功能。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-110">If it removes a parent feature, it must also remove all the child features of the removed feature.</span></span>
-   <span data-ttu-id="6b8b1-111">更新可將新的元件新增至新的或現有的功能。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-111">The update can add a new component to a new or an existing feature.</span></span>
-   <span data-ttu-id="6b8b1-112">更新不得變更任何元件的元件代碼。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-112">The update must not change the component code of any component.</span></span> <span data-ttu-id="6b8b1-113">因此，小型更新或次要升級絕不能變更元件的金鑰檔名稱，因為這需要變更元件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-113">Consequently, a small update or minor upgrade must never change the name of a component's key file because this would require changing the component code.</span></span>
-   <span data-ttu-id="6b8b1-114">更新不能變更安裝封裝之 .msi 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-114">The update must not change the name of the .msi file of the installation package.</span></span> <span data-ttu-id="6b8b1-115">相反地，因為它會修改套件，所以它應該會變更封裝程式碼。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-115">Instead, because it modifies the package, it should change the package code.</span></span> <span data-ttu-id="6b8b1-116">請注意，這表示更新可以變更 .msi 檔案中的資料表、自訂動作和對話，而不需要變更檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-116">Note that this means that the update can change the tables, custom actions, and dialogs in the .msi file without changing the file's name.</span></span>
-   <span data-ttu-id="6b8b1-117">更新可以新增、移除或修改兩個或多個功能不共用的檔案、登錄機碼或元件的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-117">The update can add, remove, or modify the files, registry keys, or shortcuts of components that are not shared by two or more features.</span></span> <span data-ttu-id="6b8b1-118">如果更新修改了已建立版本的檔案，該檔案的版本必須在檔案 [資料表](file-table.md)中遞增。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-118">If the update modifies a versioned file, that file's version must be incremented in the [File table](file-table.md).</span></span> <span data-ttu-id="6b8b1-119">如果更新移除資源，它也應該更新 [RemoveFile](removefile-table.md) 和 [RemoveRegistry](removeregistry-table.md) 資料表，以移除任何未使用的檔案、登錄機碼或已安裝的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-119">If the update removes resources, it should also update the [RemoveFile](removefile-table.md) and [RemoveRegistry](removeregistry-table.md) tables to remove any unused files, registry keys, or shortcuts that have already been installed.</span></span>
-   <span data-ttu-id="6b8b1-120">由兩個或多個功能共用的元件更新必須與使用該元件的所有應用程式和功能回溯相容。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-120">The update of a component that is shared by two or more features must be backward compatible with all applications and features that use the component.</span></span> <span data-ttu-id="6b8b1-121">只要變更可回溯相容，更新就可以修改共用元件的資源，例如檔案、登錄專案和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-121">The update can modify the resource of a shared component, such as files, registry entries, and shortcuts, as long as the changes are backward compatible.</span></span> <span data-ttu-id="6b8b1-122">建議您不要更新新增或移除共用元件中的檔案、登錄專案或快捷方式。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-122">It is not recommended that the update add or remove files, registry entries, or shortcuts from a shared component.</span></span>
-   <span data-ttu-id="6b8b1-123">小型更新隨附于 Windows Installer [修補套件](patch-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-123">A small update is shipped as a Windows Installer [patch package](patch-packages.md).</span></span> <span data-ttu-id="6b8b1-124"> (完整的產品光碟通常不提供小型更新。 ) </span><span class="sxs-lookup"><span data-stu-id="6b8b1-124">(A full product CD-ROM is usually not provided with a small update.)</span></span>

<span data-ttu-id="6b8b1-125">如果更新有下列任何一項，則必須變更產品代碼：</span><span class="sxs-lookup"><span data-stu-id="6b8b1-125">The product code must be changed if any of the following are true for the update:</span></span>

-   <span data-ttu-id="6b8b1-126">在相同系統上並存安裝原始和更新的產品必須是可行的。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-126">Coexisting installations of both original and updated products on the same system must be possible.</span></span>
-   <span data-ttu-id="6b8b1-127">.Msi 檔案的名稱已經變更。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-127">The name of the .msi file has been changed.</span></span>
-   <span data-ttu-id="6b8b1-128">現有元件的元件程式碼已變更。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-128">The component code of an existing component has changed.</span></span>
-   <span data-ttu-id="6b8b1-129">元件會從現有的功能中移除。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-129">A component is removed from an existing feature.</span></span>
-   <span data-ttu-id="6b8b1-130">現有功能的子系已成為現有功能的子系。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-130">An existing feature has been made into a child of an existing feature.</span></span>
-   <span data-ttu-id="6b8b1-131">現有的子功能已從其父項功能中移除。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-131">An existing child feature has been removed from its parent feature.</span></span>

<span data-ttu-id="6b8b1-132">請注意，將新的子功能（由全新元件組成）新增至現有的功能，並不需要變更產品代碼。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-132">Note that adding a new child feature, consisting entirely of new components, to an existing feature does not require changing the product code.</span></span>

<span data-ttu-id="6b8b1-133">您可以在 [功能資料表](feature-table.md)的 [屬性] 欄位中包含 MsidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent，以撰寫新的子功能。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-133">New child features can be authored by including msidbFeatureAttributesFollowParent and msidbFeatureAttributesUIDisallowAbsent in the Attributes field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="6b8b1-134">如果次要升級只加入新的子功能，請重新安裝 = 全部都足以強制安裝新的子功能。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-134">If the minor upgrade only adds new child features, then REINSTALL=ALL is sufficient to force the installation of the new child features.</span></span> <span data-ttu-id="6b8b1-135">如需詳細資訊，請參閱 [控制特徵選取狀態](controlling-feature-selection-states.md)。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-135">For more information, see [Controlling Feature Selection States](controlling-feature-selection-states.md).</span></span>

<span data-ttu-id="6b8b1-136">使用者可能會隱藏新的子功能。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-136">A new child feature may be hidden from the user.</span></span> <span data-ttu-id="6b8b1-137">若要同步處理新子功能與其父功能的安裝狀態，請設定子功能的 msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent 位。</span><span class="sxs-lookup"><span data-stu-id="6b8b1-137">To synchronize the installation state of a new child feature with its parent feature, set the msidbFeatureAttributesFollowParent and msidbFeatureAttributesUIDisallowAbsent bits for the child feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b8b1-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b8b1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b8b1-139">關於屬性</span><span class="sxs-lookup"><span data-stu-id="6b8b1-139">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="6b8b1-140">使用屬性</span><span class="sxs-lookup"><span data-stu-id="6b8b1-140">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="6b8b1-141">屬性參考</span><span class="sxs-lookup"><span data-stu-id="6b8b1-141">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



