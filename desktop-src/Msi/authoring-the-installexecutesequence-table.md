---
description: 自訂動作 ProcessAccounts 和 UninstallAccounts 會產生延遲的自訂動作，以建立、移除或回復使用者帳戶。
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: 撰寫 InstallExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974415"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="f4e2a-103">撰寫 InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="f4e2a-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="f4e2a-104">自訂動作 ProcessAccounts 和 UninstallAccounts 會產生延遲的自訂動作，以建立、移除或回復使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="f4e2a-105">您必須在要執行的 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中輸入自訂動作 ProcessAccounts 和 UninstallAccounts。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="f4e2a-106">將下列專案加入至 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="f4e2a-107">因為這些自訂動作必須是腳本產生的一部分，所以必須在 [InstallInitialize 動作](installinitialize-action.md)之後排序這兩個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="f4e2a-108">ProcessAccounts 上的條件可確保下列各項。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="f4e2a-109">請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="f4e2a-110">只有在元件 TestAccount 是在本機電腦上安裝時，才會執行 ProcessAccounts。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="f4e2a-111">元件測試帳戶目前未安裝，或已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="f4e2a-112">UninstallAccount 上的條件可確保下列各項：</span><span class="sxs-lookup"><span data-stu-id="f4e2a-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="f4e2a-113">只有在元件 TestAccount 是安裝在本機電腦上時，才會執行 UninstallAccounts。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="f4e2a-114">元件測試帳戶正在移除，或已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="f4e2a-115">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="f4e2a-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="f4e2a-116">動作</span><span class="sxs-lookup"><span data-stu-id="f4e2a-116">Action</span></span>            | <span data-ttu-id="f4e2a-117">條件</span><span class="sxs-lookup"><span data-stu-id="f4e2a-117">Condition</span></span>                                                           | <span data-ttu-id="f4e2a-118">順序</span><span class="sxs-lookup"><span data-stu-id="f4e2a-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="f4e2a-119">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="f4e2a-119">ProcessAccounts</span></span>   | <span data-ttu-id="f4e2a-120">VersionNT 和 (？TestAccount = 2 或？TestAccount = 4) 且 $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="f4e2a-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="f4e2a-121">1550</span><span class="sxs-lookup"><span data-stu-id="f4e2a-121">1550</span></span>     |
| <span data-ttu-id="f4e2a-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="f4e2a-122">UninstallAccounts</span></span> | <span data-ttu-id="f4e2a-123">VersionNT 嗎？TestAccount = 3， ($TestAccount = 4 或 $TestAccount = 2) </span><span class="sxs-lookup"><span data-stu-id="f4e2a-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="f4e2a-124">1560</span><span class="sxs-lookup"><span data-stu-id="f4e2a-124">1560</span></span>     |



 

<span data-ttu-id="f4e2a-125">繼續 [撰寫密碼輸入的使用者介面](authoring-the-user-interface-for-password-input.md)。</span><span class="sxs-lookup"><span data-stu-id="f4e2a-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



