---
description: 包含相關應用程式中每個元件的物件。
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: 元件集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510715"
---
# <a name="components-collection"></a><span data-ttu-id="f71fb-103">元件集合</span><span class="sxs-lookup"><span data-stu-id="f71fb-103">Components collection</span></span>

<span data-ttu-id="f71fb-104">包含相關應用程式中每個元件的物件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="f71fb-105">**元件** 集合一律與 [**應用程式**](applications.md)集合中的物件相關。</span><span class="sxs-lookup"><span data-stu-id="f71fb-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="f71fb-106">這些物件所公開的屬性會保存在元件層級所做的設定。</span><span class="sxs-lookup"><span data-stu-id="f71fb-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="f71fb-107">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。</span><span class="sxs-lookup"><span data-stu-id="f71fb-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="f71fb-108">若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="f71fb-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f71fb-109">成員</span><span class="sxs-lookup"><span data-stu-id="f71fb-109">Members</span></span>

<span data-ttu-id="f71fb-110">**元件** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="f71fb-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f71fb-111">相關集合</span><span class="sxs-lookup"><span data-stu-id="f71fb-111">Related Collections</span></span>

<span data-ttu-id="f71fb-112">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="f71fb-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f71fb-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f71fb-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f71fb-114">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="f71fb-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="f71fb-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f71fb-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f71fb-116">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f71fb-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="f71fb-117">**RolesForComponent**</span><span class="sxs-lookup"><span data-stu-id="f71fb-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="f71fb-118">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="f71fb-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="f71fb-119">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="f71fb-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f71fb-120">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="f71fb-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="f71fb-121">屬性</span><span class="sxs-lookup"><span data-stu-id="f71fb-121">Properties</span></span>

