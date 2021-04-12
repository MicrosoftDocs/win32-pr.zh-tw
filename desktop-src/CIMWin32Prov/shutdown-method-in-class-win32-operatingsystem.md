---
description: 關機&\# 8194;WMI 類別方法會卸載程式和 Dll，直到可以安全地關閉電腦為止。
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468569"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="86ca7-103">Win32 作業系統類別的 Shutdown 方法 \_</span><span class="sxs-lookup"><span data-stu-id="86ca7-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="86ca7-104">**關機** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會卸載程式和 dll，直到可以安全地關閉電腦為止。</span><span class="sxs-lookup"><span data-stu-id="86ca7-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="86ca7-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="86ca7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="86ca7-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="86ca7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="86ca7-107">語法</span><span class="sxs-lookup"><span data-stu-id="86ca7-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="86ca7-108">參數</span><span class="sxs-lookup"><span data-stu-id="86ca7-108">Parameters</span></span>

<span data-ttu-id="86ca7-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="86ca7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86ca7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="86ca7-110">Return value</span></span>

<span data-ttu-id="86ca7-111">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="86ca7-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="86ca7-112">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="86ca7-112">Any other number indicates an error.</span></span> <span data-ttu-id="86ca7-113">如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="86ca7-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="86ca7-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="86ca7-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="86ca7-115">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="86ca7-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86ca7-116">**其他** (1 4294967295) </span><span class="sxs-lookup"><span data-stu-id="86ca7-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="86ca7-117">備註</span><span class="sxs-lookup"><span data-stu-id="86ca7-117">Remarks</span></span>

<span data-ttu-id="86ca7-118">電腦偶爾需要從網路中移除，也許是為了進行排程維護，因為電腦無法正常運作，或是完成設定程式。</span><span class="sxs-lookup"><span data-stu-id="86ca7-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="86ca7-119">例如，如果 DHCP 伺服器將錯誤的 IP 位址送出，您可能會想要關閉電腦，直到可以分派服務技術人員來修正問題為止。</span><span class="sxs-lookup"><span data-stu-id="86ca7-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="86ca7-120">如果您懷疑發生安全性缺口，您可能需要關閉特定伺服器，以確保在安全性問題解決之前，無法存取這些伺服器。</span><span class="sxs-lookup"><span data-stu-id="86ca7-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="86ca7-121">某些設定作業 (例如變更電腦名稱稱) 需要您重新開機電腦，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="86ca7-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="86ca7-122">如果可能的話，這個方法會立即關閉電腦。</span><span class="sxs-lookup"><span data-stu-id="86ca7-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="86ca7-123">系統會停止所有執行中的進程，並將所有檔案緩衝區排清到磁片，然後關閉系統電源。</span><span class="sxs-lookup"><span data-stu-id="86ca7-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="86ca7-124">呼叫進程必須具有 **SE \_ SHUTDOWN \_ 名稱** 許可權，如下列範例所述。</span><span class="sxs-lookup"><span data-stu-id="86ca7-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="86ca7-125">如需設定許可權的詳細資訊，請參閱使用 VBScript [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)。</span><span class="sxs-lookup"><span data-stu-id="86ca7-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="86ca7-126">如需其他關機選項（例如登出或強制關機），請參閱 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="86ca7-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="86ca7-127">範例</span><span class="sxs-lookup"><span data-stu-id="86ca7-127">Examples</span></span>

<span data-ttu-id="86ca7-128">下列 VBScript 程式碼會關閉本機電腦。</span><span class="sxs-lookup"><span data-stu-id="86ca7-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="86ca7-129">您必須具有 Shutdown 許可權，才能成功叫用關機方法。</span><span class="sxs-lookup"><span data-stu-id="86ca7-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="86ca7-130">下列 Perl 程式碼會關閉本機電腦。</span><span class="sxs-lookup"><span data-stu-id="86ca7-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="86ca7-131">您必須具有 Shutdown 許可權，才能成功叫用關機方法。</span><span class="sxs-lookup"><span data-stu-id="86ca7-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



<span data-ttu-id="86ca7-132">下列 VBScript 程式碼會關閉指定的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="86ca7-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="86ca7-133">以要關機的遠端系統名稱填入 [ *遠端 \_ 系統 \_ 名稱* ]。</span><span class="sxs-lookup"><span data-stu-id="86ca7-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="86ca7-134">您必須具有 RemoteShutdown 許可權，才能成功叫用 **關機** 方法。</span><span class="sxs-lookup"><span data-stu-id="86ca7-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="86ca7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="86ca7-135">Requirements</span></span>



| <span data-ttu-id="86ca7-136">需求</span><span class="sxs-lookup"><span data-stu-id="86ca7-136">Requirement</span></span> | <span data-ttu-id="86ca7-137">值</span><span class="sxs-lookup"><span data-stu-id="86ca7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86ca7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86ca7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="86ca7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86ca7-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86ca7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86ca7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="86ca7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86ca7-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86ca7-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="86ca7-142">Namespace</span></span><br/>                | <span data-ttu-id="86ca7-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="86ca7-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86ca7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="86ca7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86ca7-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="86ca7-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86ca7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="86ca7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86ca7-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86ca7-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ca7-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86ca7-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="86ca7-149">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86ca7-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="86ca7-150">**Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="86ca7-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="86ca7-151">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="86ca7-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="86ca7-152">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="86ca7-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

