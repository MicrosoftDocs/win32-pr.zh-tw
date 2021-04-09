---
description: AdvtExecuteSequence 資料表會列出安裝程式在執行最上層通告動作時所呼叫的動作。 請參閱安裝程式資料表群組、使用順序資料表，以及順序資料表詳細的範例。
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: 匯入 AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693852"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="a0fa2-104">匯入 AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="a0fa2-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="a0fa2-105">[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)會列出安裝程式在執行最上層[通告動作](advertise-action.md)時所呼叫的動作。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="a0fa2-106">請參閱 [安裝程式資料表群組](installation-procedure-tables-group.md)、 [使用順序資料表](using-a-sequence-table.md)，以及 [順序資料表詳細的範例](sequence-table-detailed-example.md)。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="a0fa2-107">如果您在匯入 uisample.msi 從 Windows Installer SDK 使用的 [空白資料庫](importing-a-blank-database.md) ，則 MNP2000.msi 副本中的順序資料表已包含 [使用順序資料表](using-a-sequence-table.md)中所述的建議動作順序。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="a0fa2-108">撰寫「記事本」範例安裝套件時，不需要變更這些順序。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="a0fa2-109">使用您的資料庫編輯器開啟 MNP2000.msi，並在 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中輸入下列資料。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="a0fa2-110">AdvtExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="a0fa2-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="a0fa2-111">動作</span><span class="sxs-lookup"><span data-stu-id="a0fa2-111">Action</span></span>                | <span data-ttu-id="a0fa2-112">條件</span><span class="sxs-lookup"><span data-stu-id="a0fa2-112">Condition</span></span> | <span data-ttu-id="a0fa2-113">順序</span><span class="sxs-lookup"><span data-stu-id="a0fa2-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="a0fa2-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="a0fa2-114">CostFinalize</span></span>          |           | <span data-ttu-id="a0fa2-115">1000</span><span class="sxs-lookup"><span data-stu-id="a0fa2-115">1000</span></span>     |
| <span data-ttu-id="a0fa2-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="a0fa2-116">CostInitialize</span></span>        |           | <span data-ttu-id="a0fa2-117">800</span><span class="sxs-lookup"><span data-stu-id="a0fa2-117">800</span></span>      |
| <span data-ttu-id="a0fa2-118">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="a0fa2-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="a0fa2-119">4500</span><span class="sxs-lookup"><span data-stu-id="a0fa2-119">4500</span></span>     |
| <span data-ttu-id="a0fa2-120">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="a0fa2-120">InstallFinalize</span></span>       |           | <span data-ttu-id="a0fa2-121">6600</span><span class="sxs-lookup"><span data-stu-id="a0fa2-121">6600</span></span>     |
| <span data-ttu-id="a0fa2-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="a0fa2-122">InstallInitialize</span></span>     |           | <span data-ttu-id="a0fa2-123">1500</span><span class="sxs-lookup"><span data-stu-id="a0fa2-123">1500</span></span>     |
| <span data-ttu-id="a0fa2-124">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="a0fa2-124">InstallValidate</span></span>       |           | <span data-ttu-id="a0fa2-125">1400</span><span class="sxs-lookup"><span data-stu-id="a0fa2-125">1400</span></span>     |
| <span data-ttu-id="a0fa2-126">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="a0fa2-126">PublishComponents</span></span>     |           | <span data-ttu-id="a0fa2-127">6200</span><span class="sxs-lookup"><span data-stu-id="a0fa2-127">6200</span></span>     |
| <span data-ttu-id="a0fa2-128">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="a0fa2-128">PublishFeatures</span></span>       |           | <span data-ttu-id="a0fa2-129">6300</span><span class="sxs-lookup"><span data-stu-id="a0fa2-129">6300</span></span>     |
| <span data-ttu-id="a0fa2-130">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="a0fa2-130">PublishProduct</span></span>        |           | <span data-ttu-id="a0fa2-131">6400</span><span class="sxs-lookup"><span data-stu-id="a0fa2-131">6400</span></span>     |
| <span data-ttu-id="a0fa2-132">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="a0fa2-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="a0fa2-133">4600</span><span class="sxs-lookup"><span data-stu-id="a0fa2-133">4600</span></span>     |
| <span data-ttu-id="a0fa2-134">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="a0fa2-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="a0fa2-135">4700</span><span class="sxs-lookup"><span data-stu-id="a0fa2-135">4700</span></span>     |
| <span data-ttu-id="a0fa2-136">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="a0fa2-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="a0fa2-137">4900</span><span class="sxs-lookup"><span data-stu-id="a0fa2-137">4900</span></span>     |
| <span data-ttu-id="a0fa2-138">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="a0fa2-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="a0fa2-139">4800</span><span class="sxs-lookup"><span data-stu-id="a0fa2-139">4800</span></span>     |



 

<span data-ttu-id="a0fa2-140">安裝程式不會使用 [AdvtUISequence 資料表](advtuisequence-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="a0fa2-141">在安裝資料庫中，此資料表不應存在或保持空白。</span><span class="sxs-lookup"><span data-stu-id="a0fa2-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="a0fa2-142">繼續</span><span class="sxs-lookup"><span data-stu-id="a0fa2-142">Continue</span></span>](adding-summary-information.md)

 

 



