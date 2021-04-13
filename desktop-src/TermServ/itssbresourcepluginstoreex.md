---
title: ITsSbResourcePluginStoreEx 介面
description: 公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- ITsSbResourcePluginStoreEx 介面遠端桌面服務
- ITsSbResourcePluginStoreEx 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104297"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="fdd07-105">ITsSbResourcePluginStoreEx 介面</span><span class="sxs-lookup"><span data-stu-id="fdd07-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="fdd07-106">公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。</span><span class="sxs-lookup"><span data-stu-id="fdd07-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="fdd07-107">這些方法會新增、刪除和查詢這些物件。</span><span class="sxs-lookup"><span data-stu-id="fdd07-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="fdd07-108">這個介面僅適用于已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2。</span><span class="sxs-lookup"><span data-stu-id="fdd07-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="fdd07-109">從 Windows Server 2016 開始，可以使用 [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)介面的 [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)和 [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)方法。</span><span class="sxs-lookup"><span data-stu-id="fdd07-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="fdd07-110">成員</span><span class="sxs-lookup"><span data-stu-id="fdd07-110">Members</span></span>

<span data-ttu-id="fdd07-111">**ITsSbResourcePluginStoreEx** 介面繼承自 [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)。</span><span class="sxs-lookup"><span data-stu-id="fdd07-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="fdd07-112">**ITsSbResourcePluginStoreEx** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fdd07-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="fdd07-113">方法</span><span class="sxs-lookup"><span data-stu-id="fdd07-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fdd07-114">方法</span><span class="sxs-lookup"><span data-stu-id="fdd07-114">Methods</span></span>

<span data-ttu-id="fdd07-115">**ITsSbResourcePluginStoreEx** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fdd07-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="fdd07-116">方法</span><span class="sxs-lookup"><span data-stu-id="fdd07-116">Method</span></span>                                                                                                            | <span data-ttu-id="fdd07-117">描述</span><span class="sxs-lookup"><span data-stu-id="fdd07-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdd07-118">**AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="fdd07-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="fdd07-119">鎖定目標。</span><span class="sxs-lookup"><span data-stu-id="fdd07-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fdd07-120">**AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="fdd07-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="fdd07-121">將環境新增至資源外掛程式存放區。</span><span class="sxs-lookup"><span data-stu-id="fdd07-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="fdd07-122">**AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="fdd07-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="fdd07-123">將新的會話新增至資源外掛程式存放區。</span><span class="sxs-lookup"><span data-stu-id="fdd07-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="fdd07-124">**AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="fdd07-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="fdd07-125">將目標新增至資源外掛程式存放區。</span><span class="sxs-lookup"><span data-stu-id="fdd07-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="fdd07-126">**DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="fdd07-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="fdd07-127">刪除目標。</span><span class="sxs-lookup"><span data-stu-id="fdd07-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="fdd07-128">**EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="fdd07-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="fdd07-129">傳回陣列，其中包含存在於資源外掛程式存放區中的環境。</span><span class="sxs-lookup"><span data-stu-id="fdd07-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="fdd07-130">**EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="fdd07-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="fdd07-131">列舉已新增至資源外掛程式存放區的所有伺服器陣列。</span><span class="sxs-lookup"><span data-stu-id="fdd07-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="fdd07-132">**EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="fdd07-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="fdd07-133">列舉一組指定的會話。</span><span class="sxs-lookup"><span data-stu-id="fdd07-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="fdd07-134">**EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="fdd07-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="fdd07-135">傳回陣列，其中包含資源外掛程式存放區中存在的指定目標。</span><span class="sxs-lookup"><span data-stu-id="fdd07-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="fdd07-136">**GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="fdd07-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="fdd07-137">抓取伺服器陣列的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdd07-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="fdd07-138">**QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="fdd07-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="fdd07-139">傳回指定的環境物件。</span><span class="sxs-lookup"><span data-stu-id="fdd07-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="fdd07-140">**QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="fdd07-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="fdd07-141">傳回具有指定之會話識別碼的會話物件。</span><span class="sxs-lookup"><span data-stu-id="fdd07-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="fdd07-142">**QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="fdd07-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="fdd07-143">傳回具有指定之目標名稱和伺服器陣列名稱的目標。</span><span class="sxs-lookup"><span data-stu-id="fdd07-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="fdd07-144">**ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="fdd07-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="fdd07-145">釋放目標的鎖定。</span><span class="sxs-lookup"><span data-stu-id="fdd07-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="fdd07-146">**RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="fdd07-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="fdd07-147">從資源外掛程式存放區中移除指定的環境。</span><span class="sxs-lookup"><span data-stu-id="fdd07-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="fdd07-148">**SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="fdd07-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="fdd07-149">儲存環境。</span><span class="sxs-lookup"><span data-stu-id="fdd07-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="fdd07-150">**SaveSession**</span><span class="sxs-lookup"><span data-stu-id="fdd07-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="fdd07-151">儲存會話。</span><span class="sxs-lookup"><span data-stu-id="fdd07-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="fdd07-152">**SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="fdd07-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="fdd07-153">儲存目標。</span><span class="sxs-lookup"><span data-stu-id="fdd07-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="fdd07-154">**SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="fdd07-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="fdd07-155">在環境上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="fdd07-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="fdd07-156">**SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="fdd07-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="fdd07-157">在環境上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="fdd07-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="fdd07-158">**SetSessionState**</span><span class="sxs-lookup"><span data-stu-id="fdd07-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="fdd07-159">設定工作階段的狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd07-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="fdd07-160">**SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="fdd07-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="fdd07-161">設定目標上的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdd07-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="fdd07-162">**SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="fdd07-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="fdd07-163">設定目標上的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdd07-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="fdd07-164">**SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="fdd07-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="fdd07-165">設定目標的狀態。</span><span class="sxs-lookup"><span data-stu-id="fdd07-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="fdd07-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdd07-166">Requirements</span></span>



| <span data-ttu-id="fdd07-167">需求</span><span class="sxs-lookup"><span data-stu-id="fdd07-167">Requirement</span></span> | <span data-ttu-id="fdd07-168">值</span><span class="sxs-lookup"><span data-stu-id="fdd07-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd07-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdd07-169">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd07-170">都不支援</span><span class="sxs-lookup"><span data-stu-id="fdd07-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fdd07-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdd07-171">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd07-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fdd07-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="fdd07-173">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="fdd07-173">End of server support</span></span><br/>    | <span data-ttu-id="fdd07-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fdd07-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="fdd07-175">IID</span><span class="sxs-lookup"><span data-stu-id="fdd07-175">IID</span></span><br/>                      | <span data-ttu-id="fdd07-176">IID \_ ITsSbResourcePluginStoreEx 定義為80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="fdd07-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fdd07-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdd07-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd07-178">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="fdd07-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="fdd07-179">遠端桌面虛擬化介面</span><span class="sxs-lookup"><span data-stu-id="fdd07-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





