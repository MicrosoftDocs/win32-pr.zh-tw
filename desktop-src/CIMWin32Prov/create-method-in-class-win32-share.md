---
description: 起始伺服器資源的共用。
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Win32_Share 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936531"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="60bec-103">Win32 共用類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="60bec-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="60bec-104">**建立**[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會起始伺服器資源的共用。   </span><span class="sxs-lookup"><span data-stu-id="60bec-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="60bec-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="60bec-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="60bec-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="60bec-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="60bec-107">語法</span><span class="sxs-lookup"><span data-stu-id="60bec-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="60bec-108">參數</span><span class="sxs-lookup"><span data-stu-id="60bec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60bec-109">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60bec-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-110">Windows 共用的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="60bec-110">Local path of the Windows share.</span></span>

<span data-ttu-id="60bec-111">範例： "C： \\ Program Files"。</span><span class="sxs-lookup"><span data-stu-id="60bec-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="60bec-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60bec-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-113">將別名傳遞到在執行 Windows 的電腦系統上設定為共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="60bec-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="60bec-114">範例： "public"。</span><span class="sxs-lookup"><span data-stu-id="60bec-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="60bec-115">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60bec-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-116">傳遞要共用的資源類型。</span><span class="sxs-lookup"><span data-stu-id="60bec-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="60bec-117">類型包括磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。</span><span class="sxs-lookup"><span data-stu-id="60bec-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="60bec-118">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="60bec-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="60bec-119">**磁片磁碟機** (0) </span><span class="sxs-lookup"><span data-stu-id="60bec-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="60bec-120">**列印佇列** (1) </span><span class="sxs-lookup"><span data-stu-id="60bec-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="60bec-121">**裝置** (2) </span><span class="sxs-lookup"><span data-stu-id="60bec-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="60bec-122">**IPC** (3) </span><span class="sxs-lookup"><span data-stu-id="60bec-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="60bec-123">**磁片磁碟機系統管理員** (2147483648) </span><span class="sxs-lookup"><span data-stu-id="60bec-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="60bec-124">**列印佇列管理** (2147483649) </span><span class="sxs-lookup"><span data-stu-id="60bec-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="60bec-125">**裝置系統管理員** (2147483650) </span><span class="sxs-lookup"><span data-stu-id="60bec-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="60bec-126">**IPC 系統管理員** (2147483651) </span><span class="sxs-lookup"><span data-stu-id="60bec-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="60bec-127">*MaximumAllowed* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="60bec-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-128">允許同時使用此資源的使用者數目上限。</span><span class="sxs-lookup"><span data-stu-id="60bec-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="60bec-129">範例：10。</span><span class="sxs-lookup"><span data-stu-id="60bec-129">Example: 10.</span></span> <span data-ttu-id="60bec-130">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="60bec-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="60bec-131">*描述* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="60bec-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-132">描述所共用資源的選擇性批註。</span><span class="sxs-lookup"><span data-stu-id="60bec-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="60bec-133">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="60bec-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="60bec-134">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="60bec-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-135">使用共用資源的共用層級安全性) 執行伺服器時的密碼 (。</span><span class="sxs-lookup"><span data-stu-id="60bec-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="60bec-136">如果伺服器正在以使用者層級安全性執行，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="60bec-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="60bec-137">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="60bec-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="60bec-138">*存取* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="60bec-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60bec-139">使用者層級許可權的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="60bec-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="60bec-140">安全描述項包含資源的許可權、擁有者和存取功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="60bec-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="60bec-141">如果未提供此參數或為 **Null**，則每個人都具有共用的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="60bec-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="60bec-142">如需詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 和 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="60bec-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60bec-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="60bec-143">Return value</span></span>

<span data-ttu-id="60bec-144">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="60bec-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="60bec-145">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="60bec-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="60bec-146">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="60bec-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="60bec-147">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="60bec-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-148">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="60bec-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-149">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="60bec-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-150">**不正確名稱** (9) </span><span class="sxs-lookup"><span data-stu-id="60bec-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-151">**層級** (10) 無效</span><span class="sxs-lookup"><span data-stu-id="60bec-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-152">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="60bec-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-153">**重複的共用** (22) </span><span class="sxs-lookup"><span data-stu-id="60bec-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-154">重新 **導向路徑** (23) </span><span class="sxs-lookup"><span data-stu-id="60bec-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-155">**未知的裝置或目錄** (24) </span><span class="sxs-lookup"><span data-stu-id="60bec-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-156">**找不到網路名稱** (25) </span><span class="sxs-lookup"><span data-stu-id="60bec-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="60bec-157">**其他** (26 4294967295) </span><span class="sxs-lookup"><span data-stu-id="60bec-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="60bec-158">備註</span><span class="sxs-lookup"><span data-stu-id="60bec-158">Remarks</span></span>

<span data-ttu-id="60bec-159">**Create** 是靜態方法。</span><span class="sxs-lookup"><span data-stu-id="60bec-159">**Create** is a static method.</span></span>

<span data-ttu-id="60bec-160">只有 Administrators 或 Account Operators 本機群組的成員，或是具有通訊、列印或伺服器操作員群組成員資格的成員，才能夠成功執行 **Create**。</span><span class="sxs-lookup"><span data-stu-id="60bec-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="60bec-161">列印操作員只能新增印表機佇列。</span><span class="sxs-lookup"><span data-stu-id="60bec-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="60bec-162">通訊運算子只能新增通訊裝置佇列。</span><span class="sxs-lookup"><span data-stu-id="60bec-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="60bec-163">範例</span><span class="sxs-lookup"><span data-stu-id="60bec-163">Examples</span></span>

<span data-ttu-id="60bec-164">[匯出和匯入檔案共用](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1)PowerShell 範例會匯出並匯入檔案共用，並設定共用許可權。</span><span class="sxs-lookup"><span data-stu-id="60bec-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="60bec-165">同樣地，[ [建立共用和設定許可權](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) ] 範例也會建立新的共用，並設定共用許可權。</span><span class="sxs-lookup"><span data-stu-id="60bec-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="60bec-166">下列 PowerShell 程式碼會建立共用。</span><span class="sxs-lookup"><span data-stu-id="60bec-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="60bec-167">上述程式碼範例會傳回下列內容：</span><span class="sxs-lookup"><span data-stu-id="60bec-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="60bec-168">下列 C 程式 \# 代碼範例說明如何呼叫 create 方法。</span><span class="sxs-lookup"><span data-stu-id="60bec-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="60bec-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="60bec-169">Requirements</span></span>



| <span data-ttu-id="60bec-170">需求</span><span class="sxs-lookup"><span data-stu-id="60bec-170">Requirement</span></span> | <span data-ttu-id="60bec-171">值</span><span class="sxs-lookup"><span data-stu-id="60bec-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60bec-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60bec-172">Minimum supported client</span></span><br/> | <span data-ttu-id="60bec-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60bec-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60bec-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60bec-174">Minimum supported server</span></span><br/> | <span data-ttu-id="60bec-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60bec-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60bec-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="60bec-176">Namespace</span></span><br/>                | <span data-ttu-id="60bec-177">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60bec-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60bec-178">MOF</span><span class="sxs-lookup"><span data-stu-id="60bec-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60bec-179"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="60bec-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60bec-180">DLL</span><span class="sxs-lookup"><span data-stu-id="60bec-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60bec-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60bec-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60bec-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60bec-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="60bec-183">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60bec-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="60bec-184">**Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="60bec-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

