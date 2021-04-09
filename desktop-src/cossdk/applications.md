---
description: 針對安裝在本機電腦上的每個 COM + 應用程式，各包含一個物件。 這些物件所公開的屬性會保存在應用層級所做的所有設定。
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: 應用程式集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111056"
---
# <a name="applications-collection"></a><span data-ttu-id="ca92d-104">應用程式集合</span><span class="sxs-lookup"><span data-stu-id="ca92d-104">Applications collection</span></span>

<span data-ttu-id="ca92d-105">針對安裝在本機電腦上的每個 COM + 應用程式，各包含一個物件。</span><span class="sxs-lookup"><span data-stu-id="ca92d-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="ca92d-106">這些物件所公開的屬性會保存在應用層級所做的所有設定。</span><span class="sxs-lookup"><span data-stu-id="ca92d-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="ca92d-107">您可以使用相關 [**元件**](components.md) 集合來設定應用程式中元件的屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="ca92d-108">您可以使用相關的 [**角色**](roles.md) 集合，將角色指派給應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="ca92d-109">若要將元件安裝到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="ca92d-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="ca92d-110">若要從檔案安裝應用程式，或關閉或匯出應用程式，也請在 **COMAdminCatalog** 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="ca92d-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="ca92d-111">否則，若要建立新的應用程式，您可以將物件加入至 **應用程式** 集合。</span><span class="sxs-lookup"><span data-stu-id="ca92d-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="ca92d-112">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**加入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**移除**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="ca92d-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ca92d-113">成員</span><span class="sxs-lookup"><span data-stu-id="ca92d-113">Members</span></span>

<span data-ttu-id="ca92d-114">**應用程式** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="ca92d-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ca92d-115">相關集合</span><span class="sxs-lookup"><span data-stu-id="ca92d-115">Related Collections</span></span>

<span data-ttu-id="ca92d-116">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="ca92d-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ca92d-117">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="ca92d-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="ca92d-118">**單元**</span><span class="sxs-lookup"><span data-stu-id="ca92d-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="ca92d-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ca92d-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ca92d-120">**LegacyComponents**</span><span class="sxs-lookup"><span data-stu-id="ca92d-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="ca92d-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ca92d-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ca92d-122">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ca92d-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="ca92d-123">**角色**</span><span class="sxs-lookup"><span data-stu-id="ca92d-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="ca92d-124">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="ca92d-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ca92d-125">**分區**</span><span class="sxs-lookup"><span data-stu-id="ca92d-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="ca92d-126">**根**</span><span class="sxs-lookup"><span data-stu-id="ca92d-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ca92d-127">屬性</span><span class="sxs-lookup"><span data-stu-id="ca92d-127">Properties</span></span>

