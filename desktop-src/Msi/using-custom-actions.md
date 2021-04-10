---
description: 下列各節說明如何使用自訂動作。
ms.assetid: dd2a0681-f50d-4232-bdcc-8aee6bb121a1
title: 使用自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1937adbf64b94667fc3e7c44d82843b561dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191692"
---
# <a name="using-custom-actions"></a><span data-ttu-id="2950d-103">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="2950d-103">Using Custom Actions</span></span>

<span data-ttu-id="2950d-104">下列各節說明如何使用自訂動作。</span><span class="sxs-lookup"><span data-stu-id="2950d-104">The following sections describe using custom actions.</span></span>

-   [<span data-ttu-id="2950d-105">叫用自訂動作</span><span class="sxs-lookup"><span data-stu-id="2950d-105">Invoking Custom Actions</span></span>](invoking-custom-actions.md)
-   [<span data-ttu-id="2950d-106">排序自訂動作</span><span class="sxs-lookup"><span data-stu-id="2950d-106">Sequencing Custom Actions</span></span>](sequencing-custom-actions.md)
-   [<span data-ttu-id="2950d-107">取得順延強制自訂動作的內容資訊</span><span class="sxs-lookup"><span data-stu-id="2950d-107">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
-   [<span data-ttu-id="2950d-108">將自訂動作新增至 ProgressBar</span><span class="sxs-lookup"><span data-stu-id="2950d-108">Adding Custom Actions to the ProgressBar</span></span>](adding-custom-actions-to-the-progressbar.md)
-   [<span data-ttu-id="2950d-109">自訂動作的調試</span><span class="sxs-lookup"><span data-stu-id="2950d-109">Debugging Custom Actions</span></span>](debugging-custom-actions.md)
-   [<span data-ttu-id="2950d-110">從自訂動作判斷 UI 層級</span><span class="sxs-lookup"><span data-stu-id="2950d-110">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
-   [<span data-ttu-id="2950d-111">卸載自訂動作</span><span class="sxs-lookup"><span data-stu-id="2950d-111">Uninstalling Custom Actions</span></span>](uninstalling-custom-actions.md)
-   [<span data-ttu-id="2950d-112">從自訂動作傳回錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="2950d-112">Returning Error Messages from Custom Actions</span></span>](returning-error-messages-from-custom-actions.md)
-   [<span data-ttu-id="2950d-113">設定自訂動作的還原點</span><span class="sxs-lookup"><span data-stu-id="2950d-113">Setting a restore point from a Custom Action</span></span>](setting-a-restore-point-from-a-custom-action.md)
-   [<span data-ttu-id="2950d-114">未在自訂動作中使用的函數</span><span class="sxs-lookup"><span data-stu-id="2950d-114">Functions Not for Use in Custom Actions</span></span>](functions-not-for-use-in-custom-actions.md)
-   [<span data-ttu-id="2950d-115">使用自訂動作變更系統狀態</span><span class="sxs-lookup"><span data-stu-id="2950d-115">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)
-   [<span data-ttu-id="2950d-116">從自訂動作內部存取目前的安裝程式會話</span><span class="sxs-lookup"><span data-stu-id="2950d-116">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="2950d-117">從自訂動作內部存取資料庫或會話</span><span class="sxs-lookup"><span data-stu-id="2950d-117">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="2950d-118">使用自訂動作在安裝結束時啟動已安裝的檔案</span><span class="sxs-lookup"><span data-stu-id="2950d-118">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
-   [<span data-ttu-id="2950d-119">使用自訂動作在本機電腦上建立使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="2950d-119">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
-   [<span data-ttu-id="2950d-120">使用64位自訂動作</span><span class="sxs-lookup"><span data-stu-id="2950d-120">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)

<span data-ttu-id="2950d-121">如需自訂動作的總覽，請參閱 [關於自訂動作](about-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="2950d-121">For an overview of custom actions, see [About Custom Actions](about-custom-actions.md).</span></span>

<span data-ttu-id="2950d-122">如需在 [CustomAction 資料表](customaction-table.md)中將自訂動作編碼的詳細資訊，請參閱 [自訂動作參考](custom-action-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="2950d-122">For more information about encoding custom actions into the [CustomAction table](customaction-table.md), see [Custom Action Reference](custom-action-reference.md).</span></span>

<span data-ttu-id="2950d-123">如需自訂動作的摘要，以及它們如何編碼至 CustomAction 資料表中，請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md)。</span><span class="sxs-lookup"><span data-stu-id="2950d-123">For a summary of custom actions and how they are encoded into the CustomAction table, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span>

 

 



