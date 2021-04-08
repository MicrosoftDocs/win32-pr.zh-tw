---
title: 重新開機管理員函式
description: 重新開機管理員 API 會使用下表中所識別的功能。
ms.assetid: ed39695a-1eb6-42fe-87a0-bd690bbce028
keywords:
- 重新開機管理員重新開機管理員、參考、函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33187bff8522bfa347dc852f2cac157c2c3966a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839851"
---
# <a name="restart-manager-functions"></a><span data-ttu-id="1efe4-104">重新開機管理員函式</span><span class="sxs-lookup"><span data-stu-id="1efe4-104">Restart Manager Functions</span></span>

<span data-ttu-id="1efe4-105">重新開機管理員 API 會使用下表中所識別的功能。</span><span class="sxs-lookup"><span data-stu-id="1efe4-105">The Restart Manager API uses the functions identified in the following table.</span></span>



| <span data-ttu-id="1efe4-106">函式</span><span class="sxs-lookup"><span data-stu-id="1efe4-106">Function</span></span>                                           | <span data-ttu-id="1efe4-107">描述</span><span class="sxs-lookup"><span data-stu-id="1efe4-107">Description</span></span>                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1efe4-108">**RmAddFilter**</span><span class="sxs-lookup"><span data-stu-id="1efe4-108">**RmAddFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter)                 | <span data-ttu-id="1efe4-109">修改關機或重新開機動作。</span><span class="sxs-lookup"><span data-stu-id="1efe4-109">Modifies shutdown or restart actions.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="1efe4-110">**RmStartSession**</span><span class="sxs-lookup"><span data-stu-id="1efe4-110">**RmStartSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession)           | <span data-ttu-id="1efe4-111">啟動新的重新開機管理員會話。</span><span class="sxs-lookup"><span data-stu-id="1efe4-111">Starts a new Restart Manager session.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="1efe4-112">**RmJoinSession**</span><span class="sxs-lookup"><span data-stu-id="1efe4-112">**RmJoinSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession)             | <span data-ttu-id="1efe4-113">將應用程式的處理常式加入至現有的重新開機管理員會話。</span><span class="sxs-lookup"><span data-stu-id="1efe4-113">Joins the process of an application to an existing Restart Manager session.</span></span>                                                                                                                  |
| [<span data-ttu-id="1efe4-114">**RmEndSession**</span><span class="sxs-lookup"><span data-stu-id="1efe4-114">**RmEndSession**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession)               | <span data-ttu-id="1efe4-115">結束重新開機管理員會話。</span><span class="sxs-lookup"><span data-stu-id="1efe4-115">Ends the Restart Manager session.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="1efe4-116">**RmRegisterResources**</span><span class="sxs-lookup"><span data-stu-id="1efe4-116">**RmRegisterResources**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) | <span data-ttu-id="1efe4-117">將資源（例如檔案名、服務簡短名稱或 [**RM \_ 唯一 \_ 進程**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) 結構）註冊到重新開機管理員會話。</span><span class="sxs-lookup"><span data-stu-id="1efe4-117">Registers resources, such as filenames, service short names, or [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structures, to a Restart Manager session.</span></span>                                   |
| [<span data-ttu-id="1efe4-118">**RmGetList**</span><span class="sxs-lookup"><span data-stu-id="1efe4-118">**RmGetList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)                     | <span data-ttu-id="1efe4-119">供安裝程式用來取得受註冊資源影響的所有應用程式清單及其目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1efe4-119">Used by installers to get a list of all applications affected by registered resources and their current status.</span></span>                                                                              |
| [<span data-ttu-id="1efe4-120">**RmGetFilterList**</span><span class="sxs-lookup"><span data-stu-id="1efe4-120">**RmGetFilterList**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)         | <span data-ttu-id="1efe4-121">查詢關閉的狀態，並重新啟動已套用的修改。</span><span class="sxs-lookup"><span data-stu-id="1efe4-121">Queries the status of shutdown and restart modifications that have already been applied.</span></span>                                                                                                     |
| [<span data-ttu-id="1efe4-122">**RmShutdown**</span><span class="sxs-lookup"><span data-stu-id="1efe4-122">**RmShutdown**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)                   | <span data-ttu-id="1efe4-123">起始應用程式和服務的關閉。</span><span class="sxs-lookup"><span data-stu-id="1efe4-123">Initiates the shut down of applications and services.</span></span>                                                                                                                                        |
| [<span data-ttu-id="1efe4-124">**RmRemoveFilter**</span><span class="sxs-lookup"><span data-stu-id="1efe4-124">**RmRemoveFilter**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)           | <span data-ttu-id="1efe4-125">移除已套用的關機和重新開機修改。</span><span class="sxs-lookup"><span data-stu-id="1efe4-125">Removes shutdown and restart modifications that have already been applied.</span></span>                                                                                                                   |
| [<span data-ttu-id="1efe4-126">**RmRestart**</span><span class="sxs-lookup"><span data-stu-id="1efe4-126">**RmRestart**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart)                     | <span data-ttu-id="1efe4-127">重新開機 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) 函式已關閉的應用程式和服務，並使用 **RegisterApplicationRestart** 註冊要重新開機的應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="1efe4-127">Restarts applications and services that have been shut down by the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function and that have been registered for restart using **RegisterApplicationRestart**.</span></span> |
| [<span data-ttu-id="1efe4-128">**RmCancelCurrentTask**</span><span class="sxs-lookup"><span data-stu-id="1efe4-128">**RmCancelCurrentTask**</span></span>](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) | <span data-ttu-id="1efe4-129">取消目前的 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)、 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)或 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) 函數。</span><span class="sxs-lookup"><span data-stu-id="1efe4-129">Cancels the current [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist), [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown), or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>                                                            |



 

 

 