<span data-ttu-id="ca92d-128">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="ca92d-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ca92d-129">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="ca92d-130">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="ca92d-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="ca92d-131">啟用</span><span class="sxs-lookup"><span data-stu-id="ca92d-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="ca92d-132">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="ca92d-133">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="ca92d-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="ca92d-134">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="ca92d-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="ca92d-135">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="ca92d-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="ca92d-136">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="ca92d-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="ca92d-137">驗證</span><span class="sxs-lookup"><span data-stu-id="ca92d-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="ca92d-138">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="ca92d-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="ca92d-139">多變</span><span class="sxs-lookup"><span data-stu-id="ca92d-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="ca92d-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="ca92d-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="ca92d-141">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="ca92d-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="ca92d-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="ca92d-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="ca92d-143">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="ca92d-144">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="ca92d-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="ca92d-145">刪除</span><span class="sxs-lookup"><span data-stu-id="ca92d-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="ca92d-146">說明</span><span class="sxs-lookup"><span data-stu-id="ca92d-146">Description</span></span>](#description)
-   [<span data-ttu-id="ca92d-147">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="ca92d-148">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="ca92d-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="ca92d-149">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="ca92d-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="ca92d-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="ca92d-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="ca92d-151">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="ca92d-152">識別碼</span><span class="sxs-lookup"><span data-stu-id="ca92d-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="ca92d-153">身分識別</span><span class="sxs-lookup"><span data-stu-id="ca92d-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="ca92d-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="ca92d-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="ca92d-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="ca92d-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="ca92d-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="ca92d-157">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="ca92d-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="ca92d-158">名稱</span><span class="sxs-lookup"><span data-stu-id="ca92d-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="ca92d-159">密碼</span><span class="sxs-lookup"><span data-stu-id="ca92d-159">Password</span></span>](#password)
-   [<span data-ttu-id="ca92d-160">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="ca92d-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="ca92d-161">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="ca92d-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="ca92d-162">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="ca92d-163">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="ca92d-164">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="ca92d-165">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="ca92d-166">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="ca92d-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="ca92d-167">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="ca92d-168">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="ca92d-169">複製</span><span class="sxs-lookup"><span data-stu-id="ca92d-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="ca92d-170">RunForever</span><span class="sxs-lookup"><span data-stu-id="ca92d-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="ca92d-171">ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca92d-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="ca92d-172">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="ca92d-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="ca92d-173">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="ca92d-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="ca92d-174">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="ca92d-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="ca92d-175">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="ca92d-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="ca92d-176">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="ca92d-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="ca92d-177">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="ca92d-178">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="ca92d-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="ca92d-179">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="ca92d-180">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-180">Entry</span></span> | <span data-ttu-id="ca92d-181">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-182">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-182">Description</span></span>    | <span data-ttu-id="ca92d-183">指出應用程式是否可以在其進程中使用 3 GB 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ca92d-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="ca92d-184">如果未啟用此功能，應用程式只能使用 2 GB 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ca92d-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="ca92d-185">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-185">Access</span></span>         | <span data-ttu-id="ca92d-186">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="ca92d-187">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-187">Type</span></span>           | <span data-ttu-id="ca92d-188">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="ca92d-189">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-189">Default</span></span>        | <span data-ttu-id="ca92d-190">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="ca92d-191">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-191">Minimum system</span></span> | <span data-ttu-id="ca92d-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="ca92d-193">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="ca92d-193">AccessChecksLevel</span></span>



| <span data-ttu-id="ca92d-194">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-194">Entry</span></span> | <span data-ttu-id="ca92d-195">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-196">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-196">Description</span></span>    | <span data-ttu-id="ca92d-197">指出是否只在進程層級執行存取檢查，或在進程和元件層級執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="ca92d-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="ca92d-198">建議您在列舉中使用常數，而不要使用數值。</span><span class="sxs-lookup"><span data-stu-id="ca92d-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="ca92d-199">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-199">Access</span></span>         | <span data-ttu-id="ca92d-200">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="ca92d-201">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-201">Type</span></span>           | <span data-ttu-id="ca92d-202">很長可能的值： COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1) </span><span class="sxs-lookup"><span data-stu-id="ca92d-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="ca92d-203">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-203">Default</span></span>        | <span data-ttu-id="ca92d-204">COMAdminAccessChecksApplicationComponentLevel (1) </span><span class="sxs-lookup"><span data-stu-id="ca92d-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="ca92d-205">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-205">Minimum system</span></span> | <span data-ttu-id="ca92d-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="ca92d-207">啟用</span><span class="sxs-lookup"><span data-stu-id="ca92d-207">Activation</span></span>



| <span data-ttu-id="ca92d-208">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-208">Entry</span></span> | <span data-ttu-id="ca92d-209">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-210">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-210">Description</span></span>    | <span data-ttu-id="ca92d-211">本機啟用表示應用程式內的物件會在專用本機伺服器進程中執行， (server 應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="ca92d-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="ca92d-212">同進程啟用表示物件會在其建立者的進程中執行， (程式庫應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="ca92d-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="ca92d-213">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-213">Access</span></span>         | <span data-ttu-id="ca92d-214">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="ca92d-215">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-215">Type</span></span>           | <span data-ttu-id="ca92d-216">很長可能的值： COMAdminActivationInproc (0) COMAdminActivationLocal (1) </span><span class="sxs-lookup"><span data-stu-id="ca92d-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="ca92d-217">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-217">Default</span></span>        | <span data-ttu-id="ca92d-218">COMAdminActivationLocal (1) </span><span class="sxs-lookup"><span data-stu-id="ca92d-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="ca92d-219">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-219">Minimum system</span></span> | <span data-ttu-id="ca92d-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="ca92d-221">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="ca92d-222">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-222">Entry</span></span> | <span data-ttu-id="ca92d-223">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-224">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-224">Description</span></span>    | <span data-ttu-id="ca92d-225">指出當用戶端對應用程式進行呼叫時，是否對該應用程式執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="ca92d-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="ca92d-226">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-226">Access</span></span>         | <span data-ttu-id="ca92d-227">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="ca92d-228">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-228">Type</span></span>           | <span data-ttu-id="ca92d-229">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="ca92d-230">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-230">Default</span></span>        | <span data-ttu-id="ca92d-231">對</span><span class="sxs-lookup"><span data-stu-id="ca92d-231">True</span></span>                                                                                               |
| <span data-ttu-id="ca92d-232">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-232">Minimum system</span></span> | <span data-ttu-id="ca92d-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="ca92d-234">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="ca92d-234">ApplicationDirectory</span></span>



| <span data-ttu-id="ca92d-235">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-235">Entry</span></span> | <span data-ttu-id="ca92d-236">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-237">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-237">Description</span></span>    | <span data-ttu-id="ca92d-238">應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ca92d-238">The full path to the application.</span></span> <span data-ttu-id="ca92d-239">當您設定並存 (SxS) 元件時，需要這項資訊。</span><span class="sxs-lookup"><span data-stu-id="ca92d-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="ca92d-240">並存 (SxS) 元件可讓 ASP 應用程式指定要使用的 SxS 支援系統 DLL 版本，例如 MSVCRT.LIB、MSXML、COMCTL、GDIPLUS.DLL 等等。</span><span class="sxs-lookup"><span data-stu-id="ca92d-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="ca92d-241">例如，如果您的 ASP 應用程式依賴 MSVCRT.LIB 2.0 版，您可以確保即使在將 service pack 套用至伺服器之後，您的應用程式仍會使用 MSVCRT.LIB 2.0 版。</span><span class="sxs-lookup"><span data-stu-id="ca92d-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="ca92d-242">電腦上仍會安裝任何新版的 MSVCRT.LIB，但您的應用程式會保留2.0 版並使用。</span><span class="sxs-lookup"><span data-stu-id="ca92d-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="ca92d-243">SxS 支援的 Dll 儲存在% WINDIR% \\ WinSxS 中。</span><span class="sxs-lookup"><span data-stu-id="ca92d-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="ca92d-244">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-244">Access</span></span>         | <span data-ttu-id="ca92d-245">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ca92d-246">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-246">Type</span></span>           | <span data-ttu-id="ca92d-247">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ca92d-248">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-248">Default</span></span>        | <span data-ttu-id="ca92d-249">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ca92d-250">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-250">Minimum system</span></span> | <span data-ttu-id="ca92d-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="ca92d-252">雖然這項功能可在應用層級進行設定，但在任何應用程式集區中只能使用一個系統 DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="ca92d-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="ca92d-253">例如，如果應用程式 App1 使用 MSVCRT.LIB，2.5 版和應用程式 App2 會使用 MSVCRT.LIB、2.4 版，則 App1 和 App2 不應該在相同的應用程式集區中。</span><span class="sxs-lookup"><span data-stu-id="ca92d-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="ca92d-254">如果是，則第一次載入的應用程式會載入其 MSVCRT.LIB 的版本，而其他應用程式則會強制使用它，直到卸載應用程式為止。</span><span class="sxs-lookup"><span data-stu-id="ca92d-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="ca92d-255">如需詳細資訊，請參閱 [IIS 6.0 的 COM + 服務變更](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90))中的「並存元件」。</span><span class="sxs-lookup"><span data-stu-id="ca92d-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="ca92d-256">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="ca92d-256">ApplicationProxy</span></span>



| <span data-ttu-id="ca92d-257">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-257">Entry</span></span> | <span data-ttu-id="ca92d-258">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="ca92d-259">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-259">Description</span></span>    | <span data-ttu-id="ca92d-260">指出應用程式是否為應用程式 proxy。</span><span class="sxs-lookup"><span data-stu-id="ca92d-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="ca92d-261">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-261">Access</span></span>         | <span data-ttu-id="ca92d-262">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca92d-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="ca92d-263">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-263">Type</span></span>           | <span data-ttu-id="ca92d-264">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-264">Bool</span></span>                                                       |
| <span data-ttu-id="ca92d-265">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-265">Default</span></span>        | <span data-ttu-id="ca92d-266">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-266">False</span></span>                                                      |
| <span data-ttu-id="ca92d-267">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-267">Minimum system</span></span> | <span data-ttu-id="ca92d-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="ca92d-269">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="ca92d-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="ca92d-270">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-270">Entry</span></span> | <span data-ttu-id="ca92d-271">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-272">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-272">Description</span></span>    | <span data-ttu-id="ca92d-273">匯出應用程式 proxy 時使用的遠端伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ca92d-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="ca92d-274">它是應用程式 proxy 在用戶端電腦上安裝時所指向的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ca92d-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="ca92d-275">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-275">Access</span></span>         | <span data-ttu-id="ca92d-276">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="ca92d-277">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-277">Type</span></span>           | <span data-ttu-id="ca92d-278">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="ca92d-279">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-279">Default</span></span>        | <span data-ttu-id="ca92d-280">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="ca92d-281">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-281">Minimum system</span></span> | <span data-ttu-id="ca92d-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="ca92d-283">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="ca92d-283">AppPartitionID</span></span>



| <span data-ttu-id="ca92d-284">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-284">Entry</span></span> | <span data-ttu-id="ca92d-285">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="ca92d-286">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-286">Description</span></span>    | <span data-ttu-id="ca92d-287">表示應用程式分割識別碼的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ca92d-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="ca92d-288">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-288">Access</span></span>         | <span data-ttu-id="ca92d-289">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca92d-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="ca92d-290">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-290">Type</span></span>           | <span data-ttu-id="ca92d-291">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-291">String</span></span>                                            |
| <span data-ttu-id="ca92d-292">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="ca92d-293">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-293">Minimum system</span></span> | <span data-ttu-id="ca92d-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca92d-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="ca92d-295">驗證</span><span class="sxs-lookup"><span data-stu-id="ca92d-295">Authentication</span></span>



| <span data-ttu-id="ca92d-296">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-296">Entry</span></span> | <span data-ttu-id="ca92d-297">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-298">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-298">Description</span></span>    | <span data-ttu-id="ca92d-299">設定呼叫的驗證層級，其值會對應至遠端程序呼叫， (RPC) 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="ca92d-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="ca92d-300">選擇 COMAdminAuthenticationDefault 時，會使用 [**LocalComputer**](localcomputer.md) 集合內 DefaultAuthenticationLevel 屬性中的設定。</span><span class="sxs-lookup"><span data-stu-id="ca92d-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="ca92d-301">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-301">Access</span></span>         | <span data-ttu-id="ca92d-302">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ca92d-303">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-303">Type</span></span>           | <span data-ttu-id="ca92d-304">長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) </span><span class="sxs-lookup"><span data-stu-id="ca92d-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="ca92d-305">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-305">Default</span></span>        | <span data-ttu-id="ca92d-306">COMAdminAuthenticationPacket (4) </span><span class="sxs-lookup"><span data-stu-id="ca92d-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ca92d-307">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-307">Minimum system</span></span> | <span data-ttu-id="ca92d-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="ca92d-309">針對程式庫 (同進程) 應用程式中，唯一有效的設定是 COMAdminAuthenticationDefault 和 COMAdminAuthenticationNone。</span><span class="sxs-lookup"><span data-stu-id="ca92d-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="ca92d-310">建議您在列舉中使用常數，而不要使用數值。</span><span class="sxs-lookup"><span data-stu-id="ca92d-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="ca92d-311">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="ca92d-311">AuthenticationCapability</span></span>



| <span data-ttu-id="ca92d-312">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-312">Entry</span></span> | <span data-ttu-id="ca92d-313">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-314">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-314">Description</span></span>    | <span data-ttu-id="ca92d-315">決定模擬呼叫時所要顯示的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ca92d-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="ca92d-316">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-316">Access</span></span>         | <span data-ttu-id="ca92d-317">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="ca92d-318">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-318">Type</span></span>           | <span data-ttu-id="ca92d-319">較長的可能值： COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) </span><span class="sxs-lookup"><span data-stu-id="ca92d-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="ca92d-320">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-320">Default</span></span>        | <span data-ttu-id="ca92d-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) </span><span class="sxs-lookup"><span data-stu-id="ca92d-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="ca92d-322">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-322">Minimum system</span></span> | <span data-ttu-id="ca92d-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="ca92d-324">多變</span><span class="sxs-lookup"><span data-stu-id="ca92d-324">Changeable</span></span>



| <span data-ttu-id="ca92d-325">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-325">Entry</span></span> | <span data-ttu-id="ca92d-326">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-327">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-327">Description</span></span>    | <span data-ttu-id="ca92d-328">決定是否允許以程式設計方式或透過「元件服務」系統管理工具，來變更應用程式設定或其元件的變更。</span><span class="sxs-lookup"><span data-stu-id="ca92d-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="ca92d-329">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-329">Access</span></span>         | <span data-ttu-id="ca92d-330">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="ca92d-331">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-331">Type</span></span>           | <span data-ttu-id="ca92d-332">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ca92d-333">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-333">Default</span></span>        | <span data-ttu-id="ca92d-334">對</span><span class="sxs-lookup"><span data-stu-id="ca92d-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ca92d-335">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-335">Minimum system</span></span> | <span data-ttu-id="ca92d-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="ca92d-337">CommandLine</span><span class="sxs-lookup"><span data-stu-id="ca92d-337">CommandLine</span></span>



| <span data-ttu-id="ca92d-338">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-338">Entry</span></span> | <span data-ttu-id="ca92d-339">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-340">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-340">Description</span></span>    | <span data-ttu-id="ca92d-341">用於偵錯工具的命令列字串。</span><span class="sxs-lookup"><span data-stu-id="ca92d-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="ca92d-342">您可以使用指定的命令列，在偵錯工具中啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="ca92d-343">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-343">Access</span></span>         | <span data-ttu-id="ca92d-344">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="ca92d-345">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-345">Type</span></span>           | <span data-ttu-id="ca92d-346">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="ca92d-347">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-347">Default</span></span>        | <span data-ttu-id="ca92d-348">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="ca92d-349">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-349">Minimum system</span></span> | <span data-ttu-id="ca92d-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="ca92d-351">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="ca92d-351">ConcurrentApps</span></span>



| <span data-ttu-id="ca92d-352">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-352">Entry</span></span> | <span data-ttu-id="ca92d-353">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-354">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-354">Description</span></span>    | <span data-ttu-id="ca92d-355">指定可以同時執行之共用應用程式的最大數目。</span><span class="sxs-lookup"><span data-stu-id="ca92d-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="ca92d-356">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-356">Access</span></span>         | <span data-ttu-id="ca92d-357">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="ca92d-358">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-358">Type</span></span>           | <span data-ttu-id="ca92d-359">Long (1-1048576) </span><span class="sxs-lookup"><span data-stu-id="ca92d-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="ca92d-360">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-360">Default</span></span>        | <span data-ttu-id="ca92d-361">1</span><span class="sxs-lookup"><span data-stu-id="ca92d-361">1</span></span>                                                                                |
| <span data-ttu-id="ca92d-362">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-362">Minimum system</span></span> | <span data-ttu-id="ca92d-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="ca92d-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="ca92d-364">CreatedBy</span></span>



| <span data-ttu-id="ca92d-365">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-365">Entry</span></span> | <span data-ttu-id="ca92d-366">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="ca92d-367">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-367">Description</span></span>    | <span data-ttu-id="ca92d-368">說明如何建立應用程式的資訊字串。</span><span class="sxs-lookup"><span data-stu-id="ca92d-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="ca92d-369">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-369">Access</span></span>         | <span data-ttu-id="ca92d-370">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="ca92d-371">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-371">Type</span></span>           | <span data-ttu-id="ca92d-372">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-372">String</span></span>                                                        |
| <span data-ttu-id="ca92d-373">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-373">Default</span></span>        | <span data-ttu-id="ca92d-374">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-374">""</span></span>                                                            |
| <span data-ttu-id="ca92d-375">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-375">Minimum system</span></span> | <span data-ttu-id="ca92d-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="ca92d-377">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-377">CRMEnabled</span></span>



| <span data-ttu-id="ca92d-378">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-378">Entry</span></span> | <span data-ttu-id="ca92d-379">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="ca92d-380">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-380">Description</span></span>    | <span data-ttu-id="ca92d-381">判斷是否已啟用補償 Resource Manager。</span><span class="sxs-lookup"><span data-stu-id="ca92d-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="ca92d-382">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-382">Access</span></span>         | <span data-ttu-id="ca92d-383">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="ca92d-384">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-384">Type</span></span>           | <span data-ttu-id="ca92d-385">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-385">Bool</span></span>                                                             |
| <span data-ttu-id="ca92d-386">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-386">Default</span></span>        | <span data-ttu-id="ca92d-387">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-387">False</span></span>                                                            |
| <span data-ttu-id="ca92d-388">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-388">Minimum system</span></span> | <span data-ttu-id="ca92d-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="ca92d-390">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="ca92d-390">CRMLogFile</span></span>



| <span data-ttu-id="ca92d-391">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-391">Entry</span></span> | <span data-ttu-id="ca92d-392">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-393">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-393">Description</span></span>    | <span data-ttu-id="ca92d-394">用來保存補償資源管理員 (CRM) 記錄檔的檔案名和路徑。</span><span class="sxs-lookup"><span data-stu-id="ca92d-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="ca92d-395">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-395">Access</span></span>         | <span data-ttu-id="ca92d-396">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="ca92d-397">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-397">Type</span></span>           | <span data-ttu-id="ca92d-398">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-398">String</span></span>                                                                                 |
| <span data-ttu-id="ca92d-399">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-399">Default</span></span>        | <span data-ttu-id="ca92d-400">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-400">""</span></span>                                                                                     |
| <span data-ttu-id="ca92d-401">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-401">Minimum system</span></span> | <span data-ttu-id="ca92d-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="ca92d-403">刪除</span><span class="sxs-lookup"><span data-stu-id="ca92d-403">Deleteable</span></span>



| <span data-ttu-id="ca92d-404">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-404">Entry</span></span> | <span data-ttu-id="ca92d-405">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-406">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-406">Description</span></span>    | <span data-ttu-id="ca92d-407">設定是否可透過程式設計方式或透過元件服務管理工具來刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="ca92d-408">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-408">Access</span></span>         | <span data-ttu-id="ca92d-409">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="ca92d-410">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-410">Type</span></span>           | <span data-ttu-id="ca92d-411">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="ca92d-412">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-412">Default</span></span>        | <span data-ttu-id="ca92d-413">對</span><span class="sxs-lookup"><span data-stu-id="ca92d-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="ca92d-414">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-414">Minimum system</span></span> | <span data-ttu-id="ca92d-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="ca92d-416">Description</span><span class="sxs-lookup"><span data-stu-id="ca92d-416">Description</span></span>



| <span data-ttu-id="ca92d-417">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-417">Entry</span></span> | <span data-ttu-id="ca92d-418">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="ca92d-419">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-419">Description</span></span>    | <span data-ttu-id="ca92d-420">描述應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-420">Describes the application.</span></span> |
| <span data-ttu-id="ca92d-421">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-421">Access</span></span>         | <span data-ttu-id="ca92d-422">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-422">ReadWrite</span></span>                  |
| <span data-ttu-id="ca92d-423">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-423">Type</span></span>           | <span data-ttu-id="ca92d-424">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-424">String</span></span>                     |
| <span data-ttu-id="ca92d-425">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-425">Default</span></span>        | <span data-ttu-id="ca92d-426">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-426">""</span></span>                         |
| <span data-ttu-id="ca92d-427">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-427">Minimum system</span></span> | <span data-ttu-id="ca92d-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="ca92d-429">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-429">DumpEnabled</span></span>



| <span data-ttu-id="ca92d-430">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-430">Entry</span></span> | <span data-ttu-id="ca92d-431">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-432">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-432">Description</span></span>    | <span data-ttu-id="ca92d-433">啟用在指定目錄失敗時，將 COM + 應用程式的狀態傾印。</span><span class="sxs-lookup"><span data-stu-id="ca92d-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="ca92d-434">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-434">Access</span></span>         | <span data-ttu-id="ca92d-435">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="ca92d-436">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-436">Type</span></span>           | <span data-ttu-id="ca92d-437">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="ca92d-438">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-438">Default</span></span>        | <span data-ttu-id="ca92d-439">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-439">False</span></span>                                                                                                 |
| <span data-ttu-id="ca92d-440">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-440">Minimum system</span></span> | <span data-ttu-id="ca92d-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="ca92d-442">從 Windows Server 2003，只有系統管理員具有 COM + 傾印檔案的讀取存取許可權。</span><span class="sxs-lookup"><span data-stu-id="ca92d-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="ca92d-443">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="ca92d-443">DumpOnException</span></span>



| <span data-ttu-id="ca92d-444">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-444">Entry</span></span> | <span data-ttu-id="ca92d-445">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-446">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-446">Description</span></span>    | <span data-ttu-id="ca92d-447">當應用程式造成未處理的例外狀況，並由 COM + 執行時間終止時，啟用 COM + 應用程式的狀態傾印。</span><span class="sxs-lookup"><span data-stu-id="ca92d-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="ca92d-448">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-448">Access</span></span>         | <span data-ttu-id="ca92d-449">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="ca92d-450">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-450">Type</span></span>           | <span data-ttu-id="ca92d-451">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="ca92d-452">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-452">Default</span></span>        | <span data-ttu-id="ca92d-453">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="ca92d-454">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-454">Minimum system</span></span> | <span data-ttu-id="ca92d-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="ca92d-456">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="ca92d-456">DumpOnFailfast</span></span>



| <span data-ttu-id="ca92d-457">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-457">Entry</span></span> | <span data-ttu-id="ca92d-458">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-459">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-459">Description</span></span>    | <span data-ttu-id="ca92d-460">當應用程式失敗時，啟用 COM + 應用程式的狀態傾印。</span><span class="sxs-lookup"><span data-stu-id="ca92d-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="ca92d-461">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-461">Access</span></span>         | <span data-ttu-id="ca92d-462">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="ca92d-463">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-463">Type</span></span>           | <span data-ttu-id="ca92d-464">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-464">Bool</span></span>                                                                            |
| <span data-ttu-id="ca92d-465">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-465">Default</span></span>        | <span data-ttu-id="ca92d-466">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-466">False</span></span>                                                                           |
| <span data-ttu-id="ca92d-467">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-467">Minimum system</span></span> | <span data-ttu-id="ca92d-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="ca92d-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="ca92d-469">DumpPath</span></span>



| <span data-ttu-id="ca92d-470">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-470">Entry</span></span> | <span data-ttu-id="ca92d-471">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="ca92d-472">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-472">Description</span></span>    | <span data-ttu-id="ca92d-473">儲存傾印檔案之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="ca92d-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="ca92d-474">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-474">Access</span></span>         | <span data-ttu-id="ca92d-475">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="ca92d-476">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-476">Type</span></span>           | <span data-ttu-id="ca92d-477">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-477">String</span></span>                                                       |
| <span data-ttu-id="ca92d-478">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-478">Default</span></span>        | <span data-ttu-id="ca92d-479">"% systemroot% \\ system32 \\ com \\ dmp"</span><span class="sxs-lookup"><span data-stu-id="ca92d-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="ca92d-480">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-480">Minimum system</span></span> | <span data-ttu-id="ca92d-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="ca92d-482">從 Windows Server 2003，只有系統管理員具有 COM + 傾印檔案的讀取存取許可權。</span><span class="sxs-lookup"><span data-stu-id="ca92d-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="ca92d-483">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-483">EventsEnabled</span></span>



| <span data-ttu-id="ca92d-484">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-484">Entry</span></span> | <span data-ttu-id="ca92d-485">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="ca92d-486">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-486">Description</span></span>    | <span data-ttu-id="ca92d-487">指出是否已針對應用程式啟用事件。</span><span class="sxs-lookup"><span data-stu-id="ca92d-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="ca92d-488">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-488">Access</span></span>         | <span data-ttu-id="ca92d-489">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="ca92d-490">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-490">Type</span></span>           | <span data-ttu-id="ca92d-491">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-491">Bool</span></span>                                                      |
| <span data-ttu-id="ca92d-492">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-492">Default</span></span>        | <span data-ttu-id="ca92d-493">對</span><span class="sxs-lookup"><span data-stu-id="ca92d-493">True</span></span>                                                      |
| <span data-ttu-id="ca92d-494">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-494">Minimum system</span></span> | <span data-ttu-id="ca92d-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="ca92d-496">識別碼</span><span class="sxs-lookup"><span data-stu-id="ca92d-496">ID</span></span>



| <span data-ttu-id="ca92d-497">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-497">Entry</span></span> | <span data-ttu-id="ca92d-498">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-499">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-499">Description</span></span>    | <span data-ttu-id="ca92d-500">表示應用程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ca92d-500">A GUID representing the application.</span></span> <span data-ttu-id="ca92d-501">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ca92d-502">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-502">Access</span></span>         | <span data-ttu-id="ca92d-503">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="ca92d-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="ca92d-504">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-504">Type</span></span>           | <span data-ttu-id="ca92d-505">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="ca92d-506">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="ca92d-507">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-507">Minimum system</span></span> | <span data-ttu-id="ca92d-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="ca92d-509">身分識別</span><span class="sxs-lookup"><span data-stu-id="ca92d-509">Identity</span></span>



| <span data-ttu-id="ca92d-510">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-510">Entry</span></span> | <span data-ttu-id="ca92d-511">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-512">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-512">Description</span></span>    | <span data-ttu-id="ca92d-513">設定應用程式的伺服器進程身分識別。</span><span class="sxs-lookup"><span data-stu-id="ca92d-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="ca92d-514">請指定有效的使用者帳戶或「互動式使用者」，讓應用程式採用目前登入使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ca92d-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="ca92d-515">您也可以指定 "nt 授權 \\ localservice"、"nt 授權單位 \\ networkservice" 和 "nt 授權單位 \\ 系統" 字串。</span><span class="sxs-lookup"><span data-stu-id="ca92d-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="ca92d-516">這三個帳戶的預設密碼為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="ca92d-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="ca92d-517">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-518">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-519">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-520">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-520">Minimum system</span></span> | <span data-ttu-id="ca92d-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="ca92d-522">未針對在用戶端進程中執行的程式庫應用程式啟用識別屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="ca92d-523">在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼屬性應該與身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ca92d-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="ca92d-524">如果密碼和身分識別不同步，則在系統管理員重設應用程式之前，無法啟動該應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="ca92d-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="ca92d-525">ImpersonationLevel</span></span>



| <span data-ttu-id="ca92d-526">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-526">Entry</span></span> | <span data-ttu-id="ca92d-527">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-528">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-528">Description</span></span>    | <span data-ttu-id="ca92d-529">設定用於對其他應用程式進行呼叫的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="ca92d-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="ca92d-530">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-530">Access</span></span>         | <span data-ttu-id="ca92d-531">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="ca92d-532">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-532">Type</span></span>           | <span data-ttu-id="ca92d-533">長可能的值： COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) </span><span class="sxs-lookup"><span data-stu-id="ca92d-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="ca92d-534">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-534">Default</span></span>        | <span data-ttu-id="ca92d-535">COMAdminImpersonationImpersonate (3) </span><span class="sxs-lookup"><span data-stu-id="ca92d-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="ca92d-536">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-536">Minimum system</span></span> | <span data-ttu-id="ca92d-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="ca92d-538">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-538">IsEnabled</span></span>



