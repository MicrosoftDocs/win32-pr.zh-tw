---
title: 重新開機管理員
description: 撰寫自訂安裝程式，以消除完成更新使用中的檔案所需的系統重新開機。 從程式關閉並重新啟動所有但重要的系統服務。
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- 重新開機管理員重新開機管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023813"
---
# <a name="restart-manager"></a><span data-ttu-id="cadb9-105">重新開機管理員</span><span class="sxs-lookup"><span data-stu-id="cadb9-105">Restart Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="cadb9-106">目的</span><span class="sxs-lookup"><span data-stu-id="cadb9-106">Purpose</span></span>

<span data-ttu-id="cadb9-107">重新開機管理員 API 可以消除或減少完成安裝或更新所需的系統重新開機次數。</span><span class="sxs-lookup"><span data-stu-id="cadb9-107">The Restart Manager API can eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span> <span data-ttu-id="cadb9-108">在安裝或更新期間，軟體更新需要系統重新開機的主要原因是目前正在執行的應用程式或服務正在更新某些檔案。</span><span class="sxs-lookup"><span data-stu-id="cadb9-108">The primary reason software updates require a system restart during an installation or update is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="cadb9-109">重新開機管理員可讓所有的 [重要系統服務](critical-system-services.md) 關閉並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="cadb9-109">The Restart Manager enables all but the [critical system services](critical-system-services.md) to be shut down and restarted.</span></span> <span data-ttu-id="cadb9-110">這會釋出使用中的檔案，並允許完成安裝作業。</span><span class="sxs-lookup"><span data-stu-id="cadb9-110">This frees files that are in use and allows installation operations to complete.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="cadb9-111">適用時</span><span class="sxs-lookup"><span data-stu-id="cadb9-111">Where applicable</span></span>

<span data-ttu-id="cadb9-112">重新開機管理員 DLL 會匯出可由標準或自訂安裝程式載入的公用 C 介面。</span><span class="sxs-lookup"><span data-stu-id="cadb9-112">The Restart Manager DLL exports a public C interface that can be loaded by standard or custom installers.</span></span> <span data-ttu-id="cadb9-113">安裝程式可以使用重新開機管理員來註冊在安裝應用程式或更新期間應取代的檔案。</span><span class="sxs-lookup"><span data-stu-id="cadb9-113">The installer can use the Restart Manager to register files that should be replaced during the installation of an application or update.</span></span> <span data-ttu-id="cadb9-114">然後，在後續的更新或安裝期間，安裝程式可以使用重新開機管理員來判斷哪些檔案因為目前正在使用中而無法更新。</span><span class="sxs-lookup"><span data-stu-id="cadb9-114">Then during a subsequent update or installation, the installer can use the Restart Manager to determine which files cannot be updated because they are currently in use.</span></span> <span data-ttu-id="cadb9-115">重新開機管理員可以關閉並重新啟動目前正在使用這些檔案的非關鍵服務或應用程式。</span><span class="sxs-lookup"><span data-stu-id="cadb9-115">Restart Manager can shut down and restart the non-critical services or applications that are currently using those files.</span></span> <span data-ttu-id="cadb9-116">安裝程式可以指示重新開機管理員根據使用中的檔案、處理序識別碼 (PID) 或 Windows 服務的簡短名稱，來關閉和重新開機應用程式或服務。</span><span class="sxs-lookup"><span data-stu-id="cadb9-116">Installers can direct the Restart Manager to shut down and restart applications or services based on the file in use, the process ID (PID), or the short-name of a Windows service.</span></span>

<span data-ttu-id="cadb9-117">重新開機管理員適用于桌面樣式應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="cadb9-117">Restart Manager is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cadb9-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="cadb9-118">Developer audience</span></span>

<span data-ttu-id="cadb9-119">本檔適用于想要充分利用 Windows Vista 或 Windows Server 2008 安裝程式功能的安裝應用程式開發人員。</span><span class="sxs-lookup"><span data-stu-id="cadb9-119">This documentation is intended for developers of installation applications who want to take advantage of the installer capabilities in Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="cadb9-120">使用 [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4.0 版進行安裝和服務的應用程式會自動使用重新開機管理員來減少系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="cadb9-120">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="cadb9-121">自訂安裝程式也可以設計來呼叫重新開機管理員 API，以關閉並重新啟動應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="cadb9-121">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="cadb9-122">在無法避免系統重新開機的情況下，安裝程式可以使用重新開機管理員 API 來排程重新開機，以將使用者工作流程的停機時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="cadb9-122">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cadb9-123">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="cadb9-123">Run-time requirements</span></span>

<span data-ttu-id="cadb9-124">從 Windows Vista 和 Windows Server 2008 開始，可以使用重新開機管理員 API。</span><span class="sxs-lookup"><span data-stu-id="cadb9-124">The Restart Manager API is available beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="cadb9-125">重新開機管理員包含單一 DLL，應用程式可以載入該 DLL 來存取重新開機管理員 API。</span><span class="sxs-lookup"><span data-stu-id="cadb9-125">Restart Manager consists of a single DLL that applications can load to access the Restart Manager API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cadb9-126">本節內容</span><span class="sxs-lookup"><span data-stu-id="cadb9-126">In this section</span></span>



| <span data-ttu-id="cadb9-127">主題</span><span class="sxs-lookup"><span data-stu-id="cadb9-127">Topic</span></span>                                                                 | <span data-ttu-id="cadb9-128">描述</span><span class="sxs-lookup"><span data-stu-id="cadb9-128">Description</span></span>                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="cadb9-129">關於重新開機管理員</span><span class="sxs-lookup"><span data-stu-id="cadb9-129">About Restart Manager</span></span>](about-restart-manager.md)<br/>         | <span data-ttu-id="cadb9-130">描述重新開機管理員的總覽主題。</span><span class="sxs-lookup"><span data-stu-id="cadb9-130">Overview topics that describe the Restart Manager.</span></span><br/>   |
| [<span data-ttu-id="cadb9-131">使用重新開機管理員</span><span class="sxs-lookup"><span data-stu-id="cadb9-131">Using Restart Manager</span></span>](using-restart-manager.md)<br/>         | <span data-ttu-id="cadb9-132">使用重新開機管理員 API 的總覽主題。</span><span class="sxs-lookup"><span data-stu-id="cadb9-132">Overview topics about using the Restart Manager API.</span></span><br/> |
| [<span data-ttu-id="cadb9-133">重新開機管理員參考</span><span class="sxs-lookup"><span data-stu-id="cadb9-133">Restart Manager Reference</span></span>](restart-manager-reference.md)<br/> | <span data-ttu-id="cadb9-134">重新開機管理員 API 的參考主題。</span><span class="sxs-lookup"><span data-stu-id="cadb9-134">Reference topics for the Restart Manager API.</span></span><br/>        |



 

 

