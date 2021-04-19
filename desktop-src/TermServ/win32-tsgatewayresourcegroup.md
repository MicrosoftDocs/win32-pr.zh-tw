---
title: Win32_TSGatewayResourceGroup 類別
description: 描述資源群組，這會將一組資源 (電腦名稱稱) 對應至單一實體。
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup 類別遠端桌面服務
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965713"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="3f6bf-105">Win32 \_ TSGatewayResourceGroup 類別</span><span class="sxs-lookup"><span data-stu-id="3f6bf-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="3f6bf-106">描述資源群組，這會將一組資源 (電腦名稱稱) 對應至單一實體。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6bf-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f6bf-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="3f6bf-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f6bf-108">Members</span></span>

<span data-ttu-id="3f6bf-109">**Win32 \_ TSGatewayResourceGroup** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f6bf-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="3f6bf-110">方法</span><span class="sxs-lookup"><span data-stu-id="3f6bf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3f6bf-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3f6bf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3f6bf-112">方法</span><span class="sxs-lookup"><span data-stu-id="3f6bf-112">Methods</span></span>

<span data-ttu-id="3f6bf-113">**Win32 \_ TSGatewayResourceGroup** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="3f6bf-114">方法</span><span class="sxs-lookup"><span data-stu-id="3f6bf-114">Method</span></span>                                                                  | <span data-ttu-id="3f6bf-115">描述</span><span class="sxs-lookup"><span data-stu-id="3f6bf-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f6bf-116">**AddResources**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="3f6bf-117">將資源新增至此資源群組的 **資源** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="3f6bf-118">**建立**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="3f6bf-119">建立資源群組。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="3f6bf-120">**刪除**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="3f6bf-121">刪除此資源群組。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="3f6bf-122">**RemoveResources**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="3f6bf-123">從資源屬性中刪除此資源群組 **的資源。**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="3f6bf-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="3f6bf-125">設定此資源群組的 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="3f6bf-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="3f6bf-127">設定此資源群組的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="3f6bf-128">**SetResources**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="3f6bf-129">設定此資源群組的 **資源** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="3f6bf-130">**更新**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="3f6bf-131">更新此資源群組。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="3f6bf-132">屬性</span><span class="sxs-lookup"><span data-stu-id="3f6bf-132">Properties</span></span>

<span data-ttu-id="3f6bf-133">**Win32 \_ TSGatewayResourceGroup** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f6bf-134">**AssociatedRAPs**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6bf-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6bf-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f6bf-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f6bf-137">與此資源群組相關聯 (RD Rap) 的遠端桌面服務資源授權原則清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="3f6bf-138">**說明**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6bf-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6bf-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f6bf-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f6bf-141">資源群組的描述。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-141">Description of the resource group.</span></span> <span data-ttu-id="3f6bf-142">這個屬性可以使用 [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) 方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3f6bf-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6bf-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6bf-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f6bf-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f6bf-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3f6bf-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3f6bf-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-147">Name of the resource group.</span></span> <span data-ttu-id="3f6bf-148">這個屬性可以使用 [**SetName**](setname-win32-tsgatewayresourcegroup.md) 方法來變更。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3f6bf-149">**資源**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f6bf-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f6bf-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3f6bf-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f6bf-152">此資源群組中的資源清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="3f6bf-153">「」 \* 表示所有資源。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-153">An "\*" means all resources.</span></span> <span data-ttu-id="3f6bf-154">您可以使用 [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)、 [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)、 [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)和 [**Update**](update-win32-tsgatewayresourcegroup.md) 方法來變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f6bf-155">備註</span><span class="sxs-lookup"><span data-stu-id="3f6bf-155">Remarks</span></span>

<span data-ttu-id="3f6bf-156">您必須是 Administrators 群組的成員，才能使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="3f6bf-157">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3f6bf-158">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3f6bf-159">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3f6bf-160">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="3f6bf-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f6bf-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f6bf-161">Requirements</span></span>



| <span data-ttu-id="3f6bf-162">需求</span><span class="sxs-lookup"><span data-stu-id="3f6bf-162">Requirement</span></span> | <span data-ttu-id="3f6bf-163">值</span><span class="sxs-lookup"><span data-stu-id="3f6bf-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6bf-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f6bf-164">Minimum supported client</span></span><br/> | <span data-ttu-id="3f6bf-165">都不支援</span><span class="sxs-lookup"><span data-stu-id="3f6bf-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3f6bf-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f6bf-166">Minimum supported server</span></span><br/> | <span data-ttu-id="3f6bf-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f6bf-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3f6bf-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="3f6bf-168">Namespace</span></span><br/>                | <span data-ttu-id="3f6bf-169">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="3f6bf-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3f6bf-170">MOF</span><span class="sxs-lookup"><span data-stu-id="3f6bf-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f6bf-171"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f6bf-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f6bf-172">DLL</span><span class="sxs-lookup"><span data-stu-id="3f6bf-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f6bf-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f6bf-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3f6bf-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f6bf-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f6bf-175">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="3f6bf-176">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="3f6bf-177">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="3f6bf-178">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="3f6bf-179">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="3f6bf-180">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="3f6bf-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