| <span data-ttu-id="ca92d-539">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-539">Entry</span></span> | <span data-ttu-id="ca92d-540">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-541">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-541">Description</span></span>    | <span data-ttu-id="ca92d-542">如果 COM + 應用程式或元件已停用，則 IsEnabled 為 False。</span><span class="sxs-lookup"><span data-stu-id="ca92d-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="ca92d-543">如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。</span><span class="sxs-lookup"><span data-stu-id="ca92d-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="ca92d-544">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-544">Access</span></span>         | <span data-ttu-id="ca92d-545">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="ca92d-546">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-546">Type</span></span>           | <span data-ttu-id="ca92d-547">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="ca92d-548">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-548">Default</span></span>        | <span data-ttu-id="ca92d-549">對</span><span class="sxs-lookup"><span data-stu-id="ca92d-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="ca92d-550">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-550">Minimum system</span></span> | <span data-ttu-id="ca92d-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="ca92d-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="ca92d-552">IsSystem</span></span>



| <span data-ttu-id="ca92d-553">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-553">Entry</span></span> | <span data-ttu-id="ca92d-554">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="ca92d-555">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-555">Description</span></span>    | <span data-ttu-id="ca92d-556">識別 COM + 系統應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="ca92d-557">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-557">Access</span></span>         | <span data-ttu-id="ca92d-558">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca92d-558">ReadOnly</span></span>                             |
| <span data-ttu-id="ca92d-559">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-559">Type</span></span>           | <span data-ttu-id="ca92d-560">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-560">Bool</span></span>                                 |
| <span data-ttu-id="ca92d-561">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-561">Default</span></span>        | <span data-ttu-id="ca92d-562">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-562">False</span></span>                                |
| <span data-ttu-id="ca92d-563">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-563">Minimum system</span></span> | <span data-ttu-id="ca92d-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="ca92d-565">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="ca92d-565">MaxDumpCount</span></span>