<span data-ttu-id="f71fb-122">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="f71fb-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f71fb-123">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="f71fb-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="f71fb-124">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="f71fb-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="f71fb-125">位元</span><span class="sxs-lookup"><span data-stu-id="f71fb-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="f71fb-126">Clsid</span><span class="sxs-lookup"><span data-stu-id="f71fb-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="f71fb-127">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="f71fb-128">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f71fb-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="f71fb-129">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="f71fb-130">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f71fb-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="f71fb-131">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="f71fb-132">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="f71fb-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="f71fb-133">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="f71fb-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="f71fb-134">說明</span><span class="sxs-lookup"><span data-stu-id="f71fb-134">Description</span></span>](#description)
-   [<span data-ttu-id="f71fb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f71fb-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="f71fb-136">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="f71fb-137">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="f71fb-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="f71fb-138">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="f71fb-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="f71fb-139">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f71fb-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="f71fb-140">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="f71fb-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="f71fb-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="f71fb-142">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="f71fb-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="f71fb-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="f71fb-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="f71fb-144">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f71fb-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="f71fb-145">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="f71fb-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="f71fb-146">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="f71fb-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="f71fb-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="f71fb-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="f71fb-148">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="f71fb-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="f71fb-149">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="f71fb-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="f71fb-150">MustRunInClientCoNtext</span><span class="sxs-lookup"><span data-stu-id="f71fb-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="f71fb-151">MustRunInDefaultCoNtext</span><span class="sxs-lookup"><span data-stu-id="f71fb-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="f71fb-152">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="f71fb-153">ProgID</span><span class="sxs-lookup"><span data-stu-id="f71fb-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="f71fb-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="f71fb-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="f71fb-155">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="f71fb-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="f71fb-156">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="f71fb-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="f71fb-157">同步處理</span><span class="sxs-lookup"><span data-stu-id="f71fb-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="f71fb-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="f71fb-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="f71fb-159">交易</span><span class="sxs-lookup"><span data-stu-id="f71fb-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="f71fb-160">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="f71fb-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="f71fb-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="f71fb-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="f71fb-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="f71fb-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="f71fb-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="f71fb-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="f71fb-164">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="f71fb-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="f71fb-165">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="f71fb-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="f71fb-166">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-166">Entry</span></span> | <span data-ttu-id="f71fb-167">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="f71fb-168">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-168">Description</span></span>    | <span data-ttu-id="f71fb-169">如果元件是事件類別，則在處理訂閱者中啟用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="f71fb-170">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-170">Access</span></span>         | <span data-ttu-id="f71fb-171">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="f71fb-172">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-172">Type</span></span>           | <span data-ttu-id="f71fb-173">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-173">Bool</span></span>                                                               |
| <span data-ttu-id="f71fb-174">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-174">Default</span></span>        | <span data-ttu-id="f71fb-175">對</span><span class="sxs-lookup"><span data-stu-id="f71fb-175">True</span></span>                                                               |
| <span data-ttu-id="f71fb-176">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-176">Minimum system</span></span> | <span data-ttu-id="f71fb-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="f71fb-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="f71fb-178">ApplicationID</span></span>



| <span data-ttu-id="f71fb-179">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-179">Entry</span></span> | <span data-ttu-id="f71fb-180">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-181">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-181">Description</span></span>    | <span data-ttu-id="f71fb-182">包含元件之應用程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f71fb-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="f71fb-183">必須是有效的應用程式 GUID，在呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 之前會先進行驗證。</span><span class="sxs-lookup"><span data-stu-id="f71fb-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="f71fb-184">如果此值變更為不同應用程式的 GUID，則元件會移至該應用程式。</span><span class="sxs-lookup"><span data-stu-id="f71fb-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="f71fb-185">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-185">Access</span></span>         | <span data-ttu-id="f71fb-186">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f71fb-187">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-187">Type</span></span>           | <span data-ttu-id="f71fb-188">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f71fb-189">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-189">Default</span></span>        | <span data-ttu-id="f71fb-190">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f71fb-191">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-191">Minimum system</span></span> | <span data-ttu-id="f71fb-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="f71fb-193">位元</span><span class="sxs-lookup"><span data-stu-id="f71fb-193">Bitness</span></span>



| <span data-ttu-id="f71fb-194">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-194">Entry</span></span> | <span data-ttu-id="f71fb-195">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-196">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-196">Description</span></span>    | <span data-ttu-id="f71fb-197">表示元件的二進位位數類型。</span><span class="sxs-lookup"><span data-stu-id="f71fb-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="f71fb-198">在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="f71fb-199">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-199">Access</span></span>         | <span data-ttu-id="f71fb-200">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="f71fb-201">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-201">Type</span></span>           | <span data-ttu-id="f71fb-202">很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2) </span><span class="sxs-lookup"><span data-stu-id="f71fb-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="f71fb-203">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-203">Default</span></span>        | <span data-ttu-id="f71fb-204">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f71fb-205">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-205">Minimum system</span></span> | <span data-ttu-id="f71fb-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71fb-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="f71fb-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="f71fb-207">CLSID</span></span>



| <span data-ttu-id="f71fb-208">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-208">Entry</span></span> | <span data-ttu-id="f71fb-209">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-210">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-210">Description</span></span>    | <span data-ttu-id="f71fb-211">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f71fb-211">A GUID for the component.</span></span> <span data-ttu-id="f71fb-212">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f71fb-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f71fb-213">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-213">Access</span></span>         | <span data-ttu-id="f71fb-214">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="f71fb-215">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-215">Type</span></span>           | <span data-ttu-id="f71fb-216">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="f71fb-217">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-217">Default</span></span>        | <span data-ttu-id="f71fb-218">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="f71fb-219">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-219">Minimum system</span></span> | <span data-ttu-id="f71fb-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="f71fb-221">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="f71fb-222">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-222">Entry</span></span> | <span data-ttu-id="f71fb-223">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-224">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-224">Description</span></span>    | <span data-ttu-id="f71fb-225">指出是否要對元件的呼叫執行以角色為基礎的存取檢查，並與應用程式上的 AccessChecksLevel 和 ApplicationAccessChecksEnabled 屬性搭配使用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="f71fb-226">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-226">Access</span></span>         | <span data-ttu-id="f71fb-227">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="f71fb-228">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-228">Type</span></span>           | <span data-ttu-id="f71fb-229">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="f71fb-230">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-230">Default</span></span>        | <span data-ttu-id="f71fb-231">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="f71fb-232">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-232">Minimum system</span></span> | <span data-ttu-id="f71fb-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="f71fb-234">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="f71fb-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="f71fb-235">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-235">Entry</span></span> | <span data-ttu-id="f71fb-236">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-237">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-237">Description</span></span>    | <span data-ttu-id="f71fb-238">在交易中使用時，會指定此元件造成交易超時的時間週期。預設值為60秒，且不能超過3600秒 (1 小時) 。</span><span class="sxs-lookup"><span data-stu-id="f71fb-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="f71fb-239">超時值可以設定為0，並指定無限的交易超時時間。</span><span class="sxs-lookup"><span data-stu-id="f71fb-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="f71fb-240">若要使用這個屬性，ComponentTransactionTimeoutEnabled 必須是 True。</span><span class="sxs-lookup"><span data-stu-id="f71fb-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="f71fb-241">這個屬性的值會覆寫 [**LocalComputer**](localcomputer.md) 集合的 TransactionTimeout 屬性所指定的全域交易超時時間。</span><span class="sxs-lookup"><span data-stu-id="f71fb-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="f71fb-242">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-242">Access</span></span>         | <span data-ttu-id="f71fb-243">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f71fb-244">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-244">Type</span></span>           | <span data-ttu-id="f71fb-245">Long (0-3600) </span><span class="sxs-lookup"><span data-stu-id="f71fb-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f71fb-246">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-246">Default</span></span>        | <span data-ttu-id="f71fb-247">60</span><span class="sxs-lookup"><span data-stu-id="f71fb-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f71fb-248">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-248">Minimum system</span></span> | <span data-ttu-id="f71fb-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="f71fb-250">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="f71fb-251">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-251">Entry</span></span> | <span data-ttu-id="f71fb-252">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-253">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-253">Description</span></span>    | <span data-ttu-id="f71fb-254">指定是否啟用此元件的交易超時時間。</span><span class="sxs-lookup"><span data-stu-id="f71fb-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="f71fb-255">依預設，交易超時功能已停用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="f71fb-256">當此屬性為 True 時，會使用 ComponentTransactionTimeout 所指定的超時時間。</span><span class="sxs-lookup"><span data-stu-id="f71fb-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="f71fb-257">當這個屬性為 False 時，就會使用 [**LocalComputer**](localcomputer.md) 集合的 TransactionTimeout 屬性所指定的超時時間。</span><span class="sxs-lookup"><span data-stu-id="f71fb-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="f71fb-258">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-258">Access</span></span>         | <span data-ttu-id="f71fb-259">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f71fb-260">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-260">Type</span></span>           | <span data-ttu-id="f71fb-261">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f71fb-262">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-262">Default</span></span>        | <span data-ttu-id="f71fb-263">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f71fb-264">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-264">Minimum system</span></span> | <span data-ttu-id="f71fb-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="f71fb-266">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f71fb-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="f71fb-267">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-267">Entry</span></span> | <span data-ttu-id="f71fb-268">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-269">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-269">Description</span></span>    | <span data-ttu-id="f71fb-270">可從 COM 交易整合器 (COMTI) 將內容屬性傳遞至這個類別的內容。</span><span class="sxs-lookup"><span data-stu-id="f71fb-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="f71fb-271">COMTI 能簡化將大型主機交易和商務邏輯包裝為 COM 元件的工作。</span><span class="sxs-lookup"><span data-stu-id="f71fb-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="f71fb-272">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-272">Access</span></span>         | <span data-ttu-id="f71fb-273">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="f71fb-274">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-274">Type</span></span>           | <span data-ttu-id="f71fb-275">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="f71fb-276">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-276">Default</span></span>        | <span data-ttu-id="f71fb-277">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="f71fb-278">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-278">Minimum system</span></span> | <span data-ttu-id="f71fb-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="f71fb-280">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-280">ConstructionEnabled</span></span>



| <span data-ttu-id="f71fb-281">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-281">Entry</span></span> | <span data-ttu-id="f71fb-282">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-283">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-283">Description</span></span>    | <span data-ttu-id="f71fb-284">判斷 ConstructorString 是否會在建立時傳遞給物件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="f71fb-285">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-285">Access</span></span>         | <span data-ttu-id="f71fb-286">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="f71fb-287">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-287">Type</span></span>           | <span data-ttu-id="f71fb-288">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="f71fb-289">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-289">Default</span></span>        | <span data-ttu-id="f71fb-290">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-290">False</span></span>                                                                                    |
| <span data-ttu-id="f71fb-291">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-291">Minimum system</span></span> | <span data-ttu-id="f71fb-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="f71fb-293">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="f71fb-293">ConstructorString</span></span>



| <span data-ttu-id="f71fb-294">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-294">Entry</span></span> | <span data-ttu-id="f71fb-295">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-296">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-296">Description</span></span>    | <span data-ttu-id="f71fb-297">元件結構的初始化字串。</span><span class="sxs-lookup"><span data-stu-id="f71fb-297">Initialization string for component construction.</span></span> <span data-ttu-id="f71fb-298">您可以使用物件的函式字串，從相同的泛型元件建立不同的物件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="f71fb-299">如果 ConstructionEnabled 為 False，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f71fb-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="f71fb-300">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-300">Access</span></span>         | <span data-ttu-id="f71fb-301">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="f71fb-302">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-302">Type</span></span>           | <span data-ttu-id="f71fb-303">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="f71fb-304">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-304">Default</span></span>        | <span data-ttu-id="f71fb-305">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="f71fb-306">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-306">Minimum system</span></span> | <span data-ttu-id="f71fb-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="f71fb-308">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="f71fb-308">CreationTimeout</span></span>



| <span data-ttu-id="f71fb-309">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-309">Entry</span></span> | <span data-ttu-id="f71fb-310">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-311">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-311">Description</span></span>    | <span data-ttu-id="f71fb-312">在建立物件時，會傳回逾時錯誤之前的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="f71fb-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="f71fb-313">最大超時值為2147483647毫秒 (大約25天) 。</span><span class="sxs-lookup"><span data-stu-id="f71fb-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="f71fb-314">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-314">Access</span></span>         | <span data-ttu-id="f71fb-315">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="f71fb-316">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-316">Type</span></span>           | <span data-ttu-id="f71fb-317">Long (0-2147483647) </span><span class="sxs-lookup"><span data-stu-id="f71fb-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="f71fb-318">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-318">Default</span></span>        | <span data-ttu-id="f71fb-319">0</span><span class="sxs-lookup"><span data-stu-id="f71fb-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="f71fb-320">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-320">Minimum system</span></span> | <span data-ttu-id="f71fb-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="f71fb-322">Description</span><span class="sxs-lookup"><span data-stu-id="f71fb-322">Description</span></span>



| <span data-ttu-id="f71fb-323">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-323">Entry</span></span> | <span data-ttu-id="f71fb-324">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="f71fb-325">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-325">Description</span></span>    | <span data-ttu-id="f71fb-326">描述元件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-326">Describes the component.</span></span> |
| <span data-ttu-id="f71fb-327">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-327">Access</span></span>         | <span data-ttu-id="f71fb-328">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-328">ReadWrite</span></span>                |
| <span data-ttu-id="f71fb-329">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-329">Type</span></span>           | <span data-ttu-id="f71fb-330">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-330">String</span></span>                   |
| <span data-ttu-id="f71fb-331">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-331">Default</span></span>        | <span data-ttu-id="f71fb-332">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-332">""</span></span>                       |
| <span data-ttu-id="f71fb-333">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-333">Minimum system</span></span> | <span data-ttu-id="f71fb-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="f71fb-335">DLL</span><span class="sxs-lookup"><span data-stu-id="f71fb-335">DLL</span></span>



| <span data-ttu-id="f71fb-336">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-336">Entry</span></span> | <span data-ttu-id="f71fb-337">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="f71fb-338">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-338">Description</span></span>    | <span data-ttu-id="f71fb-339">包含元件的檔案名和路徑。</span><span class="sxs-lookup"><span data-stu-id="f71fb-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="f71fb-340">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-340">Access</span></span>         | <span data-ttu-id="f71fb-341">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="f71fb-342">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-342">Type</span></span>           | <span data-ttu-id="f71fb-343">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-343">String</span></span>                                                  |
| <span data-ttu-id="f71fb-344">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-344">Default</span></span>        | <span data-ttu-id="f71fb-345">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-345">N/A</span></span>                                                     |
| <span data-ttu-id="f71fb-346">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-346">Minimum system</span></span> | <span data-ttu-id="f71fb-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="f71fb-348">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="f71fb-349">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-349">Entry</span></span> | <span data-ttu-id="f71fb-350">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-351">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-351">Description</span></span>    | <span data-ttu-id="f71fb-352">判斷是否追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-352">Determines whether events are tracked.</span></span> <span data-ttu-id="f71fb-353">事件包含像是應用程式關閉的動作;物件建立和發行;物件參考、一致性、啟用和停用;方法呼叫、傳回和例外狀況;交易啟動、準備認可和中止;資源配置器連接、配置和回收;執行緒配置和回收。</span><span class="sxs-lookup"><span data-stu-id="f71fb-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="f71fb-354">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-354">Access</span></span>         | <span data-ttu-id="f71fb-355">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="f71fb-356">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-356">Type</span></span>           | <span data-ttu-id="f71fb-357">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f71fb-358">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-358">Default</span></span>        | <span data-ttu-id="f71fb-359">對</span><span class="sxs-lookup"><span data-stu-id="f71fb-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f71fb-360">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-360">Minimum system</span></span> | <span data-ttu-id="f71fb-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="f71fb-362">ExceptionClass</span><span class="sxs-lookup"><span data-stu-id="f71fb-362">ExceptionClass</span></span>



| <span data-ttu-id="f71fb-363">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-363">Entry</span></span> | <span data-ttu-id="f71fb-364">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-365">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-365">Description</span></span>    | <span data-ttu-id="f71fb-366">CLSID （可以是 GUID 或標記字串），可在處理重複排入佇列之元件程式的程式期間啟動替代程式。</span><span class="sxs-lookup"><span data-stu-id="f71fb-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="f71fb-367">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-367">Access</span></span>         | <span data-ttu-id="f71fb-368">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f71fb-369">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-369">Type</span></span>           | <span data-ttu-id="f71fb-370">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="f71fb-371">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-371">Default</span></span>        | <span data-ttu-id="f71fb-372">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="f71fb-373">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-373">Minimum system</span></span> | <span data-ttu-id="f71fb-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="f71fb-375">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="f71fb-375">FireInParallel</span></span>



| <span data-ttu-id="f71fb-376">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-376">Entry</span></span> | <span data-ttu-id="f71fb-377">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-378">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-378">Description</span></span>    | <span data-ttu-id="f71fb-379">如果元件是事件類別，則可讓事件以平行方式引發。</span><span class="sxs-lookup"><span data-stu-id="f71fb-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="f71fb-380">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-380">Access</span></span>         | <span data-ttu-id="f71fb-381">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="f71fb-382">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-382">Type</span></span>           | <span data-ttu-id="f71fb-383">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-383">Bool</span></span>                                                                       |
| <span data-ttu-id="f71fb-384">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-384">Default</span></span>        | <span data-ttu-id="f71fb-385">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-385">False</span></span>                                                                      |
| <span data-ttu-id="f71fb-386">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-386">Minimum system</span></span> | <span data-ttu-id="f71fb-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="f71fb-388">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="f71fb-388">IISIntrinsics</span></span>



| <span data-ttu-id="f71fb-389">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-389">Entry</span></span> | <span data-ttu-id="f71fb-390">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-391">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-391">Description</span></span>    | <span data-ttu-id="f71fb-392">啟用將 IIS 內容屬性（例如應用程式會話物件或使用者會話物件）傳遞到此類別的內容中。</span><span class="sxs-lookup"><span data-stu-id="f71fb-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="f71fb-393">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-393">Access</span></span>         | <span data-ttu-id="f71fb-394">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="f71fb-395">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-395">Type</span></span>           | <span data-ttu-id="f71fb-396">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="f71fb-397">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-397">Default</span></span>        | <span data-ttu-id="f71fb-398">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="f71fb-399">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-399">Minimum system</span></span> | <span data-ttu-id="f71fb-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="f71fb-401">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="f71fb-401">InitializeServerApplication</span></span>



| <span data-ttu-id="f71fb-402">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-402">Entry</span></span> | <span data-ttu-id="f71fb-403">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-404">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-404">Description</span></span>    | <span data-ttu-id="f71fb-405">指出元件是否用來初始化伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="f71fb-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="f71fb-406">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-406">Access</span></span>         | <span data-ttu-id="f71fb-407">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="f71fb-408">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-408">Type</span></span>           | <span data-ttu-id="f71fb-409">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-409">Bool</span></span>                                                                        |
| <span data-ttu-id="f71fb-410">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-410">Default</span></span>        | <span data-ttu-id="f71fb-411">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-411">False</span></span>                                                                       |
| <span data-ttu-id="f71fb-412">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-412">Minimum system</span></span> | <span data-ttu-id="f71fb-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f71fb-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="f71fb-414">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-414">IsEnabled</span></span>



| <span data-ttu-id="f71fb-415">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-415">Entry</span></span> | <span data-ttu-id="f71fb-416">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-417">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-417">Description</span></span>    | <span data-ttu-id="f71fb-418">如果 COM + 應用程式或元件已停用，則為 False。</span><span class="sxs-lookup"><span data-stu-id="f71fb-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="f71fb-419">如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。</span><span class="sxs-lookup"><span data-stu-id="f71fb-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="f71fb-420">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-420">Access</span></span>         | <span data-ttu-id="f71fb-421">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="f71fb-422">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-422">Type</span></span>           | <span data-ttu-id="f71fb-423">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="f71fb-424">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-424">Default</span></span>        | <span data-ttu-id="f71fb-425">對</span><span class="sxs-lookup"><span data-stu-id="f71fb-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="f71fb-426">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-426">Minimum system</span></span> | <span data-ttu-id="f71fb-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71fb-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="f71fb-428">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="f71fb-428">IsEventClass</span></span>



| <span data-ttu-id="f71fb-429">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-429">Entry</span></span> | <span data-ttu-id="f71fb-430">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="f71fb-431">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-431">Description</span></span>    | <span data-ttu-id="f71fb-432">指出元件是否為事件類別。</span><span class="sxs-lookup"><span data-stu-id="f71fb-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="f71fb-433">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-433">Access</span></span>         | <span data-ttu-id="f71fb-434">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="f71fb-435">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-435">Type</span></span>           | <span data-ttu-id="f71fb-436">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-436">Bool</span></span>                                               |
| <span data-ttu-id="f71fb-437">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-437">Default</span></span>        | <span data-ttu-id="f71fb-438">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-438">False</span></span>                                              |
| <span data-ttu-id="f71fb-439">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-439">Minimum system</span></span> | <span data-ttu-id="f71fb-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="f71fb-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="f71fb-441">IsInstalled</span></span>



| <span data-ttu-id="f71fb-442">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-442">Entry</span></span> | <span data-ttu-id="f71fb-443">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="f71fb-444">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-444">Description</span></span>    | <span data-ttu-id="f71fb-445">指出元件是否安裝在應用程式中。</span><span class="sxs-lookup"><span data-stu-id="f71fb-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="f71fb-446">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-446">Access</span></span>         | <span data-ttu-id="f71fb-447">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="f71fb-448">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-448">Type</span></span>           | <span data-ttu-id="f71fb-449">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-449">Bool</span></span>                                                            |
| <span data-ttu-id="f71fb-450">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-450">Default</span></span>        | <span data-ttu-id="f71fb-451">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-451">False</span></span>                                                           |
| <span data-ttu-id="f71fb-452">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-452">Minimum system</span></span> | <span data-ttu-id="f71fb-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f71fb-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="f71fb-454">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f71fb-454">IsPrivateComponent</span></span>



| <span data-ttu-id="f71fb-455">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-455">Entry</span></span> | <span data-ttu-id="f71fb-456">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-457">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-457">Description</span></span>    | <span data-ttu-id="f71fb-458">判斷伺服器應用程式是否為私用元件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="f71fb-459">伺服器應用程式中的私用元件只能從應用程式內啟用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="f71fb-460">例如，如果您在私用元件上呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ，它會從跨進程失敗，但會成功進行同進程。</span><span class="sxs-lookup"><span data-stu-id="f71fb-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="f71fb-461">相反地，如果您在公用元件上呼叫 **CoCreateInstance** ，則會成功進行同進程和跨進程。</span><span class="sxs-lookup"><span data-stu-id="f71fb-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="f71fb-462">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-462">Access</span></span>         | <span data-ttu-id="f71fb-463">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f71fb-464">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-464">Type</span></span>           | <span data-ttu-id="f71fb-465">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f71fb-466">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-466">Default</span></span>        | <span data-ttu-id="f71fb-467">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f71fb-468">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-468">Minimum system</span></span> | <span data-ttu-id="f71fb-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71fb-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="f71fb-470">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="f71fb-470">JustInTimeActivation</span></span>



| <span data-ttu-id="f71fb-471">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-471">Entry</span></span> | <span data-ttu-id="f71fb-472">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-473">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-473">Description</span></span>    | <span data-ttu-id="f71fb-474">判斷是否已啟用元件的 [JIT](enabling-jit-activation-for-a-component.md) 啟用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="f71fb-475">當 [交易支援](setting-the-transaction-attribute.md) 設定為必要、需要新增或支援時，這個屬性會設定為 True。</span><span class="sxs-lookup"><span data-stu-id="f71fb-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="f71fb-476">當 JustInTimeActivation 設定為 True 時，必須將 [同步處理支援](setting-the-synchronization-attribute.md) 設定為 [必要] (預設) 或需要新的。</span><span class="sxs-lookup"><span data-stu-id="f71fb-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="f71fb-477">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-477">Access</span></span>         | <span data-ttu-id="f71fb-478">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f71fb-479">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-479">Type</span></span>           | <span data-ttu-id="f71fb-480">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="f71fb-481">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-481">Default</span></span>        | <span data-ttu-id="f71fb-482">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="f71fb-483">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-483">Minimum system</span></span> | <span data-ttu-id="f71fb-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="f71fb-485">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="f71fb-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="f71fb-486">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-486">Entry</span></span> | <span data-ttu-id="f71fb-487">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-488">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-488">Description</span></span>    | <span data-ttu-id="f71fb-489">如果伺服器上已安裝並啟用元件負載平衡服務，則會判斷元件是否參與負載平衡。</span><span class="sxs-lookup"><span data-stu-id="f71fb-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="f71fb-490">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-490">Access</span></span>         | <span data-ttu-id="f71fb-491">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="f71fb-492">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-492">Type</span></span>           | <span data-ttu-id="f71fb-493">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="f71fb-494">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-494">Default</span></span>        | <span data-ttu-id="f71fb-495">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="f71fb-496">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-496">Minimum system</span></span> | <span data-ttu-id="f71fb-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="f71fb-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="f71fb-498">MaxPoolSize</span></span>



| <span data-ttu-id="f71fb-499">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-499">Entry</span></span> | <span data-ttu-id="f71fb-500">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="f71fb-501">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-501">Description</span></span>    | <span data-ttu-id="f71fb-502">集區的最大物件數目。</span><span class="sxs-lookup"><span data-stu-id="f71fb-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="f71fb-503">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-503">Access</span></span>         | <span data-ttu-id="f71fb-504">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-504">ReadWrite</span></span>                         |
| <span data-ttu-id="f71fb-505">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-505">Type</span></span>           | <span data-ttu-id="f71fb-506">Long (1-1048576) </span><span class="sxs-lookup"><span data-stu-id="f71fb-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="f71fb-507">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-507">Default</span></span>        | <span data-ttu-id="f71fb-508">1048576</span><span class="sxs-lookup"><span data-stu-id="f71fb-508">1048576</span></span>                           |
| <span data-ttu-id="f71fb-509">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-509">Minimum system</span></span> | <span data-ttu-id="f71fb-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="f71fb-511">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="f71fb-511">MinPoolSize</span></span>



| <span data-ttu-id="f71fb-512">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-512">Entry</span></span> | <span data-ttu-id="f71fb-513">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="f71fb-514">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-514">Description</span></span>    | <span data-ttu-id="f71fb-515">共置的物件數目下限。</span><span class="sxs-lookup"><span data-stu-id="f71fb-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="f71fb-516">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-516">Access</span></span>         | <span data-ttu-id="f71fb-517">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-517">ReadWrite</span></span>                         |
| <span data-ttu-id="f71fb-518">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-518">Type</span></span>           | <span data-ttu-id="f71fb-519">Long (0-1048576) </span><span class="sxs-lookup"><span data-stu-id="f71fb-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="f71fb-520">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-520">Default</span></span>        | <span data-ttu-id="f71fb-521">0</span><span class="sxs-lookup"><span data-stu-id="f71fb-521">0</span></span>                                 |
| <span data-ttu-id="f71fb-522">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-522">Minimum system</span></span> | <span data-ttu-id="f71fb-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="f71fb-524">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="f71fb-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="f71fb-525">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-525">Entry</span></span> | <span data-ttu-id="f71fb-526">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-527">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-527">Description</span></span>    | <span data-ttu-id="f71fb-528">如果元件是事件類別，則使用發行者篩選器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="f71fb-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="f71fb-529">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-529">Access</span></span>         | <span data-ttu-id="f71fb-530">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="f71fb-531">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-531">Type</span></span>           | <span data-ttu-id="f71fb-532">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-532">String</span></span>                                                                  |
| <span data-ttu-id="f71fb-533">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-533">Default</span></span>        | <span data-ttu-id="f71fb-534">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-534">N/A</span></span>                                                                     |
| <span data-ttu-id="f71fb-535">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-535">Minimum system</span></span> | <span data-ttu-id="f71fb-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="f71fb-537">MustRunInClientCoNtext</span><span class="sxs-lookup"><span data-stu-id="f71fb-537">MustRunInClientContext</span></span>



| <span data-ttu-id="f71fb-538">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-538">Entry</span></span> | <span data-ttu-id="f71fb-539">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-540">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-540">Description</span></span>    | <span data-ttu-id="f71fb-541">表示元件必須在其原始呼叫端的內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="f71fb-542">否則啟用會失敗。</span><span class="sxs-lookup"><span data-stu-id="f71fb-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="f71fb-543">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-543">Access</span></span>         | <span data-ttu-id="f71fb-544">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="f71fb-545">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-545">Type</span></span>           | <span data-ttu-id="f71fb-546">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="f71fb-547">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-547">Default</span></span>        | <span data-ttu-id="f71fb-548">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-548">False</span></span>                                                                                                     |
| <span data-ttu-id="f71fb-549">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-549">Minimum system</span></span> | <span data-ttu-id="f71fb-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71fb-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="f71fb-551">MustRunInDefaultCoNtext</span><span class="sxs-lookup"><span data-stu-id="f71fb-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="f71fb-552">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-552">Entry</span></span> | <span data-ttu-id="f71fb-553">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-554">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-554">Description</span></span>    | <span data-ttu-id="f71fb-555">指出必須在預設呼叫端的內容中啟用元件。</span><span class="sxs-lookup"><span data-stu-id="f71fb-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="f71fb-556">否則啟用會失敗。</span><span class="sxs-lookup"><span data-stu-id="f71fb-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="f71fb-557">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-557">Access</span></span>         | <span data-ttu-id="f71fb-558">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="f71fb-559">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-559">Type</span></span>           | <span data-ttu-id="f71fb-560">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="f71fb-561">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-561">Default</span></span>        | <span data-ttu-id="f71fb-562">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-562">False</span></span>                                                                                                        |
| <span data-ttu-id="f71fb-563">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-563">Minimum system</span></span> | <span data-ttu-id="f71fb-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="f71fb-565">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="f71fb-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="f71fb-566">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-566">Entry</span></span> | <span data-ttu-id="f71fb-567">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-568">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-568">Description</span></span>    | <span data-ttu-id="f71fb-569">判斷元件是否啟用 [Com + 物件](com--object-pooling.md) 共用。</span><span class="sxs-lookup"><span data-stu-id="f71fb-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="f71fb-570">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-570">Access</span></span>         | <span data-ttu-id="f71fb-571">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="f71fb-572">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-572">Type</span></span>           | <span data-ttu-id="f71fb-573">Bool</span><span class="sxs-lookup"><span data-stu-id="f71fb-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="f71fb-574">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-574">Default</span></span>        | <span data-ttu-id="f71fb-575">否</span><span class="sxs-lookup"><span data-stu-id="f71fb-575">False</span></span>                                                                                           |
| <span data-ttu-id="f71fb-576">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-576">Minimum system</span></span> | <span data-ttu-id="f71fb-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="f71fb-578">ProgID</span><span class="sxs-lookup"><span data-stu-id="f71fb-578">ProgID</span></span>



| <span data-ttu-id="f71fb-579">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-579">Entry</span></span> | <span data-ttu-id="f71fb-580">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-581">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-581">Description</span></span>    | <span data-ttu-id="f71fb-582">用來識別元件的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f71fb-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="f71fb-583">在這個集合的物件上呼叫 [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f71fb-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f71fb-584">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-584">Access</span></span>         | <span data-ttu-id="f71fb-585">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="f71fb-586">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-586">Type</span></span>           | <span data-ttu-id="f71fb-587">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="f71fb-588">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-588">Default</span></span>        | <span data-ttu-id="f71fb-589">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="f71fb-590">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-590">Minimum system</span></span> | <span data-ttu-id="f71fb-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="f71fb-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="f71fb-592">PublisherID</span></span>



| <span data-ttu-id="f71fb-593">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-593">Entry</span></span> | <span data-ttu-id="f71fb-594">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-595">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-595">Description</span></span>    | <span data-ttu-id="f71fb-596">如果元件是事件類別，則為事件發行者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f71fb-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="f71fb-597">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-597">Access</span></span>         | <span data-ttu-id="f71fb-598">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="f71fb-599">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-599">Type</span></span>           | <span data-ttu-id="f71fb-600">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-600">String</span></span>                                                                 |
| <span data-ttu-id="f71fb-601">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-601">Default</span></span>        | <span data-ttu-id="f71fb-602">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-602">""</span></span>                                                                     |
| <span data-ttu-id="f71fb-603">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-603">Minimum system</span></span> | <span data-ttu-id="f71fb-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="f71fb-605">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="f71fb-605">SoapAssemblyName</span></span>



| <span data-ttu-id="f71fb-606">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-606">Entry</span></span> | <span data-ttu-id="f71fb-607">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-608">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-608">Description</span></span>    | <span data-ttu-id="f71fb-609">識別 GAC 元件的 GUID，該元件會在以 SOAP 服務的形式叫用元件時執行。</span><span class="sxs-lookup"><span data-stu-id="f71fb-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="f71fb-610">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-610">Access</span></span>         | <span data-ttu-id="f71fb-611">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="f71fb-612">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-612">Type</span></span>           | <span data-ttu-id="f71fb-613">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-613">String</span></span>                                                                                           |
| <span data-ttu-id="f71fb-614">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-614">Default</span></span>        | <span data-ttu-id="f71fb-615">NULL</span><span class="sxs-lookup"><span data-stu-id="f71fb-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="f71fb-616">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-616">Minimum system</span></span> | <span data-ttu-id="f71fb-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f71fb-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="f71fb-618">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="f71fb-618">SoapTypeName</span></span>



| <span data-ttu-id="f71fb-619">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-619">Entry</span></span> | <span data-ttu-id="f71fb-620">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-621">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-621">Description</span></span>    | <span data-ttu-id="f71fb-622">可以叫用為 SOAP 服務之元件的 managed 型別名稱。</span><span class="sxs-lookup"><span data-stu-id="f71fb-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="f71fb-623">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-623">Access</span></span>         | <span data-ttu-id="f71fb-624">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="f71fb-625">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-625">Type</span></span>           | <span data-ttu-id="f71fb-626">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-626">String</span></span>                                                                       |
| <span data-ttu-id="f71fb-627">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-627">Default</span></span>        | <span data-ttu-id="f71fb-628">NULL</span><span class="sxs-lookup"><span data-stu-id="f71fb-628">NULL</span></span>                                                                         |
| <span data-ttu-id="f71fb-629">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-629">Minimum system</span></span> | <span data-ttu-id="f71fb-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f71fb-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="f71fb-631">同步處理</span><span class="sxs-lookup"><span data-stu-id="f71fb-631">Synchronization</span></span>



| <span data-ttu-id="f71fb-632">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-632">Entry</span></span> | <span data-ttu-id="f71fb-633">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-634">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-634">Description</span></span>    | <span data-ttu-id="f71fb-635">判斷元件的呼叫 [同步](setting-the-synchronization-attribute.md) 處理。</span><span class="sxs-lookup"><span data-stu-id="f71fb-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="f71fb-636">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-636">Access</span></span>         | <span data-ttu-id="f71fb-637">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="f71fb-638">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-638">Type</span></span>           | <span data-ttu-id="f71fb-639">長可能的值： COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4) </span><span class="sxs-lookup"><span data-stu-id="f71fb-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="f71fb-640">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-640">Default</span></span>        | <span data-ttu-id="f71fb-641">COMAdminSynchronizationIgnored (0) </span><span class="sxs-lookup"><span data-stu-id="f71fb-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="f71fb-642">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-642">Minimum system</span></span> | <span data-ttu-id="f71fb-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="f71fb-644">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="f71fb-644">ThreadingModel</span></span>



