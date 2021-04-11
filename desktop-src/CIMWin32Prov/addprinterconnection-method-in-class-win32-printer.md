---
description: 提供與網路上現有印表機的連線，並將其新增至可用印表機的清單。
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Win32_Printer 類別的 AddPrinterConnection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847118"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="caf0b-103">Win32 Printer 類別的 AddPrinterConnection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="caf0b-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="caf0b-104">**AddPrinterConnection** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會提供與網路上現有印表機的連線，並將其新增至可用印表機的清單。</span><span class="sxs-lookup"><span data-stu-id="caf0b-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="caf0b-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="caf0b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="caf0b-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="caf0b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="caf0b-107">語法</span><span class="sxs-lookup"><span data-stu-id="caf0b-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="caf0b-108">參數</span><span class="sxs-lookup"><span data-stu-id="caf0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf0b-109">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caf0b-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf0b-110">印表機的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="caf0b-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf0b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="caf0b-111">Return value</span></span>

<span data-ttu-id="caf0b-112">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="caf0b-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="caf0b-113">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="caf0b-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="caf0b-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="caf0b-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="caf0b-115">**0**</span><span class="sxs-lookup"><span data-stu-id="caf0b-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="caf0b-116">Success</span><span class="sxs-lookup"><span data-stu-id="caf0b-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="caf0b-117">**5**</span><span class="sxs-lookup"><span data-stu-id="caf0b-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="caf0b-118">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="caf0b-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="caf0b-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="caf0b-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="caf0b-120">不正確印表機名稱</span><span class="sxs-lookup"><span data-stu-id="caf0b-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="caf0b-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="caf0b-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="caf0b-122">不相容的印表機驅動程式</span><span class="sxs-lookup"><span data-stu-id="caf0b-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="caf0b-123">範例</span><span class="sxs-lookup"><span data-stu-id="caf0b-123">Examples</span></span>

<span data-ttu-id="caf0b-124">[PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell 範例會從指定的列印伺服器安裝所有的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="caf0b-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="caf0b-125">[ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell 範例會列出遠端電腦硬碟上的共用印表機，並讓您能夠將遠端電腦的印表機連線新增至您的電腦。</span><span class="sxs-lookup"><span data-stu-id="caf0b-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="caf0b-126">下列 VBScript 程式碼範例會新增本機印表機。</span><span class="sxs-lookup"><span data-stu-id="caf0b-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="caf0b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="caf0b-127">Requirements</span></span>



| <span data-ttu-id="caf0b-128">需求</span><span class="sxs-lookup"><span data-stu-id="caf0b-128">Requirement</span></span> | <span data-ttu-id="caf0b-129">值</span><span class="sxs-lookup"><span data-stu-id="caf0b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf0b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caf0b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="caf0b-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="caf0b-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="caf0b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caf0b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="caf0b-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="caf0b-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="caf0b-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="caf0b-134">Namespace</span></span><br/>                | <span data-ttu-id="caf0b-135">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="caf0b-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="caf0b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="caf0b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caf0b-137"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="caf0b-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="caf0b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="caf0b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caf0b-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf0b-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="caf0b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caf0b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf0b-141">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="caf0b-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="caf0b-142">WMI 工作：印表機和列印</span><span class="sxs-lookup"><span data-stu-id="caf0b-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="caf0b-143">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="caf0b-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

