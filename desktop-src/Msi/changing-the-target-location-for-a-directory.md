---
description: 可能的話，為目錄指定目標位置的最佳方式，就是在安裝套件中撰寫目錄表格，以提供正確的位置。 如需詳細資訊，請參閱使用目錄資料表。
ms.assetid: 2d16e036-2d7f-431d-b646-1addf2f65f3f
title: 變更目錄的目標位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818c4e9d555244dd1637e19eb249478f13ea2d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192449"
---
# <a name="changing-the-target-location-for-a-directory"></a><span data-ttu-id="44136-104">變更目錄的目標位置</span><span class="sxs-lookup"><span data-stu-id="44136-104">Changing the Target Location for a Directory</span></span>

<span data-ttu-id="44136-105">可能的話，為目錄指定目標位置的最佳方式，就是在安裝套件中撰寫 [目錄表格](directory-table.md) ，以提供正確的位置。</span><span class="sxs-lookup"><span data-stu-id="44136-105">If possible, the best way to specify the target location for a directory is to author the [Directory Table](directory-table.md) in your installation package to provide the correct location.</span></span> <span data-ttu-id="44136-106">如需詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。</span><span class="sxs-lookup"><span data-stu-id="44136-106">For more information, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="44136-107">如果您需要在安裝時變更目錄位置，您有下列選項：</span><span class="sxs-lookup"><span data-stu-id="44136-107">If you need to change the directory location at the time of the installation, you have the following options:</span></span>

-   <span data-ttu-id="44136-108">藉由在命令列上設定 [公用屬性](public-properties.md) 的值，指定目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="44136-108">Specify the location of a directory by setting the value of a [Public Property](public-properties.md) on the command line.</span></span> <span data-ttu-id="44136-109">在 [CostFinalize 動作](costfinalize-action.md)期間，安裝程式所使用的內部目錄路徑會更新為 [目錄資料表](directory-table.md)中列為索引鍵的屬性值。</span><span class="sxs-lookup"><span data-stu-id="44136-109">During the [CostFinalize Action](costfinalize-action.md), the internal directory paths used by the installer are updated to the value of properties listed as keys in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="44136-110">如需詳細資訊，請參閱在命令列上 [使用屬性](using-properties.md) 和 [設定公用屬性值](setting-public-property-values-on-the-command-line.md)。</span><span class="sxs-lookup"><span data-stu-id="44136-110">For more information, see [Using Properties](using-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span>
-   <span data-ttu-id="44136-111">使用自訂動作來指定目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="44136-111">Specify the location of a directory by using a custom action.</span></span> <span data-ttu-id="44136-112">如果在 [CostFinalize 動作](costfinalize-action.md)之前執行自訂動作，您可以使用 [自訂動作類型 51](custom-action-type-51.md) ，從格式化的文字字串設定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="44136-112">If the custom action is to run before the [CostFinalize Action](costfinalize-action.md), you can use a [Custom Action Type 51](custom-action-type-51.md) to set the value of a property from a formatted text string.</span></span> <span data-ttu-id="44136-113">如果在 [CostFinalize 動作](costfinalize-action.md)之後執行自訂動作，您可以使用 [自訂動作類型 35](custom-action-type-35.md) ，從格式化的文字字串設定目錄路徑的值。</span><span class="sxs-lookup"><span data-stu-id="44136-113">If the custom action runs after the [CostFinalize Action](costfinalize-action.md), you can use a [Custom Action Type 35](custom-action-type-35.md) to set the value of the directory path from a formatted text string.</span></span> <span data-ttu-id="44136-114">變更其中一個 [系統資料夾屬性](property-reference.md) 的自訂動作，應該包含在執行順序資料表中 ([InstallExecuteSequence 資料表](installexecutesequence-table.md) 或 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)) ，而使用者介面順序資料表 ([InstallUISequence 資料表](installuisequence-table.md) 和 [AdminUISequence 資料表](adminuisequence-table.md)) ，如此一來，在 [*完全 ui*](f-gly.md) 和 [*基本 ui*](b-gly.md) 安裝期間，資料夾就會變更。</span><span class="sxs-lookup"><span data-stu-id="44136-114">Custom actions that change one of the [System Folder Properties](property-reference.md) should be included in both the execution sequence tables ([InstallExecuteSequence Table](installexecutesequence-table.md) or [AdminExecuteSequence Table](adminexecutesequence-table.md)), and the user interface sequence tables ([InstallUISequence Table](installuisequence-table.md) and [AdminUISequence Table](adminuisequence-table.md)) so that the folder is changed during both [*full UI*](f-gly.md) and [*basic UI*](b-gly.md) installations.</span></span>
-   <span data-ttu-id="44136-115">如果安裝正在執行完整的 [*UI*](f-gly.md)，您可以使用 [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) 或 [SetTargetPath ControlEvent](settargetpath-controlevent.md) 來設定目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="44136-115">If the installation is running a [*full UI*](f-gly.md), you can use [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) or the [SetTargetPath ControlEvent](settargetpath-controlevent.md) to set the directory path.</span></span> <span data-ttu-id="44136-116">檢查 [**ProductState**](productstate.md) 屬性，以判斷是否已安裝包含此元件的產品，然後再呼叫 **MsiSetTargetPath** 或 SetTargetPath ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="44136-116">Check the [**ProductState**](productstate.md) Property to determine whether the product that contains this component is already installed before calling **MsiSetTargetPath** or the SetTargetPath ControlEvent.</span></span> <span data-ttu-id="44136-117">如果已為目前使用者或不同的使用者安裝了某些使用該路徑的元件，請不要嘗試變更目標目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="44136-117">Do not attempt to change the target directory path if some components that use that path are already installed for the current user or a different user.</span></span>

<span data-ttu-id="44136-118">下列限制適用于上述所有選項：</span><span class="sxs-lookup"><span data-stu-id="44136-118">The following restrictions apply to all of the above options:</span></span>

-   <span data-ttu-id="44136-119">如果已為目前使用者或不同的使用者安裝了某些使用路徑的元件，請不要嘗試變更目標目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="44136-119">Do not attempt to change the target directory path if some components that use the path are already installed for the current user or for a different user.</span></span>
-   <span data-ttu-id="44136-120">在 [維護安裝](maintenance-installation.md)期間，請勿嘗試變更目標目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="44136-120">Do not attempt to change the target directory path during a [Maintenance Installation](maintenance-installation.md).</span></span>

 

 