| <span data-ttu-id="f71fb-645">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-645">Entry</span></span> | <span data-ttu-id="f71fb-646">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-647">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-647">Description</span></span>    | <span data-ttu-id="f71fb-648">決定如何將元件的實例指派給方法執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f71fb-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="f71fb-649">值會對應至 COM 執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="f71fb-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="f71fb-650">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-650">Access</span></span>         | <span data-ttu-id="f71fb-651">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="f71fb-652">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-652">Type</span></span>           | <span data-ttu-id="f71fb-653">長可能的值： COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5) </span><span class="sxs-lookup"><span data-stu-id="f71fb-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="f71fb-654">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-654">Default</span></span>        | <span data-ttu-id="f71fb-655">N/A</span><span class="sxs-lookup"><span data-stu-id="f71fb-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="f71fb-656">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-656">Minimum system</span></span> | <span data-ttu-id="f71fb-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="f71fb-658">交易</span><span class="sxs-lookup"><span data-stu-id="f71fb-658">Transaction</span></span>



| <span data-ttu-id="f71fb-659">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-659">Entry</span></span> | <span data-ttu-id="f71fb-660">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-661">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-661">Description</span></span>    | <span data-ttu-id="f71fb-662">決定元件如何支援 [交易](setting-the-transaction-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="f71fb-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="f71fb-663">建議您在列舉中使用常數，而不要使用數值。</span><span class="sxs-lookup"><span data-stu-id="f71fb-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="f71fb-664">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-664">Access</span></span>         | <span data-ttu-id="f71fb-665">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="f71fb-666">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-666">Type</span></span>           | <span data-ttu-id="f71fb-667">長可能的值： COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4) </span><span class="sxs-lookup"><span data-stu-id="f71fb-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="f71fb-668">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-668">Default</span></span>        | <span data-ttu-id="f71fb-669">COMAdminTransactionNone (1) </span><span class="sxs-lookup"><span data-stu-id="f71fb-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="f71fb-670">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-670">Minimum system</span></span> | <span data-ttu-id="f71fb-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="f71fb-672">TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="f71fb-672">TxIsolationLevel</span></span>



