---
description: 包含應用程式集合中每個未配置元件的物件。 未配置的元件無法利用 COM + 服務。 這些物件所公開的屬性會保存在元件層級所做的設定。
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: LegacyComponents 集合
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688764"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="dc2bc-105">LegacyComponents 集合</span><span class="sxs-lookup"><span data-stu-id="dc2bc-105">LegacyComponents collection</span></span>

<span data-ttu-id="dc2bc-106">包含應用程式集合中每個未配置元件的物件。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="dc2bc-107">未配置的元件無法利用 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="dc2bc-108">這些物件所公開的屬性會保存在元件層級所做的設定。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="dc2bc-109">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="dc2bc-110">若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="dc2bc-111">成員</span><span class="sxs-lookup"><span data-stu-id="dc2bc-111">Members</span></span>

<span data-ttu-id="dc2bc-112">**LegacyComponents** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="dc2bc-113">相關集合</span><span class="sxs-lookup"><span data-stu-id="dc2bc-113">Related Collections</span></span>

<span data-ttu-id="dc2bc-114">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="dc2bc-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="dc2bc-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc2bc-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="dc2bc-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="dc2bc-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="dc2bc-117">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="dc2bc-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="dc2bc-118">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="dc2bc-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="dc2bc-119">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="dc2bc-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="dc2bc-120">屬性</span><span class="sxs-lookup"><span data-stu-id="dc2bc-120">Properties</span></span>

