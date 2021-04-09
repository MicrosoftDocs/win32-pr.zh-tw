---
description: 包含單一物件，該物件對應至您要存取其目錄的電腦。 此物件會保存電腦層級的設定資訊。
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: LocalComputer 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689176"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="b4f87-104">LocalComputer 集合</span><span class="sxs-lookup"><span data-stu-id="b4f87-104">LocalComputer collection</span></span>

<span data-ttu-id="b4f87-105">包含單一物件，該物件對應至您要存取其目錄的電腦。</span><span class="sxs-lookup"><span data-stu-id="b4f87-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="b4f87-106">此物件會保存電腦層級的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b4f87-106">This object holds computer level settings information.</span></span> <span data-ttu-id="b4f87-107">如果您在從 [**COMAdminCatalog**](comadmincatalog.md)類別建立的物件上呼叫 [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect)方法， **LocalComputer** 集合中的物件將會包含您要存取其目錄之遠端電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b4f87-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="b4f87-108">此集合不支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)和 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法。</span><span class="sxs-lookup"><span data-stu-id="b4f87-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b4f87-109">成員</span><span class="sxs-lookup"><span data-stu-id="b4f87-109">Members</span></span>

<span data-ttu-id="b4f87-110">**LocalComputer** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="b4f87-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b4f87-111">相關集合</span><span class="sxs-lookup"><span data-stu-id="b4f87-111">Related Collections</span></span>

<span data-ttu-id="b4f87-112">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="b4f87-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b4f87-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b4f87-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b4f87-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b4f87-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b4f87-115">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b4f87-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b4f87-116">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="b4f87-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b4f87-117">**根**</span><span class="sxs-lookup"><span data-stu-id="b4f87-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b4f87-118">屬性</span><span class="sxs-lookup"><span data-stu-id="b4f87-118">Properties</span></span>