| <span data-ttu-id="f71fb-673">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-673">Entry</span></span> | <span data-ttu-id="f71fb-674">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71fb-675">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-675">Description</span></span>    | <span data-ttu-id="f71fb-676">指出交易隔離等級。</span><span class="sxs-lookup"><span data-stu-id="f71fb-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="f71fb-677">有五個隔離等級：無、讀取未認可、讀取認可、可重複讀取和序列化。</span><span class="sxs-lookup"><span data-stu-id="f71fb-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="f71fb-678">預設的隔離等級是序列化的。</span><span class="sxs-lookup"><span data-stu-id="f71fb-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="f71fb-679">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-679">Access</span></span>         | <span data-ttu-id="f71fb-680">讀寫</span><span class="sxs-lookup"><span data-stu-id="f71fb-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="f71fb-681">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-681">Type</span></span>           | <span data-ttu-id="f71fb-682">長可能的值： COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4) </span><span class="sxs-lookup"><span data-stu-id="f71fb-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="f71fb-683">預設</span><span class="sxs-lookup"><span data-stu-id="f71fb-683">Default</span></span>        | <span data-ttu-id="f71fb-684">COMAdminTxIsolationLevelSerializable (4) </span><span class="sxs-lookup"><span data-stu-id="f71fb-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="f71fb-685">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-685">Minimum system</span></span> | <span data-ttu-id="f71fb-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f71fb-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="f71fb-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="f71fb-687">VersionBuild</span></span>



