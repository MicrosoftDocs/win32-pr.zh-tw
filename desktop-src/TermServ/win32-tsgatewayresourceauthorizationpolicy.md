---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別
description: 描述 (RD \ 160; 的遠端桌面資源授權原則。RAP) 。 RD \ 160;RAP 用來決定是否授權使用者透過遠端桌面閘道 (RD 閘道) 連接到指定的資源。
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025018"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="9341d-106">Win32 \_ TSGatewayResourceAuthorizationPolicy 類別</span><span class="sxs-lookup"><span data-stu-id="9341d-106">Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="9341d-107">描述 (RD RAP) 的遠端桌面資源授權原則。</span><span class="sxs-lookup"><span data-stu-id="9341d-107">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="9341d-108">RD RAP 用來決定是否授權使用者透過遠端桌面閘道 (RD 閘道) 連接到指定的資源。</span><span class="sxs-lookup"><span data-stu-id="9341d-108">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="9341d-109">語法</span><span class="sxs-lookup"><span data-stu-id="9341d-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a><span data-ttu-id="9341d-110">成員</span><span class="sxs-lookup"><span data-stu-id="9341d-110">Members</span></span>

<span data-ttu-id="9341d-111">**Win32 \_ TSGatewayResourceAuthorizationPolicy** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9341d-111">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these types of members:</span></span>