<span data-ttu-id="b4f87-119">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b4f87-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b4f87-120">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="b4f87-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="b4f87-121">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="b4f87-122">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="b4f87-123">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="b4f87-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="b4f87-124">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="b4f87-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="b4f87-125">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="b4f87-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="b4f87-126">說明</span><span class="sxs-lookup"><span data-stu-id="b4f87-126">Description</span></span>](#description)
-   [<span data-ttu-id="b4f87-127">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="b4f87-128">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="b4f87-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="b4f87-129">IsRouter</span><span class="sxs-lookup"><span data-stu-id="b4f87-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="b4f87-130">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="b4f87-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="b4f87-131">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="b4f87-132">名稱</span><span class="sxs-lookup"><span data-stu-id="b4f87-132">Name</span></span>](#name)
-   [<span data-ttu-id="b4f87-133">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b4f87-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="b4f87-134">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="b4f87-135">連接埠</span><span class="sxs-lookup"><span data-stu-id="b4f87-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="b4f87-136">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="b4f87-137">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="b4f87-138">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="b4f87-139">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="b4f87-140">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="b4f87-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="b4f87-141">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="b4f87-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="b4f87-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="b4f87-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="b4f87-143">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="b4f87-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="b4f87-144">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-144">Entry</span></span> | <span data-ttu-id="b4f87-145">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="b4f87-146">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-146">Description</span></span>    | <span data-ttu-id="b4f87-147">依預設，應用程式 proxy 所使用的遠端伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b4f87-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="b4f87-148">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-148">Access</span></span>         | <span data-ttu-id="b4f87-149">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="b4f87-150">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-150">Type</span></span>           | <span data-ttu-id="b4f87-151">String</span><span class="sxs-lookup"><span data-stu-id="b4f87-151">String</span></span>                                                     |
| <span data-ttu-id="b4f87-152">預設值</span><span class="sxs-lookup"><span data-stu-id="b4f87-152">Default</span></span>        | <span data-ttu-id="b4f87-153">""</span><span class="sxs-lookup"><span data-stu-id="b4f87-153">""</span></span>                                                         |
| <span data-ttu-id="b4f87-154">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-154">Minimum system</span></span> | <span data-ttu-id="b4f87-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="b4f87-156">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-156">CISEnabled</span></span>



| <span data-ttu-id="b4f87-157">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-157">Entry</span></span> | <span data-ttu-id="b4f87-158">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="b4f87-159">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-159">Description</span></span>    | <span data-ttu-id="b4f87-160">指出是否啟用 COM 網際網路服務。</span><span class="sxs-lookup"><span data-stu-id="b4f87-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="b4f87-161">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-161">Access</span></span>         | <span data-ttu-id="b4f87-162">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="b4f87-163">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-163">Type</span></span>           | <span data-ttu-id="b4f87-164">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-164">Bool</span></span>                                                |
| <span data-ttu-id="b4f87-165">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-165">Default</span></span>        | <span data-ttu-id="b4f87-166">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-166">False</span></span>                                               |
| <span data-ttu-id="b4f87-167">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-167">Minimum system</span></span> | <span data-ttu-id="b4f87-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="b4f87-169">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-169">DCOMEnabled</span></span>



| <span data-ttu-id="b4f87-170">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-170">Entry</span></span> | <span data-ttu-id="b4f87-171">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="b4f87-172">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-172">Description</span></span>    | <span data-ttu-id="b4f87-173">設定為 True 可在電腦上啟用 DCOM。</span><span class="sxs-lookup"><span data-stu-id="b4f87-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="b4f87-174">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-174">Access</span></span>         | <span data-ttu-id="b4f87-175">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="b4f87-176">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-176">Type</span></span>           | <span data-ttu-id="b4f87-177">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-177">Bool</span></span>                                        |
| <span data-ttu-id="b4f87-178">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-178">Default</span></span>        | <span data-ttu-id="b4f87-179">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-179">True</span></span>                                        |
| <span data-ttu-id="b4f87-180">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-180">Minimum system</span></span> | <span data-ttu-id="b4f87-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="b4f87-182">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="b4f87-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="b4f87-183">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-183">Entry</span></span> | <span data-ttu-id="b4f87-184">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-185">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-185">Description</span></span>    | <span data-ttu-id="b4f87-186">將驗證設定為預設的應用程式所使用的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="b4f87-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="b4f87-187">值會對應至遠端程序呼叫， (RPC) 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="b4f87-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="b4f87-188">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-188">Access</span></span>         | <span data-ttu-id="b4f87-189">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="b4f87-190">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-190">Type</span></span>           | <span data-ttu-id="b4f87-191">長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) </span><span class="sxs-lookup"><span data-stu-id="b4f87-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="b4f87-192">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-192">Default</span></span>        | <span data-ttu-id="b4f87-193">COMAdminAuthenticationConnect (2) </span><span class="sxs-lookup"><span data-stu-id="b4f87-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="b4f87-194">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-194">Minimum system</span></span> | <span data-ttu-id="b4f87-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="b4f87-196">當 COM 呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，COMAdminAuthenticationDefault 會對應至 COMAdminAuthenticationConnect。</span><span class="sxs-lookup"><span data-stu-id="b4f87-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="b4f87-197">建議您在列舉中使用常數，而不要使用數值。</span><span class="sxs-lookup"><span data-stu-id="b4f87-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="b4f87-198">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="b4f87-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="b4f87-199">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-199">Entry</span></span> | <span data-ttu-id="b4f87-200">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-201">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-201">Description</span></span>    | <span data-ttu-id="b4f87-202">如果未設定，則為允許的模擬層級。</span><span class="sxs-lookup"><span data-stu-id="b4f87-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="b4f87-203">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-203">Access</span></span>         | <span data-ttu-id="b4f87-204">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="b4f87-205">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-205">Type</span></span>           | <span data-ttu-id="b4f87-206">長可能的值： COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) </span><span class="sxs-lookup"><span data-stu-id="b4f87-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="b4f87-207">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-207">Default</span></span>        | <span data-ttu-id="b4f87-208">COMAdminImpersonationIdentify (2) </span><span class="sxs-lookup"><span data-stu-id="b4f87-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="b4f87-209">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-209">Minimum system</span></span> | <span data-ttu-id="b4f87-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="b4f87-211">建議您在列舉中使用常數，而不是數值。</span><span class="sxs-lookup"><span data-stu-id="b4f87-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="b4f87-212">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="b4f87-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="b4f87-213">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-213">Entry</span></span> | <span data-ttu-id="b4f87-214">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-215">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-215">Description</span></span>    | <span data-ttu-id="b4f87-216">判斷提供的埠預設類型是否應該是 Internet (True) 或內部網路 (False) 。</span><span class="sxs-lookup"><span data-stu-id="b4f87-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="b4f87-217">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-217">Access</span></span>         | <span data-ttu-id="b4f87-218">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="b4f87-219">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-219">Type</span></span>           | <span data-ttu-id="b4f87-220">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="b4f87-221">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-221">Default</span></span>        | <span data-ttu-id="b4f87-222">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-222">False</span></span>                                                                                               |
| <span data-ttu-id="b4f87-223">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-223">Minimum system</span></span> | <span data-ttu-id="b4f87-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="b4f87-225">Description</span><span class="sxs-lookup"><span data-stu-id="b4f87-225">Description</span></span>