| <span data-ttu-id="f71fb-688">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-688">Entry</span></span> | <span data-ttu-id="f71fb-689">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="f71fb-690">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-690">Description</span></span>    | <span data-ttu-id="f71fb-691">版本組建識別碼。</span><span class="sxs-lookup"><span data-stu-id="f71fb-691">Version build identifier.</span></span> |
| <span data-ttu-id="f71fb-692">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-692">Access</span></span>         | <span data-ttu-id="f71fb-693">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-693">ReadOnly</span></span>                  |
| <span data-ttu-id="f71fb-694">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-694">Type</span></span>           | <span data-ttu-id="f71fb-695">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-695">String</span></span>                    |
| <span data-ttu-id="f71fb-696">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-696">Default</span></span>        | <span data-ttu-id="f71fb-697">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-697">""</span></span>                        |
| <span data-ttu-id="f71fb-698">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-698">Minimum system</span></span> | <span data-ttu-id="f71fb-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="f71fb-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="f71fb-700">VersionMajor</span></span>



| <span data-ttu-id="f71fb-701">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-701">Entry</span></span> | <span data-ttu-id="f71fb-702">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="f71fb-703">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-703">Description</span></span>    | <span data-ttu-id="f71fb-704">版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="f71fb-704">Version identifier.</span></span> |
| <span data-ttu-id="f71fb-705">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-705">Access</span></span>         | <span data-ttu-id="f71fb-706">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-706">ReadOnly</span></span>            |
| <span data-ttu-id="f71fb-707">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-707">Type</span></span>           | <span data-ttu-id="f71fb-708">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-708">String</span></span>              |
| <span data-ttu-id="f71fb-709">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-709">Default</span></span>        | <span data-ttu-id="f71fb-710">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-710">""</span></span>                  |
| <span data-ttu-id="f71fb-711">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-711">Minimum system</span></span> | <span data-ttu-id="f71fb-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="f71fb-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="f71fb-713">VersionMinor</span></span>



