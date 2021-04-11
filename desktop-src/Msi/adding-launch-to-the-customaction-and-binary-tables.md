---
description: 將記錄加入至 CustomAction 資料表，以啟動自訂動作。
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: 將啟動新增至 CustomAction 和二進位資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115389"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="8a0c6-103">將啟動新增至 CustomAction 和二進位資料表</span><span class="sxs-lookup"><span data-stu-id="8a0c6-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="8a0c6-104">將記錄加入至 [CustomAction 資料表](customaction-table.md) ，以啟動自訂動作。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="8a0c6-105">在 [CustomAction] 資料表的 [動作] 資料行中，輸入自訂動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="8a0c6-106">在 [自訂動作] 資料表的 [類型] 資料行中，輸入啟動65的總計數數值型別。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="8a0c6-107">CustomAction 資料表的 [來源資料行] 會在包含 DLL 之二進位資料的 [二進位資料表](binary-table.md) 記錄中指定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="8a0c6-108">在 CustomAction 資料表的 [來源資料行] 中輸入 Tutorial.dll。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="8a0c6-109">CustomAction 資料表的 [目標] 欄位中指定的進入點必須符合從 DLL 匯出的專案點。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="8a0c6-110">在 CustomAction 資料表的目標資料行中輸入 LaunchTutorial。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="8a0c6-111">CustomAction 資料表</span><span class="sxs-lookup"><span data-stu-id="8a0c6-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="8a0c6-112">動作</span><span class="sxs-lookup"><span data-stu-id="8a0c6-112">Action</span></span> | <span data-ttu-id="8a0c6-113">類型</span><span class="sxs-lookup"><span data-stu-id="8a0c6-113">Type</span></span> | <span data-ttu-id="8a0c6-114">來源</span><span class="sxs-lookup"><span data-stu-id="8a0c6-114">Source</span></span>       | <span data-ttu-id="8a0c6-115">目標</span><span class="sxs-lookup"><span data-stu-id="8a0c6-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="8a0c6-116">啟動</span><span class="sxs-lookup"><span data-stu-id="8a0c6-116">Launch</span></span> | <span data-ttu-id="8a0c6-117">65</span><span class="sxs-lookup"><span data-stu-id="8a0c6-117">65</span></span>   | <span data-ttu-id="8a0c6-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="8a0c6-118">Tutorial.dll</span></span> | <span data-ttu-id="8a0c6-119">LaunchTutorial</span><span class="sxs-lookup"><span data-stu-id="8a0c6-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="8a0c6-120">將您在教學課程中建立的 Tutorial.dll，加入至二進位資料表的二進位資料流程。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="8a0c6-121">二進位資料表</span><span class="sxs-lookup"><span data-stu-id="8a0c6-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="8a0c6-122">Name</span><span class="sxs-lookup"><span data-stu-id="8a0c6-122">Name</span></span>         | <span data-ttu-id="8a0c6-123">資料</span><span class="sxs-lookup"><span data-stu-id="8a0c6-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="8a0c6-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="8a0c6-124">Tutorial.dll</span></span> | <span data-ttu-id="8a0c6-125">{*為 DLL 新增的二進位資料*}</span><span class="sxs-lookup"><span data-stu-id="8a0c6-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="8a0c6-126">繼續在 [安裝結束時新增控制項事件，以執行啟動](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)。</span><span class="sxs-lookup"><span data-stu-id="8a0c6-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



