---
description: FileCostaction 會起始動態 costingof 標準安裝動作。
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: FileCost 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027603"
---
# <a name="filecost-action"></a><span data-ttu-id="e713f-103">FileCost 動作</span><span class="sxs-lookup"><span data-stu-id="e713f-103">FileCost Action</span></span>

<span data-ttu-id="e713f-104">FileCostaction 會起始標準安裝動作的動態 [*成本*](c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="e713f-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e713f-105">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="e713f-105">ActionData Messages</span></span>

<span data-ttu-id="e713f-106">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="e713f-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e713f-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="e713f-107">Sequence Restrictions</span></span>

<span data-ttu-id="e713f-108">任何會影響成本的標準或 [自訂動作](custom-actions.md) ，都應該在 [CostInitialize](costinitialize-action.md) 動作之前排序。</span><span class="sxs-lookup"><span data-stu-id="e713f-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="e713f-109">在 CostInitialize 動作之後立即呼叫 FileCost 動作。</span><span class="sxs-lookup"><span data-stu-id="e713f-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="e713f-110">然後，在 CostInitialize 動作之後呼叫 [CostFinalize](costfinalize-action.md) 動作，以透過 [元件](component-table.md) 資料表將所有最終成本計算提供給安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e713f-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="e713f-111">[CostInitialize](costinitialize-action.md)動作必須在 FileCost 動作之前執行。</span><span class="sxs-lookup"><span data-stu-id="e713f-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="e713f-112">然後，安裝程式會以每個元件為基礎，判斷檔案 [資料表中](file-table.md) 每個檔案的磁碟空間成本， (查看 [元件表格](component-table.md)) ，同時採用 [*磁片*](v-gly.md) 區叢集以及可能需要覆寫的現有檔案。</span><span class="sxs-lookup"><span data-stu-id="e713f-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="e713f-113">也會考慮使用或釋放磁碟空間的所有動作。</span><span class="sxs-lookup"><span data-stu-id="e713f-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="e713f-114">如果找到現有的檔案，則會執行檔案版本檢查，以判斷是否真的需要安裝新的檔案。</span><span class="sxs-lookup"><span data-stu-id="e713f-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="e713f-115">如果現有的檔案是相同或更高的版本號碼，則不會覆寫現有的檔案，也不會產生任何磁碟空間成本。</span><span class="sxs-lookup"><span data-stu-id="e713f-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="e713f-116">在所有情況下，安裝程式都會使用版本號碼檢查的結果來設定每個檔案的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="e713f-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="e713f-117">FileCost 動作會使用 theinstaller 來初始化成本計算。</span><span class="sxs-lookup"><span data-stu-id="e713f-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="e713f-118">在執行 [CostFinalize](costfinalize-action.md)動作之前，不會發生實際的動態 [*成本*](c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="e713f-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e713f-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e713f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e713f-120">檔案成本</span><span class="sxs-lookup"><span data-stu-id="e713f-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