| <span data-ttu-id="ca92d-566">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-566">Entry</span></span> | <span data-ttu-id="ca92d-567">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-568">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-568">Description</span></span>    | <span data-ttu-id="ca92d-569">表示覆寫之前要產生的檔案數目上限。</span><span class="sxs-lookup"><span data-stu-id="ca92d-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="ca92d-570">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-570">Access</span></span>         | <span data-ttu-id="ca92d-571">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="ca92d-572">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-572">Type</span></span>           | <span data-ttu-id="ca92d-573">Long (1-200) </span><span class="sxs-lookup"><span data-stu-id="ca92d-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="ca92d-574">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-574">Default</span></span>        | <span data-ttu-id="ca92d-575">5</span><span class="sxs-lookup"><span data-stu-id="ca92d-575">5</span></span>                                                                                |
| <span data-ttu-id="ca92d-576">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-576">Minimum system</span></span> | <span data-ttu-id="ca92d-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="ca92d-578">Name</span><span class="sxs-lookup"><span data-stu-id="ca92d-578">Name</span></span>



| <span data-ttu-id="ca92d-579">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-579">Entry</span></span> | <span data-ttu-id="ca92d-580">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-581">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-581">Description</span></span>    | <span data-ttu-id="ca92d-582">應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca92d-582">The name of the application.</span></span> <span data-ttu-id="ca92d-583">移除字串開頭和結尾的額外空間。在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ca92d-584">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-584">Access</span></span>         | <span data-ttu-id="ca92d-585">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="ca92d-586">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-586">Type</span></span>           | <span data-ttu-id="ca92d-587">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="ca92d-588">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-588">Default</span></span>        | <span data-ttu-id="ca92d-589">「新增應用程式」</span><span class="sxs-lookup"><span data-stu-id="ca92d-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-590">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-590">Minimum system</span></span> | <span data-ttu-id="ca92d-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="ca92d-592">應為應用程式選擇唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca92d-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="ca92d-593">如果使用相同的名稱建立多個應用程式，它可能會干擾依名稱參考應用程式，因而導致無法預期的行為。</span><span class="sxs-lookup"><span data-stu-id="ca92d-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="ca92d-594">密碼</span><span class="sxs-lookup"><span data-stu-id="ca92d-594">Password</span></span>



