---
description: 次要升級是對許多資源進行變更的更新。
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: 次要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851171"
---
# <a name="minor-upgrades"></a><span data-ttu-id="301f8-103">次要升級</span><span class="sxs-lookup"><span data-stu-id="301f8-103">Minor Upgrades</span></span>

<span data-ttu-id="301f8-104">次要升級是對許多資源進行變更的更新。</span><span class="sxs-lookup"><span data-stu-id="301f8-104">A minor upgrade is an update that makes changes to many resources.</span></span> <span data-ttu-id="301f8-105">這些變更都不需要變更 [**ProductCode**](productcode.md)。</span><span class="sxs-lookup"><span data-stu-id="301f8-105">None of the changes can require changing the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="301f8-106">更新需要進行 [重大升級](major-upgrades.md) 以變更 **ProductCode**。</span><span class="sxs-lookup"><span data-stu-id="301f8-106">An update requires a [major upgrade](major-upgrades.md) to change the **ProductCode**.</span></span> <span data-ttu-id="301f8-107">次要升級可以用來新增功能和元件，但無法重新組織功能元件樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="301f8-107">A minor upgrade can be used to add new features and components but cannot reorganize the feature-component tree.</span></span> <span data-ttu-id="301f8-108">次要升級可提供產品差異，而不需要實際定義不同的產品。</span><span class="sxs-lookup"><span data-stu-id="301f8-108">Minor upgrades provide product differentiation without actually defining a different product.</span></span> <span data-ttu-id="301f8-109">一般的次要升級包含先前小型更新中的所有修正，並結合成修補程式。</span><span class="sxs-lookup"><span data-stu-id="301f8-109">A typical minor upgrade includes all fixes in previous small updates combined into a patch.</span></span> <span data-ttu-id="301f8-110">次要升級通常也稱為 service pack (SP) update。</span><span class="sxs-lookup"><span data-stu-id="301f8-110">A minor upgrade is also commonly referred to as a service pack (SP) update.</span></span> <span data-ttu-id="301f8-111">如需哪些更新不需要變更 **ProductCode** 的詳細資訊，請參閱 [變更產品代碼](changing-the-product-code.md)。</span><span class="sxs-lookup"><span data-stu-id="301f8-111">For more information about which updates do not require changing the **ProductCode** see [Changing the Product Code](changing-the-product-code.md).</span></span>

<span data-ttu-id="301f8-112">次要升級會變更 [**ProductVersion**](productversion.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="301f8-112">A minor upgrade changes the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="301f8-113">變更應用程式的產品版本表示不同的更新具有順序。</span><span class="sxs-lookup"><span data-stu-id="301f8-113">Changing the product version of the application means that the different updates have an order.</span></span> <span data-ttu-id="301f8-114">例如，如果已有修補程式更新 v 9.0 至9.1 版，而另一個修補程式存在於 patch v 9.1 到 v 9.2，則安裝程式可以在套用修補程式之前先檢查產品版本，以強制執行正確的順序。</span><span class="sxs-lookup"><span data-stu-id="301f8-114">For example, if a patch existed to update v 9.0 to v 9.1, and another patch existed to patch v 9.1 to v 9.2, the installer can enforce the correct order by checking the product version before applying the patch.</span></span> <span data-ttu-id="301f8-115">這也可防止將 v 9.1 至 v 9.2 修補程式套用至 v 9.0。</span><span class="sxs-lookup"><span data-stu-id="301f8-115">This also prevents the v 9.1 to v 9.2 patch from being applied to v 9.0.</span></span> <span data-ttu-id="301f8-116">針對修補程式，此順序會透過 [修補套件](patch-packages.md)中所含轉換中所設定的產品版本驗證位來強制執行。</span><span class="sxs-lookup"><span data-stu-id="301f8-116">For patches, this ordering is enforced through the product version–validation bits set in the transforms included in the [patch package](patch-packages.md).</span></span>

<span data-ttu-id="301f8-117">次要升級和小型更新的差異在於，次要升級會變更封裝程式碼和產品版本。</span><span class="sxs-lookup"><span data-stu-id="301f8-117">A minor upgrade and a small update differ in that a minor upgrade changes the package code and product version.</span></span> <span data-ttu-id="301f8-118">請參閱 [小型更新](small-updates.md) ，以取得可由小型更新或次要升級處理之更新類型的指導方針。</span><span class="sxs-lookup"><span data-stu-id="301f8-118">See [Small Updates](small-updates.md) for guidelines on the kinds of updates that can be handled by a small update or minor upgrade.</span></span> <span data-ttu-id="301f8-119">次要升級會以完整的產品安裝套件或 [修補套件](patch-packages.md)的形式運送。</span><span class="sxs-lookup"><span data-stu-id="301f8-119">Minor upgrades are shipped as a full product installation package or as a [patch package](patch-packages.md).</span></span> <span data-ttu-id="301f8-120">不過，次要升級無法針對新版本使用不同的磁片區標籤。</span><span class="sxs-lookup"><span data-stu-id="301f8-120">However, a minor upgrade cannot use a different volume label for the new version.</span></span>

<span data-ttu-id="301f8-121">如需有關如何套用次要升級的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="301f8-121">For information on how to apply a minor upgrade, see the following topics:</span></span>

-   [<span data-ttu-id="301f8-122">藉由修補產品的本機安裝來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="301f8-122">Applying Small Updates by Patching the Local Installation of the Product</span></span>](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [<span data-ttu-id="301f8-123">重新安裝產品以套用小型更新</span><span class="sxs-lookup"><span data-stu-id="301f8-123">Applying Small Updates by Reinstalling the Product</span></span>](applying-small-updates-by-reinstalling-the-product.md)
-   [<span data-ttu-id="301f8-124">藉由修補系統管理映射來套用小型更新</span><span class="sxs-lookup"><span data-stu-id="301f8-124">Applying Small Updates by Patching an Administrative Image</span></span>](applying-small-updates-by-patching-an-administrative-image.md)

 

 