| <span data-ttu-id="b4f87-226">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-226">Entry</span></span> | <span data-ttu-id="b4f87-227">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="b4f87-228">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-228">Description</span></span>    | <span data-ttu-id="b4f87-229">電腦的描述。</span><span class="sxs-lookup"><span data-stu-id="b4f87-229">A description of the computer.</span></span> |
| <span data-ttu-id="b4f87-230">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-230">Access</span></span>         | <span data-ttu-id="b4f87-231">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-231">ReadWrite</span></span>                      |
| <span data-ttu-id="b4f87-232">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-232">Type</span></span>           | <span data-ttu-id="b4f87-233">String</span><span class="sxs-lookup"><span data-stu-id="b4f87-233">String</span></span>                         |
| <span data-ttu-id="b4f87-234">預設值</span><span class="sxs-lookup"><span data-stu-id="b4f87-234">Default</span></span>        | <span data-ttu-id="b4f87-235">""</span><span class="sxs-lookup"><span data-stu-id="b4f87-235">""</span></span>                             |
| <span data-ttu-id="b4f87-236">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-236">Minimum system</span></span> | <span data-ttu-id="b4f87-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="b4f87-238">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="b4f87-239">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-239">Entry</span></span> | <span data-ttu-id="b4f87-240">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-241">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-241">Description</span></span>    | <span data-ttu-id="b4f87-242">指出是否將分割區對應的使用者簽入網域存放區。</span><span class="sxs-lookup"><span data-stu-id="b4f87-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="b4f87-243">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-243">Access</span></span>         | <span data-ttu-id="b4f87-244">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="b4f87-245">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-245">Type</span></span>           | <span data-ttu-id="b4f87-246">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="b4f87-247">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-247">Default</span></span>        | <span data-ttu-id="b4f87-248">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-248">True</span></span>                                                                                   |
| <span data-ttu-id="b4f87-249">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-249">Minimum system</span></span> | <span data-ttu-id="b4f87-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4f87-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="b4f87-251">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="b4f87-251">InternetPortsListed</span></span>



| <span data-ttu-id="b4f87-252">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-252">Entry</span></span> | <span data-ttu-id="b4f87-253">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-254">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-254">Description</span></span>    | <span data-ttu-id="b4f87-255">判斷 [埠] 屬性中所列的埠是否要用於網際網路 (True) 或內部網路 (False) 。</span><span class="sxs-lookup"><span data-stu-id="b4f87-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="b4f87-256">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-256">Access</span></span>         | <span data-ttu-id="b4f87-257">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="b4f87-258">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-258">Type</span></span>           | <span data-ttu-id="b4f87-259">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="b4f87-260">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-260">Default</span></span>        | <span data-ttu-id="b4f87-261">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="b4f87-262">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-262">Minimum system</span></span> | <span data-ttu-id="b4f87-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="b4f87-264">IsRouter</span><span class="sxs-lookup"><span data-stu-id="b4f87-264">IsRouter</span></span>



