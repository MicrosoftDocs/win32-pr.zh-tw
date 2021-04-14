---
description: 建立新的印表機驅動程式。
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Win32_PrinterDriver 類別的 AddPrinterDriver 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385878"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="4d19e-103">Win32 PrinterDriver 類別的 AddPrinterDriver 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4d19e-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="4d19e-104">**AddPrinterDriver** 類別方法會建立新的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4d19e-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="4d19e-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4d19e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4d19e-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4d19e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d19e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d19e-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4d19e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d19e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d19e-109">*DriverInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d19e-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d19e-110">[**Win32 \_ PrinterDriver**](win32-printerdriver.md)類別的實例，代表印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4d19e-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d19e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d19e-111">Return value</span></span>

<span data-ttu-id="4d19e-112">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d19e-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="4d19e-113">針對不同于下列清單中所列的值，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants)。</span><span class="sxs-lookup"><span data-stu-id="4d19e-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="4d19e-114">**0**</span><span class="sxs-lookup"><span data-stu-id="4d19e-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4d19e-115">成功。</span><span class="sxs-lookup"><span data-stu-id="4d19e-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4d19e-116">**5**</span><span class="sxs-lookup"><span data-stu-id="4d19e-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4d19e-117">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="4d19e-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4d19e-118">**87**</span><span class="sxs-lookup"><span data-stu-id="4d19e-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="4d19e-119">參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d19e-119">The parameter is incorrect.</span></span> <span data-ttu-id="4d19e-120">當物件未正確填滿，或在系統中找不到驅動程式時，可能會發生此問題。</span><span class="sxs-lookup"><span data-stu-id="4d19e-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="4d19e-121">或者，[名稱] 屬性可能與 .inf 檔案中指定的模型不同。</span><span class="sxs-lookup"><span data-stu-id="4d19e-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="4d19e-122">或者，PathFile 屬性上可能會有遺漏的反斜線 ( " \\ " ) 。</span><span class="sxs-lookup"><span data-stu-id="4d19e-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="4d19e-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="4d19e-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="4d19e-124">印表機驅動程式未知。</span><span class="sxs-lookup"><span data-stu-id="4d19e-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d19e-125">備註</span><span class="sxs-lookup"><span data-stu-id="4d19e-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d19e-126">使用 **AddPrinterDriver** 方法時，您必須使用 **SeLoadDriverPrivilege** 來載入或卸載設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4d19e-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4d19e-127">範例</span><span class="sxs-lookup"><span data-stu-id="4d19e-127">Examples</span></span>

<span data-ttu-id="4d19e-128">[[在驅動程式封包中找不到安裝印表機驅動程式](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) ] VBScript 程式碼範例會使用 Drivers.cab 中找不到的列印驅動程式來安裝假設的印表機。</span><span class="sxs-lookup"><span data-stu-id="4d19e-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="4d19e-129">下列 VBScript 範例會安裝 Apple LaserWriter 8500 印表機的印表機驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4d19e-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="4d19e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d19e-130">Requirements</span></span>



| <span data-ttu-id="4d19e-131">需求</span><span class="sxs-lookup"><span data-stu-id="4d19e-131">Requirement</span></span> | <span data-ttu-id="4d19e-132">值</span><span class="sxs-lookup"><span data-stu-id="4d19e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d19e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d19e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4d19e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d19e-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4d19e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d19e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4d19e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d19e-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4d19e-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d19e-137">Namespace</span></span><br/>                | <span data-ttu-id="4d19e-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4d19e-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="4d19e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4d19e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d19e-140"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d19e-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d19e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4d19e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d19e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d19e-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4d19e-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d19e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d19e-144">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4d19e-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4d19e-145">**Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="4d19e-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

