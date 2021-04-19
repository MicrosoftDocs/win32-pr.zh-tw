---
description: 如果使用者已安裝較新的版本，則可以撰寫 Windows Installer 升級套件來安裝主要升級。
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: 防止舊套件安裝在較新的版本上
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983591"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="8b681-103">防止舊套件安裝在較新的版本上</span><span class="sxs-lookup"><span data-stu-id="8b681-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="8b681-104">如果使用者已安裝較新的版本，則可以撰寫 Windows Installer 升級套件來安裝主要升級。</span><span class="sxs-lookup"><span data-stu-id="8b681-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="8b681-105">本主題中的程式僅能防止可能因為執行主要升級封裝而造成的降級。</span><span class="sxs-lookup"><span data-stu-id="8b681-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="8b681-106">此程式依賴 [FindRelatedProducts 動作](findrelatedproducts-action.md)，此動作只會在第一次安裝期間執行，而且無法在維護模式下執行 (重新安裝) 。</span><span class="sxs-lookup"><span data-stu-id="8b681-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="8b681-107">因為次要升級是使用重新安裝來執行，所以此程式無法用來判斷次要升級套件是否正在嘗試降級應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b681-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="8b681-108">如需詳細資訊，請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="8b681-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="8b681-109">**防止舊套件安裝在較新的版本上**</span><span class="sxs-lookup"><span data-stu-id="8b681-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="8b681-110">輸入可能符合 [升級資料表](upgrade-table.md)的 UpgradeCode 資料行之相關產品群組的 [ [**UpgradeCode**](upgradecode.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="8b681-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="8b681-111">在 [[升級] 資料表](upgrade-table.md)的 [屬性] 資料行中，輸入 **msidbUpgradeAttributesOnlyDetect** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="8b681-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="8b681-112">在 [ [升級] 資料表](upgrade-table.md)的 [VersionMin] 資料行中，輸入此封裝所提供的升級版本。</span><span class="sxs-lookup"><span data-stu-id="8b681-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="8b681-113">將 VersionMax 資料行保留空白。</span><span class="sxs-lookup"><span data-stu-id="8b681-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="8b681-114">在 [[升級] 資料表](upgrade-table.md)的 [ActionProperty] 資料行中，輸入[FindRelatedProducts 動作](findrelatedproducts-action.md)要設定之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b681-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="8b681-115">將 [**SecureCustomProperties**](securecustomproperties.md) 屬性和 [升級資料表](upgrade-table.md) 的 ActionProperty 資料行中所指定的屬性加入至 [屬性資料表](property-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8b681-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="8b681-116">在[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的 FindRelatedProducts 動作之後，加入[自訂動作類型 19](custom-action-type-19.md) 。</span><span class="sxs-lookup"><span data-stu-id="8b681-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="8b681-117">在 [CustomAction 資料表](customaction-table.md) 中包含此動作的記錄，然後輸入要在目標資料行中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="8b681-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="8b681-118">類型19自訂動作內建于安裝程式中，因此沒有可寫入的程式碼。</span><span class="sxs-lookup"><span data-stu-id="8b681-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="8b681-119">在 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中，于包含 [自訂動作類型 19](custom-action-type-19.md)的 [記錄] 的 [條件] 資料行中，輸入 ActionProperty 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b681-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="8b681-120">這種情況下，只有當 [升級資料表](upgrade-table.md) 偵測到已安裝較新版本時，才會執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="8b681-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="8b681-121">例如，將相關產品群組升級至3.0 版的 Windows Installer 封裝，可能會在其 [Upgrade](upgrade-table.md)、 [CustomAction](customaction-table.md)、 [InstallExecuteSequence](installexecutesequence-table.md)和 [Property](property-table.md) 資料表中包含下列記錄。</span><span class="sxs-lookup"><span data-stu-id="8b681-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="8b681-122">群組中的所有相關產品都有相同的 UpgradeCode，但是如果電腦上已安裝3.0 以後的版本，安裝程式就不會安裝此升級套件。</span><span class="sxs-lookup"><span data-stu-id="8b681-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="8b681-123">在此情況下，安裝程式會顯示錯誤訊息，且安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="8b681-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="8b681-124">3.0 版升級套件會安裝在1.0 和2.0 版。</span><span class="sxs-lookup"><span data-stu-id="8b681-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="8b681-125">升級資料表</span><span class="sxs-lookup"><span data-stu-id="8b681-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="8b681-126">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="8b681-126">UpgradeCode</span></span>                            | <span data-ttu-id="8b681-127">VersionMin</span><span class="sxs-lookup"><span data-stu-id="8b681-127">VersionMin</span></span> | <span data-ttu-id="8b681-128">VersionMax</span><span class="sxs-lookup"><span data-stu-id="8b681-128">VersionMax</span></span> | <span data-ttu-id="8b681-129">語言</span><span class="sxs-lookup"><span data-stu-id="8b681-129">Language</span></span> | <span data-ttu-id="8b681-130">屬性</span><span class="sxs-lookup"><span data-stu-id="8b681-130">Attributes</span></span>                                | <span data-ttu-id="8b681-131">移除</span><span class="sxs-lookup"><span data-stu-id="8b681-131">Remove</span></span> | <span data-ttu-id="8b681-132">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="8b681-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="8b681-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="8b681-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="8b681-134">3.0</span><span class="sxs-lookup"><span data-stu-id="8b681-134">3.0</span></span>        |            |          | <span data-ttu-id="8b681-135">msidbUpgradeAttributesOnlyDetect</span><span class="sxs-lookup"><span data-stu-id="8b681-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="8b681-136">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="8b681-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="8b681-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="8b681-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="8b681-138">1.0</span><span class="sxs-lookup"><span data-stu-id="8b681-138">1.0</span></span>        | <span data-ttu-id="8b681-139">3.0</span><span class="sxs-lookup"><span data-stu-id="8b681-139">3.0</span></span>        |          | <span data-ttu-id="8b681-140">msidbUpgradeAttributesVersionMinInclusive</span><span class="sxs-lookup"><span data-stu-id="8b681-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="8b681-141">UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="8b681-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="8b681-142">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="8b681-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="8b681-143">動作</span><span class="sxs-lookup"><span data-stu-id="8b681-143">Action</span></span> | <span data-ttu-id="8b681-144">類型</span><span class="sxs-lookup"><span data-stu-id="8b681-144">Type</span></span> | <span data-ttu-id="8b681-145">來源</span><span class="sxs-lookup"><span data-stu-id="8b681-145">Source</span></span> | <span data-ttu-id="8b681-146">目標</span><span class="sxs-lookup"><span data-stu-id="8b681-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="8b681-147">CA1</span><span class="sxs-lookup"><span data-stu-id="8b681-147">CA1</span></span>    | <span data-ttu-id="8b681-148">19</span><span class="sxs-lookup"><span data-stu-id="8b681-148">19</span></span>   |        | <span data-ttu-id="8b681-149">已安裝較高的升級。</span><span class="sxs-lookup"><span data-stu-id="8b681-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="8b681-150">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="8b681-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="8b681-151">動作</span><span class="sxs-lookup"><span data-stu-id="8b681-151">Action</span></span>              | <span data-ttu-id="8b681-152">條件</span><span class="sxs-lookup"><span data-stu-id="8b681-152">Condition</span></span>       | <span data-ttu-id="8b681-153">順序</span><span class="sxs-lookup"><span data-stu-id="8b681-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="8b681-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="8b681-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="8b681-155">200</span><span class="sxs-lookup"><span data-stu-id="8b681-155">200</span></span>      |
    | <span data-ttu-id="8b681-156">CA1</span><span class="sxs-lookup"><span data-stu-id="8b681-156">CA1</span></span>                 | <span data-ttu-id="8b681-157">NEWPRODUCTFOUND</span><span class="sxs-lookup"><span data-stu-id="8b681-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="8b681-158">201</span><span class="sxs-lookup"><span data-stu-id="8b681-158">201</span></span>      |

    

     

    [<span data-ttu-id="8b681-159">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="8b681-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="8b681-160">屬性</span><span class="sxs-lookup"><span data-stu-id="8b681-160">Property</span></span>                                                 | <span data-ttu-id="8b681-161">值</span><span class="sxs-lookup"><span data-stu-id="8b681-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="8b681-162">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="8b681-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="8b681-163">NEWPRODUCTFOUND;UPGRADEFOUND</span><span class="sxs-lookup"><span data-stu-id="8b681-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 



