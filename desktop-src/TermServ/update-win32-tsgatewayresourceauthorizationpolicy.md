---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 Update 方法
description: 更新目前的遠端桌面資源授權原則 (RD \ 160;RAP) 。
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Update 方法遠端桌面服務
- Update 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，Update 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104280"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="3d52e-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 Update 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3d52e-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="3d52e-107"> (RD RAP) 更新目前的遠端桌面資源授權原則。</span><span class="sxs-lookup"><span data-stu-id="3d52e-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d52e-108">語法</span><span class="sxs-lookup"><span data-stu-id="3d52e-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="3d52e-109">參數</span><span class="sxs-lookup"><span data-stu-id="3d52e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d52e-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-111">RD RAP 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d52e-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-112">*描述* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-113">RD RAP 的描述。</span><span class="sxs-lookup"><span data-stu-id="3d52e-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-114">*已啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-115">指出是否應該啟用 RD RAP。</span><span class="sxs-lookup"><span data-stu-id="3d52e-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-116">*ResourceGroupName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-117">與此 RD RAP 相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3d52e-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-118">*ResourceGroupType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-119">資源群組類型。</span><span class="sxs-lookup"><span data-stu-id="3d52e-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="3d52e-120">RG</span><span class="sxs-lookup"><span data-stu-id="3d52e-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-121">資源群組。</span><span class="sxs-lookup"><span data-stu-id="3d52e-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-122">CG</span><span class="sxs-lookup"><span data-stu-id="3d52e-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-123">電腦群組，儲存在 Active Directory Domain Services 中。</span><span class="sxs-lookup"><span data-stu-id="3d52e-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-124">ALL</span><span class="sxs-lookup"><span data-stu-id="3d52e-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-125">所有資源。</span><span class="sxs-lookup"><span data-stu-id="3d52e-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d52e-126">*UserGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-127">以分號分隔的使用者組名清單。</span><span class="sxs-lookup"><span data-stu-id="3d52e-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="3d52e-128">名稱的格式為 *網域 \\ UserGroupName*。</span><span class="sxs-lookup"><span data-stu-id="3d52e-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="3d52e-129">如果使用者隸屬于這些使用者群組中的任何一項，則會允許存取。</span><span class="sxs-lookup"><span data-stu-id="3d52e-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-130">*ProtocolNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-131">針對此原則啟用的通訊協定名稱清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3d52e-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="3d52e-132">名稱必須符合 [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)類別的 [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)方法傳回。</span><span class="sxs-lookup"><span data-stu-id="3d52e-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3d52e-133">*PortNumbers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d52e-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d52e-134">針對此原則啟用的埠號碼清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3d52e-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="3d52e-135">若要允許任何埠號碼，請設定 " \* "。</span><span class="sxs-lookup"><span data-stu-id="3d52e-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d52e-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d52e-136">Return value</span></span>

<span data-ttu-id="3d52e-137">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3d52e-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3d52e-138">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="3d52e-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3d52e-139">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="3d52e-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d52e-140">備註</span><span class="sxs-lookup"><span data-stu-id="3d52e-140">Remarks</span></span>

<span data-ttu-id="3d52e-141">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3d52e-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3d52e-142">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="3d52e-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3d52e-143">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3d52e-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3d52e-144">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="3d52e-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3d52e-145">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="3d52e-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d52e-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d52e-146">Requirements</span></span>



| <span data-ttu-id="3d52e-147">需求</span><span class="sxs-lookup"><span data-stu-id="3d52e-147">Requirement</span></span> | <span data-ttu-id="3d52e-148">值</span><span class="sxs-lookup"><span data-stu-id="3d52e-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d52e-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d52e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3d52e-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="3d52e-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3d52e-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d52e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3d52e-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d52e-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3d52e-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="3d52e-153">Namespace</span></span><br/>                | <span data-ttu-id="3d52e-154">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="3d52e-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3d52e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="3d52e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d52e-156"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d52e-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d52e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="3d52e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d52e-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d52e-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3d52e-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d52e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d52e-160">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="3d52e-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