| <span data-ttu-id="f71fb-714">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-714">Entry</span></span> | <span data-ttu-id="f71fb-715">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="f71fb-716">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-716">Description</span></span>    | <span data-ttu-id="f71fb-717">版本子識別碼。</span><span class="sxs-lookup"><span data-stu-id="f71fb-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="f71fb-718">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-718">Access</span></span>         | <span data-ttu-id="f71fb-719">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-719">ReadOnly</span></span>                |
| <span data-ttu-id="f71fb-720">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-720">Type</span></span>           | <span data-ttu-id="f71fb-721">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-721">String</span></span>                  |
| <span data-ttu-id="f71fb-722">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-722">Default</span></span>        | <span data-ttu-id="f71fb-723">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-723">""</span></span>                      |
| <span data-ttu-id="f71fb-724">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-724">Minimum system</span></span> | <span data-ttu-id="f71fb-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="f71fb-726">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="f71fb-726">VersionSubBuild</span></span>



| <span data-ttu-id="f71fb-727">進入</span><span class="sxs-lookup"><span data-stu-id="f71fb-727">Entry</span></span> | <span data-ttu-id="f71fb-728">值</span><span class="sxs-lookup"><span data-stu-id="f71fb-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="f71fb-729">描述</span><span class="sxs-lookup"><span data-stu-id="f71fb-729">Description</span></span>    | <span data-ttu-id="f71fb-730">版本子組建識別碼。</span><span class="sxs-lookup"><span data-stu-id="f71fb-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="f71fb-731">Access</span><span class="sxs-lookup"><span data-stu-id="f71fb-731">Access</span></span>         | <span data-ttu-id="f71fb-732">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f71fb-732">ReadOnly</span></span>                      |
| <span data-ttu-id="f71fb-733">類型</span><span class="sxs-lookup"><span data-stu-id="f71fb-733">Type</span></span>           | <span data-ttu-id="f71fb-734">String</span><span class="sxs-lookup"><span data-stu-id="f71fb-734">String</span></span>                        |
| <span data-ttu-id="f71fb-735">預設值</span><span class="sxs-lookup"><span data-stu-id="f71fb-735">Default</span></span>        | <span data-ttu-id="f71fb-736">""</span><span class="sxs-lookup"><span data-stu-id="f71fb-736">""</span></span>                            |
| <span data-ttu-id="f71fb-737">最小系統</span><span class="sxs-lookup"><span data-stu-id="f71fb-737">Minimum system</span></span> | <span data-ttu-id="f71fb-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f71fb-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="f71fb-739">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f71fb-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71fb-740">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="f71fb-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
