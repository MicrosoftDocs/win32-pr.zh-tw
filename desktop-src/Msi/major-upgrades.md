---
description: 重大升級是需要變更 [ProductCode] 屬性之產品的完整更新。
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: 主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512016"
---
# <a name="major-upgrades"></a><span data-ttu-id="cc0ee-103">主要升級</span><span class="sxs-lookup"><span data-stu-id="cc0ee-103">Major Upgrades</span></span>

<span data-ttu-id="cc0ee-104">重大升級是需要變更 [ [**ProductCode**](productcode.md) ] 屬性之產品的完整更新。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-104">A major upgrade is a comprehensive update of a product that needs a change of the [**ProductCode**](productcode.md) Property.</span></span>

<span data-ttu-id="cc0ee-105">一般的主要升級會移除舊版的應用程式，並安裝新的版本。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-105">A typical major upgrade removes a previous version of an application and installs a new version.</span></span> <span data-ttu-id="cc0ee-106">主要升級可以重新組織功能元件樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-106">A major upgrade can reorganize the feature component tree.</span></span> <span data-ttu-id="cc0ee-107">如需詳細資訊，請參閱 [ [**ProductCode**](productcode.md) ] 和 [[變更產品代碼](changing-the-product-code.md)]。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-107">For more information, see [**ProductCode**](productcode.md) and [Changing the Product Code](changing-the-product-code.md).</span></span>

<span data-ttu-id="cc0ee-108">在使用 Windows Installer 進行主要升級期間，安裝程式會在使用者電腦上搜尋與擱置升級相關的應用程式，並在偵測到使用者電腦時，從系統登錄抓取已安裝應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-108">During a major upgrade using Windows Installer, the installer searches the user's computer for applications that are related to the pending upgrade, and when it detects one, it retrieves the version of the installed application from the system registry.</span></span> <span data-ttu-id="cc0ee-109">然後，安裝程式會使用升級資料庫中的資訊來判斷是否要升級已安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-109">The installer then uses information in the upgrade database to determine whether to upgrade the installed application.</span></span>

