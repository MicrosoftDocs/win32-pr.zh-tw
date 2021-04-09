---
description: WMI 具有安全性常數，用於 \_ \_ SystemSecurity：： GetCallerAccessRights 的命名空間存取檢查。
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: '命名空間存取權限常數 (Wbemcli .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026074"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="a2130-103">命名空間存取權限常數</span><span class="sxs-lookup"><span data-stu-id="a2130-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="a2130-104">WMI 具有安全性常數，用於 [**\_ \_ SystemSecurity：： GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)的命名空間存取檢查。</span><span class="sxs-lookup"><span data-stu-id="a2130-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="a2130-105">如需存取控制清單 (Acl、Dacl 或 Sacl) 的安全性資訊，請參閱 [ (acl 的存取控制清單)](/windows/desktop/SecAuthZ/access-control-lists) 和 [**標準存取權限**](/windows/desktop/SecAuthZ/standard-access-rights)。</span><span class="sxs-lookup"><span data-stu-id="a2130-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="a2130-106">這些常數定義于 **WBEM \_ 安全性 \_ 旗標** 列舉中。</span><span class="sxs-lookup"><span data-stu-id="a2130-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="a2130-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="a2130-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2130-108">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="a2130-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="a2130-109">啟用帳戶並授與使用者讀取權限。</span><span class="sxs-lookup"><span data-stu-id="a2130-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="a2130-110">這是所有使用者的預設存取權，並且對應至 [*WMI 控制項*](gloss-w.md)[安全性] 索引標籤上的 [啟用帳戶] 許可權。</span><span class="sxs-lookup"><span data-stu-id="a2130-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="a2130-111">如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="a2130-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2130-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ 方法 \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="a2130-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2130-113">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="a2130-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="a2130-114">允許執行方法。</span><span class="sxs-lookup"><span data-stu-id="a2130-114">Allows the execution of methods.</span></span> <span data-ttu-id="a2130-115">提供者可以執行額外的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="a2130-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="a2130-116">這是所有使用者的預設存取權，並且對應至 WMI 控制項 [安全性] 索引標籤上的 [執行方法] 許可權。</span><span class="sxs-lookup"><span data-stu-id="a2130-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2130-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ 完整 \_ 寫入 \_ 代表**</span><span class="sxs-lookup"><span data-stu-id="a2130-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2130-118">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="a2130-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="a2130-119">允許使用者帳戶寫入 WMI 存放庫和實例中的類別。</span><span class="sxs-lookup"><span data-stu-id="a2130-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="a2130-120">使用者無法寫入系統類別。</span><span class="sxs-lookup"><span data-stu-id="a2130-120">A user cannot write to system classes.</span></span> <span data-ttu-id="a2130-121">只有 Administrators 群組的成員具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="a2130-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="a2130-122">**WBEM \_FULL \_ write \_ REP** 對應于 WMI 控制項 [安全性] 索引標籤的完整寫入權限。</span><span class="sxs-lookup"><span data-stu-id="a2130-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2130-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ 部分 \_ 寫入 \_ 代表**</span><span class="sxs-lookup"><span data-stu-id="a2130-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2130-124">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="a2130-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="a2130-125">可讓您將資料寫入至實例，而不是類別。</span><span class="sxs-lookup"><span data-stu-id="a2130-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="a2130-126">使用者無法將類別寫入 WMI 存放 [*庫*](gloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="a2130-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="a2130-127">只有 Administrators 群組的成員才有這個許可權。</span><span class="sxs-lookup"><span data-stu-id="a2130-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="a2130-128">**WBEM \_部分 \_ 寫入的 \_ 代表** 會對應至 WMI 控制項 [安全性] 索引標籤的部分寫入權限。</span><span class="sxs-lookup"><span data-stu-id="a2130-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2130-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ 寫入 \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="a2130-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2130-130">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="a2130-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="a2130-131">允許將類別和實例寫入提供者。</span><span class="sxs-lookup"><span data-stu-id="a2130-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="a2130-132">請注意，提供者可以在模擬使用者時進行額外的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="a2130-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="a2130-133">這是所有使用者的預設存取權，並且對應至 WMI 控制項 [安全性] 索引標籤的提供者寫入權限。</span><span class="sxs-lookup"><span data-stu-id="a2130-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a2130-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ 遠端 \_ 訪問**</span><span class="sxs-lookup"><span data-stu-id="a2130-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2130-135">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="a2130-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="a2130-136">允許使用者帳戶從遠端執行上述許可權所允許的任何作業。</span><span class="sxs-lookup"><span data-stu-id="a2130-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="a2130-137">只有 Administrators 群組的成員才有這個許可權。</span><span class="sxs-lookup"><span data-stu-id="a2130-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="a2130-138">**WBEM \_[遠端 \_ 訪問** ] 對應至 WMI 控制項 [安全性] 索引標籤上的 [遠端啟用] 許可權。</span><span class="sxs-lookup"><span data-stu-id="a2130-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2130-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2130-139">Requirements</span></span>



| <span data-ttu-id="a2130-140">需求</span><span class="sxs-lookup"><span data-stu-id="a2130-140">Requirement</span></span> | <span data-ttu-id="a2130-141">值</span><span class="sxs-lookup"><span data-stu-id="a2130-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2130-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2130-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a2130-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2130-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="a2130-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2130-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a2130-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2130-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="a2130-146">標頭</span><span class="sxs-lookup"><span data-stu-id="a2130-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2130-147"><dt>Wbemcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2130-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2130-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2130-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2130-149">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="a2130-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="a2130-150">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="a2130-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="a2130-151">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="a2130-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="a2130-152">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="a2130-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="a2130-153">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="a2130-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