| <span data-ttu-id="ca92d-595">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-595">Entry</span></span> | <span data-ttu-id="ca92d-596">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-597">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-597">Description</span></span>    | <span data-ttu-id="ca92d-598">設定伺服器進程在身分識別下登入所使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="ca92d-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="ca92d-599">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-599">Access</span></span>         | <span data-ttu-id="ca92d-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="ca92d-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="ca92d-601">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-601">Type</span></span>           | <span data-ttu-id="ca92d-602">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-602">String</span></span>                                                                     |
| <span data-ttu-id="ca92d-603">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-603">Default</span></span>        | <span data-ttu-id="ca92d-604">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-604">""</span></span>                                                                         |
| <span data-ttu-id="ca92d-605">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-605">Minimum system</span></span> | <span data-ttu-id="ca92d-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="ca92d-607">在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ca92d-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="ca92d-608">如果密碼和身分識別不同步，則在系統管理員重設應用程式之前，無法啟動該應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="ca92d-609">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="ca92d-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="ca92d-610">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-610">Entry</span></span> | <span data-ttu-id="ca92d-611">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-612">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-612">Description</span></span>    | <span data-ttu-id="ca92d-613">指出在哪些情況下，會對應用程式的佇列要求進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ca92d-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="ca92d-614">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-614">Access</span></span>         | <span data-ttu-id="ca92d-615">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="ca92d-616">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-616">Type</span></span>           | <span data-ttu-id="ca92d-617">很長可能的值： COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2) </span><span class="sxs-lookup"><span data-stu-id="ca92d-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="ca92d-618">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-618">Default</span></span>        | <span data-ttu-id="ca92d-619">COMAdminQCMessageAuthenticateSecureApps (0) </span><span class="sxs-lookup"><span data-stu-id="ca92d-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="ca92d-620">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-620">Minimum system</span></span> | <span data-ttu-id="ca92d-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="ca92d-622">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="ca92d-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="ca92d-623">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-623">Entry</span></span> | <span data-ttu-id="ca92d-624">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-625">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-625">Description</span></span>    | <span data-ttu-id="ca92d-626">指出並行接聽程式執行緒的最大數目。</span><span class="sxs-lookup"><span data-stu-id="ca92d-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="ca92d-627">這個屬性的有效範圍是0到1000。</span><span class="sxs-lookup"><span data-stu-id="ca92d-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="ca92d-628">針對新建立的應用程式，此設定衍生自目前用來判斷接聽程式執行緒預設數目的演算法：伺服器中 Cpu 數目的16倍。</span><span class="sxs-lookup"><span data-stu-id="ca92d-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="ca92d-629">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-629">Access</span></span>         | <span data-ttu-id="ca92d-630">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ca92d-631">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-631">Type</span></span>           | <span data-ttu-id="ca92d-632">Long (0-1000) </span><span class="sxs-lookup"><span data-stu-id="ca92d-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ca92d-633">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-633">Default</span></span>        | <span data-ttu-id="ca92d-634">0</span><span class="sxs-lookup"><span data-stu-id="ca92d-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ca92d-635">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-635">Minimum system</span></span> | <span data-ttu-id="ca92d-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="ca92d-637">您也可以從 [元件服務] 系統管理工具的 [ **佇列** ] 索引標籤，使用 [讀取/寫入] 功能來取得這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="ca92d-638">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="ca92d-639">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-639">Entry</span></span> | <span data-ttu-id="ca92d-640">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-641">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-641">Description</span></span>    | <span data-ttu-id="ca92d-642">指出是否已針對應用程式啟用佇列元件接聽程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="ca92d-643">若已啟用，則會在應用程式啟動時啟動接聽程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="ca92d-644">只有當 QueuingEnabled 設定為 True 時，這個屬性才會生效。</span><span class="sxs-lookup"><span data-stu-id="ca92d-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="ca92d-645">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-645">Access</span></span>         | <span data-ttu-id="ca92d-646">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="ca92d-647">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-647">Type</span></span>           | <span data-ttu-id="ca92d-648">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="ca92d-649">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-649">Default</span></span>        | <span data-ttu-id="ca92d-650">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="ca92d-651">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-651">Minimum system</span></span> | <span data-ttu-id="ca92d-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="ca92d-653">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-653">QueuingEnabled</span></span>



