---
description: ICE13 會驗證順序資料表中的對話是否出現在 AdminUISequence 或 InstallUISequence 資料表中。 對話方塊不得列在 InstallExecuteSequence、AdminExecuteSequence 或 AdvtExecuteSequence 資料表中。
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944536"
---
# <a name="ice13"></a><span data-ttu-id="f166b-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="f166b-104">ICE13</span></span>

<span data-ttu-id="f166b-105">ICE13 會驗證順序資料表中的對話是否出現在 [AdminUISequence](adminuisequence-table.md)或 [InstallUISequence](installuisequence-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="f166b-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="f166b-106">對話方塊不得列在 [InstallExecuteSequence](installexecutesequence-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)或 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="f166b-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="f166b-107">結果</span><span class="sxs-lookup"><span data-stu-id="f166b-107">Result</span></span>

<span data-ttu-id="f166b-108">如果對話方塊出現在執行順序資料表中，ICE13 會張貼一則錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f166b-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="f166b-109">範例</span><span class="sxs-lookup"><span data-stu-id="f166b-109">Example</span></span>

<span data-ttu-id="f166b-110">在下列範例中，ICE13 會張貼錯誤訊息，指出 ' WelcomeDialog ' 不能列在 ' InstallExecuteSequence ' 資料表中。</span><span class="sxs-lookup"><span data-stu-id="f166b-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="f166b-111">[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f166b-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="f166b-112">動作</span><span class="sxs-lookup"><span data-stu-id="f166b-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="f166b-113">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="f166b-113">InstallFinalize</span></span> |
| <span data-ttu-id="f166b-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f166b-114">CostFinalize</span></span>    |
| <span data-ttu-id="f166b-115">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="f166b-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="f166b-116">[InstallUISequence 資料表](installuisequence-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f166b-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="f166b-117">動作</span><span class="sxs-lookup"><span data-stu-id="f166b-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="f166b-118">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="f166b-118">CostFinalize</span></span>   |
| <span data-ttu-id="f166b-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="f166b-119">CostInitialize</span></span> |
| <span data-ttu-id="f166b-120">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="f166b-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="f166b-121">[對話方塊資料表](dialog-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="f166b-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="f166b-122">對話</span><span class="sxs-lookup"><span data-stu-id="f166b-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="f166b-123">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="f166b-123">BrowseDialog</span></span>  |
| <span data-ttu-id="f166b-124">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="f166b-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f166b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f166b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f166b-126">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="f166b-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



