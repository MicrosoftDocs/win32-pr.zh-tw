---
description: 成本是指判斷安裝的總磁碟空間需求的過程。
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: 檔案成本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a4e6221775c2b9ecc429bd32f136e519a2b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981479"
---
# <a name="file-costing"></a><span data-ttu-id="30c52-103">檔案成本</span><span class="sxs-lookup"><span data-stu-id="30c52-103">File Costing</span></span>

<span data-ttu-id="30c52-104">成本是指判斷安裝的總磁碟空間需求的過程。</span><span class="sxs-lookup"><span data-stu-id="30c52-104">Costing is the process of determining the total disk space requirements for an installation.</span></span> <span data-ttu-id="30c52-105">在檔案成本處理常式中計算的元素包括安裝或移除檔案的磁碟空間量，以及由登錄專案、快捷方式和其他檔案所佔用的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="30c52-105">The elements calculated in the file costing process include the amount of disk space in which files are installed or removed, as well as the amount of disk space taken up by registry entries, shortcuts, and other miscellaneous files.</span></span> <span data-ttu-id="30c52-106">已排程要覆寫的現有檔案也會以磁片的總成本計算。</span><span class="sxs-lookup"><span data-stu-id="30c52-106">Existing files scheduled to be overwritten are also calculated in the disk cost totals.</span></span>

<span data-ttu-id="30c52-107">總成本會以每個[元件](components-and-features.md) 為基礎累積，並由三個不同的部分組成：本地成本、來源成本和移除成本。</span><span class="sxs-lookup"><span data-stu-id="30c52-107">Total costs are accumulated on a per-[component](components-and-features.md) basis and consist of three separate parts: local costs, source costs, and removal costs.</span></span> <span data-ttu-id="30c52-108">這些元件會對應至元件安裝在本機、安裝從來源媒體執行，或移除時所產生的磁片成本。</span><span class="sxs-lookup"><span data-stu-id="30c52-108">These parts correspond to the disk cost that is incurred if the component is installed locally, installed to run from the source media, or removed.</span></span>

<span data-ttu-id="30c52-109">所有涉及安裝檔案成本的計算，取決於要安裝或移除檔案的磁片區。</span><span class="sxs-lookup"><span data-stu-id="30c52-109">All calculations involving the cost of installing files depend upon the disk volume to which the file is to be installed or removed.</span></span> <span data-ttu-id="30c52-110">每次與元件相關聯的目錄變更時，都必須重新計算該元件所控制之安裝檔案的成本。</span><span class="sxs-lookup"><span data-stu-id="30c52-110">Each time the directory associated with a component changes, the costs of the installation files controlled by that component must be recalculated.</span></span> <span data-ttu-id="30c52-111">例如，由於目錄變更可能也表示磁片區變更，因此必須重新計算叢集檔案大小。</span><span class="sxs-lookup"><span data-stu-id="30c52-111">For example, because a directory change might also imply a volume change, the clustered file sizes must be recalculated.</span></span> <span data-ttu-id="30c52-112">此外，必須檢查新的目錄，以判斷是否有任何可能覆寫的現有檔案都必須列入考慮。</span><span class="sxs-lookup"><span data-stu-id="30c52-112">In addition, the new directory must be checked to determine whether any existing files that may be overwritten must be taken into account.</span></span>

<span data-ttu-id="30c52-113">呼叫 [CostInitialize](costinitialize-action.md) 動作之後，必須呼叫 [FileCost](filecost-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="30c52-113">After the [CostInitialize](costinitialize-action.md) action is called, the [FileCost](filecost-action.md) action must be called.</span></span> <span data-ttu-id="30c52-114">CostInitialize 動作會初始化安裝程式的內部常式，以動態計算與標準安裝動作相關的磁片成本。</span><span class="sxs-lookup"><span data-stu-id="30c52-114">The CostInitialize action initializes the installer's internal routines that dynamically calculate the disk costs involved with the standard installation actions.</span></span> <span data-ttu-id="30c52-115">此時不會進行任何其他動態成本計算。</span><span class="sxs-lookup"><span data-stu-id="30c52-115">No other dynamic cost calculations are done at this point.</span></span>

<span data-ttu-id="30c52-116">接下來，必須呼叫 [CostFinalize](costfinalize-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="30c52-116">Next, the [CostFinalize](costfinalize-action.md) action must be called.</span></span> <span data-ttu-id="30c52-117">此動作會完成所有成本計算，並透過 [元件](component-table.md) 資料表來提供成本資料。</span><span class="sxs-lookup"><span data-stu-id="30c52-117">This action finalizes all cost calculations and makes the costing data available through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="30c52-118">在 [CostFinalize](costfinalize-action.md) 動作完成執行之後， [元件](component-table.md) 資料表就會完全初始化，而且可以視需要起始包含 [SelectionTree](selectiontree-control.md) 控制項的使用者介面對話方塊序列。</span><span class="sxs-lookup"><span data-stu-id="30c52-118">After the [CostFinalize](costfinalize-action.md) action completes execution, the [Component](component-table.md) table is fully initialized and a user interface dialog box sequence containing a [SelectionTree](selectiontree-control.md) control can be initiated if needed.</span></span> <span data-ttu-id="30c52-119">使用者介面對話方塊可提供選項，將 [功能](feature-table.md) 資料表中任何功能的選取狀態或目的地目錄變更為使用者。</span><span class="sxs-lookup"><span data-stu-id="30c52-119">The user interface dialog boxes may offer the option to change the selection state or destination directory of any feature in the [Feature](feature-table.md) table to the user.</span></span> <span data-ttu-id="30c52-120">元件的選取狀態變更時，此程式很類似。不過，在此情況下，只會重新計算已變更元件的動態成本。</span><span class="sxs-lookup"><span data-stu-id="30c52-120">The process is similar when the selection state of a component changes; however, in this case, the dynamic cost of the changed component only is recalculated.</span></span>

<span data-ttu-id="30c52-121">使用者在使用者介面中完成選取功能之後，應呼叫 [InstallValidate](installvalidate-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="30c52-121">Once the user has completed selecting features in the user interface, the [InstallValidate](installvalidate-action.md) action should be called.</span></span> <span data-ttu-id="30c52-122">此動作會確認成本已屬性化的所有磁片區都有足夠的空間可進行安裝。</span><span class="sxs-lookup"><span data-stu-id="30c52-122">This action verifies that all volumes to which cost has been attributed have sufficient space for the installation.</span></span>

 

 



