---
description: 重新開機&\# 8194;WMI 類別方法會關閉電腦系統，然後重新開機它。
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的重新開機方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936435"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="7d97c-103">Win32 作業系統類別的重新開機方法 \_</span><span class="sxs-lookup"><span data-stu-id="7d97c-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="7d97c-104">**重新開機** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會關閉電腦系統，然後重新開機它。</span><span class="sxs-lookup"><span data-stu-id="7d97c-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="7d97c-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7d97c-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="7d97c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d97c-107">語法</span><span class="sxs-lookup"><span data-stu-id="7d97c-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="7d97c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7d97c-108">Parameters</span></span>

<span data-ttu-id="7d97c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d97c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d97c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d97c-110">Return value</span></span>

<span data-ttu-id="7d97c-111">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="7d97c-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="7d97c-112">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d97c-112">Any other number indicates an error.</span></span> <span data-ttu-id="7d97c-113">如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="7d97c-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7d97c-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="7d97c-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7d97c-115">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="7d97c-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d97c-116">**其他** (1 4294967295) </span><span class="sxs-lookup"><span data-stu-id="7d97c-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7d97c-117">備註</span><span class="sxs-lookup"><span data-stu-id="7d97c-117">Remarks</span></span>

<span data-ttu-id="7d97c-118">以程式設計方式重新開機電腦的能力，可讓系統管理員從遠端執行許多電腦管理工作。</span><span class="sxs-lookup"><span data-stu-id="7d97c-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="7d97c-119">例如，如果您建立腳本來安裝軟體或進行設定變更，而需要重新開機電腦，您可以在腳本中包含 restart 命令，並從遠端執行整個作業。</span><span class="sxs-lookup"><span data-stu-id="7d97c-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="7d97c-120">**重新** 啟動方法可以用來重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="7d97c-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="7d97c-121">如同 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) 方法， **重新開機** 方法會要求腳本使用安全性認證的使用者擁有關機許可權。</span><span class="sxs-lookup"><span data-stu-id="7d97c-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="7d97c-122">範例</span><span class="sxs-lookup"><span data-stu-id="7d97c-122">Examples</span></span>

<span data-ttu-id="7d97c-123">下列 VBScript 程式碼範例會叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的 Reboot 方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="7d97c-124">您必須具有 Shutdown 許可權，才能成功叫用關機方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="7d97c-125">下列 Perl 程式碼會叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的重新開機方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="7d97c-126">您必須具有 Shutdown 許可權，才能成功叫用關機方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="7d97c-127">下列 VBScript 會在遠端系統上叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的 Reboot 方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="7d97c-128">以 \_ \_ 要重新開機的遠端系統名稱填入遠端系統名稱。</span><span class="sxs-lookup"><span data-stu-id="7d97c-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="7d97c-129">您必須具有 RemoteShutdown 許可權，才能成功叫用重新開機方法</span><span class="sxs-lookup"><span data-stu-id="7d97c-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="7d97c-130">他遵循 Perl 會在遠端系統上叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的 Reboot 方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="7d97c-131">以 \_ \_ 要重新開機的遠端系統名稱填入遠端系統名稱。</span><span class="sxs-lookup"><span data-stu-id="7d97c-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="7d97c-132">您必須具有 RemoteShutdown 許可權，才能成功叫用重新開機方法。</span><span class="sxs-lookup"><span data-stu-id="7d97c-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="7d97c-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d97c-133">Requirements</span></span>



| <span data-ttu-id="7d97c-134">需求</span><span class="sxs-lookup"><span data-stu-id="7d97c-134">Requirement</span></span> | <span data-ttu-id="7d97c-135">值</span><span class="sxs-lookup"><span data-stu-id="7d97c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d97c-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d97c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7d97c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d97c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d97c-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d97c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7d97c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d97c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d97c-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d97c-140">Namespace</span></span><br/>                | <span data-ttu-id="7d97c-141">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d97c-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d97c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7d97c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d97c-143"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d97c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7d97c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d97c-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d97c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d97c-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d97c-147">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d97c-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7d97c-148">**Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="7d97c-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="7d97c-149">**CIM \_ 作業系統. Shutdown 方法**</span><span class="sxs-lookup"><span data-stu-id="7d97c-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="7d97c-150">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="7d97c-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

