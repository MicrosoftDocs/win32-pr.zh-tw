---
description: 成功完成安裝腳本時，會執行 Commit 自訂動作。
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: 認可自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174af16a84f71ff90a1fc35c76054ee503449b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980968"
---
# <a name="commit-custom-actions"></a><span data-ttu-id="4aa28-103">認可自訂動作</span><span class="sxs-lookup"><span data-stu-id="4aa28-103">Commit Custom Actions</span></span>

<span data-ttu-id="4aa28-104">成功完成安裝腳本時，會執行 Commit 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="4aa28-104">Commit Custom actions are executed upon successful completion of the installation script.</span></span> <span data-ttu-id="4aa28-105">如果 [InstallFinalize 動作](installfinalize-action.md) 成功，安裝程式就會執行任何現有的 Commit 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="4aa28-105">If the [InstallFinalize action](installfinalize-action.md) is successful, the installer will then run any existing Commit Custom actions.</span></span> <span data-ttu-id="4aa28-106">在此案例中，安裝程式所設定的唯一模式參數是 MSIRUNMODE \_ COMMIT。</span><span class="sxs-lookup"><span data-stu-id="4aa28-106">The only mode parameter the installer sets in this case is MSIRUNMODE\_COMMIT.</span></span> <span data-ttu-id="4aa28-107">如需執行模式參數的說明，請參閱 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) 。</span><span class="sxs-lookup"><span data-stu-id="4aa28-107">See [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) for a description of the run mode parameters.</span></span>

<span data-ttu-id="4aa28-108">您可以藉由將選項旗標加入至 [CustomAction 資料表](customaction-table.md)的 [類型] 欄位，來指定 commit 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="4aa28-108">A commit custom action can be specified by adding an option flag to the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="4aa28-109">請參閱指定認可自訂動作之選項旗標的 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md) 。</span><span class="sxs-lookup"><span data-stu-id="4aa28-109">See [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md) for the option flag designating a commit custom action.</span></span>

<span data-ttu-id="4aa28-110">Commit 自訂動作是 [rollback 自訂動作](rollback-custom-actions.md) 的補充，可與 rollback 自訂動作搭配使用，以反轉直接對系統進行變更的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="4aa28-110">A commit custom action is the complement to a [rollback custom action](rollback-custom-actions.md) and can be used with rollback custom actions to reverse custom actions that make changes directly to the system.</span></span>

<span data-ttu-id="4aa28-111">請注意，復原自訂動作可能無法移除認可自訂動作所做的所有變更。</span><span class="sxs-lookup"><span data-stu-id="4aa28-111">Note that a rollback custom action may not be able to remove all of the changes made by commit custom actions.</span></span> <span data-ttu-id="4aa28-112">雖然安裝程式會將 rollback 和 commit 自訂動作寫入至復原腳本，但 commit 自訂動作只會在安裝程式成功處理安裝腳本之後執行。</span><span class="sxs-lookup"><span data-stu-id="4aa28-112">Although the installer writes both rollback and commit custom actions into the rollback script, commit custom actions only run after the installer has successfully processed the installation script.</span></span> <span data-ttu-id="4aa28-113">Commit 自訂動作是要在復原腳本中執行的第一個動作。</span><span class="sxs-lookup"><span data-stu-id="4aa28-113">Commit custom actions are the first actions to run in the rollback script.</span></span> <span data-ttu-id="4aa28-114">如果 commit 自訂動作失敗，安裝程式就會起始復原，但只能復原已寫入至復原腳本的作業。</span><span class="sxs-lookup"><span data-stu-id="4aa28-114">If a commit custom action fails, the installer initiates rollback but can only rollback those operations already written to the rollback script.</span></span> <span data-ttu-id="4aa28-115">這表示，視 commit 自訂動作而定，回復可能無法復原動作所做的變更。</span><span class="sxs-lookup"><span data-stu-id="4aa28-115">This means that depending on the commit custom action, a rollback may not be able to undo the changes made by the action.</span></span> <span data-ttu-id="4aa28-116">您可以藉由撰寫自訂動作來忽略傳回碼，來忽略認可自訂動作中的失敗。</span><span class="sxs-lookup"><span data-stu-id="4aa28-116">You can ignore failures in commit custom actions by authoring the custom action to ignore return codes.</span></span>

<span data-ttu-id="4aa28-117">停用回復時，不會執行 rollback 和 commit 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="4aa28-117">Rollback and commit custom actions do not run when rollback is disabled.</span></span> <span data-ttu-id="4aa28-118">如果封裝作者要求這些自訂動作類型進行適當的安裝，則在停用回復時，就應該在防止安裝繼續的情況下使用 [**RollbackDisabled**](rollbackdisabled.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4aa28-118">If a package author requires these types of custom actions for proper installation, they should use the [**RollbackDisabled**](rollbackdisabled.md) Property in a condition that prevents the installation from continuing when rollback is disabled.</span></span>

 

 