| <span data-ttu-id="b4f87-265">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-265">Entry</span></span> | <span data-ttu-id="b4f87-266">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-267">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-267">Description</span></span>    | <span data-ttu-id="b4f87-268">如果電腦是 (CLB) 服務的元件負載平衡的路由器，請設定為 True。</span><span class="sxs-lookup"><span data-stu-id="b4f87-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="b4f87-269">只有當元件負載平衡服務目前已安裝在電腦上時，才能將這個屬性設定為 True。否則，COMADMIN E 的錯誤 \_ \_ 需要 \_ 不同的 \_ 平臺。</span><span class="sxs-lookup"><span data-stu-id="b4f87-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="b4f87-270">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-270">Access</span></span>         | <span data-ttu-id="b4f87-271">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b4f87-272">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-272">Type</span></span>           | <span data-ttu-id="b4f87-273">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b4f87-274">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-274">Default</span></span>        | <span data-ttu-id="b4f87-275">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b4f87-276">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-276">Minimum system</span></span> | <span data-ttu-id="b4f87-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="b4f87-278">如果此屬性設定為 True，則會設定 CLB 伺服器，並在啟動時啟動。</span><span class="sxs-lookup"><span data-stu-id="b4f87-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="b4f87-279">如果伺服器尚未存在，便會將伺服器加入至 ApplicationCluster 集合。</span><span class="sxs-lookup"><span data-stu-id="b4f87-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="b4f87-280">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="b4f87-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="b4f87-281">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-281">Entry</span></span> | <span data-ttu-id="b4f87-282">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="b4f87-283">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-283">Description</span></span>    | <span data-ttu-id="b4f87-284">要平衡的物件 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b4f87-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="b4f87-285">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-285">Access</span></span>         | <span data-ttu-id="b4f87-286">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-286">ReadWrite</span></span>                           |
| <span data-ttu-id="b4f87-287">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-287">Type</span></span>           | <span data-ttu-id="b4f87-288">String</span><span class="sxs-lookup"><span data-stu-id="b4f87-288">String</span></span>                              |
| <span data-ttu-id="b4f87-289">預設值</span><span class="sxs-lookup"><span data-stu-id="b4f87-289">Default</span></span>        | <span data-ttu-id="b4f87-290">NULL</span><span class="sxs-lookup"><span data-stu-id="b4f87-290">NULL</span></span>                                |
| <span data-ttu-id="b4f87-291">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-291">Minimum system</span></span> | <span data-ttu-id="b4f87-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4f87-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="b4f87-293">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="b4f87-294">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-294">Entry</span></span> | <span data-ttu-id="b4f87-295">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-296">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-296">Description</span></span>    | <span data-ttu-id="b4f87-297">指出是否將分割區對應的使用者簽入本機存放區。</span><span class="sxs-lookup"><span data-stu-id="b4f87-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="b4f87-298">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-298">Access</span></span>         | <span data-ttu-id="b4f87-299">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="b4f87-300">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-300">Type</span></span>           | <span data-ttu-id="b4f87-301">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="b4f87-302">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-302">Default</span></span>        | <span data-ttu-id="b4f87-303">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-303">True</span></span>                                                                                  |
| <span data-ttu-id="b4f87-304">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-304">Minimum system</span></span> | <span data-ttu-id="b4f87-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4f87-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="b4f87-306">Name</span><span class="sxs-lookup"><span data-stu-id="b4f87-306">Name</span></span>



