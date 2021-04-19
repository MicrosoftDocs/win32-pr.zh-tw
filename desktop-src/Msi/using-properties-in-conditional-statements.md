---
description: 已設定之屬性的邏輯值為 True。
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: 在條件陳述式中使用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970816"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="5bc24-103">在條件陳述式中使用屬性</span><span class="sxs-lookup"><span data-stu-id="5bc24-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="5bc24-104">已設定之屬性的邏輯值為 True。</span><span class="sxs-lookup"><span data-stu-id="5bc24-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="5bc24-105">若要判斷是否已設定屬性，但未實際取得其值，請測試邏輯運算式 "MyProperty" 或 "Not MyProperty"。</span><span class="sxs-lookup"><span data-stu-id="5bc24-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="5bc24-106">當設定屬性 MyProperty 時，前者會評估為 True，後者則會評估為 False。</span><span class="sxs-lookup"><span data-stu-id="5bc24-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="5bc24-107">一或多個屬性可以與運算子結合，以形成條件陳述式中所使用的邏輯運算式。</span><span class="sxs-lookup"><span data-stu-id="5bc24-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="5bc24-108">如需有關可在條件陳述式中使用之運算子的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="5bc24-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="5bc24-109">您可以在 [條件資料表](condition-table.md) 的 [條件] 資料行中輸入使用屬性的條件陳述式，以修改 [功能資料表](feature-table.md)中任何專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="5bc24-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="5bc24-110">具有一或多個屬性的條件陳述式，通常用於資料庫資料表的 [條件] 資料行中。</span><span class="sxs-lookup"><span data-stu-id="5bc24-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="5bc24-111">下表各有條件運算式的資料行：</span><span class="sxs-lookup"><span data-stu-id="5bc24-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="5bc24-112">條件資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="5bc24-113">ControlEvent 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="5bc24-114">LaunchCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="5bc24-115">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="5bc24-116">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="5bc24-117">ControlCondition 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="5bc24-118">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="5bc24-119">AdvtExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="5bc24-120">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="5bc24-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="5bc24-121">請注意，六個動作順序資料表有條件的欄位。</span><span class="sxs-lookup"><span data-stu-id="5bc24-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="5bc24-122">如果此欄位中的條件運算式評估為 False，則安裝程式會略過該動作。</span><span class="sxs-lookup"><span data-stu-id="5bc24-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="5bc24-123">如果您在 UI 序列中，藉由在其中一個使用者介面順序資料表中撰寫自訂動作來設定 [私用屬性](private-properties.md) ，該屬性就不會在執行順序中設定。</span><span class="sxs-lookup"><span data-stu-id="5bc24-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="5bc24-124">若要在執行順序中設定屬性，您也必須在執行順序資料表中放置自訂動作。</span><span class="sxs-lookup"><span data-stu-id="5bc24-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="5bc24-125">或者，您可以將屬性設為 [公用屬性](public-properties.md) ，並將它包含在 [**SecureCustomProperties**](securecustomproperties.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="5bc24-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="5bc24-126">如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md) 或 [使用屬性](using-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="5bc24-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 



