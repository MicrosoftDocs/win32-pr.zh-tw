---
description: 在磁片上叫用 chkdsk 操作。
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別的 Chkdsk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111108"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="79d57-103">Win32 LogicalDisk 類別的 Chkdsk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="79d57-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="79d57-104">**Chkdsk** 實例方法會叫用磁片上的 **chkdsk** 操作。</span><span class="sxs-lookup"><span data-stu-id="79d57-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="79d57-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="79d57-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="79d57-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="79d57-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="79d57-107">語法</span><span class="sxs-lookup"><span data-stu-id="79d57-107">Syntax</span></span>


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a><span data-ttu-id="79d57-108">參數</span><span class="sxs-lookup"><span data-stu-id="79d57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d57-109">*FixErrors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79d57-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d57-110">指出在磁片上找到的錯誤應完成的工作。</span><span class="sxs-lookup"><span data-stu-id="79d57-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="79d57-111">若 **為 true**，則會修正錯誤。</span><span class="sxs-lookup"><span data-stu-id="79d57-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="79d57-112">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="79d57-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79d57-113">*VigorousIndexCheck* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79d57-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d57-114">若 **為 true**，則應該執行較不加強的索引項目檢查。</span><span class="sxs-lookup"><span data-stu-id="79d57-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="79d57-115">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="79d57-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79d57-116">*SkipFolderCycle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79d57-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d57-117">若 **為 true**，則應略過資料夾迴圈檢查。</span><span class="sxs-lookup"><span data-stu-id="79d57-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="79d57-118">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="79d57-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="79d57-119">*ForceDismount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79d57-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d57-120">若 **為 true**，則應該在檢查之前強制卸載磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="79d57-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="79d57-121">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="79d57-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79d57-122">*RecoverBadSectors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79d57-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d57-123">若 **為 true**，則應該找出不正確的磁區，而且應該從這些磁區復原可讀取的資訊。</span><span class="sxs-lookup"><span data-stu-id="79d57-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="79d57-124">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="79d57-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="79d57-125">*OKToRunAtBootUp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79d57-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d57-126">若 **為 true**，則會在下次開機時執行 **chkdsk** 作業，以防無法執行作業，因為在呼叫這個方法時，磁片會被鎖定。</span><span class="sxs-lookup"><span data-stu-id="79d57-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="79d57-127">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="79d57-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d57-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="79d57-128">Return value</span></span>

<span data-ttu-id="79d57-129">如果成功，則傳回 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="79d57-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="79d57-130">其他值會列在下列清單中。</span><span class="sxs-lookup"><span data-stu-id="79d57-130">Other values are listed in the following list.</span></span> <span data-ttu-id="79d57-131">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="79d57-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="79d57-132">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="79d57-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="79d57-133">**成功-Chkdsk 已完成**</span><span class="sxs-lookup"><span data-stu-id="79d57-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="79d57-134">0</span><span class="sxs-lookup"><span data-stu-id="79d57-134">0</span></span>

<span data-ttu-id="79d57-135">成功- [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) 已完成</span><span class="sxs-lookup"><span data-stu-id="79d57-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="79d57-136">**在重新開機時成功鎖定和 chkdsk 排程**</span><span class="sxs-lookup"><span data-stu-id="79d57-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="79d57-137">1</span><span class="sxs-lookup"><span data-stu-id="79d57-137">1</span></span>

</dd> <dt>

<span data-ttu-id="79d57-138">**失敗-未知的檔案系統**</span><span class="sxs-lookup"><span data-stu-id="79d57-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="79d57-139">2</span><span class="sxs-lookup"><span data-stu-id="79d57-139">2</span></span>

</dd> <dt>

<span data-ttu-id="79d57-140">**失敗-未知的錯誤**</span><span class="sxs-lookup"><span data-stu-id="79d57-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="79d57-141">3</span><span class="sxs-lookup"><span data-stu-id="79d57-141">3</span></span>

</dd> <dt>

<span data-ttu-id="79d57-142">**失敗-不支援的檔案系統**</span><span class="sxs-lookup"><span data-stu-id="79d57-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="79d57-143">4</span><span class="sxs-lookup"><span data-stu-id="79d57-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79d57-144">備註</span><span class="sxs-lookup"><span data-stu-id="79d57-144">Remarks</span></span>

<span data-ttu-id="79d57-145">此方法僅適用于代表電腦中實體磁片的邏輯磁片實例。</span><span class="sxs-lookup"><span data-stu-id="79d57-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="79d57-146">它不適用於對應的邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="79d57-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="79d57-147">範例</span><span class="sxs-lookup"><span data-stu-id="79d57-147">Examples</span></span>

<span data-ttu-id="79d57-148">如果設定了 chkdsk/f 旗標，伺服器 PowerShell 程式碼範例會檢查遠端系統，並傳回 true 或 false，以在伺服器 PowerShell 程式碼範例[上設定 chkdsk 中途位](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) 。</span><span class="sxs-lookup"><span data-stu-id="79d57-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="79d57-149">[遠端掃描磁片](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267)PowerShell 程式碼範例會從遠端啟動或排程掃描磁片。</span><span class="sxs-lookup"><span data-stu-id="79d57-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="79d57-150">下列 VBScript 程式碼範例會針對電腦上的 D 磁片磁碟機執行 ChkDsk.exe。</span><span class="sxs-lookup"><span data-stu-id="79d57-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="79d57-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="79d57-151">Requirements</span></span>



| <span data-ttu-id="79d57-152">需求</span><span class="sxs-lookup"><span data-stu-id="79d57-152">Requirement</span></span> | <span data-ttu-id="79d57-153">值</span><span class="sxs-lookup"><span data-stu-id="79d57-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79d57-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79d57-154">Minimum supported client</span></span><br/> | <span data-ttu-id="79d57-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79d57-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79d57-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79d57-156">Minimum supported server</span></span><br/> | <span data-ttu-id="79d57-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79d57-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79d57-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="79d57-158">Namespace</span></span><br/>                | <span data-ttu-id="79d57-159">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="79d57-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79d57-160">MOF</span><span class="sxs-lookup"><span data-stu-id="79d57-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79d57-161"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="79d57-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79d57-162">DLL</span><span class="sxs-lookup"><span data-stu-id="79d57-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79d57-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79d57-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d57-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79d57-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d57-165">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="79d57-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="79d57-166">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="79d57-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