| <span data-ttu-id="b4f87-307">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-307">Entry</span></span> | <span data-ttu-id="b4f87-308">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-309">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-309">Description</span></span>    | <span data-ttu-id="b4f87-310">電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4f87-310">The name of the computer.</span></span> <span data-ttu-id="b4f87-311">移除字串開頭和結尾的額外空間。當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 或 [**名稱**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b4f87-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b4f87-312">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-312">Access</span></span>         | <span data-ttu-id="b4f87-313">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="b4f87-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b4f87-314">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-314">Type</span></span>           | <span data-ttu-id="b4f87-315">String</span><span class="sxs-lookup"><span data-stu-id="b4f87-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b4f87-316">預設值</span><span class="sxs-lookup"><span data-stu-id="b4f87-316">Default</span></span>        | <span data-ttu-id="b4f87-317">"我的電腦"</span><span class="sxs-lookup"><span data-stu-id="b4f87-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b4f87-318">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-318">Minimum system</span></span> | <span data-ttu-id="b4f87-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="b4f87-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b4f87-320">OperatingSystem</span></span>



| <span data-ttu-id="b4f87-321">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-321">Entry</span></span> | <span data-ttu-id="b4f87-322">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-323">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-323">Description</span></span>    | <span data-ttu-id="b4f87-324">安裝在本機電腦上的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b4f87-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b4f87-325">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-325">Access</span></span>         | <span data-ttu-id="b4f87-326">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b4f87-327">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-327">Type</span></span>           | <span data-ttu-id="b4f87-328">可能的最大值： COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16) </span><span class="sxs-lookup"><span data-stu-id="b4f87-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="b4f87-329">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-329">Default</span></span>        | <span data-ttu-id="b4f87-330">COMAdminOSNotInitialized (0) </span><span class="sxs-lookup"><span data-stu-id="b4f87-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b4f87-331">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-331">Minimum system</span></span> | <span data-ttu-id="b4f87-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="b4f87-333">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-333">PartitionsEnabled</span></span>



| <span data-ttu-id="b4f87-334">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-334">Entry</span></span> | <span data-ttu-id="b4f87-335">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-336">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-336">Description</span></span>    | <span data-ttu-id="b4f87-337">指出是否可以在本機電腦上使用 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="b4f87-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="b4f87-338">如果這個屬性為 False，任何使用 COM + 分割的嘗試都會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b4f87-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="b4f87-339">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-339">Access</span></span>         | <span data-ttu-id="b4f87-340">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="b4f87-341">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-341">Type</span></span>           | <span data-ttu-id="b4f87-342">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="b4f87-343">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-343">Default</span></span>        | <span data-ttu-id="b4f87-344">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="b4f87-345">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-345">Minimum system</span></span> | <span data-ttu-id="b4f87-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4f87-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="b4f87-347">連接埠</span><span class="sxs-lookup"><span data-stu-id="b4f87-347">Ports</span></span>



| <span data-ttu-id="b4f87-348">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-348">Entry</span></span> | <span data-ttu-id="b4f87-349">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-350">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-350">Description</span></span>    | <span data-ttu-id="b4f87-351">字串，描述針對網際網路或內部網路使用的埠，視 InternetPortsListed 屬性而定;例如 "500-599: 600-800"。</span><span class="sxs-lookup"><span data-stu-id="b4f87-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="b4f87-352">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-352">Access</span></span>         | <span data-ttu-id="b4f87-353">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="b4f87-354">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-354">Type</span></span>           | <span data-ttu-id="b4f87-355">String</span><span class="sxs-lookup"><span data-stu-id="b4f87-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="b4f87-356">預設值</span><span class="sxs-lookup"><span data-stu-id="b4f87-356">Default</span></span>        | <span data-ttu-id="b4f87-357">""</span><span class="sxs-lookup"><span data-stu-id="b4f87-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="b4f87-358">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-358">Minimum system</span></span> | <span data-ttu-id="b4f87-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="b4f87-360">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="b4f87-361">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-361">Entry</span></span> | <span data-ttu-id="b4f87-362">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="b4f87-363">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-363">Description</span></span>    | <span data-ttu-id="b4f87-364">可使用資源機。</span><span class="sxs-lookup"><span data-stu-id="b4f87-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="b4f87-365">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-365">Access</span></span>         | <span data-ttu-id="b4f87-366">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-366">ReadWrite</span></span>                           |
| <span data-ttu-id="b4f87-367">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-367">Type</span></span>           | <span data-ttu-id="b4f87-368">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-368">Bool</span></span>                                |
| <span data-ttu-id="b4f87-369">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-369">Default</span></span>        | <span data-ttu-id="b4f87-370">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-370">True</span></span>                                |
| <span data-ttu-id="b4f87-371">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-371">Minimum system</span></span> | <span data-ttu-id="b4f87-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="b4f87-373">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="b4f87-374">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-374">Entry</span></span> | <span data-ttu-id="b4f87-375">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-376">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-376">Description</span></span>    | <span data-ttu-id="b4f87-377">控制是否啟用 RPC IIS proxy。</span><span class="sxs-lookup"><span data-stu-id="b4f87-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="b4f87-378">RPC IIS proxy 是與 IIS 搭配使用，以便從 IIS 轉寄對 RPC 機制的呼叫，並且是 COM 網際網路服務的其中一個核心，也就是藉由將 CISEnabled 設定為 True 來啟用。</span><span class="sxs-lookup"><span data-stu-id="b4f87-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="b4f87-379">如需 RPCProxyEnabled 的詳細資訊，請參閱 [HTTP RPC 安全性](/windows/desktop/Rpc/rpc-over-http-security)。</span><span class="sxs-lookup"><span data-stu-id="b4f87-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="b4f87-380">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-380">Access</span></span>         | <span data-ttu-id="b4f87-381">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b4f87-382">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-382">Type</span></span>           | <span data-ttu-id="b4f87-383">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b4f87-384">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-384">Default</span></span>        | <span data-ttu-id="b4f87-385">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b4f87-386">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-386">Minimum system</span></span> | <span data-ttu-id="b4f87-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="b4f87-388">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="b4f87-389">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-389">Entry</span></span> | <span data-ttu-id="b4f87-390">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-391">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-391">Description</span></span>    | <span data-ttu-id="b4f87-392">在 DCOM 電腦中強制 [**執行對 IUnknown：： AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Iunknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法的跨進程呼叫會受到保護。</span><span class="sxs-lookup"><span data-stu-id="b4f87-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="b4f87-393">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-393">Access</span></span>         | <span data-ttu-id="b4f87-394">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="b4f87-395">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-395">Type</span></span>           | <span data-ttu-id="b4f87-396">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="b4f87-397">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-397">Default</span></span>        | <span data-ttu-id="b4f87-398">否</span><span class="sxs-lookup"><span data-stu-id="b4f87-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="b4f87-399">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-399">Minimum system</span></span> | <span data-ttu-id="b4f87-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="b4f87-401">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="b4f87-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="b4f87-402">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-402">Entry</span></span> | <span data-ttu-id="b4f87-403">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="b4f87-404">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-404">Description</span></span>    | <span data-ttu-id="b4f87-405">如果在物件上啟用安全性追蹤，則設定為 True。</span><span class="sxs-lookup"><span data-stu-id="b4f87-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="b4f87-406">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-406">Access</span></span>         | <span data-ttu-id="b4f87-407">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="b4f87-408">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-408">Type</span></span>           | <span data-ttu-id="b4f87-409">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-409">Bool</span></span>                                                    |
| <span data-ttu-id="b4f87-410">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-410">Default</span></span>        | <span data-ttu-id="b4f87-411">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-411">True</span></span>                                                    |
| <span data-ttu-id="b4f87-412">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-412">Minimum system</span></span> | <span data-ttu-id="b4f87-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="b4f87-414">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="b4f87-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="b4f87-415">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-415">Entry</span></span> | <span data-ttu-id="b4f87-416">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-417">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-417">Description</span></span>    | <span data-ttu-id="b4f87-418">決定軟體限制原則 (SRP) 如何處理啟動為啟動的連接。</span><span class="sxs-lookup"><span data-stu-id="b4f87-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="b4f87-419">如果設定為 True，則會將為伺服器物件設定的 SRP 信任層級與用戶端物件的 SRP 信任層級進行比較，並使用較高 (更嚴格的) 信任層級來執行伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="b4f87-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="b4f87-420">如果設定為 False，則不論伺服器設定所在的 SRP 信任層級為何，伺服器物件都會以用戶端物件的 SRP 信任層級執行。</span><span class="sxs-lookup"><span data-stu-id="b4f87-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="b4f87-421">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-421">Access</span></span>         | <span data-ttu-id="b4f87-422">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b4f87-423">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-423">Type</span></span>           | <span data-ttu-id="b4f87-424">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b4f87-425">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-425">Default</span></span>        | <span data-ttu-id="b4f87-426">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b4f87-427">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-427">Minimum system</span></span> | <span data-ttu-id="b4f87-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4f87-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="b4f87-429">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="b4f87-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="b4f87-430">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-430">Entry</span></span> | <span data-ttu-id="b4f87-431">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-432">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-432">Description</span></span>    | <span data-ttu-id="b4f87-433">判斷軟體限制原則 (SRP) 如何處理與現有進程的已嘗試連接。</span><span class="sxs-lookup"><span data-stu-id="b4f87-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="b4f87-434">如果設定為 False，則不會檢查是否有適當的 SRP 信任層級來連接至執行中的物件。</span><span class="sxs-lookup"><span data-stu-id="b4f87-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="b4f87-435">如果設定為 True，則執行中的物件必須有相等或更高的 (比用戶端物件更嚴格的) SRP 信任層級。</span><span class="sxs-lookup"><span data-stu-id="b4f87-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="b4f87-436">例如，具有不受限制之 SRP 信任層級的用戶端物件，無法連接到具有不允許之 SRP 信任層級的執行中物件。</span><span class="sxs-lookup"><span data-stu-id="b4f87-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="b4f87-437">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-437">Access</span></span>         | <span data-ttu-id="b4f87-438">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b4f87-439">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-439">Type</span></span>           | <span data-ttu-id="b4f87-440">Bool</span><span class="sxs-lookup"><span data-stu-id="b4f87-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b4f87-441">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-441">Default</span></span>        | <span data-ttu-id="b4f87-442">對</span><span class="sxs-lookup"><span data-stu-id="b4f87-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b4f87-443">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-443">Minimum system</span></span> | <span data-ttu-id="b4f87-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4f87-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="b4f87-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="b4f87-445">TransactionTimeout</span></span>



| <span data-ttu-id="b4f87-446">進入</span><span class="sxs-lookup"><span data-stu-id="b4f87-446">Entry</span></span> | <span data-ttu-id="b4f87-447">值</span><span class="sxs-lookup"><span data-stu-id="b4f87-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f87-448">描述</span><span class="sxs-lookup"><span data-stu-id="b4f87-448">Description</span></span>    | <span data-ttu-id="b4f87-449">如果您要在交易內執行許多作業，則應該設定為足夠的值（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b4f87-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="b4f87-450">預設的超時期限為60秒，而最大超時期限為3600秒 (1 小時) 。</span><span class="sxs-lookup"><span data-stu-id="b4f87-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="b4f87-451">將這個屬性設定為0會停用交易超時。</span><span class="sxs-lookup"><span data-stu-id="b4f87-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="b4f87-452">您可以使用 [**元件**](components.md) 集合的 ComponentTransactionTimeout 屬性，以個別元件覆寫這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b4f87-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="b4f87-453">Access</span><span class="sxs-lookup"><span data-stu-id="b4f87-453">Access</span></span>         | <span data-ttu-id="b4f87-454">讀寫</span><span class="sxs-lookup"><span data-stu-id="b4f87-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b4f87-455">類型</span><span class="sxs-lookup"><span data-stu-id="b4f87-455">Type</span></span>           | <span data-ttu-id="b4f87-456">Long (0-3600) </span><span class="sxs-lookup"><span data-stu-id="b4f87-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b4f87-457">預設</span><span class="sxs-lookup"><span data-stu-id="b4f87-457">Default</span></span>        | <span data-ttu-id="b4f87-458">60</span><span class="sxs-lookup"><span data-stu-id="b4f87-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b4f87-459">最小系統</span><span class="sxs-lookup"><span data-stu-id="b4f87-459">Minimum system</span></span> | <span data-ttu-id="b4f87-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b4f87-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="b4f87-461">範例</span><span class="sxs-lookup"><span data-stu-id="b4f87-461">Example</span></span>

<span data-ttu-id="b4f87-462">下列 Microsoft Visual Basic 範例示範如何連接到遠端電腦，並使用遠端電腦的 **LocalComputer** 集合來取得其 SecurityTrackingEnabled 屬性。</span><span class="sxs-lookup"><span data-stu-id="b4f87-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="b4f87-463">若要使用此範例，請新增 COM + 系統管理員類型程式庫做為您 Visual Basic 專案的參考。</span><span class="sxs-lookup"><span data-stu-id="b4f87-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="b4f87-464">若要使用函數，請提供遠端電腦名稱稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="b4f87-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="b4f87-465">下列 Visual Basic 程式碼示範如何連接到名為 "RemoteComputerName" 的電腦。</span><span class="sxs-lookup"><span data-stu-id="b4f87-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="b4f87-466">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4f87-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f87-467">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="b4f87-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
