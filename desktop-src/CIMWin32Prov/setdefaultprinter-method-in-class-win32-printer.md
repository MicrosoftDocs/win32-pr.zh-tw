---
description: SetDefaultPrinter WMI 類別方法會為呼叫方法的使用者設定預設系統印表機。
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Win32_Printer 類別的 SetDefaultPrinter 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847601"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="e671b-103">Win32 Printer 類別的 SetDefaultPrinter 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e671b-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="e671b-104">**SetDefaultPrinter** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會為呼叫方法的使用者設定預設系統印表機。</span><span class="sxs-lookup"><span data-stu-id="e671b-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="e671b-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="e671b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e671b-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="e671b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e671b-107">語法</span><span class="sxs-lookup"><span data-stu-id="e671b-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="e671b-108">參數</span><span class="sxs-lookup"><span data-stu-id="e671b-108">Parameters</span></span>

<span data-ttu-id="e671b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e671b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e671b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e671b-110">Return value</span></span>

<span data-ttu-id="e671b-111">如果成功，則傳回 0 (零) ，如果發生錯誤，則傳回其他值。</span><span class="sxs-lookup"><span data-stu-id="e671b-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="e671b-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="e671b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e671b-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="e671b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="e671b-114">範例</span><span class="sxs-lookup"><span data-stu-id="e671b-114">Examples</span></span>

<span data-ttu-id="e671b-115">[安裝 Tcp/ip 印表機埠和印表機](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7)VBScript 範例會安裝 tcp/ip 印表機埠、安裝印表機，然後將印表機設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="e671b-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="e671b-116">下列 VBScript 程式碼範例會設定電腦上的預設印表機。</span><span class="sxs-lookup"><span data-stu-id="e671b-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="e671b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e671b-117">Requirements</span></span>



| <span data-ttu-id="e671b-118">需求</span><span class="sxs-lookup"><span data-stu-id="e671b-118">Requirement</span></span> | <span data-ttu-id="e671b-119">值</span><span class="sxs-lookup"><span data-stu-id="e671b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e671b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e671b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e671b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e671b-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e671b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e671b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e671b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e671b-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e671b-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="e671b-124">Namespace</span></span><br/>                | <span data-ttu-id="e671b-125">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e671b-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e671b-126">MOF</span><span class="sxs-lookup"><span data-stu-id="e671b-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e671b-127"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e671b-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e671b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e671b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e671b-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e671b-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e671b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e671b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e671b-131">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e671b-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e671b-132">WMI 工作：印表機和列印</span><span class="sxs-lookup"><span data-stu-id="e671b-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="e671b-133">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="e671b-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

