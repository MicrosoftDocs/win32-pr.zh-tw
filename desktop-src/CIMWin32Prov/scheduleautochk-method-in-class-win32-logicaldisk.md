---
description: 排程在下次重新開機時，于 Win32 LogicalDisk 所代表的磁片磁碟機上執行的 Autochk （ \_ 如果已設定中途位）。
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別的 ScheduleAutoChk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936175"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="f3d9d-103">Win32 LogicalDisk 類別的 ScheduleAutoChk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f3d9d-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="f3d9d-104">如果設定了中途的位， **ScheduleAutoChk** 類別方法會排程在下次重新開機時，于 [**Win32 \_ LogicalDisk**](win32-logicaldisk.md) 所代表的磁片磁碟機上執行 Autochk。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="f3d9d-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f3d9d-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d9d-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3d9d-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="f3d9d-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3d9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3d9d-109">*LogicalDisk* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3d9d-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3d9d-110">指定下次重新開機時要針對 Autochk 排程的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="f3d9d-111">字串語法是由磁碟機號後面接著邏輯磁片的冒號所組成，例如： "C："</span><span class="sxs-lookup"><span data-stu-id="f3d9d-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="f3d9d-112">當資料來自不明來源或您不信任的來源時，請一律檢查 *LogicalDisk* 陣列中的磁碟機號有效性。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3d9d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3d9d-113">Return value</span></span>

<span data-ttu-id="f3d9d-114">如果成功，則傳回值為 0 (零) ，如果發生任何其他錯誤，則傳回其他值。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="f3d9d-115">值列在下列清單中。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-115">Values are listed in the following list.</span></span> <span data-ttu-id="f3d9d-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f3d9d-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f3d9d-118">**沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f3d9d-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f3d9d-119">**錯誤-遠端磁片磁碟機** (1) </span><span class="sxs-lookup"><span data-stu-id="f3d9d-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f3d9d-120">**錯誤-抽取式磁碟** 機 (2) </span><span class="sxs-lookup"><span data-stu-id="f3d9d-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f3d9d-121">**錯誤-磁片磁碟機不是根目錄** (3) </span><span class="sxs-lookup"><span data-stu-id="f3d9d-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f3d9d-122">**錯誤-未知的磁片磁碟機** (4) </span><span class="sxs-lookup"><span data-stu-id="f3d9d-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f3d9d-123">備註</span><span class="sxs-lookup"><span data-stu-id="f3d9d-123">Remarks</span></span>

<span data-ttu-id="f3d9d-124">此方法僅適用于代表電腦中實體磁片的邏輯磁片實例。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="f3d9d-125">這個方法不適用於對應的邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="f3d9d-126">範例</span><span class="sxs-lookup"><span data-stu-id="f3d9d-126">Examples</span></span>

<span data-ttu-id="f3d9d-127">下列 VBScript 和 PowerShell 範例會排程 Autochk.exe 下次電腦重新開機時，對 C 磁片磁碟機執行。</span><span class="sxs-lookup"><span data-stu-id="f3d9d-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="f3d9d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3d9d-128">Requirements</span></span>



| <span data-ttu-id="f3d9d-129">需求</span><span class="sxs-lookup"><span data-stu-id="f3d9d-129">Requirement</span></span> | <span data-ttu-id="f3d9d-130">值</span><span class="sxs-lookup"><span data-stu-id="f3d9d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d9d-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3d9d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d9d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3d9d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3d9d-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3d9d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d9d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3d9d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3d9d-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3d9d-135">Namespace</span></span><br/>                | <span data-ttu-id="f3d9d-136">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3d9d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3d9d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f3d9d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3d9d-138"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3d9d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3d9d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f3d9d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3d9d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3d9d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d9d-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3d9d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d9d-142">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="f3d9d-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

