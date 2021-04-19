---
description: RemoveExistingProducts 動作會經歷升級資料表的 ActionProperty 資料行中所列的產品代碼，並叫用並行安裝以依序移除產品。
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: RemoveExistingProducts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971805"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="22cb4-103">RemoveExistingProducts 動作</span><span class="sxs-lookup"><span data-stu-id="22cb4-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="22cb4-104">RemoveExistingProducts 動作會經歷 [升級資料表](upgrade-table.md) 的 ActionProperty 資料行中所列的產品代碼，並叫用並行安裝以依序移除產品。</span><span class="sxs-lookup"><span data-stu-id="22cb4-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="22cb4-105">針對每個並行安裝，安裝程式會將 [ [**ProductCode**](productcode.md) ] 屬性設定為 [產品代碼]，並將 [ [**移除**](remove.md) ] 屬性設定為升級資料表之 [移除] 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="22cb4-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="22cb4-106">如果 [移除] 欄位是空白的，其值會預設為 [全部]，而安裝程式會移除整個產品。</span><span class="sxs-lookup"><span data-stu-id="22cb4-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="22cb4-107">安裝程式只會在第一次安裝產品時執行 RemoveExistingProducts 動作。</span><span class="sxs-lookup"><span data-stu-id="22cb4-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="22cb4-108">它不會在 [維護安裝](maintenance-installation.md) 或卸載期間執行此動作。</span><span class="sxs-lookup"><span data-stu-id="22cb4-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="22cb4-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="22cb4-109">Sequence Restrictions</span></span>

<span data-ttu-id="22cb4-110">您必須在下列其中一個位置的動作順序中排程 RemoveExistingProducts 動作。</span><span class="sxs-lookup"><span data-stu-id="22cb4-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="22cb4-111">在 [InstallValidate 動作](installvalidate-action.md) 與 [InstallInitialize 動作](installinitialize-action.md)之間。</span><span class="sxs-lookup"><span data-stu-id="22cb4-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="22cb4-112">在此情況下，安裝程式會先完全移除舊的應用程式，再安裝新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="22cb4-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="22cb4-113">因為所有重複使用的檔案都必須重新複製，所以此動作的放置效率不佳。</span><span class="sxs-lookup"><span data-stu-id="22cb4-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="22cb4-114">在 [InstallInitialize 動作](installinitialize-action.md) 之後，以及產生執行腳本的任何動作之前。</span><span class="sxs-lookup"><span data-stu-id="22cb4-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="22cb4-115">介於 [InstallExecute 動作](installexecute-action.md)或 [InstallExecuteAgain 動作](installexecuteagain-action.md)之間，以及 [InstallFinalize 動作](installfinalize-action.md)之間。</span><span class="sxs-lookup"><span data-stu-id="22cb4-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="22cb4-116">通常，最後三個動作會在另一個之後排程： InstallExecute、RemoveExistingProducts 和 InstallFinalize。</span><span class="sxs-lookup"><span data-stu-id="22cb4-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="22cb4-117">在此情況下，會先安裝更新的檔案，然後移除舊的檔案。</span><span class="sxs-lookup"><span data-stu-id="22cb4-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="22cb4-118">但是，如果移除舊的應用程式失敗，則安裝程式會復原舊應用程式的移除以及新應用程式的安裝。</span><span class="sxs-lookup"><span data-stu-id="22cb4-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="22cb4-119">在 [InstallFinalize 動作](installfinalize-action.md)之後。</span><span class="sxs-lookup"><span data-stu-id="22cb4-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="22cb4-120">這是最有效率的動作放置位置。</span><span class="sxs-lookup"><span data-stu-id="22cb4-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="22cb4-121">在此情況下，安裝程式會先更新檔案，然後再移除舊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="22cb4-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="22cb4-122">在安裝期間，只會安裝所要更新的檔案。</span><span class="sxs-lookup"><span data-stu-id="22cb4-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="22cb4-123">如果移除舊的應用程式失敗，則安裝程式只會復原舊應用程式的卸載。</span><span class="sxs-lookup"><span data-stu-id="22cb4-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="22cb4-124">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="22cb4-124">ActionData Messages</span></span>



| <span data-ttu-id="22cb4-125">欄位</span><span class="sxs-lookup"><span data-stu-id="22cb4-125">Field</span></span> | <span data-ttu-id="22cb4-126">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="22cb4-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="22cb4-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="22cb4-127">\[1\]</span></span> | <span data-ttu-id="22cb4-128">已移除產品。</span><span class="sxs-lookup"><span data-stu-id="22cb4-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="22cb4-129">備註</span><span class="sxs-lookup"><span data-stu-id="22cb4-129">Remarks</span></span>

<span data-ttu-id="22cb4-130">Windows Installer 會在執行此動作時設定 [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="22cb4-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