<span data-ttu-id="dc2bc-121">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="dc2bc-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="dc2bc-122">Accesspermissions.list</span><span class="sxs-lookup"><span data-stu-id="dc2bc-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="dc2bc-123">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="dc2bc-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="dc2bc-124">AppID</span><span class="sxs-lookup"><span data-stu-id="dc2bc-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="dc2bc-125">AppName</span><span class="sxs-lookup"><span data-stu-id="dc2bc-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="dc2bc-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="dc2bc-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="dc2bc-127">位元</span><span class="sxs-lookup"><span data-stu-id="dc2bc-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="dc2bc-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="dc2bc-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="dc2bc-129">Clsid</span><span class="sxs-lookup"><span data-stu-id="dc2bc-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="dc2bc-130">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="dc2bc-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="dc2bc-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="dc2bc-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="dc2bc-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="dc2bc-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="dc2bc-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="dc2bc-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="dc2bc-134">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="dc2bc-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="dc2bc-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="dc2bc-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="dc2bc-136">LocalService</span><span class="sxs-lookup"><span data-stu-id="dc2bc-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="dc2bc-137">密碼</span><span class="sxs-lookup"><span data-stu-id="dc2bc-137">Password</span></span>](#password)
-   [<span data-ttu-id="dc2bc-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="dc2bc-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="dc2bc-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="dc2bc-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="dc2bc-140">Runas.exe</span><span class="sxs-lookup"><span data-stu-id="dc2bc-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="dc2bc-141">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="dc2bc-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="dc2bc-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="dc2bc-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="dc2bc-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="dc2bc-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="dc2bc-144">Accesspermissions.list</span><span class="sxs-lookup"><span data-stu-id="dc2bc-144">AccessPermissions</span></span>



| <span data-ttu-id="dc2bc-145">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-145">Entry</span></span> | <span data-ttu-id="dc2bc-146">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-147">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-147">Description</span></span>    | <span data-ttu-id="dc2bc-148">指定允許或拒絕存取元件的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="dc2bc-149">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-149">Access</span></span>         | <span data-ttu-id="dc2bc-150">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="dc2bc-151">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-151">Type</span></span>           | <span data-ttu-id="dc2bc-152">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-152">String</span></span>                                                                          |
| <span data-ttu-id="dc2bc-153">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-153">Default</span></span>        | <span data-ttu-id="dc2bc-154">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-154">N/A</span></span>                                                                             |
| <span data-ttu-id="dc2bc-155">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-155">Minimum system</span></span> | <span data-ttu-id="dc2bc-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="dc2bc-157">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="dc2bc-157">ActivateAtStorage</span></span>



| <span data-ttu-id="dc2bc-158">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-158">Entry</span></span> | <span data-ttu-id="dc2bc-159">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-160">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-160">Description</span></span>    | <span data-ttu-id="dc2bc-161">指定是否要在資料儲存體電腦上執行伺服器。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="dc2bc-162">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-162">Access</span></span>         | <span data-ttu-id="dc2bc-163">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="dc2bc-164">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-164">Type</span></span>           | <span data-ttu-id="dc2bc-165">字串可能的值： "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="dc2bc-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="dc2bc-166">預設</span><span class="sxs-lookup"><span data-stu-id="dc2bc-166">Default</span></span>        | <span data-ttu-id="dc2bc-167">"N"</span><span class="sxs-lookup"><span data-stu-id="dc2bc-167">"N"</span></span>                                                              |
| <span data-ttu-id="dc2bc-168">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-168">Minimum system</span></span> | <span data-ttu-id="dc2bc-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="dc2bc-170">AppID</span><span class="sxs-lookup"><span data-stu-id="dc2bc-170">AppID</span></span>



| <span data-ttu-id="dc2bc-171">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-171">Entry</span></span> | <span data-ttu-id="dc2bc-172">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="dc2bc-173">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-173">Description</span></span>    | <span data-ttu-id="dc2bc-174">應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-174">The application ID.</span></span> |
| <span data-ttu-id="dc2bc-175">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-175">Access</span></span>         | <span data-ttu-id="dc2bc-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-176">ReadOnly</span></span>            |
| <span data-ttu-id="dc2bc-177">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-177">Type</span></span>           | <span data-ttu-id="dc2bc-178">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-178">String</span></span>              |
| <span data-ttu-id="dc2bc-179">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-179">Default</span></span>        | <span data-ttu-id="dc2bc-180">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-180">N/A</span></span>                 |
| <span data-ttu-id="dc2bc-181">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-181">Minimum system</span></span> | <span data-ttu-id="dc2bc-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="dc2bc-183">AppName</span><span class="sxs-lookup"><span data-stu-id="dc2bc-183">AppName</span></span>



| <span data-ttu-id="dc2bc-184">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-184">Entry</span></span> | <span data-ttu-id="dc2bc-185">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="dc2bc-186">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-186">Description</span></span>    | <span data-ttu-id="dc2bc-187">應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-187">The name of the application.</span></span> |
| <span data-ttu-id="dc2bc-188">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-188">Access</span></span>         | <span data-ttu-id="dc2bc-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-189">ReadOnly</span></span>                     |
| <span data-ttu-id="dc2bc-190">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-190">Type</span></span>           | <span data-ttu-id="dc2bc-191">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-191">String</span></span>                       |
| <span data-ttu-id="dc2bc-192">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-192">Default</span></span>        | <span data-ttu-id="dc2bc-193">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-193">N/A</span></span>                          |
| <span data-ttu-id="dc2bc-194">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-194">Minimum system</span></span> | <span data-ttu-id="dc2bc-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="dc2bc-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="dc2bc-196">AuthenticationLevel</span></span>



| <span data-ttu-id="dc2bc-197">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-197">Entry</span></span> | <span data-ttu-id="dc2bc-198">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-199">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-199">Description</span></span>    | <span data-ttu-id="dc2bc-200">設定呼叫的驗證層級，其值會對應至遠端程序呼叫， (RPC) 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="dc2bc-201">選擇 COMAdminAuthenticationDefault 時，會使用 [**LocalComputer**](localcomputer.md) 集合內 DefaultAuthenticationLevel 屬性中的設定。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="dc2bc-202">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-202">Access</span></span>         | <span data-ttu-id="dc2bc-203">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="dc2bc-204">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-204">Type</span></span>           | <span data-ttu-id="dc2bc-205">長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) </span><span class="sxs-lookup"><span data-stu-id="dc2bc-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="dc2bc-206">預設</span><span class="sxs-lookup"><span data-stu-id="dc2bc-206">Default</span></span>        | <span data-ttu-id="dc2bc-207">COMAdminAuthenticationDefault (0) </span><span class="sxs-lookup"><span data-stu-id="dc2bc-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="dc2bc-208">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-208">Minimum system</span></span> | <span data-ttu-id="dc2bc-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="dc2bc-210">建議您在列舉中使用常數，而不要使用數值。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="dc2bc-211">位元</span><span class="sxs-lookup"><span data-stu-id="dc2bc-211">Bitness</span></span>



| <span data-ttu-id="dc2bc-212">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-212">Entry</span></span> | <span data-ttu-id="dc2bc-213">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-214">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-214">Description</span></span>    | <span data-ttu-id="dc2bc-215">表示元件的二進位位數類型。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="dc2bc-216">在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="dc2bc-217">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-217">Access</span></span>         | <span data-ttu-id="dc2bc-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="dc2bc-219">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-219">Type</span></span>           | <span data-ttu-id="dc2bc-220">很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2) </span><span class="sxs-lookup"><span data-stu-id="dc2bc-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="dc2bc-221">預設</span><span class="sxs-lookup"><span data-stu-id="dc2bc-221">Default</span></span>        | <span data-ttu-id="dc2bc-222">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="dc2bc-223">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-223">Minimum system</span></span> | <span data-ttu-id="dc2bc-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="dc2bc-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="dc2bc-225">ClassName</span></span>



| <span data-ttu-id="dc2bc-226">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-226">Entry</span></span> | <span data-ttu-id="dc2bc-227">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="dc2bc-228">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-228">Description</span></span>    | <span data-ttu-id="dc2bc-229">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-229">The name of the class.</span></span> |
| <span data-ttu-id="dc2bc-230">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-230">Access</span></span>         | <span data-ttu-id="dc2bc-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-231">ReadOnly</span></span>               |
| <span data-ttu-id="dc2bc-232">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-232">Type</span></span>           | <span data-ttu-id="dc2bc-233">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-233">String</span></span>                 |
| <span data-ttu-id="dc2bc-234">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-234">Default</span></span>        | <span data-ttu-id="dc2bc-235">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-235">N/A</span></span>                    |
| <span data-ttu-id="dc2bc-236">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-236">Minimum system</span></span> | <span data-ttu-id="dc2bc-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="dc2bc-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="dc2bc-238">CLSID</span></span>



| <span data-ttu-id="dc2bc-239">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-239">Entry</span></span> | <span data-ttu-id="dc2bc-240">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-241">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-241">Description</span></span>    | <span data-ttu-id="dc2bc-242">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-242">A GUID for the component.</span></span> <span data-ttu-id="dc2bc-243">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="dc2bc-244">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-244">Access</span></span>         | <span data-ttu-id="dc2bc-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="dc2bc-246">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-246">Type</span></span>           | <span data-ttu-id="dc2bc-247">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="dc2bc-248">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-248">Default</span></span>        | <span data-ttu-id="dc2bc-249">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="dc2bc-250">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-250">Minimum system</span></span> | <span data-ttu-id="dc2bc-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="dc2bc-252">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="dc2bc-252">DllSurrogate</span></span>



| <span data-ttu-id="dc2bc-253">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-253">Entry</span></span> | <span data-ttu-id="dc2bc-254">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="dc2bc-255">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-255">Description</span></span>    | <span data-ttu-id="dc2bc-256">指定 surragate 伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="dc2bc-257">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-257">Access</span></span>         | <span data-ttu-id="dc2bc-258">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="dc2bc-259">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-259">Type</span></span>           | <span data-ttu-id="dc2bc-260">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-260">String</span></span>                                                     |
| <span data-ttu-id="dc2bc-261">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-261">Default</span></span>        | <span data-ttu-id="dc2bc-262">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-262">N/A</span></span>                                                        |
| <span data-ttu-id="dc2bc-263">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-263">Minimum system</span></span> | <span data-ttu-id="dc2bc-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="dc2bc-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="dc2bc-265">InprocHandler32</span></span>



| <span data-ttu-id="dc2bc-266">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-266">Entry</span></span> | <span data-ttu-id="dc2bc-267">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-268">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-268">Description</span></span>    | <span data-ttu-id="dc2bc-269">指定32位同進程自訂處理常式 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="dc2bc-270">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-270">Access</span></span>         | <span data-ttu-id="dc2bc-271">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="dc2bc-272">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-272">Type</span></span>           | <span data-ttu-id="dc2bc-273">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-273">String</span></span>                                                             |
| <span data-ttu-id="dc2bc-274">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-274">Default</span></span>        | <span data-ttu-id="dc2bc-275">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-275">N/A</span></span>                                                                |
| <span data-ttu-id="dc2bc-276">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-276">Minimum system</span></span> | <span data-ttu-id="dc2bc-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="dc2bc-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="dc2bc-278">InprocServer32</span></span>



| <span data-ttu-id="dc2bc-279">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-279">Entry</span></span> | <span data-ttu-id="dc2bc-280">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="dc2bc-281">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-281">Description</span></span>    | <span data-ttu-id="dc2bc-282">指定32位同進程伺服器 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="dc2bc-283">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-283">Access</span></span>         | <span data-ttu-id="dc2bc-284">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="dc2bc-285">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-285">Type</span></span>           | <span data-ttu-id="dc2bc-286">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-286">String</span></span>                                                     |
| <span data-ttu-id="dc2bc-287">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-287">Default</span></span>        | <span data-ttu-id="dc2bc-288">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-288">N/A</span></span>                                                        |
| <span data-ttu-id="dc2bc-289">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-289">Minimum system</span></span> | <span data-ttu-id="dc2bc-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="dc2bc-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="dc2bc-291">IsEnabled</span></span>



| <span data-ttu-id="dc2bc-292">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-292">Entry</span></span> | <span data-ttu-id="dc2bc-293">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-294">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-294">Description</span></span>    | <span data-ttu-id="dc2bc-295">如果 COM + 應用程式或元件已停用，則 IsEnabled 為 False。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="dc2bc-296">如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="dc2bc-297">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-297">Access</span></span>         | <span data-ttu-id="dc2bc-298">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="dc2bc-299">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-299">Type</span></span>           | <span data-ttu-id="dc2bc-300">Bool</span><span class="sxs-lookup"><span data-stu-id="dc2bc-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="dc2bc-301">預設</span><span class="sxs-lookup"><span data-stu-id="dc2bc-301">Default</span></span>        | <span data-ttu-id="dc2bc-302">對</span><span class="sxs-lookup"><span data-stu-id="dc2bc-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="dc2bc-303">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-303">Minimum system</span></span> | <span data-ttu-id="dc2bc-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="dc2bc-305">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="dc2bc-305">LaunchPermissions</span></span>



| <span data-ttu-id="dc2bc-306">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-306">Entry</span></span> | <span data-ttu-id="dc2bc-307">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-308">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-308">Description</span></span>    | <span data-ttu-id="dc2bc-309">指定允許或拒絕啟動此元件之許可權的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="dc2bc-310">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-310">Access</span></span>         | <span data-ttu-id="dc2bc-311">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="dc2bc-312">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-312">Type</span></span>           | <span data-ttu-id="dc2bc-313">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-313">String</span></span>                                                                                 |
| <span data-ttu-id="dc2bc-314">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-314">Default</span></span>        | <span data-ttu-id="dc2bc-315">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="dc2bc-316">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-316">Minimum system</span></span> | <span data-ttu-id="dc2bc-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="dc2bc-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="dc2bc-318">LocalServer32</span></span>



| <span data-ttu-id="dc2bc-319">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-319">Entry</span></span> | <span data-ttu-id="dc2bc-320">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-321">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-321">Description</span></span>    | <span data-ttu-id="dc2bc-322">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="dc2bc-323">若要協助保護系統安全性，請在路徑中使用加上引號的字串，以指出可執行檔尾和引數的開始位置。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="dc2bc-324">例如，" \\ " C： \\ Program Files \\ Company files \\Application.exe\\ "param1 param2"。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="dc2bc-325">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-325">Access</span></span>         | <span data-ttu-id="dc2bc-326">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="dc2bc-327">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-327">Type</span></span>           | <span data-ttu-id="dc2bc-328">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="dc2bc-329">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-329">Default</span></span>        | <span data-ttu-id="dc2bc-330">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="dc2bc-331">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-331">Minimum system</span></span> | <span data-ttu-id="dc2bc-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="dc2bc-333">LocalService</span><span class="sxs-lookup"><span data-stu-id="dc2bc-333">LocalService</span></span>



| <span data-ttu-id="dc2bc-334">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-334">Entry</span></span> | <span data-ttu-id="dc2bc-335">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="dc2bc-336">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-336">Description</span></span>    | <span data-ttu-id="dc2bc-337">指定服務應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="dc2bc-338">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-338">Access</span></span>         | <span data-ttu-id="dc2bc-339">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="dc2bc-340">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-340">Type</span></span>           | <span data-ttu-id="dc2bc-341">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-341">String</span></span>                                              |
| <span data-ttu-id="dc2bc-342">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-342">Default</span></span>        | <span data-ttu-id="dc2bc-343">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-343">N/A</span></span>                                                 |
| <span data-ttu-id="dc2bc-344">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-344">Minimum system</span></span> | <span data-ttu-id="dc2bc-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="dc2bc-346">密碼</span><span class="sxs-lookup"><span data-stu-id="dc2bc-346">Password</span></span>



| <span data-ttu-id="dc2bc-347">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-347">Entry</span></span> | <span data-ttu-id="dc2bc-348">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-349">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-349">Description</span></span>    | <span data-ttu-id="dc2bc-350">設定伺服器進程在指定的 RunAs 身分識別下登入所使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="dc2bc-351">在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與 RunAs 身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="dc2bc-352">如果密碼和身分識別不同步，則必須等到系統管理員重設元件之後，才能啟動該元件。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="dc2bc-353">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-353">Access</span></span>         | <span data-ttu-id="dc2bc-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="dc2bc-355">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-355">Type</span></span>           | <span data-ttu-id="dc2bc-356">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="dc2bc-357">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-357">Default</span></span>        | <span data-ttu-id="dc2bc-358">NULL</span><span class="sxs-lookup"><span data-stu-id="dc2bc-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="dc2bc-359">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-359">Minimum system</span></span> | <span data-ttu-id="dc2bc-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="dc2bc-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="dc2bc-361">ProgID</span></span>



| <span data-ttu-id="dc2bc-362">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-362">Entry</span></span> | <span data-ttu-id="dc2bc-363">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-364">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-364">Description</span></span>    | <span data-ttu-id="dc2bc-365">識別元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-365">A name identifying the component.</span></span> <span data-ttu-id="dc2bc-366">在這個集合的物件上呼叫 Name 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="dc2bc-367">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-367">Access</span></span>         | <span data-ttu-id="dc2bc-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="dc2bc-369">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-369">Type</span></span>           | <span data-ttu-id="dc2bc-370">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="dc2bc-371">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-371">Default</span></span>        | <span data-ttu-id="dc2bc-372">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="dc2bc-373">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-373">Minimum system</span></span> | <span data-ttu-id="dc2bc-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="dc2bc-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="dc2bc-375">RemoteServer</span></span>



| <span data-ttu-id="dc2bc-376">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-376">Entry</span></span> | <span data-ttu-id="dc2bc-377">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="dc2bc-378">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-378">Description</span></span>    | <span data-ttu-id="dc2bc-379">指定遠端伺服器電腦。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="dc2bc-380">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-380">Access</span></span>         | <span data-ttu-id="dc2bc-381">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-381">ReadWrite</span></span>                             |
| <span data-ttu-id="dc2bc-382">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-382">Type</span></span>           | <span data-ttu-id="dc2bc-383">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-383">String</span></span>                                |
| <span data-ttu-id="dc2bc-384">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-384">Default</span></span>        | <span data-ttu-id="dc2bc-385">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-385">N/A</span></span>                                   |
| <span data-ttu-id="dc2bc-386">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-386">Minimum system</span></span> | <span data-ttu-id="dc2bc-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="dc2bc-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="dc2bc-388">RunAs</span></span>



| <span data-ttu-id="dc2bc-389">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-389">Entry</span></span> | <span data-ttu-id="dc2bc-390">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-391">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-391">Description</span></span>    | <span data-ttu-id="dc2bc-392">指定要在其上執行元件之身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="dc2bc-393">在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與 RunAs 身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="dc2bc-394">如果密碼和身分識別不同步，則必須等到系統管理員重設元件之後，才能啟動該元件。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="dc2bc-395">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-395">Access</span></span>         | <span data-ttu-id="dc2bc-396">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="dc2bc-397">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-397">Type</span></span>           | <span data-ttu-id="dc2bc-398">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="dc2bc-399">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-399">Default</span></span>        | <span data-ttu-id="dc2bc-400">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="dc2bc-401">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-401">Minimum system</span></span> | <span data-ttu-id="dc2bc-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="dc2bc-403">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="dc2bc-403">ServiceParameter</span></span>



| <span data-ttu-id="dc2bc-404">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-404">Entry</span></span> | <span data-ttu-id="dc2bc-405">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-406">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-406">Description</span></span>    | <span data-ttu-id="dc2bc-407">指定當叫用為服務應用程式時，傳遞給應用程式的參數。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="dc2bc-408">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-408">Access</span></span>         | <span data-ttu-id="dc2bc-409">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="dc2bc-410">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-410">Type</span></span>           | <span data-ttu-id="dc2bc-411">String</span><span class="sxs-lookup"><span data-stu-id="dc2bc-411">String</span></span>                                                                                    |
| <span data-ttu-id="dc2bc-412">預設值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-412">Default</span></span>        | <span data-ttu-id="dc2bc-413">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="dc2bc-414">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-414">Minimum system</span></span> | <span data-ttu-id="dc2bc-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="dc2bc-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="dc2bc-416">SRPTrustLevel</span></span>



| <span data-ttu-id="dc2bc-417">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-417">Entry</span></span> | <span data-ttu-id="dc2bc-418">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-419">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-419">Description</span></span>    | <span data-ttu-id="dc2bc-420">指出元件 (SRP) 信任層級的軟體限制原則。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="dc2bc-421">SRP 信任層級是指您願意提供給元件的信任層級。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="dc2bc-422">不受限制的 SRP 信任層級會對應到更安全的 \_ LEVELID \_ FULLYTRUSTED 列舉值，而不允許的 srp 信任層級則對應到安全性不 \_ 允許的 LEVELID \_ 列舉值。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="dc2bc-423">信任層級的列舉定義于 Winsafer 中。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="dc2bc-424">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-424">Access</span></span>         | <span data-ttu-id="dc2bc-425">讀寫</span><span class="sxs-lookup"><span data-stu-id="dc2bc-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="dc2bc-426">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-426">Type</span></span>           | <span data-ttu-id="dc2bc-427">較長的可能值：更安全的 \_ LEVELID 不 \_ 允許 (0X0) 更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000) </span><span class="sxs-lookup"><span data-stu-id="dc2bc-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="dc2bc-428">預設</span><span class="sxs-lookup"><span data-stu-id="dc2bc-428">Default</span></span>        | <span data-ttu-id="dc2bc-429">更安全的 \_ LEVELID \_ FULLYTRUSTED</span><span class="sxs-lookup"><span data-stu-id="dc2bc-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="dc2bc-430">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-430">Minimum system</span></span> | <span data-ttu-id="dc2bc-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="dc2bc-432">您願意信任但不受限制存取的元件應該附加最嚴格的安全性。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="dc2bc-433">不受限制的應用程式只能載入未受限制的元件，而不允許的應用程式無法執行，因此無法載入任何元件。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="dc2bc-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="dc2bc-434">ThreadingModel</span></span>



