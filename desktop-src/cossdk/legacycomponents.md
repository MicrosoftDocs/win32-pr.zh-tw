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
# <a name="legacycomponents-collection"></a><span data-ttu-id="b5279-105">LegacyComponents 集合</span><span class="sxs-lookup"><span data-stu-id="b5279-105">LegacyComponents collection</span></span>

<span data-ttu-id="b5279-106">包含應用程式集合中每個未配置元件的物件。</span><span class="sxs-lookup"><span data-stu-id="b5279-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="b5279-107">未配置的元件無法利用 COM + 服務。</span><span class="sxs-lookup"><span data-stu-id="b5279-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="b5279-108">這些物件所公開的屬性會保存在元件層級所做的設定。</span><span class="sxs-lookup"><span data-stu-id="b5279-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="b5279-109">此集合支援 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove)方法，但不支援 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法。</span><span class="sxs-lookup"><span data-stu-id="b5279-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="b5279-110">若要安裝或匯入元件到應用程式，請在 [**COMAdminCatalog**](comadmincatalog.md) 物件上使用方法。</span><span class="sxs-lookup"><span data-stu-id="b5279-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b5279-111">成員</span><span class="sxs-lookup"><span data-stu-id="b5279-111">Members</span></span>

<span data-ttu-id="b5279-112">**LegacyComponents** 集合繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="b5279-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b5279-113">相關集合</span><span class="sxs-lookup"><span data-stu-id="b5279-113">Related Collections</span></span>

<span data-ttu-id="b5279-114">您可以從這個集合流覽至下列任何集合：</span><span class="sxs-lookup"><span data-stu-id="b5279-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b5279-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b5279-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b5279-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b5279-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b5279-117">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="b5279-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b5279-118">您可以從下列集合流覽至這個集合：</span><span class="sxs-lookup"><span data-stu-id="b5279-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b5279-119">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="b5279-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="b5279-120">屬性</span><span class="sxs-lookup"><span data-stu-id="b5279-120">Properties</span></span>

