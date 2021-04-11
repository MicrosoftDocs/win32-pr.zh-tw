---
description: InstallExecute 動作會執行包含動作順序中所有作業的腳本，自安裝開始或上次 InstallExecute 動作或 InstallExecuteAgain 動作起。
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: InstallExecute 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112264"
---
# <a name="installexecute-action"></a><span data-ttu-id="afddf-103">InstallExecute 動作</span><span class="sxs-lookup"><span data-stu-id="afddf-103">InstallExecute Action</span></span>

<span data-ttu-id="afddf-104">InstallExecute 動作會執行包含動作順序中所有作業的腳本，自安裝開始或上次 InstallExecute 動作或 [InstallExecuteAgain 動作](installexecuteagain-action.md)起。</span><span class="sxs-lookup"><span data-stu-id="afddf-104">The InstallExecute action runs a script containing all operations in the action sequence since either the start of the installation or the last InstallExecute action or [InstallExecuteAgain action](installexecuteagain-action.md).</span></span> <span data-ttu-id="afddf-105">InstallExecute 動作會更新系統而不結束交易。</span><span class="sxs-lookup"><span data-stu-id="afddf-105">The InstallExecute action updates the system without ending the transaction.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="afddf-106">順序限制</span><span class="sxs-lookup"><span data-stu-id="afddf-106">Sequence Restrictions</span></span>

<span data-ttu-id="afddf-107">InstallExecute 動作位於 [InstallInitialize 動作](installinitialize-action.md) 和 [InstallFinalize 動作](installfinalize-action.md)之間。</span><span class="sxs-lookup"><span data-stu-id="afddf-107">The InstallExecute action comes between the [InstallInitialize action](installinitialize-action.md) and the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="afddf-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="afddf-108">ActionData Messages</span></span>

<span data-ttu-id="afddf-109">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="afddf-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="afddf-110">備註</span><span class="sxs-lookup"><span data-stu-id="afddf-110">Remarks</span></span>

<span data-ttu-id="afddf-111">[InstallExecuteAgain 動作](installexecuteagain-action.md)執行的動作與 InstallExecute 動作相同。</span><span class="sxs-lookup"><span data-stu-id="afddf-111">The [InstallExecuteAgain action](installexecuteagain-action.md) does the same thing as the InstallExecute action.</span></span> <span data-ttu-id="afddf-112">由於順序資料表只有一個主鍵，因此動作資料行不能在特定順序資料表中重複執行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="afddf-112">Because the sequence tables have only one primary key, the Action column, the same action cannot be repeated in a particular sequence table.</span></span> <span data-ttu-id="afddf-113">有兩個動作會執行相同的動作（InstallExecute 和 InstallExecuteAgain），以便在 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中有兩次需要 InstallExecute 的功能。</span><span class="sxs-lookup"><span data-stu-id="afddf-113">Two actions exist that do the same thing, InstallExecute and InstallExecuteAgain, for cases where the functionality of InstallExecute is needed twice in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="afddf-114">如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="afddf-114">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