| <span data-ttu-id="dc2bc-435">進入</span><span class="sxs-lookup"><span data-stu-id="dc2bc-435">Entry</span></span> | <span data-ttu-id="dc2bc-436">值</span><span class="sxs-lookup"><span data-stu-id="dc2bc-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc2bc-437">描述</span><span class="sxs-lookup"><span data-stu-id="dc2bc-437">Description</span></span>    | <span data-ttu-id="dc2bc-438">決定如何將元件的實例指派給方法執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="dc2bc-439">值會對應至 COM 執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="dc2bc-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="dc2bc-440">Access</span><span class="sxs-lookup"><span data-stu-id="dc2bc-440">Access</span></span>         | <span data-ttu-id="dc2bc-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc2bc-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="dc2bc-442">類型</span><span class="sxs-lookup"><span data-stu-id="dc2bc-442">Type</span></span>           | <span data-ttu-id="dc2bc-443">長可能的值： COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) </span><span class="sxs-lookup"><span data-stu-id="dc2bc-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="dc2bc-444">預設</span><span class="sxs-lookup"><span data-stu-id="dc2bc-444">Default</span></span>        | <span data-ttu-id="dc2bc-445">N/A</span><span class="sxs-lookup"><span data-stu-id="dc2bc-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="dc2bc-446">最小系統</span><span class="sxs-lookup"><span data-stu-id="dc2bc-446">Minimum system</span></span> | <span data-ttu-id="dc2bc-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc2bc-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="dc2bc-448">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc2bc-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2bc-449">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="dc2bc-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
