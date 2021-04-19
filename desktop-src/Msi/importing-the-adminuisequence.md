---
description: AdminUISequence 資料表會列出安裝程式在執行最上層系統管理員動作時所呼叫的動作，而且內部使用者介面層級會設定為完整 UI 或縮減的 UI。
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: 匯入 AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978038"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="78220-103">匯入 AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="78220-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="78220-104">[AdminUISequence 資料表](adminuisequence-table.md)會列出安裝程式在執行最上層系統[管理員動作](admin-action.md)時所呼叫的動作，而且內部使用者介面層級會設定為完整 UI 或縮減的 ui。</span><span class="sxs-lookup"><span data-stu-id="78220-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="78220-105">如果使用者介面層級設定為基本 UI 或沒有 UI，則安裝程式會略過此資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="78220-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="78220-106">請參閱 [消費者介面](user-interface.md) 和 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="78220-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="78220-107">請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。</span><span class="sxs-lookup"><span data-stu-id="78220-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="78220-108">如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。</span><span class="sxs-lookup"><span data-stu-id="78220-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="78220-109">安裝「記事本」範例時，不需要變更這些順序。</span><span class="sxs-lookup"><span data-stu-id="78220-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="78220-110">使用您的資料庫編輯器開啟 MNP2000.msi，並在 AdminExecuteSequence 資料表中輸入下列資料。</span><span class="sxs-lookup"><span data-stu-id="78220-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="78220-111">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="78220-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="78220-112">動作</span><span class="sxs-lookup"><span data-stu-id="78220-112">Action</span></span>          | <span data-ttu-id="78220-113">條件</span><span class="sxs-lookup"><span data-stu-id="78220-113">Condition</span></span> | <span data-ttu-id="78220-114">順序</span><span class="sxs-lookup"><span data-stu-id="78220-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="78220-115">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="78220-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="78220-116">1230</span><span class="sxs-lookup"><span data-stu-id="78220-116">1230</span></span>     |
| <span data-ttu-id="78220-117">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="78220-117">CostFinalize</span></span>    |           | <span data-ttu-id="78220-118">1000</span><span class="sxs-lookup"><span data-stu-id="78220-118">1000</span></span>     |
| <span data-ttu-id="78220-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="78220-119">CostInitialize</span></span>  |           | <span data-ttu-id="78220-120">800</span><span class="sxs-lookup"><span data-stu-id="78220-120">800</span></span>      |
| <span data-ttu-id="78220-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="78220-121">ExecuteAction</span></span>   |           | <span data-ttu-id="78220-122">1300</span><span class="sxs-lookup"><span data-stu-id="78220-122">1300</span></span>     |
| <span data-ttu-id="78220-123">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="78220-123">ExitDlg</span></span>         |           | <span data-ttu-id="78220-124">-1</span><span class="sxs-lookup"><span data-stu-id="78220-124">-1</span></span>       |
| <span data-ttu-id="78220-125">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="78220-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="78220-126">-3</span><span class="sxs-lookup"><span data-stu-id="78220-126">-3</span></span>       |
| <span data-ttu-id="78220-127">FileCost</span><span class="sxs-lookup"><span data-stu-id="78220-127">FileCost</span></span>        |           | <span data-ttu-id="78220-128">900</span><span class="sxs-lookup"><span data-stu-id="78220-128">900</span></span>      |
| <span data-ttu-id="78220-129">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="78220-129">PrepareDlg</span></span>      |           | <span data-ttu-id="78220-130">140</span><span class="sxs-lookup"><span data-stu-id="78220-130">140</span></span>      |
| <span data-ttu-id="78220-131">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="78220-131">ProgressDlg</span></span>     |           | <span data-ttu-id="78220-132">1280</span><span class="sxs-lookup"><span data-stu-id="78220-132">1280</span></span>     |
| <span data-ttu-id="78220-133">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="78220-133">UserExitDlg</span></span>     |           | <span data-ttu-id="78220-134">-2</span><span class="sxs-lookup"><span data-stu-id="78220-134">-2</span></span>       |



 

[<span data-ttu-id="78220-135">繼續</span><span class="sxs-lookup"><span data-stu-id="78220-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



