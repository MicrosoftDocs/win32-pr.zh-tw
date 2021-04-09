---
description: Win32ShutdownTracker 方法提供 Win32 作業系統中的 Win32Shutdown 方法所支援的一組相同關機選項 \_ ，但是它也可讓您指定批註、關機原因或超時。
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 Win32ShutdownTracker 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110216"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="e9ed1-103">Win32 作業系統類別的 Win32ShutdownTracker 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e9ed1-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="e9ed1-104">**Win32ShutdownTracker** 方法提供 [**Win32 \_ 作業系統**](win32-operatingsystem.md)中的 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)方法所支援的一組相同關機選項，但是它也可讓您指定批註、關機原因或超時。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ed1-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9ed1-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e9ed1-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ed1-107">*Timeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9ed1-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-108">發生關機之前的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="e9ed1-109">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-110">*批註* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9ed1-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-111">要在 [關閉] 對話方塊中顯示的訊息，該對話方塊也會儲存為事件記錄檔專案中的批註。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-112">*ReasonCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9ed1-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-113">初始關機的原因。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e9ed1-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-115">用來關閉電腦的一組點陣圖旗標。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="e9ed1-116">若要強制執行命令，請將 Force 旗標 (4) 新增至命令值。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="e9ed1-117">在遠端電腦上使用 Force 搭配關機或重新開機，會立即關閉所有 (包括 WMI、COM 等等) ，或重新開機遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="e9ed1-118">這會產生不定的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="e9ed1-119">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-120">登出</span><span class="sxs-lookup"><span data-stu-id="e9ed1-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-121">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-122">強制登出 (0 + 4) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-123">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-124">關機</span><span class="sxs-lookup"><span data-stu-id="e9ed1-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-125">5 (0x5) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-126">強制關機 (1 + 4) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-127">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-128">重新啟動</span><span class="sxs-lookup"><span data-stu-id="e9ed1-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-129">6 (0x6) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-130">強制重新開機 (2 + 4) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-131">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-132">關閉電源</span><span class="sxs-lookup"><span data-stu-id="e9ed1-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="e9ed1-133">12 (0xC) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="e9ed1-134">強制關機 (8 + 4) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ed1-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9ed1-135">Return value</span></span>

<span data-ttu-id="e9ed1-136">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="e9ed1-137">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-137">Any other number indicates an error.</span></span> <span data-ttu-id="e9ed1-138">如需錯誤碼，請參閱 [**WMI 錯誤常數**](../wmisdk/wmi-error-constants.md) 或 [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e9ed1-139">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](../debug/system-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="e9ed1-140">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9ed1-141">**其他** (1 – 4294967295) </span><span class="sxs-lookup"><span data-stu-id="e9ed1-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ed1-142">備註</span><span class="sxs-lookup"><span data-stu-id="e9ed1-142">Remarks</span></span>

<span data-ttu-id="e9ed1-143">呼叫進程必須具有 **SE \_ SHUTDOWN \_ 名稱** 許可權。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="e9ed1-144">範例</span><span class="sxs-lookup"><span data-stu-id="e9ed1-144">Examples</span></span>

<span data-ttu-id="e9ed1-145">下列 VBScript 程式碼範例說明如何呼叫 **Win32ShutdownTracker**。</span><span class="sxs-lookup"><span data-stu-id="e9ed1-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="e9ed1-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9ed1-146">Requirements</span></span>



| <span data-ttu-id="e9ed1-147">需求</span><span class="sxs-lookup"><span data-stu-id="e9ed1-147">Requirement</span></span> | <span data-ttu-id="e9ed1-148">值</span><span class="sxs-lookup"><span data-stu-id="e9ed1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ed1-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9ed1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ed1-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9ed1-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9ed1-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9ed1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ed1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9ed1-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9ed1-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9ed1-153">Namespace</span></span><br/>                | <span data-ttu-id="e9ed1-154">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e9ed1-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9ed1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="e9ed1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9ed1-156"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9ed1-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9ed1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ed1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ed1-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ed1-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ed1-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9ed1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ed1-160">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="e9ed1-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e9ed1-161">**Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="e9ed1-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="e9ed1-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="e9ed1-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
