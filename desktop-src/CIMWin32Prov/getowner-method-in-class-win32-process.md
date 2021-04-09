---
description: GetOwner&\# 8194;WMI 類別方法會抓取執行進程的使用者名稱和功能變數名稱。
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Win32_Process 類別的 GetOwner 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110489"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="b5c68-103">Win32 進程類別的 GetOwner 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b5c68-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="b5c68-104">**GetOwner** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會抓取進程執行時所使用的使用者名稱和功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b5c68-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="b5c68-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="b5c68-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b5c68-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="b5c68-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c68-107">語法</span><span class="sxs-lookup"><span data-stu-id="b5c68-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="b5c68-108">參數</span><span class="sxs-lookup"><span data-stu-id="b5c68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c68-109">*使用者* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b5c68-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c68-110">傳回這個進程擁有者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b5c68-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="b5c68-111">*網域* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b5c68-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5c68-112">傳回執行此進程所用的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b5c68-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c68-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5c68-113">Return value</span></span>

<span data-ttu-id="b5c68-114">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="b5c68-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="b5c68-115">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b5c68-115">Any other number indicates an error.</span></span> <span data-ttu-id="b5c68-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="b5c68-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b5c68-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="b5c68-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b5c68-118">**成功完成** (0) </span><span class="sxs-lookup"><span data-stu-id="b5c68-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5c68-119">**拒絕存取** (2) </span><span class="sxs-lookup"><span data-stu-id="b5c68-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b5c68-120">**許可權不足** (3) </span><span class="sxs-lookup"><span data-stu-id="b5c68-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b5c68-121">**未知的失敗** (8) </span><span class="sxs-lookup"><span data-stu-id="b5c68-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b5c68-122"> (9) **找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="b5c68-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b5c68-123">**不正確參數** (21) </span><span class="sxs-lookup"><span data-stu-id="b5c68-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b5c68-124">**其他** (22 4294967295) </span><span class="sxs-lookup"><span data-stu-id="b5c68-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="b5c68-125">範例</span><span class="sxs-lookup"><span data-stu-id="b5c68-125">Examples</span></span>

<span data-ttu-id="b5c68-126">[監視進程的 CPU Pct （依名稱與擁有者](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) ）VBScript 範例會收集 CPU 或處理器使用率百分比，並查閱進程擁有者。</span><span class="sxs-lookup"><span data-stu-id="b5c68-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="b5c68-127">所有 explorer.exe 進程的擁有者 [都會將使用者清單的「取得所有伺服器」記錄到](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell 範例 querys WMI。</span><span class="sxs-lookup"><span data-stu-id="b5c68-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="b5c68-128">下列 VBScript 程式碼範例會取得每個正在執行之進程的擁有者。</span><span class="sxs-lookup"><span data-stu-id="b5c68-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="b5c68-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5c68-129">Requirements</span></span>



| <span data-ttu-id="b5c68-130">需求</span><span class="sxs-lookup"><span data-stu-id="b5c68-130">Requirement</span></span> | <span data-ttu-id="b5c68-131">值</span><span class="sxs-lookup"><span data-stu-id="b5c68-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c68-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5c68-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b5c68-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5c68-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5c68-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5c68-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b5c68-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5c68-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5c68-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="b5c68-136">Namespace</span></span><br/>                | <span data-ttu-id="b5c68-137">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b5c68-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5c68-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b5c68-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5c68-139"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5c68-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5c68-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b5c68-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5c68-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5c68-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c68-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5c68-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5c68-143">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5c68-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b5c68-144">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="b5c68-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

