---
description: FindRelatedProducts 動作會依序執行每個升級資料表的記錄，並將每個資料列中的升級程式碼、產品版本和語言，與系統上安裝的產品進行比較。
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: FindRelatedProducts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319843"
---
# <a name="findrelatedproducts-action"></a><span data-ttu-id="9ece2-103">FindRelatedProducts 動作</span><span class="sxs-lookup"><span data-stu-id="9ece2-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="9ece2-104">FindRelatedProducts 動作會依序執行每個 [升級資料表](upgrade-table.md) 的記錄，並將每個資料列中的升級程式碼、產品版本和語言，與系統上安裝的產品進行比較。</span><span class="sxs-lookup"><span data-stu-id="9ece2-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="9ece2-105">當 FindRelatedProducts 偵測到升級資訊與已安裝產品之間的對應時，會將產品程式碼附加至 UpgradeTable 的 ActionProperty 資料行中指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ece2-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="9ece2-106">只有在第一次安裝產品時，才會執行 FindRelatedProducts 動作。</span><span class="sxs-lookup"><span data-stu-id="9ece2-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="9ece2-107">FindRelatedProducts 動作不會在維護模式或卸載期間執行。</span><span class="sxs-lookup"><span data-stu-id="9ece2-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="9ece2-108">查詢的資料庫資料表</span><span class="sxs-lookup"><span data-stu-id="9ece2-108">Database Tables Queried</span></span>

<span data-ttu-id="9ece2-109">此動作會查詢下表：</span><span class="sxs-lookup"><span data-stu-id="9ece2-109">This action queries the following table:</span></span>

[<span data-ttu-id="9ece2-110">升級資料表</span><span class="sxs-lookup"><span data-stu-id="9ece2-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="9ece2-111">使用的屬性</span><span class="sxs-lookup"><span data-stu-id="9ece2-111">Properties Used</span></span>

<span data-ttu-id="9ece2-112">FindRelatedProducts 動作會使用 [**UpgradeCode**](upgradecode.md) 屬性以及撰寫到升級資料表中的版本和語言資訊，來偵測受擱置升級影響的已安裝產品。</span><span class="sxs-lookup"><span data-stu-id="9ece2-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="9ece2-113">它會將偵測到之產品的產品代碼附加至 UpgradeTable 的 ActionProperty 資料行中的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ece2-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="9ece2-114">FindRelatedProducts 只會辨識已使用 Windows Installer 安裝的現有產品，以及定義 [**UpgradeCode**](upgradecode.md) 屬性、 [**ProductVersion**](productversion.md) 屬性和 [**ProductLanguage**](productlanguage.md) 屬性值的現有產品，這是 [ [**範本摘要**](template-summary.md) ] 屬性中所列的其中一種語言。</span><span class="sxs-lookup"><span data-stu-id="9ece2-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="9ece2-115">請注意，FindRelatedProducts 會使用 [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)所傳回的語言。</span><span class="sxs-lookup"><span data-stu-id="9ece2-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="9ece2-116">若要讓 FindRelatedProducts 正常運作，封裝作者必須確定 [屬性工作表](property-table.md)中的 [**ProductLanguage**](productlanguage.md)屬性已設定為也列在 [[**範本摘要**](template-summary.md)] 屬性中的語言。</span><span class="sxs-lookup"><span data-stu-id="9ece2-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="9ece2-117">請參閱 [準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)。</span><span class="sxs-lookup"><span data-stu-id="9ece2-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9ece2-118">順序限制</span><span class="sxs-lookup"><span data-stu-id="9ece2-118">Sequence Restrictions</span></span>

<span data-ttu-id="9ece2-119">FindRelatedProducts 應該撰寫在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence](installexecutesequence-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="9ece2-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="9ece2-120">如果動作已在 InstallUISequence 中執行，則安裝程式會防止 FindRelated 產品在 InstallExecuteSequence 中執行。</span><span class="sxs-lookup"><span data-stu-id="9ece2-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="9ece2-121">FindRelatedProducts 動作必須位於 [MigrateFeatureStates 動作](migratefeaturestates-action.md) 和 [RemoveExistingProducts 動作](removeexistingproducts-action.md)之前。</span><span class="sxs-lookup"><span data-stu-id="9ece2-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9ece2-122">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="9ece2-122">ActionData Messages</span></span>

<span data-ttu-id="9ece2-123">FindRelatedProducts 會傳送其在系統上偵測到的每個相關產品的動作資料訊息。</span><span class="sxs-lookup"><span data-stu-id="9ece2-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