| <span data-ttu-id="ca92d-654">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-654">Entry</span></span> | <span data-ttu-id="ca92d-655">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-656">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-656">Description</span></span>    | <span data-ttu-id="ca92d-657">指出是否為應用程式啟用 COM + 佇列元件服務。</span><span class="sxs-lookup"><span data-stu-id="ca92d-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="ca92d-658">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-658">Access</span></span>         | <span data-ttu-id="ca92d-659">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="ca92d-660">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-660">Type</span></span>           | <span data-ttu-id="ca92d-661">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="ca92d-662">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-662">Default</span></span>        | <span data-ttu-id="ca92d-663">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-663">False</span></span>                                                                                |
| <span data-ttu-id="ca92d-664">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-664">Minimum system</span></span> | <span data-ttu-id="ca92d-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="ca92d-666">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="ca92d-667">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-667">Entry</span></span> | <span data-ttu-id="ca92d-668">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-669">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-669">Description</span></span>    | <span data-ttu-id="ca92d-670">指出回收進程之前，應用程式中所要接受的已設定物件的最大啟用數目。</span><span class="sxs-lookup"><span data-stu-id="ca92d-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="ca92d-671">預設啟用數目為0。</span><span class="sxs-lookup"><span data-stu-id="ca92d-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="ca92d-672">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-672">Access</span></span>         | <span data-ttu-id="ca92d-673">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="ca92d-674">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-674">Type</span></span>           | <span data-ttu-id="ca92d-675">Long (0-1048576) </span><span class="sxs-lookup"><span data-stu-id="ca92d-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="ca92d-676">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-676">Default</span></span>        | <span data-ttu-id="ca92d-677">0</span><span class="sxs-lookup"><span data-stu-id="ca92d-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="ca92d-678">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-678">Minimum system</span></span> | <span data-ttu-id="ca92d-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="ca92d-680">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-680">RecycleCallLimit</span></span>



