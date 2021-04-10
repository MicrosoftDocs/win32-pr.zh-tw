---
title: QMGR 介面
description: 使用下列佇列管理員 (QMGR) 介面，以下載檔案並監視下載佇列中的作業。
ms.assetid: b5b59d4f-fa18-4225-8b6f-5d4033c61650
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cc571dcc5bbf182b3f715ee34bb6c3e94b5502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183047"
---
# <a name="qmgr-interfaces"></a><span data-ttu-id="e9437-103">QMGR 介面</span><span class="sxs-lookup"><span data-stu-id="e9437-103">QMGR Interfaces</span></span>

<span data-ttu-id="e9437-104">\[佇列管理員 (QMGR) 介面可用於主題的需求一節中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e9437-104">\[Queue Manager (QMGR) interfaces are available for use in the operating systems specified in a topic's Requirements section.</span></span> <span data-ttu-id="e9437-105">在後續的版本中，我們可能會修改其功能或不再提供。</span><span class="sxs-lookup"><span data-stu-id="e9437-105">They may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e9437-106">請改用 [BITS 介面](bits-interfaces.md)。\]</span><span class="sxs-lookup"><span data-stu-id="e9437-106">Instead, use the [BITS interfaces](bits-interfaces.md).\]</span></span>

<span data-ttu-id="e9437-107">使用下列佇列管理員 (QMGR) 介面，以下載檔案並監視下載佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="e9437-107">Use the following Queue Manager (QMGR) interfaces to download files and monitor jobs within the download queue.</span></span>



| <span data-ttu-id="e9437-108">介面</span><span class="sxs-lookup"><span data-stu-id="e9437-108">Interface</span></span>                                                                 | <span data-ttu-id="e9437-109">描述</span><span class="sxs-lookup"><span data-stu-id="e9437-109">Description</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9437-110">**IBackgroundCopyCallback1**</span><span class="sxs-lookup"><span data-stu-id="e9437-110">**IBackgroundCopyCallback1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopycallback1)<br/>   | <span data-ttu-id="e9437-111">當事件發生時，執行以接收通知。</span><span class="sxs-lookup"><span data-stu-id="e9437-111">Implement to receive notification when events occur.</span></span><br/>                                                                                               |
| [<span data-ttu-id="e9437-112">**IBackgroundCopyGroup**</span><span class="sxs-lookup"><span data-stu-id="e9437-112">**IBackgroundCopyGroup**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopygroup)<br/>           | <span data-ttu-id="e9437-113">使用管理群組。</span><span class="sxs-lookup"><span data-stu-id="e9437-113">Use to manage the group.</span></span> <span data-ttu-id="e9437-114">例如，將作業新增至群組、設定群組的屬性，以及啟動和停止下載佇列中的群組。</span><span class="sxs-lookup"><span data-stu-id="e9437-114">For example, add a job to the group, set the properties of the group, and start and stop the group in the download queue.</span></span><br/> |
| [<span data-ttu-id="e9437-115">**IBackgroundCopyJob1**</span><span class="sxs-lookup"><span data-stu-id="e9437-115">**IBackgroundCopyJob1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyjob1)<br/>             | <span data-ttu-id="e9437-116">用來將檔案新增至作業，並取得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e9437-116">Use to add files to the job and retrieve the job's status.</span></span><br/>                                                                                         |
| [<span data-ttu-id="e9437-117">**IBackgroundCopyQMgr**</span><span class="sxs-lookup"><span data-stu-id="e9437-117">**IBackgroundCopyQMgr**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ibackgroundcopyqmgr)<br/>             | <span data-ttu-id="e9437-118">用來建立新的群組、取出現有的群組，或列舉佇列中的所有群組。</span><span class="sxs-lookup"><span data-stu-id="e9437-118">Use to create a new group, retrieve an existing group, or enumerate all groups in the queue.</span></span><br/>                                                       |
| [<span data-ttu-id="e9437-119">**IEnumBackgroundCopyGroups**</span><span class="sxs-lookup"><span data-stu-id="e9437-119">**IEnumBackgroundCopyGroups**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopygroups)<br/> | <span data-ttu-id="e9437-120">用來取得下載佇列中的群組清單。</span><span class="sxs-lookup"><span data-stu-id="e9437-120">Use to retrieve a list of groups in the download queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="e9437-121">**IEnumBackgroundCopyJobs1**</span><span class="sxs-lookup"><span data-stu-id="e9437-121">**IEnumBackgroundCopyJobs1**</span></span>](/windows/desktop/api/Qmgr/nn-qmgr-ienumbackgroundcopyjobs1)<br/>   | <span data-ttu-id="e9437-122">用來取得群組中的作業清單。</span><span class="sxs-lookup"><span data-stu-id="e9437-122">Use to retrieve a list of jobs in the group.</span></span><br/>                                                                                                       |



 

 

 





