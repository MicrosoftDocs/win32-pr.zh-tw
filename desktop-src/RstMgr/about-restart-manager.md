---
title: 關於重新開機管理員
description: 軟體安裝和更新需要系統重新開機的主要原因是，正在執行的應用程式或服務目前正在使用一些正在更新的檔案。
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- 重新開機管理員重新開機管理員，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682926"
---
# <a name="about-restart-manager"></a><span data-ttu-id="3881a-104">關於重新開機管理員</span><span class="sxs-lookup"><span data-stu-id="3881a-104">About Restart Manager</span></span>

<span data-ttu-id="3881a-105">軟體安裝和更新需要系統重新開機的主要原因是，正在執行的應用程式或服務目前正在使用一些正在更新的檔案。</span><span class="sxs-lookup"><span data-stu-id="3881a-105">The primary reason software installation and updates require a system restart is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="3881a-106">重新開機管理員可讓所有重要的應用程式和服務關閉並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="3881a-106">Restart Manager enables all but the critical applications and services to be shut down and restarted .</span></span> <span data-ttu-id="3881a-107">這會釋出使用中的檔案，並允許安裝作業完成。</span><span class="sxs-lookup"><span data-stu-id="3881a-107">This frees the files that are in use and allows installation operations to complete.</span></span> <span data-ttu-id="3881a-108">它也可以消除或減少完成安裝或更新所需的系統重新開機次數。</span><span class="sxs-lookup"><span data-stu-id="3881a-108">It can also eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span>

<span data-ttu-id="3881a-109">重新開機管理員會依下列順序停止應用程式，並在更新應用程式之後，重新開機已註冊為以相反順序重新開機的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3881a-109">The Restart Manager stops applications in the following order, and after the applications have been updated, restarts applications that have been registered for restart in the reverse order.</span></span>

1.  <span data-ttu-id="3881a-110">GUI 應用程式</span><span class="sxs-lookup"><span data-stu-id="3881a-110">GUI applications</span></span>
2.  <span data-ttu-id="3881a-111">主控台應用程式</span><span class="sxs-lookup"><span data-stu-id="3881a-111">Console applications</span></span>
3.  <span data-ttu-id="3881a-112">Windows 服務</span><span class="sxs-lookup"><span data-stu-id="3881a-112">Windows services</span></span>
4.  <span data-ttu-id="3881a-113">Windows explorer</span><span class="sxs-lookup"><span data-stu-id="3881a-113">Windows explorer</span></span>

<span data-ttu-id="3881a-114">只有當呼叫者有權進行此作業時，重新開機管理員才會關閉應用程式或服務。</span><span class="sxs-lookup"><span data-stu-id="3881a-114">Restart Manager shuts down application or services only if the caller has permission to do so.</span></span> <span data-ttu-id="3881a-115">請注意，不支援跨會話的關機。</span><span class="sxs-lookup"><span data-stu-id="3881a-115">Note that shutdown across sessions is not supported.</span></span>

<span data-ttu-id="3881a-116">使用 [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4.0 版進行安裝和服務的應用程式會自動使用重新開機管理員來減少系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="3881a-116">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="3881a-117">自訂安裝程式也可以設計來呼叫重新開機管理員 API，以關閉並重新啟動應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="3881a-117">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="3881a-118">在無法避免系統重新開機的情況下，安裝程式可以使用重新開機管理員 API 來排程重新開機，以將使用者工作流程的停機時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="3881a-118">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

<span data-ttu-id="3881a-119">如需在安裝和更新期間使用重新開機管理員 API 的詳細資訊，請參閱 [使用重新開機管理員](using-restart-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="3881a-119">For information about using the Restart Manager API during installation and updates, see [Using Restart Manager](using-restart-manager.md).</span></span>

<span data-ttu-id="3881a-120">重新開機管理員無法停止和重新開機重要的系統服務，不需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="3881a-120">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="3881a-121">如需識別重要系統服務的詳細資訊，請參閱 [重要的系統服務](critical-system-services.md)。</span><span class="sxs-lookup"><span data-stu-id="3881a-121">For more information about identifying critical system services, see [Critical System Services](critical-system-services.md).</span></span>

<span data-ttu-id="3881a-122">您的應用程式和服務應該準備好由重新開機管理員關閉，並儲存清除重新開機所需的使用者資料和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="3881a-122">Your applications and services should be prepared to be shut down by the Restart Manager and save user data and state information that are needed for a clean restart.</span></span> <span data-ttu-id="3881a-123">如需如何準備您的應用程式和服務以使用重新開機管理員的詳細資訊，請參閱 [應用程式和服務的指導方針](guidelines-for-applications-and-services.md)。</span><span class="sxs-lookup"><span data-stu-id="3881a-123">For more information about how to prepare your applications and services to work with the Restart Manager, see [Guidelines for Applications and Services](guidelines-for-applications-and-services.md).</span></span>

<span data-ttu-id="3881a-124">如需重新開機管理員 API 的列舉、結構和函式的參考資訊，請參閱 [重新開機管理員參考](restart-manager-reference.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="3881a-124">For reference information about the enumerations, structures, and functions of the Restart Manager API, see the [Restart Manager Reference](restart-manager-reference.md) section</span></span>

 

 