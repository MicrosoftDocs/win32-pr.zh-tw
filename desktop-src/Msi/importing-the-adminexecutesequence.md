---
description: AdminExecuteSequence 資料表會列出安裝程式在呼叫最上層系統管理員動作時所執行的動作。 請參閱安裝程式資料表群組、使用順序資料表，以及順序資料表詳細的範例。
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: 匯入 AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691068"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="1c775-104">匯入 AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="1c775-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="1c775-105">[AdminExecuteSequence 資料表](adminexecutesequence-table.md)會列出安裝程式在呼叫最上層系統[管理員動作](admin-action.md)時所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="1c775-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="1c775-106">請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。</span><span class="sxs-lookup"><span data-stu-id="1c775-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="1c775-107">如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。</span><span class="sxs-lookup"><span data-stu-id="1c775-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="1c775-108">撰寫「記事本」範例安裝套件時，不需要變更這些順序。</span><span class="sxs-lookup"><span data-stu-id="1c775-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="1c775-109">使用您的資料庫編輯器開啟 MNP2000.msi，並在 AdminExecuteSequence 資料表中輸入下列資料。</span><span class="sxs-lookup"><span data-stu-id="1c775-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="1c775-110">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="1c775-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="1c775-111">動作</span><span class="sxs-lookup"><span data-stu-id="1c775-111">Action</span></span>              | <span data-ttu-id="1c775-112">條件</span><span class="sxs-lookup"><span data-stu-id="1c775-112">Condition</span></span> | <span data-ttu-id="1c775-113">順序</span><span class="sxs-lookup"><span data-stu-id="1c775-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="1c775-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="1c775-114">CostFinalize</span></span>        |           | <span data-ttu-id="1c775-115">1000</span><span class="sxs-lookup"><span data-stu-id="1c775-115">1000</span></span>     |
| <span data-ttu-id="1c775-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="1c775-116">CostInitialize</span></span>      |           | <span data-ttu-id="1c775-117">800</span><span class="sxs-lookup"><span data-stu-id="1c775-117">800</span></span>      |
| <span data-ttu-id="1c775-118">FileCost</span><span class="sxs-lookup"><span data-stu-id="1c775-118">FileCost</span></span>            |           | <span data-ttu-id="1c775-119">900</span><span class="sxs-lookup"><span data-stu-id="1c775-119">900</span></span>      |
| <span data-ttu-id="1c775-120">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="1c775-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="1c775-121">3900</span><span class="sxs-lookup"><span data-stu-id="1c775-121">3900</span></span>     |
| <span data-ttu-id="1c775-122">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="1c775-122">InstallFiles</span></span>        |           | <span data-ttu-id="1c775-123">4000</span><span class="sxs-lookup"><span data-stu-id="1c775-123">4000</span></span>     |
| <span data-ttu-id="1c775-124">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="1c775-124">InstallFinalize</span></span>     |           | <span data-ttu-id="1c775-125">6600</span><span class="sxs-lookup"><span data-stu-id="1c775-125">6600</span></span>     |
| <span data-ttu-id="1c775-126">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="1c775-126">InstallInitialize</span></span>   |           | <span data-ttu-id="1c775-127">1500</span><span class="sxs-lookup"><span data-stu-id="1c775-127">1500</span></span>     |
| <span data-ttu-id="1c775-128">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="1c775-128">InstallValidate</span></span>     |           | <span data-ttu-id="1c775-129">1400</span><span class="sxs-lookup"><span data-stu-id="1c775-129">1400</span></span>     |



 

[<span data-ttu-id="1c775-130">繼續</span><span class="sxs-lookup"><span data-stu-id="1c775-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



