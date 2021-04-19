---
description: 在某些情況下，作者可能會決定需要中斷建立元件的規則，如在將應用程式組織為元件及變更元件程式碼中所述。
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: 如果元件規則中斷，會發生什麼事？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f61a0a819856c5014aa70acfaeb46be5043e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978015"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a><span data-ttu-id="33eff-103">如果元件規則中斷，會發生什麼事？</span><span class="sxs-lookup"><span data-stu-id="33eff-103">What happens if the component rules are broken?</span></span>

<span data-ttu-id="33eff-104">在某些情況下，作者可能會決定需要中斷建立元件的規則，如在將 [應用程式組織為元件](organizing-applications-into-components.md) 及 [變更元件程式碼](changing-the-component-code.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="33eff-104">In certain cases, authors may decide they need to break the rules for creating components as discussed in [Organizing Applications into Components](organizing-applications-into-components.md) and [Changing the Component Code](changing-the-component-code.md).</span></span> <span data-ttu-id="33eff-105">作者必須留意執行這項操作的可能結果，也必須保證他們的元件絕對不會安裝在使用者系統上的其他應用程式或元件損毀。</span><span class="sxs-lookup"><span data-stu-id="33eff-105">Authors need to be aware of the possible consequences of doing this and must otherwise guarantee that their components are never installed where they can damage other applications or components on the user's system.</span></span>

<span data-ttu-id="33eff-106">下列清單描述作者有時候會中斷建議元件規則和可能結果的方式。</span><span class="sxs-lookup"><span data-stu-id="33eff-106">The following list describes ways that authors sometimes break the recommended component rules and the possible consequences.</span></span>

<span data-ttu-id="33eff-107">作者將資源新增至元件，而不需要變更元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="33eff-107">An author adds resources to a component without the changing the component code.</span></span>

-   <span data-ttu-id="33eff-108">與舊元件一起安裝的產品，不會有其安裝資料庫中所新增資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33eff-108">Products installed with the old component have no information about the added resources in their installation database.</span></span>
-   <span data-ttu-id="33eff-109">如果有新增資源的新產品和舊的產品都安裝在同一部電腦上，則在第一次卸載新產品時，可能會遺留資源。</span><span class="sxs-lookup"><span data-stu-id="33eff-109">If both a new product that has the added resources and an old product are installed on the same computer, the resources can be left behind if the new product is uninstalled first.</span></span>
-   <span data-ttu-id="33eff-110">沒有新增資源的舊產品無法修復較新版本的元件。</span><span class="sxs-lookup"><span data-stu-id="33eff-110">An old product without the added resources cannot repair the newer version of the component.</span></span> <span data-ttu-id="33eff-111">重新安裝舊的產品並不會還原新增的資源。</span><span class="sxs-lookup"><span data-stu-id="33eff-111">Reinstalling the old product does not restore the added resources.</span></span>

<span data-ttu-id="33eff-112">作者移除元件中的資源，而不會變更元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="33eff-112">An author removes resources from a component without changing the component code.</span></span>

-   <span data-ttu-id="33eff-113">隨新元件一起安裝的產品，不會有其安裝資料庫中移除之資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33eff-113">Products installed with the new component have no information about the removed resources in their installation database.</span></span>
-   <span data-ttu-id="33eff-114">如果舊的產品、具有資源資訊和新產品都安裝在同一部電腦上，則如果先卸載舊的產品，則可以遺留資源。</span><span class="sxs-lookup"><span data-stu-id="33eff-114">If both an old product, having the resource information, and a new product are installed on the same computer, the resources can be left behind if the old product is uninstalled first.</span></span>
-   <span data-ttu-id="33eff-115">具有已移除資源的新產品無法修復較舊版本的產品。</span><span class="sxs-lookup"><span data-stu-id="33eff-115">A new product with the removed resources cannot repair the older version of the product.</span></span> <span data-ttu-id="33eff-116">重新安裝新產品並不會還原移除的資源。</span><span class="sxs-lookup"><span data-stu-id="33eff-116">Reinstalling the new product does not restore the removed resources.</span></span>

<span data-ttu-id="33eff-117">作者包含與舊版不相容的檔案，而不會變更元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="33eff-117">An author includes a file that is incompatible with previous versions without changing the component code.</span></span>

<span data-ttu-id="33eff-118">如果元件中包含不相容的檔案而不變更元件程式碼，則 [預設檔案版本控制](default-file-versioning.md) 會導致安裝程式以最新的不相容檔案覆寫原始檔案。</span><span class="sxs-lookup"><span data-stu-id="33eff-118">If an incompatible file is included in a component without changing the component code, [default file versioning](default-file-versioning.md) causes the installer to overwrite the original file with the more recent incompatible file.</span></span> <span data-ttu-id="33eff-119">這可能會損毀需要原始檔案的舊產品。</span><span class="sxs-lookup"><span data-stu-id="33eff-119">This can damage old products needing the original file.</span></span> <span data-ttu-id="33eff-120">它也可能會防止安裝程式修復舊的產品，因為元件的金鑰路徑檔案版本會決定元件的版本。</span><span class="sxs-lookup"><span data-stu-id="33eff-120">It may also prevent the installer from repairing the old product because the version of a component's key path file determines the version of the component.</span></span> <span data-ttu-id="33eff-121">如果已安裝較新版本的金鑰路徑檔案，安裝程式就不會安裝舊版的元件。</span><span class="sxs-lookup"><span data-stu-id="33eff-121">If a newer version of the key path file is already installed, the installer does not install an older version of the component.</span></span> <span data-ttu-id="33eff-122">如需詳細資訊，請參閱檔案 [版本控制規則](file-versioning-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="33eff-122">For more information, see [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="33eff-123">在此情況下，必須先移除新的產品，才能重新安裝舊的產品。</span><span class="sxs-lookup"><span data-stu-id="33eff-123">In this case, the new product must be removed before the old product can be reinstalled.</span></span>

-   <span data-ttu-id="33eff-124">[預設檔案版本控制](default-file-versioning.md) 會導致安裝程式以最新的不相容檔案覆寫原始檔案。</span><span class="sxs-lookup"><span data-stu-id="33eff-124">[Default file versioning](default-file-versioning.md) causes the installer to overwrite the original file with the more recent incompatible file.</span></span>
-   <span data-ttu-id="33eff-125">需要原始檔案的舊產品已損毀。</span><span class="sxs-lookup"><span data-stu-id="33eff-125">Old products that need the original file are damaged.</span></span>
-   <span data-ttu-id="33eff-126">它也可能會防止安裝程式修復舊的產品，因為元件的金鑰路徑檔案版本會決定元件的版本。</span><span class="sxs-lookup"><span data-stu-id="33eff-126">It may also prevent the installer from repairing the old product because the version of a component's key path file determines the version of the component.</span></span> <span data-ttu-id="33eff-127">如果已安裝較新版本的金鑰路徑檔案，安裝程式就不會安裝舊版的元件。</span><span class="sxs-lookup"><span data-stu-id="33eff-127">If a newer version of the key path file is already installed, the installer does not install the older version of the component.</span></span> <span data-ttu-id="33eff-128">如需詳細資訊，請參閱檔案 [版本控制規則](file-versioning-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="33eff-128">For more information, see [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="33eff-129">在此情況下，必須先移除新的產品，才能重新安裝舊的產品。</span><span class="sxs-lookup"><span data-stu-id="33eff-129">In this case, the new product must be removed before the old product can be reinstalled.</span></span>

<span data-ttu-id="33eff-130">作者在兩個不同的元件中包含相同的資源。</span><span class="sxs-lookup"><span data-stu-id="33eff-130">An author includes the same resource in two different components.</span></span>

<span data-ttu-id="33eff-131">如果有兩個元件的資源位於相同的名稱和位置，而且這兩個元件都安裝在相同的資料夾中，則移除任一元件會移除共同的資源，這會破壞其餘的元件。</span><span class="sxs-lookup"><span data-stu-id="33eff-131">If two components have a resource under the same name and location and both components are installed into the same folder, then the removal of either component removes the common resource, which damages the remaining component.</span></span>

-   <span data-ttu-id="33eff-132">卸載任一元件會移除資源並中斷另一個元件。</span><span class="sxs-lookup"><span data-stu-id="33eff-132">Uninstalling either component removes the resource and breaks the other component.</span></span>
-   <span data-ttu-id="33eff-133">元件參考計數機制已損毀。</span><span class="sxs-lookup"><span data-stu-id="33eff-133">The component reference-counting mechanism is damaged.</span></span>

 

 