| <span data-ttu-id="ca92d-681">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-681">Entry</span></span> | <span data-ttu-id="ca92d-682">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-683">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-683">Description</span></span>    | <span data-ttu-id="ca92d-684">表示在回收進程之前，允許應用程式中已設定物件接受的呼叫數目上限。</span><span class="sxs-lookup"><span data-stu-id="ca92d-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="ca92d-685">預設的呼叫數目為0。</span><span class="sxs-lookup"><span data-stu-id="ca92d-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="ca92d-686">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-686">Access</span></span>         | <span data-ttu-id="ca92d-687">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="ca92d-688">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-688">Type</span></span>           | <span data-ttu-id="ca92d-689">Long (0-1048576) </span><span class="sxs-lookup"><span data-stu-id="ca92d-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="ca92d-690">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-690">Default</span></span>        | <span data-ttu-id="ca92d-691">0</span><span class="sxs-lookup"><span data-stu-id="ca92d-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="ca92d-692">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-692">Minimum system</span></span> | <span data-ttu-id="ca92d-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="ca92d-694">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="ca92d-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="ca92d-695">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-695">Entry</span></span> | <span data-ttu-id="ca92d-696">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-697">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-697">Description</span></span>    | <span data-ttu-id="ca92d-698">表示以分鐘為單位的時間 () ，讓回收的進程在關閉之前執行。</span><span class="sxs-lookup"><span data-stu-id="ca92d-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="ca92d-699">倒數計時會在進程回收之後立即開始。</span><span class="sxs-lookup"><span data-stu-id="ca92d-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="ca92d-700">到期時間上限為1440分鐘 (24 小時) ，預設值為15分鐘。</span><span class="sxs-lookup"><span data-stu-id="ca92d-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="ca92d-701">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-701">Access</span></span>         | <span data-ttu-id="ca92d-702">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ca92d-703">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-703">Type</span></span>           | <span data-ttu-id="ca92d-704">Long (1-1440) </span><span class="sxs-lookup"><span data-stu-id="ca92d-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-705">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-705">Default</span></span>        | <span data-ttu-id="ca92d-706">15</span><span class="sxs-lookup"><span data-stu-id="ca92d-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ca92d-707">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-707">Minimum system</span></span> | <span data-ttu-id="ca92d-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="ca92d-709">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="ca92d-710">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-710">Entry</span></span> | <span data-ttu-id="ca92d-711">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-712">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-712">Description</span></span>    | <span data-ttu-id="ca92d-713">表示在回收之前允許進程執行的最大分鐘數。</span><span class="sxs-lookup"><span data-stu-id="ca92d-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="ca92d-714">存留期上限為30240分鐘 (21 天) ，預設值為0分鐘。</span><span class="sxs-lookup"><span data-stu-id="ca92d-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="ca92d-715">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-715">Access</span></span>         | <span data-ttu-id="ca92d-716">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="ca92d-717">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-717">Type</span></span>           | <span data-ttu-id="ca92d-718">Long (0-30240) </span><span class="sxs-lookup"><span data-stu-id="ca92d-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="ca92d-719">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-719">Default</span></span>        | <span data-ttu-id="ca92d-720">0</span><span class="sxs-lookup"><span data-stu-id="ca92d-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="ca92d-721">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-721">Minimum system</span></span> | <span data-ttu-id="ca92d-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="ca92d-723">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="ca92d-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="ca92d-724">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-724">Entry</span></span> | <span data-ttu-id="ca92d-725">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-726">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-726">Description</span></span>    | <span data-ttu-id="ca92d-727">指出記憶體使用量的最大數量 (（以 kb 為單位），) 在回收之前允許進程。</span><span class="sxs-lookup"><span data-stu-id="ca92d-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="ca92d-728">如果進程記憶體使用量超過指定的時間長度超過一分鐘，則會回收進程。</span><span class="sxs-lookup"><span data-stu-id="ca92d-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="ca92d-729">記憶體使用量的預設數量為 0 KB。</span><span class="sxs-lookup"><span data-stu-id="ca92d-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="ca92d-730">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-730">Access</span></span>         | <span data-ttu-id="ca92d-731">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ca92d-732">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-732">Type</span></span>           | <span data-ttu-id="ca92d-733">Long (0-1048576) </span><span class="sxs-lookup"><span data-stu-id="ca92d-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ca92d-734">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-734">Default</span></span>        | <span data-ttu-id="ca92d-735">0</span><span class="sxs-lookup"><span data-stu-id="ca92d-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ca92d-736">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-736">Minimum system</span></span> | <span data-ttu-id="ca92d-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="ca92d-738">複製</span><span class="sxs-lookup"><span data-stu-id="ca92d-738">Replicable</span></span>



| <span data-ttu-id="ca92d-739">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-739">Entry</span></span> | <span data-ttu-id="ca92d-740">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="ca92d-741">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-741">Description</span></span>    | <span data-ttu-id="ca92d-742">指出是否可以複寫應用程式。</span><span class="sxs-lookup"><span data-stu-id="ca92d-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="ca92d-743">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-743">Access</span></span>         | <span data-ttu-id="ca92d-744">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="ca92d-745">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-745">Type</span></span>           | <span data-ttu-id="ca92d-746">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-746">Bool</span></span>                                                 |
| <span data-ttu-id="ca92d-747">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-747">Default</span></span>        | <span data-ttu-id="ca92d-748">對</span><span class="sxs-lookup"><span data-stu-id="ca92d-748">True</span></span>                                                 |
| <span data-ttu-id="ca92d-749">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-749">Minimum system</span></span> | <span data-ttu-id="ca92d-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="ca92d-751">RunForever</span><span class="sxs-lookup"><span data-stu-id="ca92d-751">RunForever</span></span>



| <span data-ttu-id="ca92d-752">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-752">Entry</span></span> | <span data-ttu-id="ca92d-753">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-754">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-754">Description</span></span>    | <span data-ttu-id="ca92d-755">如果應用程式閒置，可讓伺服器進程繼續執行。</span><span class="sxs-lookup"><span data-stu-id="ca92d-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="ca92d-756">如果設定為 True，則當閒置時，不會關閉伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="ca92d-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="ca92d-757">如果設定為 False，則會根據 ShutdownAfter 屬性所設定的值來關閉進程。</span><span class="sxs-lookup"><span data-stu-id="ca92d-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="ca92d-758">RunForever 未啟用程式庫 () 應用程式的程式庫。</span><span class="sxs-lookup"><span data-stu-id="ca92d-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="ca92d-759">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-759">Access</span></span>         | <span data-ttu-id="ca92d-760">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ca92d-761">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-761">Type</span></span>           | <span data-ttu-id="ca92d-762">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ca92d-763">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-763">Default</span></span>        | <span data-ttu-id="ca92d-764">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-765">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-765">Minimum system</span></span> | <span data-ttu-id="ca92d-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="ca92d-767">ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca92d-767">ServiceName</span></span>



| <span data-ttu-id="ca92d-768">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-768">Entry</span></span> | <span data-ttu-id="ca92d-769">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-770">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-770">Description</span></span>    | <span data-ttu-id="ca92d-771">對應至設定要執行為服務應用程式之應用程式的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ca92d-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="ca92d-772">如果這個值為 **Null**，則不會將應用程式設定為以服務方式執行。</span><span class="sxs-lookup"><span data-stu-id="ca92d-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="ca92d-773">否則，您可以使用服務名稱來尋找服務的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="ca92d-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="ca92d-774">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-774">Access</span></span>         | <span data-ttu-id="ca92d-775">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca92d-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ca92d-776">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-776">Type</span></span>           | <span data-ttu-id="ca92d-777">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ca92d-778">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-778">Default</span></span>        | <span data-ttu-id="ca92d-779">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ca92d-780">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-780">Minimum system</span></span> | <span data-ttu-id="ca92d-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="ca92d-782">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="ca92d-782">ShutdownAfter</span></span>



| <span data-ttu-id="ca92d-783">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-783">Entry</span></span> | <span data-ttu-id="ca92d-784">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-785">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-785">Description</span></span>    | <span data-ttu-id="ca92d-786">設定在伺服器進程變成閒置之後，關閉該進程之前的延遲。</span><span class="sxs-lookup"><span data-stu-id="ca92d-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="ca92d-787">關機延遲的範圍是從0到1440分鐘 (24 小時) 。</span><span class="sxs-lookup"><span data-stu-id="ca92d-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="ca92d-788">如果 RunForever 設定為 True，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="ca92d-789">ShutdownAfter 未啟用程式庫 () 應用程式的程式庫。</span><span class="sxs-lookup"><span data-stu-id="ca92d-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="ca92d-790">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-790">Access</span></span>         | <span data-ttu-id="ca92d-791">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ca92d-792">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-792">Type</span></span>           | <span data-ttu-id="ca92d-793">Long (0-1440) </span><span class="sxs-lookup"><span data-stu-id="ca92d-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ca92d-794">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-794">Default</span></span>        | <span data-ttu-id="ca92d-795">3</span><span class="sxs-lookup"><span data-stu-id="ca92d-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ca92d-796">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-796">Minimum system</span></span> | <span data-ttu-id="ca92d-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca92d-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="ca92d-798">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="ca92d-798">SoapActivated</span></span>



| <span data-ttu-id="ca92d-799">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-799">Entry</span></span> | <span data-ttu-id="ca92d-800">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-801">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-801">Description</span></span>    | <span data-ttu-id="ca92d-802">指出此應用程式是否會透過 SOAP 通訊協定公開以供取用。</span><span class="sxs-lookup"><span data-stu-id="ca92d-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="ca92d-803">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-803">Access</span></span>         | <span data-ttu-id="ca92d-804">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="ca92d-805">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-805">Type</span></span>           | <span data-ttu-id="ca92d-806">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="ca92d-807">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-807">Default</span></span>        | <span data-ttu-id="ca92d-808">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-808">False</span></span>                                                                                |
| <span data-ttu-id="ca92d-809">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-809">Minimum system</span></span> | <span data-ttu-id="ca92d-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca92d-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="ca92d-811">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="ca92d-811">SoapBaseUrl</span></span>



