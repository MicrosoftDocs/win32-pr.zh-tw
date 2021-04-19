---
description: 排除在下次重新開機時執行的 autochk 作業中的磁片。
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Win32_LogicalDisk 類別的 ExcludeFromAutochk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997065"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="a43ca-103">Win32 LogicalDisk 類別的 ExcludeFromAutochk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a43ca-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="a43ca-104">**ExcludeFromAutochk** 方法不會在下次重新開機時，從執行的 **autochk** 作業中排除磁片。</span><span class="sxs-lookup"><span data-stu-id="a43ca-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="a43ca-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a43ca-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a43ca-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a43ca-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a43ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="a43ca-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="a43ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="a43ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a43ca-109">*LogicalDisk* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a43ca-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a43ca-110">下次重新開機時，應從 **autochk** 排除的磁片磁碟機清單。</span><span class="sxs-lookup"><span data-stu-id="a43ca-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="a43ca-111">字串語法是由磁碟機號後面接著邏輯磁片的冒號所組成。</span><span class="sxs-lookup"><span data-stu-id="a43ca-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="a43ca-112">範例： "C："</span><span class="sxs-lookup"><span data-stu-id="a43ca-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a43ca-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a43ca-113">Return value</span></span>

<span data-ttu-id="a43ca-114">如果沒有發生錯誤，則傳回值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="a43ca-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="a43ca-115">值列在下列清單中。</span><span class="sxs-lookup"><span data-stu-id="a43ca-115">Values are listed in the following list.</span></span> <span data-ttu-id="a43ca-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="a43ca-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a43ca-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="a43ca-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a43ca-118">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="a43ca-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a43ca-119">**錯誤-遠端磁片磁碟機** (1) </span><span class="sxs-lookup"><span data-stu-id="a43ca-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a43ca-120">**錯誤-抽取式磁碟** 機 (2) </span><span class="sxs-lookup"><span data-stu-id="a43ca-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a43ca-121">**錯誤-磁片磁碟機不是根目錄** (3) </span><span class="sxs-lookup"><span data-stu-id="a43ca-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a43ca-122">**錯誤-未知的磁片磁碟機** (4) </span><span class="sxs-lookup"><span data-stu-id="a43ca-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a43ca-123">備註</span><span class="sxs-lookup"><span data-stu-id="a43ca-123">Remarks</span></span>

<span data-ttu-id="a43ca-124">如果未排除，則會在磁片設定中途位時，在磁片上執行 **autochk** 。</span><span class="sxs-lookup"><span data-stu-id="a43ca-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="a43ca-125">請注意，排除磁片的呼叫不是累計的。</span><span class="sxs-lookup"><span data-stu-id="a43ca-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="a43ca-126">如果進行呼叫以排除某些磁片，則不會將新的清單新增至已標示為排除的磁片清單。</span><span class="sxs-lookup"><span data-stu-id="a43ca-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="a43ca-127">新的磁片清單會覆寫先前的清單。</span><span class="sxs-lookup"><span data-stu-id="a43ca-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="a43ca-128">此方法僅適用于代表電腦中實體磁片的邏輯磁片實例。</span><span class="sxs-lookup"><span data-stu-id="a43ca-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="a43ca-129">它不適用於對應的邏輯磁碟機。</span><span class="sxs-lookup"><span data-stu-id="a43ca-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="a43ca-130">範例</span><span class="sxs-lookup"><span data-stu-id="a43ca-130">Examples</span></span>

<span data-ttu-id="a43ca-131">下列 VBScript 程式碼範例可確保在下一次電腦重新開機時，Autochk.exe 不會在 C 磁片磁碟機上執行，即使磁片磁碟機 C 上已設定「中途位」也是如此。</span><span class="sxs-lookup"><span data-stu-id="a43ca-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="a43ca-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="a43ca-132">Requirements</span></span>



| <span data-ttu-id="a43ca-133">需求</span><span class="sxs-lookup"><span data-stu-id="a43ca-133">Requirement</span></span> | <span data-ttu-id="a43ca-134">值</span><span class="sxs-lookup"><span data-stu-id="a43ca-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a43ca-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a43ca-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a43ca-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a43ca-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a43ca-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a43ca-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a43ca-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a43ca-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a43ca-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="a43ca-139">Namespace</span></span><br/>                | <span data-ttu-id="a43ca-140">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a43ca-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a43ca-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a43ca-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a43ca-142"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a43ca-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a43ca-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a43ca-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a43ca-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a43ca-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a43ca-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a43ca-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43ca-146">**Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="a43ca-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="a43ca-147">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="a43ca-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

