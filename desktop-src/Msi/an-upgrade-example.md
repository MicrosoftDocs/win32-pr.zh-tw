---
description: 下列各節會針對安裝範例中所述的應用程式撰寫升級套件的範例。
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: 升級範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980812"
---
# <a name="an-upgrade-example"></a><span data-ttu-id="c1461-103">升級範例</span><span class="sxs-lookup"><span data-stu-id="c1461-103">An Upgrade Example</span></span>

<span data-ttu-id="c1461-104">下列各節會針對 [安裝範例](an-installation-example.md)中所述的應用程式撰寫升級套件的範例。</span><span class="sxs-lookup"><span data-stu-id="c1461-104">The following sections present an example of authoring an upgrade package for the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="c1461-105">此範例的最基本使用者介面範例，會在 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md) 中提供，做為檔 Uisample.msi。</span><span class="sxs-lookup"><span data-stu-id="c1461-105">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="c1461-106">如果您有 SDK，就可以存取重現範例安裝套件、使用者介面和範例升級套件所需的所有工具和資料。</span><span class="sxs-lookup"><span data-stu-id="c1461-106">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and sample upgrade package.</span></span>

<span data-ttu-id="c1461-107">此範例說明如何建立 Windows Installer 套件，以將假想產品 MNP2000 升級為稱為 MNP2001 的新產品。</span><span class="sxs-lookup"><span data-stu-id="c1461-107">This example illustrates how to create a Windows Installer package that upgrades the hypothetical product MNP2000 to a new product called MNP2001.</span></span> <span data-ttu-id="c1461-108">範例升級套件會將主要升級套用至需要變更產品代碼的產品。</span><span class="sxs-lookup"><span data-stu-id="c1461-108">The example upgrade package applies a major upgrade to the product which requires changing the product code.</span></span> <span data-ttu-id="c1461-109">如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)一節中的[重大升級](major-upgrades.md)主題。</span><span class="sxs-lookup"><span data-stu-id="c1461-109">For more information about major upgrades, see the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section.</span></span>

<span data-ttu-id="c1461-110">範例升級套件具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="c1461-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="c1461-111">若要符合接收此升級至 MNP2001 的資格，使用者必須先前已使用 Windows Installer，將1.0 到 1.4 (內含) 版本的英文語言。</span><span class="sxs-lookup"><span data-stu-id="c1461-111">To qualify to receive this upgrade to MNP2001, a user must have previously installed the 1.0 to 1.4 (inclusive) versions of English language MNP2000 using Windows Installer.</span></span>
-   <span data-ttu-id="c1461-112">當使用者嘗試安裝升級套件時，Windows Installer 的升級功能會在使用者電腦上搜尋任何符合升級資格的產品。</span><span class="sxs-lookup"><span data-stu-id="c1461-112">When a user attempts to install the upgrade package, the upgrade functionality of Windows Installer searches the user's computer for any products that qualify for the upgrade.</span></span>
-   <span data-ttu-id="c1461-113">Windows Installer 將所有原始產品的功能設定遷移到升級的產品。</span><span class="sxs-lookup"><span data-stu-id="c1461-113">Windows Installer migrates all the of the original product's feature settings to the upgraded product.</span></span>
-   <span data-ttu-id="c1461-114">安裝程式會從使用者的電腦移除所有已淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="c1461-114">The installer removes all obsolete features from the user's computer.</span></span>
-   <span data-ttu-id="c1461-115">安裝程式會安裝屬於升級的所有新功能。</span><span class="sxs-lookup"><span data-stu-id="c1461-115">The installer installs all new features belonging to the upgrade.</span></span>
-   <span data-ttu-id="c1461-116">卸載升級套件會將產品從使用者的電腦中移除，而不會還原舊版產品。</span><span class="sxs-lookup"><span data-stu-id="c1461-116">An uninstall of the upgrade package removes the product from the user's computer, and does not restore the earlier version of the product.</span></span>
-   <span data-ttu-id="c1461-117">範例升級會更新新檔案和功能的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="c1461-117">The sample upgrade updates shortcuts to new files and features.</span></span>

    [<span data-ttu-id="c1461-118">規劃主要升級</span><span class="sxs-lookup"><span data-stu-id="c1461-118">Planning a Major Upgrade</span></span>](planning-a-major-upgrade.md)

    [<span data-ttu-id="c1461-119">匯入原始安裝資料庫</span><span class="sxs-lookup"><span data-stu-id="c1461-119">Importing Original Installation Database</span></span>](importing-original-installation-database.md)

    [<span data-ttu-id="c1461-120">更新升級的目錄結構</span><span class="sxs-lookup"><span data-stu-id="c1461-120">Updating Directory Structure for an Upgrade</span></span>](updating-directory-structure-for-an-upgrade.md)

    [<span data-ttu-id="c1461-121">更新升級的檔案和檔案屬性</span><span class="sxs-lookup"><span data-stu-id="c1461-121">Updating Files and File Attributes for an Upgrade</span></span>](updating-files-and-file-attributes-for-an-upgrade.md)

    [<span data-ttu-id="c1461-122">更新升級的元件</span><span class="sxs-lookup"><span data-stu-id="c1461-122">Updating Components for an Upgrade</span></span>](updating-components-for-an-upgrade.md)

    [<span data-ttu-id="c1461-123">更新升級的功能</span><span class="sxs-lookup"><span data-stu-id="c1461-123">Updating Features for an Upgrade</span></span>](updating-features-for-an-upgrade.md)

    [<span data-ttu-id="c1461-124">更新升級的快捷方式</span><span class="sxs-lookup"><span data-stu-id="c1461-124">Updating Shortcuts for an Upgrade</span></span>](updating-shortcuts-for-an-upgrade.md)

    [<span data-ttu-id="c1461-125">更新升級的升級資料表</span><span class="sxs-lookup"><span data-stu-id="c1461-125">Updating Upgrade Table for an Upgrade</span></span>](updating-upgrade-table-for-an-upgrade.md)

    [<span data-ttu-id="c1461-126">更新升級的屬性</span><span class="sxs-lookup"><span data-stu-id="c1461-126">Updating Properties for an Upgrade</span></span>](updating-properties-for-an-upgrade.md)

    [<span data-ttu-id="c1461-127">更新升級的順序資料表</span><span class="sxs-lookup"><span data-stu-id="c1461-127">Updating Sequence Tables for an Upgrade</span></span>](updating-sequence-tables-for-an-upgrade.md)

    [<span data-ttu-id="c1461-128">更新升級的摘要資訊</span><span class="sxs-lookup"><span data-stu-id="c1461-128">Updating Summary Information for an Upgrade</span></span>](updating-summary-information-for-an-upgrade.md)

    [<span data-ttu-id="c1461-129">驗證安裝升級</span><span class="sxs-lookup"><span data-stu-id="c1461-129">Validating an Installation Upgrade</span></span>](validating-an-installation-upgrade.md)

 

 



