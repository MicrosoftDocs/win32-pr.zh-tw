---
description: 將 rights 參數設定為點陣圖，每個位都對應至存取權限。
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 GetCallerAccessRights 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998319"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="10c47-103">\_ \_ SystemSecurity 類別的 GetCallerAccessRights 方法</span><span class="sxs-lookup"><span data-stu-id="10c47-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="10c47-104">**\_ \_ SystemSecurity：： GetCallerAccessRights** 方法會將 *許可權* 參數設定為點陣圖，每個位都對應至存取權限。</span><span class="sxs-lookup"><span data-stu-id="10c47-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="10c47-105">任何用戶端都可以呼叫這個來判斷用戶端擁有的許可權。</span><span class="sxs-lookup"><span data-stu-id="10c47-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="10c47-106">此方法適用于啟用或停用功能的用戶端。</span><span class="sxs-lookup"><span data-stu-id="10c47-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="10c47-107">例如，如果目前登入的使用者沒有方法執行許可權，GUI 應用程式可能會停用按鈕。</span><span class="sxs-lookup"><span data-stu-id="10c47-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="10c47-108">任何啟用的用戶端都有呼叫 **GetCallerAccessRights** 的許可權，即使該用戶端沒有一般方法執行許可權也一樣。</span><span class="sxs-lookup"><span data-stu-id="10c47-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c47-109">語法</span><span class="sxs-lookup"><span data-stu-id="10c47-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="10c47-110">參數</span><span class="sxs-lookup"><span data-stu-id="10c47-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c47-111">*權利* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="10c47-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10c47-112">用戶端的存取權限。</span><span class="sxs-lookup"><span data-stu-id="10c47-112">Access rights of the client.</span></span> <span data-ttu-id="10c47-113">如需詳細資訊，請參閱 [**\_ \_ SystemSecurity**](--systemsecurity.md)和 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="10c47-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="10c47-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_啟用** (1 (0x1) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-115">啟用帳戶並授與使用者讀取權限。</span><span class="sxs-lookup"><span data-stu-id="10c47-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="10c47-116">這是所有使用者的預設存取權限。</span><span class="sxs-lookup"><span data-stu-id="10c47-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="10c47-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_方法 \_ 執行** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-118">允許執行方法。</span><span class="sxs-lookup"><span data-stu-id="10c47-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="10c47-119">提供者可能會執行額外的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="10c47-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="10c47-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_FULL \_ WRITE \_ REP** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-121">允許呼叫者、安全性內容或使用者寫入類別和實例（系統類別除外）。</span><span class="sxs-lookup"><span data-stu-id="10c47-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="10c47-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_部分 \_ 寫入 \_ 代表** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-123">允許呼叫者、安全性內容或使用者將提供者實例（而非靜態類別或靜態實例）寫入存放庫。</span><span class="sxs-lookup"><span data-stu-id="10c47-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="10c47-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ (16 (0x10 寫入 \_ 提供者**) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-125">允許呼叫者、安全性內容或使用者將類別和實例寫入提供者。</span><span class="sxs-lookup"><span data-stu-id="10c47-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="10c47-126">模擬提供者可能會進行額外的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="10c47-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="10c47-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_遠端 \_ 訪問** (32 (0x20) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-128">允許使用者帳戶從遠端執行其他位所設定之許可權所允許的任何作業。</span><span class="sxs-lookup"><span data-stu-id="10c47-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="10c47-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**讀取 \_控制** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-130">允許對安全描述項的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="10c47-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="10c47-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**寫入 \_DAC** (262144 (0x40000) ) </span><span class="sxs-lookup"><span data-stu-id="10c47-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="10c47-132">允許對 (DACL) 的任意存取控制清單進行寫入存取。</span><span class="sxs-lookup"><span data-stu-id="10c47-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c47-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="10c47-133">Return value</span></span>

<span data-ttu-id="10c47-134">這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="10c47-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="10c47-135">下列清單列出對 [**Set9XUserList**](--systemsecurity-set9xuserlist.md)而言很重要的傳回值。</span><span class="sxs-lookup"><span data-stu-id="10c47-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="10c47-136">針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果 [ReturnValue](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="10c47-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="10c47-137">如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="10c47-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="10c47-138">**\_ \_ \_ 已停用 WBEM E 方法**</span><span class="sxs-lookup"><span data-stu-id="10c47-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="10c47-139">支援的 Windows 版本不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="10c47-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10c47-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="10c47-140">Requirements</span></span>



| <span data-ttu-id="10c47-141">需求</span><span class="sxs-lookup"><span data-stu-id="10c47-141">Requirement</span></span> | <span data-ttu-id="10c47-142">值</span><span class="sxs-lookup"><span data-stu-id="10c47-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="10c47-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10c47-143">Minimum supported client</span></span><br/> | <span data-ttu-id="10c47-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10c47-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="10c47-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10c47-145">Minimum supported server</span></span><br/> | <span data-ttu-id="10c47-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10c47-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="10c47-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="10c47-147">Namespace</span></span><br/>                | <span data-ttu-id="10c47-148">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="10c47-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="10c47-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10c47-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c47-150">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="10c47-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="10c47-151">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="10c47-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="10c47-152">**\_\_SystemSecurity::GetSD**</span><span class="sxs-lookup"><span data-stu-id="10c47-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="10c47-153">**\_\_SystemSecurity::SetSD**</span><span class="sxs-lookup"><span data-stu-id="10c47-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="10c47-154">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="10c47-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="10c47-155">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="10c47-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="10c47-156">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="10c47-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="10c47-157">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="10c47-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="10c47-158">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="10c47-158">WMI Security Constants</span></span>
</dt> </dl>

 