| <span data-ttu-id="ca92d-812">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-812">Entry</span></span> | <span data-ttu-id="ca92d-813">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-814">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-814">Description</span></span>    | <span data-ttu-id="ca92d-815">此應用程式透過 SOAP 通訊協定公開的 URL 端點。</span><span class="sxs-lookup"><span data-stu-id="ca92d-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="ca92d-816">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-816">Access</span></span>         | <span data-ttu-id="ca92d-817">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="ca92d-818">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-818">Type</span></span>           | <span data-ttu-id="ca92d-819">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-819">String</span></span>                                                                       |
| <span data-ttu-id="ca92d-820">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-820">Default</span></span>        | <span data-ttu-id="ca92d-821">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-821">""</span></span>                                                                           |
| <span data-ttu-id="ca92d-822">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-822">Minimum system</span></span> | <span data-ttu-id="ca92d-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca92d-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="ca92d-824">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="ca92d-824">SoapMailTo</span></span>



| <span data-ttu-id="ca92d-825">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-825">Entry</span></span> | <span data-ttu-id="ca92d-826">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-827">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-827">Description</span></span>    | <span data-ttu-id="ca92d-828">此應用程式透過 SOAP 通訊協定公開的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="ca92d-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="ca92d-829">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-829">Access</span></span>         | <span data-ttu-id="ca92d-830">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="ca92d-831">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-831">Type</span></span>           | <span data-ttu-id="ca92d-832">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-832">String</span></span>                                                                        |
| <span data-ttu-id="ca92d-833">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-833">Default</span></span>        | <span data-ttu-id="ca92d-834">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-834">""</span></span>                                                                            |
| <span data-ttu-id="ca92d-835">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-835">Minimum system</span></span> | <span data-ttu-id="ca92d-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca92d-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="ca92d-837">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="ca92d-837">SoapVRoot</span></span>



| <span data-ttu-id="ca92d-838">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-838">Entry</span></span> | <span data-ttu-id="ca92d-839">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-840">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-840">Description</span></span>    | <span data-ttu-id="ca92d-841">IIS 虛擬根目錄，在此根目錄中會透過 SOAP 通訊協定來公開應用程式的存取腳本。</span><span class="sxs-lookup"><span data-stu-id="ca92d-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="ca92d-842">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-842">Access</span></span>         | <span data-ttu-id="ca92d-843">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="ca92d-844">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-844">Type</span></span>           | <span data-ttu-id="ca92d-845">String</span><span class="sxs-lookup"><span data-stu-id="ca92d-845">String</span></span>                                                                                                               |
| <span data-ttu-id="ca92d-846">預設值</span><span class="sxs-lookup"><span data-stu-id="ca92d-846">Default</span></span>        | <span data-ttu-id="ca92d-847">""</span><span class="sxs-lookup"><span data-stu-id="ca92d-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="ca92d-848">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-848">Minimum system</span></span> | <span data-ttu-id="ca92d-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca92d-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="ca92d-850">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="ca92d-850">SRPEnabled</span></span>



| <span data-ttu-id="ca92d-851">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-851">Entry</span></span> | <span data-ttu-id="ca92d-852">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-853">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-853">Description</span></span>    | <span data-ttu-id="ca92d-854">判斷應用程式 (SRP) 的軟體限制原則。</span><span class="sxs-lookup"><span data-stu-id="ca92d-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="ca92d-855">如果設定為 True，則會使用應用程式的 SRPTrustLevel 屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="ca92d-856">如果設定為 False，則會使用本機安全性設定中的軟體限制原則。</span><span class="sxs-lookup"><span data-stu-id="ca92d-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="ca92d-857">本機安全性設定是透過 Microsoft Management Console 的 [本機安全性原則] 嵌入式管理單元來控制。</span><span class="sxs-lookup"><span data-stu-id="ca92d-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="ca92d-858">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-858">Access</span></span>         | <span data-ttu-id="ca92d-859">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ca92d-860">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-860">Type</span></span>           | <span data-ttu-id="ca92d-861">Bool</span><span class="sxs-lookup"><span data-stu-id="ca92d-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ca92d-862">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-862">Default</span></span>        | <span data-ttu-id="ca92d-863">否</span><span class="sxs-lookup"><span data-stu-id="ca92d-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ca92d-864">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-864">Minimum system</span></span> | <span data-ttu-id="ca92d-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="ca92d-866">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="ca92d-866">SRPTrustLevel</span></span>



| <span data-ttu-id="ca92d-867">進入</span><span class="sxs-lookup"><span data-stu-id="ca92d-867">Entry</span></span> | <span data-ttu-id="ca92d-868">值</span><span class="sxs-lookup"><span data-stu-id="ca92d-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca92d-869">描述</span><span class="sxs-lookup"><span data-stu-id="ca92d-869">Description</span></span>    | <span data-ttu-id="ca92d-870">指出軟體限制原則 (SRP) 應用程式信任層級。</span><span class="sxs-lookup"><span data-stu-id="ca92d-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="ca92d-871">只有當 SRPEnabled 屬性設定為 True 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="ca92d-872">SRP 信任層級是指您願意授與應用程式的信任層級。</span><span class="sxs-lookup"><span data-stu-id="ca92d-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="ca92d-873">不受限制的 SRP 信任層級會對應到更安全的 \_ LEVELID \_ FULLYTRUSTED 列舉值，而不允許的 srp 信任層級則對應到安全性不 \_ 允許的 LEVELID \_ 列舉值。</span><span class="sxs-lookup"><span data-stu-id="ca92d-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="ca92d-874">信任層級的列舉定義于 Winsafer 中。</span><span class="sxs-lookup"><span data-stu-id="ca92d-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="ca92d-875">Access</span><span class="sxs-lookup"><span data-stu-id="ca92d-875">Access</span></span>         | <span data-ttu-id="ca92d-876">讀寫</span><span class="sxs-lookup"><span data-stu-id="ca92d-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ca92d-877">類型</span><span class="sxs-lookup"><span data-stu-id="ca92d-877">Type</span></span>           | <span data-ttu-id="ca92d-878">較長的可能值：更安全的 \_ LEVELID 不 \_ 允許 (0X0) 更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000) </span><span class="sxs-lookup"><span data-stu-id="ca92d-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ca92d-879">預設</span><span class="sxs-lookup"><span data-stu-id="ca92d-879">Default</span></span>        | <span data-ttu-id="ca92d-880">更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000) </span><span class="sxs-lookup"><span data-stu-id="ca92d-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ca92d-881">最小系統</span><span class="sxs-lookup"><span data-stu-id="ca92d-881">Minimum system</span></span> | <span data-ttu-id="ca92d-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca92d-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="ca92d-883">您願意信任但不受限制存取的應用程式應該附加最嚴格的安全性。</span><span class="sxs-lookup"><span data-stu-id="ca92d-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="ca92d-884">不受限制的應用程式只能載入未受限制的元件，而不允許的應用程式無法執行，因此無法載入任何元件。</span><span class="sxs-lookup"><span data-stu-id="ca92d-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca92d-885">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca92d-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca92d-886">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="ca92d-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
