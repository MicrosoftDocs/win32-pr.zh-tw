---
description: 使用者介面序列會匯入到範例資料庫中。
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: 匯入 InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193681"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="92fa2-103">匯入 InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="92fa2-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="92fa2-104">[InstallUISequence 資料表](installuisequence-table.md)會列出執行最上層[安裝動作](install-action.md)時所執行的動作，以及將內部使用者介面層級設定為完整 ui 或縮減 ui 的動作。</span><span class="sxs-lookup"><span data-stu-id="92fa2-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="92fa2-105">如果使用者介面層級設定為基本 UI 或無 UI，則安裝程式會略過此資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="92fa2-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="92fa2-106">請參閱 [消費者介面](user-interface.md) 和 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="92fa2-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="92fa2-107">請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。</span><span class="sxs-lookup"><span data-stu-id="92fa2-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="92fa2-108">如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。</span><span class="sxs-lookup"><span data-stu-id="92fa2-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="92fa2-109">撰寫「記事本」安裝套件時，不需要變更這些順序。</span><span class="sxs-lookup"><span data-stu-id="92fa2-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="92fa2-110">使用您的資料庫編輯器開啟 MNP2000.msi，並在 InstallUISequence 資料表中輸入下列資料。</span><span class="sxs-lookup"><span data-stu-id="92fa2-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="92fa2-111">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="92fa2-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="92fa2-112">動作</span><span class="sxs-lookup"><span data-stu-id="92fa2-112">Action</span></span>                | <span data-ttu-id="92fa2-113">條件</span><span class="sxs-lookup"><span data-stu-id="92fa2-113">Condition</span></span>                                    | <span data-ttu-id="92fa2-114">順序</span><span class="sxs-lookup"><span data-stu-id="92fa2-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="92fa2-115">AppSearch</span><span class="sxs-lookup"><span data-stu-id="92fa2-115">AppSearch</span></span>             |                                              | <span data-ttu-id="92fa2-116">400</span><span class="sxs-lookup"><span data-stu-id="92fa2-116">400</span></span>      |
| <span data-ttu-id="92fa2-117">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="92fa2-117">CCPSearch</span></span>             | <span data-ttu-id="92fa2-118">未安裝</span><span class="sxs-lookup"><span data-stu-id="92fa2-118">NOT Installed</span></span>                                | <span data-ttu-id="92fa2-119">500</span><span class="sxs-lookup"><span data-stu-id="92fa2-119">500</span></span>      |
| <span data-ttu-id="92fa2-120">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="92fa2-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="92fa2-121">1000</span><span class="sxs-lookup"><span data-stu-id="92fa2-121">1000</span></span>     |
| <span data-ttu-id="92fa2-122">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="92fa2-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="92fa2-123">800</span><span class="sxs-lookup"><span data-stu-id="92fa2-123">800</span></span>      |
| <span data-ttu-id="92fa2-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="92fa2-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="92fa2-125">1300</span><span class="sxs-lookup"><span data-stu-id="92fa2-125">1300</span></span>     |
| <span data-ttu-id="92fa2-126">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="92fa2-127">-1</span><span class="sxs-lookup"><span data-stu-id="92fa2-127">-1</span></span>       |
| <span data-ttu-id="92fa2-128">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="92fa2-129">-3</span><span class="sxs-lookup"><span data-stu-id="92fa2-129">-3</span></span>       |
| <span data-ttu-id="92fa2-130">FileCost</span><span class="sxs-lookup"><span data-stu-id="92fa2-130">FileCost</span></span>              |                                              | <span data-ttu-id="92fa2-131">900</span><span class="sxs-lookup"><span data-stu-id="92fa2-131">900</span></span>      |
| <span data-ttu-id="92fa2-132">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="92fa2-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="92fa2-133">100</span><span class="sxs-lookup"><span data-stu-id="92fa2-133">100</span></span>      |
| <span data-ttu-id="92fa2-134">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="92fa2-135">已安裝且不會繼續，且未預先選取</span><span class="sxs-lookup"><span data-stu-id="92fa2-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="92fa2-136">1250</span><span class="sxs-lookup"><span data-stu-id="92fa2-136">1250</span></span>     |
| <span data-ttu-id="92fa2-137">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="92fa2-138">140</span><span class="sxs-lookup"><span data-stu-id="92fa2-138">140</span></span>      |
| <span data-ttu-id="92fa2-139">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="92fa2-140">1280</span><span class="sxs-lookup"><span data-stu-id="92fa2-140">1280</span></span>     |
| <span data-ttu-id="92fa2-141">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-141">ResumeDlg</span></span>             | <span data-ttu-id="92fa2-142">已安裝並 (繼續或預先選取) </span><span class="sxs-lookup"><span data-stu-id="92fa2-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="92fa2-143">1240</span><span class="sxs-lookup"><span data-stu-id="92fa2-143">1240</span></span>     |
| <span data-ttu-id="92fa2-144">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="92fa2-144">RMCCPSearch</span></span>           | <span data-ttu-id="92fa2-145">未安裝</span><span class="sxs-lookup"><span data-stu-id="92fa2-145">NOT Installed</span></span>                                | <span data-ttu-id="92fa2-146">600</span><span class="sxs-lookup"><span data-stu-id="92fa2-146">600</span></span>      |
| <span data-ttu-id="92fa2-147">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="92fa2-148">-2</span><span class="sxs-lookup"><span data-stu-id="92fa2-148">-2</span></span>       |
| <span data-ttu-id="92fa2-149">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="92fa2-149">WelcomeDlg</span></span>            | <span data-ttu-id="92fa2-150">未安裝</span><span class="sxs-lookup"><span data-stu-id="92fa2-150">NOT Installed</span></span>                                | <span data-ttu-id="92fa2-151">1230</span><span class="sxs-lookup"><span data-stu-id="92fa2-151">1230</span></span>     |
| <span data-ttu-id="92fa2-152">MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="92fa2-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="92fa2-153">1200</span><span class="sxs-lookup"><span data-stu-id="92fa2-153">1200</span></span>     |
| <span data-ttu-id="92fa2-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="92fa2-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="92fa2-155">200</span><span class="sxs-lookup"><span data-stu-id="92fa2-155">200</span></span>      |



 

[<span data-ttu-id="92fa2-156">繼續</span><span class="sxs-lookup"><span data-stu-id="92fa2-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