<span data-ttu-id="b5279-121">集合內的 [**COMAdminCatalogObject**](comadmincatalogobject.md) 物件支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b5279-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b5279-122">Accesspermissions.list</span><span class="sxs-lookup"><span data-stu-id="b5279-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="b5279-123">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="b5279-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="b5279-124">AppID</span><span class="sxs-lookup"><span data-stu-id="b5279-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="b5279-125">AppName</span><span class="sxs-lookup"><span data-stu-id="b5279-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="b5279-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="b5279-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="b5279-127">位元</span><span class="sxs-lookup"><span data-stu-id="b5279-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="b5279-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="b5279-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="b5279-129">Clsid</span><span class="sxs-lookup"><span data-stu-id="b5279-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="b5279-130">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="b5279-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="b5279-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="b5279-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="b5279-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b5279-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="b5279-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b5279-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="b5279-134">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="b5279-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="b5279-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b5279-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="b5279-136">LocalService</span><span class="sxs-lookup"><span data-stu-id="b5279-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="b5279-137">密碼</span><span class="sxs-lookup"><span data-stu-id="b5279-137">Password</span></span>](#password)
-   [<span data-ttu-id="b5279-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="b5279-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="b5279-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="b5279-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="b5279-140">Runas.exe</span><span class="sxs-lookup"><span data-stu-id="b5279-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="b5279-141">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="b5279-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="b5279-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="b5279-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="b5279-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="b5279-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="b5279-144">Accesspermissions.list</span><span class="sxs-lookup"><span data-stu-id="b5279-144">AccessPermissions</span></span>



| <span data-ttu-id="b5279-145">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-145">Entry</span></span> | <span data-ttu-id="b5279-146">值</span><span class="sxs-lookup"><span data-stu-id="b5279-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-147">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-147">Description</span></span>    | <span data-ttu-id="b5279-148">指定允許或拒絕存取元件的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5279-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="b5279-149">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-149">Access</span></span>         | <span data-ttu-id="b5279-150">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="b5279-151">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-151">Type</span></span>           | <span data-ttu-id="b5279-152">String</span><span class="sxs-lookup"><span data-stu-id="b5279-152">String</span></span>                                                                          |
| <span data-ttu-id="b5279-153">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-153">Default</span></span>        | <span data-ttu-id="b5279-154">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-154">N/A</span></span>                                                                             |
| <span data-ttu-id="b5279-155">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-155">Minimum system</span></span> | <span data-ttu-id="b5279-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="b5279-157">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="b5279-157">ActivateAtStorage</span></span>



| <span data-ttu-id="b5279-158">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-158">Entry</span></span> | <span data-ttu-id="b5279-159">值</span><span class="sxs-lookup"><span data-stu-id="b5279-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="b5279-160">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-160">Description</span></span>    | <span data-ttu-id="b5279-161">指定是否要在資料儲存體電腦上執行伺服器。</span><span class="sxs-lookup"><span data-stu-id="b5279-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="b5279-162">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-162">Access</span></span>         | <span data-ttu-id="b5279-163">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="b5279-164">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-164">Type</span></span>           | <span data-ttu-id="b5279-165">字串可能的值： "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="b5279-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="b5279-166">預設</span><span class="sxs-lookup"><span data-stu-id="b5279-166">Default</span></span>        | <span data-ttu-id="b5279-167">"N"</span><span class="sxs-lookup"><span data-stu-id="b5279-167">"N"</span></span>                                                              |
| <span data-ttu-id="b5279-168">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-168">Minimum system</span></span> | <span data-ttu-id="b5279-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="b5279-170">AppID</span><span class="sxs-lookup"><span data-stu-id="b5279-170">AppID</span></span>



| <span data-ttu-id="b5279-171">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-171">Entry</span></span> | <span data-ttu-id="b5279-172">值</span><span class="sxs-lookup"><span data-stu-id="b5279-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="b5279-173">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-173">Description</span></span>    | <span data-ttu-id="b5279-174">應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5279-174">The application ID.</span></span> |
| <span data-ttu-id="b5279-175">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-175">Access</span></span>         | <span data-ttu-id="b5279-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-176">ReadOnly</span></span>            |
| <span data-ttu-id="b5279-177">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-177">Type</span></span>           | <span data-ttu-id="b5279-178">String</span><span class="sxs-lookup"><span data-stu-id="b5279-178">String</span></span>              |
| <span data-ttu-id="b5279-179">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-179">Default</span></span>        | <span data-ttu-id="b5279-180">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-180">N/A</span></span>                 |
| <span data-ttu-id="b5279-181">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-181">Minimum system</span></span> | <span data-ttu-id="b5279-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="b5279-183">AppName</span><span class="sxs-lookup"><span data-stu-id="b5279-183">AppName</span></span>



| <span data-ttu-id="b5279-184">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-184">Entry</span></span> | <span data-ttu-id="b5279-185">值</span><span class="sxs-lookup"><span data-stu-id="b5279-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="b5279-186">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-186">Description</span></span>    | <span data-ttu-id="b5279-187">應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5279-187">The name of the application.</span></span> |
| <span data-ttu-id="b5279-188">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-188">Access</span></span>         | <span data-ttu-id="b5279-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-189">ReadOnly</span></span>                     |
| <span data-ttu-id="b5279-190">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-190">Type</span></span>           | <span data-ttu-id="b5279-191">String</span><span class="sxs-lookup"><span data-stu-id="b5279-191">String</span></span>                       |
| <span data-ttu-id="b5279-192">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-192">Default</span></span>        | <span data-ttu-id="b5279-193">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-193">N/A</span></span>                          |
| <span data-ttu-id="b5279-194">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-194">Minimum system</span></span> | <span data-ttu-id="b5279-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="b5279-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="b5279-196">AuthenticationLevel</span></span>



| <span data-ttu-id="b5279-197">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-197">Entry</span></span> | <span data-ttu-id="b5279-198">值</span><span class="sxs-lookup"><span data-stu-id="b5279-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-199">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-199">Description</span></span>    | <span data-ttu-id="b5279-200">設定呼叫的驗證層級，其值會對應至遠端程序呼叫， (RPC) 驗證設定。</span><span class="sxs-lookup"><span data-stu-id="b5279-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="b5279-201">選擇 COMAdminAuthenticationDefault 時，會使用 [**LocalComputer**](localcomputer.md) 集合內 DefaultAuthenticationLevel 屬性中的設定。</span><span class="sxs-lookup"><span data-stu-id="b5279-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="b5279-202">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-202">Access</span></span>         | <span data-ttu-id="b5279-203">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b5279-204">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-204">Type</span></span>           | <span data-ttu-id="b5279-205">長可能的值： COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) </span><span class="sxs-lookup"><span data-stu-id="b5279-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="b5279-206">預設</span><span class="sxs-lookup"><span data-stu-id="b5279-206">Default</span></span>        | <span data-ttu-id="b5279-207">COMAdminAuthenticationDefault (0) </span><span class="sxs-lookup"><span data-stu-id="b5279-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b5279-208">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-208">Minimum system</span></span> | <span data-ttu-id="b5279-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="b5279-210">建議您在列舉中使用常數，而不要使用數值。</span><span class="sxs-lookup"><span data-stu-id="b5279-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="b5279-211">位元</span><span class="sxs-lookup"><span data-stu-id="b5279-211">Bitness</span></span>



| <span data-ttu-id="b5279-212">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-212">Entry</span></span> | <span data-ttu-id="b5279-213">值</span><span class="sxs-lookup"><span data-stu-id="b5279-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-214">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-214">Description</span></span>    | <span data-ttu-id="b5279-215">表示元件的二進位位數類型。</span><span class="sxs-lookup"><span data-stu-id="b5279-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="b5279-216">在使用64位 Windows 的系統上，這個屬性會區分64位元件與32位元件。</span><span class="sxs-lookup"><span data-stu-id="b5279-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="b5279-217">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-217">Access</span></span>         | <span data-ttu-id="b5279-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="b5279-219">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-219">Type</span></span>           | <span data-ttu-id="b5279-220">很長可能的值： COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2) </span><span class="sxs-lookup"><span data-stu-id="b5279-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="b5279-221">預設</span><span class="sxs-lookup"><span data-stu-id="b5279-221">Default</span></span>        | <span data-ttu-id="b5279-222">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b5279-223">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-223">Minimum system</span></span> | <span data-ttu-id="b5279-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="b5279-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="b5279-225">ClassName</span></span>



| <span data-ttu-id="b5279-226">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-226">Entry</span></span> | <span data-ttu-id="b5279-227">值</span><span class="sxs-lookup"><span data-stu-id="b5279-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="b5279-228">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-228">Description</span></span>    | <span data-ttu-id="b5279-229">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5279-229">The name of the class.</span></span> |
| <span data-ttu-id="b5279-230">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-230">Access</span></span>         | <span data-ttu-id="b5279-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-231">ReadOnly</span></span>               |
| <span data-ttu-id="b5279-232">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-232">Type</span></span>           | <span data-ttu-id="b5279-233">String</span><span class="sxs-lookup"><span data-stu-id="b5279-233">String</span></span>                 |
| <span data-ttu-id="b5279-234">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-234">Default</span></span>        | <span data-ttu-id="b5279-235">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-235">N/A</span></span>                    |
| <span data-ttu-id="b5279-236">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-236">Minimum system</span></span> | <span data-ttu-id="b5279-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="b5279-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="b5279-238">CLSID</span></span>



| <span data-ttu-id="b5279-239">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-239">Entry</span></span> | <span data-ttu-id="b5279-240">值</span><span class="sxs-lookup"><span data-stu-id="b5279-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-241">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-241">Description</span></span>    | <span data-ttu-id="b5279-242">元件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b5279-242">A GUID for the component.</span></span> <span data-ttu-id="b5279-243">當在此集合的物件上呼叫索引 [**鍵**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b5279-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b5279-244">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-244">Access</span></span>         | <span data-ttu-id="b5279-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="b5279-246">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-246">Type</span></span>           | <span data-ttu-id="b5279-247">String</span><span class="sxs-lookup"><span data-stu-id="b5279-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="b5279-248">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-248">Default</span></span>        | <span data-ttu-id="b5279-249">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="b5279-250">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-250">Minimum system</span></span> | <span data-ttu-id="b5279-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="b5279-252">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="b5279-252">DllSurrogate</span></span>



| <span data-ttu-id="b5279-253">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-253">Entry</span></span> | <span data-ttu-id="b5279-254">值</span><span class="sxs-lookup"><span data-stu-id="b5279-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="b5279-255">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-255">Description</span></span>    | <span data-ttu-id="b5279-256">指定 surragate 伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b5279-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="b5279-257">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-257">Access</span></span>         | <span data-ttu-id="b5279-258">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="b5279-259">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-259">Type</span></span>           | <span data-ttu-id="b5279-260">String</span><span class="sxs-lookup"><span data-stu-id="b5279-260">String</span></span>                                                     |
| <span data-ttu-id="b5279-261">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-261">Default</span></span>        | <span data-ttu-id="b5279-262">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-262">N/A</span></span>                                                        |
| <span data-ttu-id="b5279-263">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-263">Minimum system</span></span> | <span data-ttu-id="b5279-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="b5279-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="b5279-265">InprocHandler32</span></span>



| <span data-ttu-id="b5279-266">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-266">Entry</span></span> | <span data-ttu-id="b5279-267">值</span><span class="sxs-lookup"><span data-stu-id="b5279-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="b5279-268">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-268">Description</span></span>    | <span data-ttu-id="b5279-269">指定32位同進程自訂處理常式 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b5279-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="b5279-270">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-270">Access</span></span>         | <span data-ttu-id="b5279-271">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="b5279-272">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-272">Type</span></span>           | <span data-ttu-id="b5279-273">String</span><span class="sxs-lookup"><span data-stu-id="b5279-273">String</span></span>                                                             |
| <span data-ttu-id="b5279-274">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-274">Default</span></span>        | <span data-ttu-id="b5279-275">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-275">N/A</span></span>                                                                |
| <span data-ttu-id="b5279-276">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-276">Minimum system</span></span> | <span data-ttu-id="b5279-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="b5279-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="b5279-278">InprocServer32</span></span>



| <span data-ttu-id="b5279-279">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-279">Entry</span></span> | <span data-ttu-id="b5279-280">值</span><span class="sxs-lookup"><span data-stu-id="b5279-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="b5279-281">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-281">Description</span></span>    | <span data-ttu-id="b5279-282">指定32位同進程伺服器 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b5279-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="b5279-283">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-283">Access</span></span>         | <span data-ttu-id="b5279-284">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="b5279-285">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-285">Type</span></span>           | <span data-ttu-id="b5279-286">String</span><span class="sxs-lookup"><span data-stu-id="b5279-286">String</span></span>                                                     |
| <span data-ttu-id="b5279-287">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-287">Default</span></span>        | <span data-ttu-id="b5279-288">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-288">N/A</span></span>                                                        |
| <span data-ttu-id="b5279-289">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-289">Minimum system</span></span> | <span data-ttu-id="b5279-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="b5279-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b5279-291">IsEnabled</span></span>



| <span data-ttu-id="b5279-292">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-292">Entry</span></span> | <span data-ttu-id="b5279-293">值</span><span class="sxs-lookup"><span data-stu-id="b5279-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-294">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-294">Description</span></span>    | <span data-ttu-id="b5279-295">如果 COM + 應用程式或元件已停用，則 IsEnabled 為 False。</span><span class="sxs-lookup"><span data-stu-id="b5279-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="b5279-296">如果已啟用 COM + 應用程式或元件，IsEnabled 為 True。</span><span class="sxs-lookup"><span data-stu-id="b5279-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="b5279-297">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-297">Access</span></span>         | <span data-ttu-id="b5279-298">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="b5279-299">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-299">Type</span></span>           | <span data-ttu-id="b5279-300">Bool</span><span class="sxs-lookup"><span data-stu-id="b5279-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="b5279-301">預設</span><span class="sxs-lookup"><span data-stu-id="b5279-301">Default</span></span>        | <span data-ttu-id="b5279-302">對</span><span class="sxs-lookup"><span data-stu-id="b5279-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="b5279-303">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-303">Minimum system</span></span> | <span data-ttu-id="b5279-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="b5279-305">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="b5279-305">LaunchPermissions</span></span>



| <span data-ttu-id="b5279-306">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-306">Entry</span></span> | <span data-ttu-id="b5279-307">值</span><span class="sxs-lookup"><span data-stu-id="b5279-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-308">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-308">Description</span></span>    | <span data-ttu-id="b5279-309">指定允許或拒絕啟動此元件之許可權的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5279-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="b5279-310">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-310">Access</span></span>         | <span data-ttu-id="b5279-311">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="b5279-312">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-312">Type</span></span>           | <span data-ttu-id="b5279-313">String</span><span class="sxs-lookup"><span data-stu-id="b5279-313">String</span></span>                                                                                 |
| <span data-ttu-id="b5279-314">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-314">Default</span></span>        | <span data-ttu-id="b5279-315">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="b5279-316">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-316">Minimum system</span></span> | <span data-ttu-id="b5279-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="b5279-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b5279-318">LocalServer32</span></span>



| <span data-ttu-id="b5279-319">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-319">Entry</span></span> | <span data-ttu-id="b5279-320">值</span><span class="sxs-lookup"><span data-stu-id="b5279-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-321">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-321">Description</span></span>    | <span data-ttu-id="b5279-322">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b5279-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="b5279-323">若要協助保護系統安全性，請在路徑中使用加上引號的字串，以指出可執行檔尾和引數的開始位置。</span><span class="sxs-lookup"><span data-stu-id="b5279-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="b5279-324">例如，" \\ " C： \\ Program Files \\ Company files \\Application.exe\\ "param1 param2"。</span><span class="sxs-lookup"><span data-stu-id="b5279-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="b5279-325">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-325">Access</span></span>         | <span data-ttu-id="b5279-326">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b5279-327">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-327">Type</span></span>           | <span data-ttu-id="b5279-328">String</span><span class="sxs-lookup"><span data-stu-id="b5279-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b5279-329">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-329">Default</span></span>        | <span data-ttu-id="b5279-330">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b5279-331">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-331">Minimum system</span></span> | <span data-ttu-id="b5279-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="b5279-333">LocalService</span><span class="sxs-lookup"><span data-stu-id="b5279-333">LocalService</span></span>



| <span data-ttu-id="b5279-334">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-334">Entry</span></span> | <span data-ttu-id="b5279-335">值</span><span class="sxs-lookup"><span data-stu-id="b5279-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="b5279-336">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-336">Description</span></span>    | <span data-ttu-id="b5279-337">指定服務應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b5279-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="b5279-338">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-338">Access</span></span>         | <span data-ttu-id="b5279-339">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="b5279-340">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-340">Type</span></span>           | <span data-ttu-id="b5279-341">String</span><span class="sxs-lookup"><span data-stu-id="b5279-341">String</span></span>                                              |
| <span data-ttu-id="b5279-342">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-342">Default</span></span>        | <span data-ttu-id="b5279-343">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-343">N/A</span></span>                                                 |
| <span data-ttu-id="b5279-344">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-344">Minimum system</span></span> | <span data-ttu-id="b5279-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="b5279-346">密碼</span><span class="sxs-lookup"><span data-stu-id="b5279-346">Password</span></span>



| <span data-ttu-id="b5279-347">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-347">Entry</span></span> | <span data-ttu-id="b5279-348">值</span><span class="sxs-lookup"><span data-stu-id="b5279-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-349">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-349">Description</span></span>    | <span data-ttu-id="b5279-350">設定伺服器進程在指定的 RunAs 身分識別下登入所使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="b5279-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="b5279-351">在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與 RunAs 身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b5279-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="b5279-352">如果密碼和身分識別不同步，則必須等到系統管理員重設元件之後，才能啟動該元件。</span><span class="sxs-lookup"><span data-stu-id="b5279-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="b5279-353">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-353">Access</span></span>         | <span data-ttu-id="b5279-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b5279-355">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-355">Type</span></span>           | <span data-ttu-id="b5279-356">String</span><span class="sxs-lookup"><span data-stu-id="b5279-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="b5279-357">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-357">Default</span></span>        | <span data-ttu-id="b5279-358">NULL</span><span class="sxs-lookup"><span data-stu-id="b5279-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b5279-359">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-359">Minimum system</span></span> | <span data-ttu-id="b5279-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="b5279-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="b5279-361">ProgID</span></span>



| <span data-ttu-id="b5279-362">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-362">Entry</span></span> | <span data-ttu-id="b5279-363">值</span><span class="sxs-lookup"><span data-stu-id="b5279-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-364">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-364">Description</span></span>    | <span data-ttu-id="b5279-365">識別元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5279-365">A name identifying the component.</span></span> <span data-ttu-id="b5279-366">在這個集合的物件上呼叫 Name 屬性方法時，就會傳回這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b5279-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b5279-367">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-367">Access</span></span>         | <span data-ttu-id="b5279-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="b5279-369">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-369">Type</span></span>           | <span data-ttu-id="b5279-370">String</span><span class="sxs-lookup"><span data-stu-id="b5279-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="b5279-371">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-371">Default</span></span>        | <span data-ttu-id="b5279-372">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="b5279-373">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-373">Minimum system</span></span> | <span data-ttu-id="b5279-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="b5279-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="b5279-375">RemoteServer</span></span>



| <span data-ttu-id="b5279-376">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-376">Entry</span></span> | <span data-ttu-id="b5279-377">值</span><span class="sxs-lookup"><span data-stu-id="b5279-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="b5279-378">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-378">Description</span></span>    | <span data-ttu-id="b5279-379">指定遠端伺服器電腦。</span><span class="sxs-lookup"><span data-stu-id="b5279-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="b5279-380">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-380">Access</span></span>         | <span data-ttu-id="b5279-381">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-381">ReadWrite</span></span>                             |
| <span data-ttu-id="b5279-382">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-382">Type</span></span>           | <span data-ttu-id="b5279-383">String</span><span class="sxs-lookup"><span data-stu-id="b5279-383">String</span></span>                                |
| <span data-ttu-id="b5279-384">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-384">Default</span></span>        | <span data-ttu-id="b5279-385">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-385">N/A</span></span>                                   |
| <span data-ttu-id="b5279-386">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-386">Minimum system</span></span> | <span data-ttu-id="b5279-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="b5279-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="b5279-388">RunAs</span></span>



| <span data-ttu-id="b5279-389">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-389">Entry</span></span> | <span data-ttu-id="b5279-390">值</span><span class="sxs-lookup"><span data-stu-id="b5279-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-391">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-391">Description</span></span>    | <span data-ttu-id="b5279-392">指定要在其上執行元件之身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="b5279-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="b5279-393">在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前，密碼應該與 RunAs 身分識別同時設定，因為密碼和身分識別會在儲存之前進行驗證。</span><span class="sxs-lookup"><span data-stu-id="b5279-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="b5279-394">如果密碼和身分識別不同步，則必須等到系統管理員重設元件之後，才能啟動該元件。</span><span class="sxs-lookup"><span data-stu-id="b5279-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="b5279-395">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-395">Access</span></span>         | <span data-ttu-id="b5279-396">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b5279-397">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-397">Type</span></span>           | <span data-ttu-id="b5279-398">String</span><span class="sxs-lookup"><span data-stu-id="b5279-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="b5279-399">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-399">Default</span></span>        | <span data-ttu-id="b5279-400">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b5279-401">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-401">Minimum system</span></span> | <span data-ttu-id="b5279-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="b5279-403">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="b5279-403">ServiceParameter</span></span>



| <span data-ttu-id="b5279-404">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-404">Entry</span></span> | <span data-ttu-id="b5279-405">值</span><span class="sxs-lookup"><span data-stu-id="b5279-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-406">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-406">Description</span></span>    | <span data-ttu-id="b5279-407">指定當叫用為服務應用程式時，傳遞給應用程式的參數。</span><span class="sxs-lookup"><span data-stu-id="b5279-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="b5279-408">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-408">Access</span></span>         | <span data-ttu-id="b5279-409">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="b5279-410">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-410">Type</span></span>           | <span data-ttu-id="b5279-411">String</span><span class="sxs-lookup"><span data-stu-id="b5279-411">String</span></span>                                                                                    |
| <span data-ttu-id="b5279-412">預設值</span><span class="sxs-lookup"><span data-stu-id="b5279-412">Default</span></span>        | <span data-ttu-id="b5279-413">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="b5279-414">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-414">Minimum system</span></span> | <span data-ttu-id="b5279-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="b5279-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="b5279-416">SRPTrustLevel</span></span>



| <span data-ttu-id="b5279-417">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-417">Entry</span></span> | <span data-ttu-id="b5279-418">值</span><span class="sxs-lookup"><span data-stu-id="b5279-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-419">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-419">Description</span></span>    | <span data-ttu-id="b5279-420">指出元件 (SRP) 信任層級的軟體限制原則。</span><span class="sxs-lookup"><span data-stu-id="b5279-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="b5279-421">SRP 信任層級是指您願意提供給元件的信任層級。</span><span class="sxs-lookup"><span data-stu-id="b5279-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="b5279-422">不受限制的 SRP 信任層級會對應到更安全的 \_ LEVELID \_ FULLYTRUSTED 列舉值，而不允許的 srp 信任層級則對應到安全性不 \_ 允許的 LEVELID \_ 列舉值。</span><span class="sxs-lookup"><span data-stu-id="b5279-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="b5279-423">信任層級的列舉定義于 Winsafer 中。</span><span class="sxs-lookup"><span data-stu-id="b5279-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="b5279-424">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-424">Access</span></span>         | <span data-ttu-id="b5279-425">讀寫</span><span class="sxs-lookup"><span data-stu-id="b5279-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b5279-426">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-426">Type</span></span>           | <span data-ttu-id="b5279-427">較長的可能值：更安全的 \_ LEVELID 不 \_ 允許 (0X0) 更安全的 \_ LEVELID \_ FULLYTRUSTED (0x40000) </span><span class="sxs-lookup"><span data-stu-id="b5279-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b5279-428">預設</span><span class="sxs-lookup"><span data-stu-id="b5279-428">Default</span></span>        | <span data-ttu-id="b5279-429">更安全的 \_ LEVELID \_ FULLYTRUSTED</span><span class="sxs-lookup"><span data-stu-id="b5279-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b5279-430">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-430">Minimum system</span></span> | <span data-ttu-id="b5279-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="b5279-432">您願意信任但不受限制存取的元件應該附加最嚴格的安全性。</span><span class="sxs-lookup"><span data-stu-id="b5279-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="b5279-433">不受限制的應用程式只能載入未受限制的元件，而不允許的應用程式無法執行，因此無法載入任何元件。</span><span class="sxs-lookup"><span data-stu-id="b5279-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="b5279-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="b5279-434">ThreadingModel</span></span>



| <span data-ttu-id="b5279-435">進入</span><span class="sxs-lookup"><span data-stu-id="b5279-435">Entry</span></span> | <span data-ttu-id="b5279-436">值</span><span class="sxs-lookup"><span data-stu-id="b5279-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5279-437">描述</span><span class="sxs-lookup"><span data-stu-id="b5279-437">Description</span></span>    | <span data-ttu-id="b5279-438">決定如何將元件的實例指派給方法執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="b5279-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="b5279-439">值會對應至 COM 執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="b5279-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="b5279-440">Access</span><span class="sxs-lookup"><span data-stu-id="b5279-440">Access</span></span>         | <span data-ttu-id="b5279-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5279-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="b5279-442">類型</span><span class="sxs-lookup"><span data-stu-id="b5279-442">Type</span></span>           | <span data-ttu-id="b5279-443">長可能的值： COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) </span><span class="sxs-lookup"><span data-stu-id="b5279-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="b5279-444">預設</span><span class="sxs-lookup"><span data-stu-id="b5279-444">Default</span></span>        | <span data-ttu-id="b5279-445">N/A</span><span class="sxs-lookup"><span data-stu-id="b5279-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="b5279-446">最小系統</span><span class="sxs-lookup"><span data-stu-id="b5279-446">Minimum system</span></span> | <span data-ttu-id="b5279-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5279-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="b5279-448">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5279-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5279-449">COM + 系統管理集合</span><span class="sxs-lookup"><span data-stu-id="b5279-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
