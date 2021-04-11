---
description: InstallExecuteAgain 動作會執行包含動作順序中所有作業的腳本，自安裝開始或最後一個 InstallExecuteAgain 動作或最後一個 InstallExecute 動作起。
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: InstallExecuteAgain 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943348"
---
# <a name="installexecuteagain-action"></a><span data-ttu-id="e6999-103">InstallExecuteAgain 動作</span><span class="sxs-lookup"><span data-stu-id="e6999-103">InstallExecuteAgain Action</span></span>

<span data-ttu-id="e6999-104">InstallExecuteAgain 動作會執行包含動作順序中所有作業的腳本，自安裝開始或最後一個 InstallExecuteAgain 動作或最後一個 [InstallExecute 動作](installexecute-action.md)起。</span><span class="sxs-lookup"><span data-stu-id="e6999-104">The InstallExecuteAgain action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecuteAgain action or the last [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="e6999-105">InstallExecute 動作會更新系統而不結束交易。</span><span class="sxs-lookup"><span data-stu-id="e6999-105">The InstallExecute action updates the system without ending the transaction.</span></span> <span data-ttu-id="e6999-106">InstallExecuteAgain 與 [InstallExecute 動作](installexecute-action.md) 執行相同的作業，但只應在 InstallExecute 之後使用。</span><span class="sxs-lookup"><span data-stu-id="e6999-106">InstallExecuteAgain performs the same operation as the [InstallExecute action](installexecute-action.md) but should only be used after InstallExecute.</span></span>

<span data-ttu-id="e6999-107">應該一律設定 InstallExecuteAgain，使其不會在移除期間執行。</span><span class="sxs-lookup"><span data-stu-id="e6999-107">InstallExecuteAgain should always be set so that it does not run during removal.</span></span> <span data-ttu-id="e6999-108">如需詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。</span><span class="sxs-lookup"><span data-stu-id="e6999-108">For information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e6999-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="e6999-109">Sequence Restrictions</span></span>

<span data-ttu-id="e6999-110">InstallExecute 動作位於 [InstallInitialize 動作](installinitialize-action.md) 和 [InstallFinalize 動作](installfinalize-action.md)之間。</span><span class="sxs-lookup"><span data-stu-id="e6999-110">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e6999-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="e6999-111">ActionData Messages</span></span>

<span data-ttu-id="e6999-112">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="e6999-112">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6999-113">備註</span><span class="sxs-lookup"><span data-stu-id="e6999-113">Remarks</span></span>

<span data-ttu-id="e6999-114">InstallExecuteAgain 動作執行的動作與 [InstallExecute 動作](installexecute-action.md)相同。</span><span class="sxs-lookup"><span data-stu-id="e6999-114">The InstallExecuteAgain action does the same thing as the [InstallExecute action](installexecute-action.md).</span></span> <span data-ttu-id="e6999-115">由於順序資料表只有一個主鍵，因此動作資料行不能在特定順序資料表中重複執行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="e6999-115">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="e6999-116">有兩個動作會執行相同的動作（InstallExecute 和 InstallExecuteAgain），以便在 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中有兩次需要 InstallExecute 的功能。</span><span class="sxs-lookup"><span data-stu-id="e6999-116">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="e6999-117">如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="e6999-117">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