<span data-ttu-id="cc0ee-110">若要啟用安裝程式升級功能，每個封裝都應該有 [**UpgradeCode**](upgradecode.md) 屬性和 [升級資料表](upgrade-table.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-110">To enable the installer upgrade capabilities, each package should have an [**UpgradeCode**](upgradecode.md) Property and an [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="cc0ee-111">每個獨立產品或產品套件都應該有自己的 **UpgradeCode**。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-111">Each stand-alone product or product suite should have its own **UpgradeCode**.</span></span> <span data-ttu-id="cc0ee-112">如需使用 **UpgradeCode** 的詳細資訊，請參閱 [使用 UpgradeCode](using-an-upgradecode.md)一節。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-112">For more information about using the **UpgradeCode** see the section [Using an UpgradeCode](using-an-upgradecode.md).</span></span> <span data-ttu-id="cc0ee-113">升級資料表中的每一筆記錄都會提供升級程式碼、產品版本和語言資訊的組合，用來識別一組受升級影響的產品。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-113">Each record in the Upgrade table gives a combination of the upgrade code, product version, and language information used to identify a set of products affected by the upgrade.</span></span> <span data-ttu-id="cc0ee-114">當 [FindRelatedProducts 動作](findrelatedproducts-action.md) 偵測到系統上已安裝受影響的產品時，它會將產品程式碼附加至升級資料表之 ActionProperty 資料行中的屬性。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-114">When the [FindRelatedProducts Action](findrelatedproducts-action.md) detects that an affected product is installed on the system, it appends the product code to a property in the ActionProperty column of the Upgrade table.</span></span> <span data-ttu-id="cc0ee-115">[RemoveExistingProducts 動作](removeexistingproducts-action.md)和[MigrateFeatureStates 動作](migratefeaturestates-action.md)會移除或遷移 ActionProperty 清單中列出的產品。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-115">The [RemoveExistingProducts action](removeexistingproducts-action.md) and the [MigrateFeatureStates Action](migratefeaturestates-action.md) remove or migrate the products listed in the ActionProperty list.</span></span> <span data-ttu-id="cc0ee-116">套件作者也可以遵循主題中所述的程式： [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-116">Package authors can also follow the procedure described in the topic: [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="cc0ee-117">您可以撰寫 Windows Installer 升級套件，如果使用者已安裝較新版本的應用程式，則不會安裝主要升級。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-117">Windows Installer upgrade packages can be authored such that major upgrades will not install if the user already has a newer version of the application installed.</span></span> <span data-ttu-id="cc0ee-118">如需如何撰寫不會透過較新版本安裝之套件的詳細資訊，請參閱 [防止舊套件安裝在較新版本上](preventing-an-old-package-from-installing-over-a-newer-version.md)</span><span class="sxs-lookup"><span data-stu-id="cc0ee-118">For more information about how to author a package that will not install over a newer version, see [Preventing an Old Package from Installing Over a Newer Version](preventing-an-old-package-from-installing-over-a-newer-version.md)</span></span>

> [!Note]  
> <span data-ttu-id="cc0ee-119">Windows Installer 只會使用產品版本的前三個欄位。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-119">Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="cc0ee-120">如需這些欄位的說明，請參閱 [**ProductVersion**](productversion.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-120">See [**ProductVersion**](productversion.md) Property for descriptions of these fields.</span></span> <span data-ttu-id="cc0ee-121">如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-121">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

 

<span data-ttu-id="cc0ee-122">建議的方法是安裝更新產品的完整套件，以套用主要升級。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-122">The recommended method of applying a major upgrade by installing the full package for the updated product.</span></span> <span data-ttu-id="cc0ee-123">如需有關如何藉由安裝產品來套用主要升級的詳細資訊，請參閱 [安裝產品](applying-major-upgrades-by-installing-the-product.md)以套用主要升級。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-123">For information about how to apply a major upgrade by installing the product, see [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

<span data-ttu-id="cc0ee-124">套用為產品 [修補套件](patch-packages.md) 的主要升級，不能與其他更新一起排序，也不是 [可卸載修補程式](uninstallable-patches.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-124">A major upgrade applied as a [Patch Package](patch-packages.md) for the product cannot be sequenced with other updates and is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="cc0ee-125">如需如何將主要升級修補封裝套用至 Windows Installer 套件的詳細資訊，請參閱 [修補產品的本機安裝以套用主要升級](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-125">For information about how to apply a major upgrade patch package to a Windows Installer package see [Applying Major Upgrades by Patching the Local Installation of the Product](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md).</span></span> <span data-ttu-id="cc0ee-126">不建議使用修補套件進行主要升級的應用程式，而是安裝完整產品以套用主要升級。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-126">The application of a major upgrade using a patch package is not recommended, instead apply major upgrades by installing the full product.</span></span>

> [!Note]  
> <span data-ttu-id="cc0ee-127">如果應用程式安裝在每個使用者的 [安裝內容](installation-context.md)中，則任何主要的應用程式升級也都必須使用每個使用者的內容來執行。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-127">If an application is installed in the per-user [installation context](installation-context.md), any major upgrade to the application must also be performed using the per-user context.</span></span> <span data-ttu-id="cc0ee-128">如果應用程式安裝在每部電腦的安裝內容中，則任何主要的應用程式升級也都必須使用每一電腦的內容來執行。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-128">If an application is installed in the per-machine installation context, any major upgrade to the application must also be performed using the per-machine context.</span></span> <span data-ttu-id="cc0ee-129">Windows Installer 不會在安裝內容之間安裝主要升級。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-129">The Windows Installer will not install major upgrades across installation context.</span></span>

 

<span data-ttu-id="cc0ee-130">您可以使用 [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)屬性，條件在 [InstallValidate](installvalidate-action.md)之後排序的自訂動作，以處理主要升級：</span><span class="sxs-lookup"><span data-stu-id="cc0ee-130">You can condition custom actions that are sequenced after [InstallValidate](installvalidate-action.md) to handle major upgrades by using the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) property:</span></span>

-   <span data-ttu-id="cc0ee-131">如果您想要在卸載產品期間執行自訂動作，而不是在主要升級移除產品期間執行，請使用此狀況。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-131">If you want a custom action to run during an uninstallation of the product, but not during the removal of the product by a major upgrade, use this condition.</span></span>

    <span data-ttu-id="cc0ee-132">REMOVE = "ALL" 而非 [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)</span><span class="sxs-lookup"><span data-stu-id="cc0ee-132">REMOVE="ALL" AND NOT [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)</span></span>

-   <span data-ttu-id="cc0ee-133">如果您只想要在主要升級期間執行自訂動作，請使用此條件。</span><span class="sxs-lookup"><span data-stu-id="cc0ee-133">If you want a custom action to run only during a major upgrade, use this condition.</span></span>

    [<span data-ttu-id="cc0ee-134">**UPGRADINGPRODUCTCODE**</span><span class="sxs-lookup"><span data-stu-id="cc0ee-134">**UPGRADINGPRODUCTCODE**</span></span>](upgradingproductcode.md)

 

 



