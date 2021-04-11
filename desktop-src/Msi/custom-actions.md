---
description: Windows Installer 提供許多內建動作來執行安裝程式。 如需這些動作的清單，請參閱標準動作參考。
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: 自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026884"
---
# <a name="custom-actions"></a><span data-ttu-id="5c942-104">自訂動作</span><span class="sxs-lookup"><span data-stu-id="5c942-104">Custom Actions</span></span>

<span data-ttu-id="5c942-105">Windows Installer 提供許多內建動作來執行安裝程式。</span><span class="sxs-lookup"><span data-stu-id="5c942-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="5c942-106">如需這些動作的清單，請參閱 [標準動作參考](standard-actions-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="5c942-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="5c942-107">標準動作足以在大部分情況下執行安裝。</span><span class="sxs-lookup"><span data-stu-id="5c942-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="5c942-108">不過，在某些情況下，安裝套件的開發人員會發現需要撰寫自訂動作。</span><span class="sxs-lookup"><span data-stu-id="5c942-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="5c942-109">例如：</span><span class="sxs-lookup"><span data-stu-id="5c942-109">For example:</span></span>

-   <span data-ttu-id="5c942-110">您想要在安裝期間啟動可執行檔（安裝在使用者電腦上，或與應用程式一起安裝時）。</span><span class="sxs-lookup"><span data-stu-id="5c942-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="5c942-111">您想要在安裝期間于動態連結程式庫 (DLL) 中定義的特殊函式進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="5c942-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="5c942-112">在安裝期間，您想要使用 Microsoft Visual Basic Scripting Edition 或 Microsoft JScript 常值腳本文字所撰寫的函式。</span><span class="sxs-lookup"><span data-stu-id="5c942-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="5c942-113">您想要順延強制某些動作，直到執行安裝腳本的時間為止。</span><span class="sxs-lookup"><span data-stu-id="5c942-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="5c942-114">您想要將時間和進度資訊加入至 ProgressBar 控制項和 TimeRemaining 文字控制項。</span><span class="sxs-lookup"><span data-stu-id="5c942-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="5c942-115">下列各節說明自訂動作，以及如何將它們併入安裝套件：</span><span class="sxs-lookup"><span data-stu-id="5c942-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="5c942-116">關於自訂動作</span><span class="sxs-lookup"><span data-stu-id="5c942-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="5c942-117">使用自訂動作</span><span class="sxs-lookup"><span data-stu-id="5c942-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="5c942-118">自訂動作參考</span><span class="sxs-lookup"><span data-stu-id="5c942-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="5c942-119">所有自訂動作類型的摘要清單</span><span class="sxs-lookup"><span data-stu-id="5c942-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 



