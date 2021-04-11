---
description: 若要使用 Windows Installer 來套用主要升級，原始產品安裝套件必須指定 UpgradeCode 屬性（如準備應用程式以進行未來的主要升級所述），而且升級套件必須有升級資料表。
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: 更新升級的升級資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115080"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="6847a-103">更新升級的升級資料表</span><span class="sxs-lookup"><span data-stu-id="6847a-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="6847a-104">若要使用 Windows Installer 來套用主要升級，原始產品安裝套件必須指定 [**UpgradeCode**](upgradecode.md) 屬性（如 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)所述），而且升級套件必須有 [升級資料表](upgrade-table.md)。</span><span class="sxs-lookup"><span data-stu-id="6847a-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="6847a-105">如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)的[主要升級](major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="6847a-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="6847a-106">MNP2000.msi 的安裝套件指派了 [**UpgradeCode**](upgradecode.md) 屬性，如 [指定屬性](specifying-properties.md)一節中所述。</span><span class="sxs-lookup"><span data-stu-id="6847a-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="6847a-107">如果使用者已安裝1.0 至1.4 版的 MNP2000，則 Windows Installer 會套用升級， (包含的英文語言版本) 。</span><span class="sxs-lookup"><span data-stu-id="6847a-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="6847a-108">Windows Installer 將所有原始產品的功能設定遷移到升級的產品。</span><span class="sxs-lookup"><span data-stu-id="6847a-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="6847a-109">安裝程式會移除屬於產品升級未使用之原始產品的檔案。</span><span class="sxs-lookup"><span data-stu-id="6847a-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="6847a-110">如果您的 MNP2001.msi 副本不包含 [升級資料表](upgrade-table.md)、使用 Orca 或另一個資料表編輯器，將空的升級資料表從 Schema.msi 匯入至資料庫。</span><span class="sxs-lookup"><span data-stu-id="6847a-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="6847a-111">SDK 提供 Schema.msi 的複本。</span><span class="sxs-lookup"><span data-stu-id="6847a-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="6847a-112">使用您的資料庫編輯器開啟 MNP2001.msi，並將下列資料輸入空白的升級資料表中。</span><span class="sxs-lookup"><span data-stu-id="6847a-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="6847a-113">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="6847a-113">UpgradeCode</span></span>                            | <span data-ttu-id="6847a-114">VersionMin</span><span class="sxs-lookup"><span data-stu-id="6847a-114">VersionMin</span></span> | <span data-ttu-id="6847a-115">VersionMax</span><span class="sxs-lookup"><span data-stu-id="6847a-115">VersionMax</span></span> | <span data-ttu-id="6847a-116">語言</span><span class="sxs-lookup"><span data-stu-id="6847a-116">Language</span></span> | <span data-ttu-id="6847a-117">屬性</span><span class="sxs-lookup"><span data-stu-id="6847a-117">Attributes</span></span> | <span data-ttu-id="6847a-118">移除</span><span class="sxs-lookup"><span data-stu-id="6847a-118">Remove</span></span> | <span data-ttu-id="6847a-119">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="6847a-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="6847a-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="6847a-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="6847a-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="6847a-121">01.00.0000</span></span> | <span data-ttu-id="6847a-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="6847a-122">01.40.0000</span></span> | <span data-ttu-id="6847a-123">1033</span><span class="sxs-lookup"><span data-stu-id="6847a-123">1033</span></span>     | <span data-ttu-id="6847a-124">769</span><span class="sxs-lookup"><span data-stu-id="6847a-124">769</span></span>        |        | <span data-ttu-id="6847a-125">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="6847a-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="6847a-126">繼續</span><span class="sxs-lookup"><span data-stu-id="6847a-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



