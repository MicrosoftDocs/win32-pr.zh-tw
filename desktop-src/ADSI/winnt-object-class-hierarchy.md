---
title: WinNT 物件類別階層
description: WinNT 物件類別階層從 Namespace 物件開始。
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- WinNT 服務提供者 ADSI、物件類別階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507024"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="c6e5c-104">WinNT 物件類別階層</span><span class="sxs-lookup"><span data-stu-id="c6e5c-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="c6e5c-105">WinNT 物件類別階層從 Namespace 物件開始。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="c6e5c-106">Object 類別</span><span class="sxs-lookup"><span data-stu-id="c6e5c-106">Object class</span></span>                   | <span data-ttu-id="c6e5c-107">Description</span><span class="sxs-lookup"><span data-stu-id="c6e5c-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c6e5c-108">命名空間</span><span class="sxs-lookup"><span data-stu-id="c6e5c-108">Namespace</span></span><br/>           | <span data-ttu-id="c6e5c-109">最上層物件容器。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="c6e5c-110">網域</span><span class="sxs-lookup"><span data-stu-id="c6e5c-110">Domain</span></span><br/>              | <span data-ttu-id="c6e5c-111">Windows NT 網域。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="c6e5c-112">User</span><span class="sxs-lookup"><span data-stu-id="c6e5c-112">User</span></span><br/>                | <span data-ttu-id="c6e5c-113">使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="c6e5c-114">Group</span><span class="sxs-lookup"><span data-stu-id="c6e5c-114">Group</span></span><br/>               | <span data-ttu-id="c6e5c-115">用於管理存取權限的群組帳戶。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="c6e5c-116">UserGroupCollection</span><span class="sxs-lookup"><span data-stu-id="c6e5c-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="c6e5c-117">一組執行 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="c6e5c-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="c6e5c-118">GroupCollection</span></span><br/>     | <span data-ttu-id="c6e5c-119">一組執行 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)的其他群組。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="c6e5c-120">電腦</span><span class="sxs-lookup"><span data-stu-id="c6e5c-120">Computer</span></span><br/>            | <span data-ttu-id="c6e5c-121">Windows NT 4.0 伺服器或工作站。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="c6e5c-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="c6e5c-122">PrintJob</span></span><br/>            | <span data-ttu-id="c6e5c-123">列印佇列中的列印工作。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="c6e5c-124">PrintJobsCollection</span><span class="sxs-lookup"><span data-stu-id="c6e5c-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="c6e5c-125">一組列印工作。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="c6e5c-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="c6e5c-126">PrintQueue</span></span><br/>          | <span data-ttu-id="c6e5c-127">列印印表機多工緩衝處理程式上的佇列。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="c6e5c-128">服務</span><span class="sxs-lookup"><span data-stu-id="c6e5c-128">Service</span></span><br/>             | <span data-ttu-id="c6e5c-129">以服務方式執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="c6e5c-130">FileService</span><span class="sxs-lookup"><span data-stu-id="c6e5c-130">FileService</span></span><br/>         | <span data-ttu-id="c6e5c-131">存取檔案系統的服務。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="c6e5c-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="c6e5c-132">FileShare</span></span><br/>           | <span data-ttu-id="c6e5c-133">檔案共用點。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="c6e5c-134">資源</span><span class="sxs-lookup"><span data-stu-id="c6e5c-134">Resource</span></span><br/>            | <span data-ttu-id="c6e5c-135">服務中的資源。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="c6e5c-136">工作階段</span><span class="sxs-lookup"><span data-stu-id="c6e5c-136">Session</span></span><br/>             | <span data-ttu-id="c6e5c-137">作用中的檔案服務連接。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="c6e5c-138">User</span><span class="sxs-lookup"><span data-stu-id="c6e5c-138">User</span></span><br/>                | <span data-ttu-id="c6e5c-139">本機使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="c6e5c-140">Group</span><span class="sxs-lookup"><span data-stu-id="c6e5c-140">Group</span></span><br/>               | <span data-ttu-id="c6e5c-141">本機群組。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="c6e5c-142">UserCollection</span><span class="sxs-lookup"><span data-stu-id="c6e5c-142">UserCollection</span></span><br/>      | <span data-ttu-id="c6e5c-143">本機使用者的集合。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="c6e5c-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="c6e5c-144">GroupCollection</span></span><br/>     | <span data-ttu-id="c6e5c-145">本機群組的集合。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="c6e5c-146">結構描述</span><span class="sxs-lookup"><span data-stu-id="c6e5c-146">Schema</span></span><br/>              | <span data-ttu-id="c6e5c-147">WinNT 架構容器。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="c6e5c-148">類別</span><span class="sxs-lookup"><span data-stu-id="c6e5c-148">Class</span></span><br/>               | <span data-ttu-id="c6e5c-149">架構類別定義。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="c6e5c-150">屬性</span><span class="sxs-lookup"><span data-stu-id="c6e5c-150">Property</span></span><br/>            | <span data-ttu-id="c6e5c-151">架構屬性定義。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="c6e5c-152">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6e5c-152">Syntax</span></span><br/>              | <span data-ttu-id="c6e5c-153">屬性的語法。</span><span class="sxs-lookup"><span data-stu-id="c6e5c-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





