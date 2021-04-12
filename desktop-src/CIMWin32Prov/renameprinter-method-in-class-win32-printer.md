---
description: 重新命名印表機。
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Win32_Printer 類別的 RenamePrinter 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187594"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="e058e-103">Win32 Printer 類別的 RenamePrinter 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e058e-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="e058e-104">**RenamePrinter** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名印表機。</span><span class="sxs-lookup"><span data-stu-id="e058e-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="e058e-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="e058e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e058e-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="e058e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e058e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e058e-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="e058e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e058e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e058e-109">*NewPrinterName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e058e-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e058e-110">新的印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="e058e-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e058e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e058e-111">Return value</span></span>

<span data-ttu-id="e058e-112">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="e058e-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="e058e-113">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="e058e-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e058e-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="e058e-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e058e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="e058e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e058e-116">Success</span><span class="sxs-lookup"><span data-stu-id="e058e-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="e058e-117">**5**</span><span class="sxs-lookup"><span data-stu-id="e058e-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e058e-118">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="e058e-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="e058e-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="e058e-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="e058e-120">不正確印表機名稱</span><span class="sxs-lookup"><span data-stu-id="e058e-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e058e-121">範例</span><span class="sxs-lookup"><span data-stu-id="e058e-121">Examples</span></span>

<span data-ttu-id="e058e-122">下列 VBScript 範例會重新命名印表機和其印表機共用名稱。</span><span class="sxs-lookup"><span data-stu-id="e058e-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="e058e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e058e-123">Requirements</span></span>



| <span data-ttu-id="e058e-124">需求</span><span class="sxs-lookup"><span data-stu-id="e058e-124">Requirement</span></span> | <span data-ttu-id="e058e-125">值</span><span class="sxs-lookup"><span data-stu-id="e058e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e058e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e058e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e058e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e058e-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e058e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e058e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e058e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e058e-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e058e-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="e058e-130">Namespace</span></span><br/>                | <span data-ttu-id="e058e-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e058e-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e058e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e058e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e058e-133"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e058e-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e058e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e058e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e058e-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e058e-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e058e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e058e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e058e-137">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e058e-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e058e-138">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="e058e-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