-   [<span data-ttu-id="9341d-112">方法</span><span class="sxs-lookup"><span data-stu-id="9341d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9341d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9341d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9341d-114">方法</span><span class="sxs-lookup"><span data-stu-id="9341d-114">Methods</span></span>

<span data-ttu-id="9341d-115">**Win32 \_ TSGatewayResourceAuthorizationPolicy** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9341d-115">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these methods.</span></span>



| <span data-ttu-id="9341d-116">方法</span><span class="sxs-lookup"><span data-stu-id="9341d-116">Method</span></span>                                                                                          | <span data-ttu-id="9341d-117">描述</span><span class="sxs-lookup"><span data-stu-id="9341d-117">Description</span></span>                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9341d-118">**AddUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="9341d-118">**AddUserGroupNames**</span></span>](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="9341d-119">將指定的使用者組名加入至 **UserGroupNames** 屬性中的現有使用者群組。</span><span class="sxs-lookup"><span data-stu-id="9341d-119">Adds the specified user group names to the existing user groups in the **UserGroupNames** property.</span></span><br/>      |
| [<span data-ttu-id="9341d-120">**建立**</span><span class="sxs-lookup"><span data-stu-id="9341d-120">**Create**</span></span>](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="9341d-121">建立 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="9341d-121">Creates an RD RAP.</span></span><br/>                                                                                       |
| [<span data-ttu-id="9341d-122">**刪除**</span><span class="sxs-lookup"><span data-stu-id="9341d-122">**Delete**</span></span>](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="9341d-123">刪除目前的 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="9341d-123">Deletes the current RD RAP.</span></span><br/>                                                                              |
| [<span data-ttu-id="9341d-124">**RemoveUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="9341d-124">**RemoveUserGroupNames**</span></span>](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | <span data-ttu-id="9341d-125">從 **UserGroupNames** 屬性中的現有使用者群組中移除指定的使用者組名。</span><span class="sxs-lookup"><span data-stu-id="9341d-125">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span><br/> |
| [<span data-ttu-id="9341d-126">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="9341d-126">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="9341d-127">設定 RD RAP 的 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9341d-127">Sets the **Description** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="9341d-128">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="9341d-128">**SetEnabled**</span></span>](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | <span data-ttu-id="9341d-129">藉由設定 **Enabled** 屬性來啟用或停用 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="9341d-129">Enables or disables the RD RAP by setting the **Enabled** property.</span></span><br/>                                      |
| [<span data-ttu-id="9341d-130">**SetName**</span><span class="sxs-lookup"><span data-stu-id="9341d-130">**SetName**</span></span>](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | <span data-ttu-id="9341d-131">設定 RD RAP 的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9341d-131">Sets the **Name** property for the RD RAP.</span></span><br/>                                                               |
| [<span data-ttu-id="9341d-132">**SetPortNumbers**</span><span class="sxs-lookup"><span data-stu-id="9341d-132">**SetPortNumbers**</span></span>](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | <span data-ttu-id="9341d-133">設定 RD RAP 的 **PortNumbers** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9341d-133">Sets the **PortNumbers** property for the RD RAP.</span></span><br/>                                                        |
| [<span data-ttu-id="9341d-134">**SetResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="9341d-134">**SetResourceGroup**</span></span>](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | <span data-ttu-id="9341d-135">設定 **ResourceGroupType** 和 **ResourceGroupName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9341d-135">Sets the **ResourceGroupType** and **ResourceGroupName** properties.</span></span><br/>                                     |
| [<span data-ttu-id="9341d-136">**SetUserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="9341d-136">**SetUserGroupNames**</span></span>](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | <span data-ttu-id="9341d-137">設定 RD RAP 的 **UserGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9341d-137">Sets the **UserGroupNames** property for the RD RAP.</span></span><br/>                                                     |
| [<span data-ttu-id="9341d-138">**更新**</span><span class="sxs-lookup"><span data-stu-id="9341d-138">**Update**</span></span>](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | <span data-ttu-id="9341d-139">更新目前的 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="9341d-139">Updates the current RD RAP.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="9341d-140">屬性</span><span class="sxs-lookup"><span data-stu-id="9341d-140">Properties</span></span>

<span data-ttu-id="9341d-141">**Win32 \_ TSGatewayResourceAuthorizationPolicy** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9341d-141">The **Win32\_TSGatewayResourceAuthorizationPolicy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9341d-142">**說明**</span><span class="sxs-lookup"><span data-stu-id="9341d-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-145">RD RAP 的描述。</span><span class="sxs-lookup"><span data-stu-id="9341d-145">Description of the RD RAP.</span></span> <span data-ttu-id="9341d-146">這個屬性會以 [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。</span><span class="sxs-lookup"><span data-stu-id="9341d-146">This property is changed with the [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-147">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="9341d-147">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9341d-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-150">指出是否已啟用此 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="9341d-150">Indicates whether this RD RAP is enabled.</span></span> <span data-ttu-id="9341d-151">這個屬性會以 [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。</span><span class="sxs-lookup"><span data-stu-id="9341d-151">This property is changed with the [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-152">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9341d-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9341d-155">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9341d-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9341d-156">RD RAP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9341d-156">Name of the RD RAP.</span></span> <span data-ttu-id="9341d-157">這個屬性會以 [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。</span><span class="sxs-lookup"><span data-stu-id="9341d-157">This property is changed with the [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-158">**PortNumbers**</span><span class="sxs-lookup"><span data-stu-id="9341d-158">**PortNumbers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-161">此原則允許的分號分隔通訊埠編號清單。</span><span class="sxs-lookup"><span data-stu-id="9341d-161">List of semicolon-separated port numbers that are allowed for this policy.</span></span> <span data-ttu-id="9341d-162">若要允許任何埠號碼，請設定 " \* "。</span><span class="sxs-lookup"><span data-stu-id="9341d-162">To allow any port number, set "\*".</span></span>

</dd> <dt>

<span data-ttu-id="9341d-163">**ProtocolNames**</span><span class="sxs-lookup"><span data-stu-id="9341d-163">**ProtocolNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-166">針對此原則啟用之以分號分隔的通訊協定名稱清單。</span><span class="sxs-lookup"><span data-stu-id="9341d-166">List of semicolon-separated protocol names that are enabled for this policy.</span></span> <span data-ttu-id="9341d-167">名稱必須符合 [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)類別的 [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)方法傳回。</span><span class="sxs-lookup"><span data-stu-id="9341d-167">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-168">**resourceGroupName**</span><span class="sxs-lookup"><span data-stu-id="9341d-168">**ResourceGroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-171">資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="9341d-171">Resource group name.</span></span> <span data-ttu-id="9341d-172">這個屬性會以 [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。</span><span class="sxs-lookup"><span data-stu-id="9341d-172">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-173">**ResourceGroupType**</span><span class="sxs-lookup"><span data-stu-id="9341d-173">**ResourceGroupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-176">識別資源群組的類型。</span><span class="sxs-lookup"><span data-stu-id="9341d-176">Identifies the type of the resource group.</span></span> <span data-ttu-id="9341d-177">這個屬性會以 [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。</span><span class="sxs-lookup"><span data-stu-id="9341d-177">This property is changed with the [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) method.</span></span>

<dt>

<span data-ttu-id="9341d-178">RG</span><span class="sxs-lookup"><span data-stu-id="9341d-178">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="9341d-179">資源群組。</span><span class="sxs-lookup"><span data-stu-id="9341d-179">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-180">CG</span><span class="sxs-lookup"><span data-stu-id="9341d-180">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="9341d-181">電腦群組，儲存在 Active Directory Domain Services 中。</span><span class="sxs-lookup"><span data-stu-id="9341d-181">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="9341d-182">ALL</span><span class="sxs-lookup"><span data-stu-id="9341d-182">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="9341d-183">所有資源。</span><span class="sxs-lookup"><span data-stu-id="9341d-183">All resources.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9341d-184">**UserGroupNames**</span><span class="sxs-lookup"><span data-stu-id="9341d-184">**UserGroupNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9341d-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9341d-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9341d-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9341d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9341d-187">以分號分隔的使用者組名清單。</span><span class="sxs-lookup"><span data-stu-id="9341d-187">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="9341d-188">如果使用者隸屬于這些使用者群組中的任何一項，則會允許存取。</span><span class="sxs-lookup"><span data-stu-id="9341d-188">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="9341d-189">這個屬性會隨著 [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)、 [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)和 [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) 方法而變更。</span><span class="sxs-lookup"><span data-stu-id="9341d-189">This property is changed with the [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), and [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9341d-190">備註</span><span class="sxs-lookup"><span data-stu-id="9341d-190">Remarks</span></span>

<span data-ttu-id="9341d-191">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="9341d-191">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="9341d-192">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9341d-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9341d-193">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9341d-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9341d-194">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9341d-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9341d-195">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="9341d-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9341d-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="9341d-196">Requirements</span></span>



| <span data-ttu-id="9341d-197">需求</span><span class="sxs-lookup"><span data-stu-id="9341d-197">Requirement</span></span> | <span data-ttu-id="9341d-198">值</span><span class="sxs-lookup"><span data-stu-id="9341d-198">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9341d-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9341d-199">Minimum supported client</span></span><br/> | <span data-ttu-id="9341d-200">都不支援</span><span class="sxs-lookup"><span data-stu-id="9341d-200">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9341d-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9341d-201">Minimum supported server</span></span><br/> | <span data-ttu-id="9341d-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9341d-202">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9341d-203">命名空間</span><span class="sxs-lookup"><span data-stu-id="9341d-203">Namespace</span></span><br/>                | <span data-ttu-id="9341d-204">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="9341d-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9341d-205">MOF</span><span class="sxs-lookup"><span data-stu-id="9341d-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9341d-206"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="9341d-206"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9341d-207">DLL</span><span class="sxs-lookup"><span data-stu-id="9341d-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9341d-208"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9341d-208"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9341d-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9341d-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9341d-210">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="9341d-210">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="9341d-211">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="9341d-211">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="9341d-212">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="9341d-212">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="9341d-213">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="9341d-213">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="9341d-214">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="9341d-214">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="9341d-215">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="9341d-215">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

