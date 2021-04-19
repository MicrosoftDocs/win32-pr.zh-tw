---
description: 列印測試頁面。
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: Win32_Printer 類別的 PrintTestPage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973985"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="3b831-103">Win32 Printer 類別的 PrintTestPage 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3b831-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="3b831-104">**PrintTestPage** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會列印測試頁面。</span><span class="sxs-lookup"><span data-stu-id="3b831-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="3b831-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="3b831-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b831-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="3b831-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b831-107">語法</span><span class="sxs-lookup"><span data-stu-id="3b831-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="3b831-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b831-108">Parameters</span></span>

<span data-ttu-id="3b831-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3b831-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b831-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b831-110">Return value</span></span>

<span data-ttu-id="3b831-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b831-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3b831-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="3b831-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3b831-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="3b831-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3b831-114">**0**</span><span class="sxs-lookup"><span data-stu-id="3b831-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3b831-115">Success</span><span class="sxs-lookup"><span data-stu-id="3b831-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="3b831-116">**5**</span><span class="sxs-lookup"><span data-stu-id="3b831-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3b831-117">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="3b831-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3b831-118">範例</span><span class="sxs-lookup"><span data-stu-id="3b831-118">Examples</span></span>

<span data-ttu-id="3b831-119">下列 PowerShell 程式碼範例會列印測試頁面。</span><span class="sxs-lookup"><span data-stu-id="3b831-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="3b831-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b831-120">Requirements</span></span>



| <span data-ttu-id="3b831-121">需求</span><span class="sxs-lookup"><span data-stu-id="3b831-121">Requirement</span></span> | <span data-ttu-id="3b831-122">值</span><span class="sxs-lookup"><span data-stu-id="3b831-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b831-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b831-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3b831-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b831-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="3b831-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b831-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3b831-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b831-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="3b831-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b831-127">Namespace</span></span><br/>                | <span data-ttu-id="3b831-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3b831-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="3b831-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3b831-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b831-130"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b831-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b831-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3b831-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b831-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b831-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3b831-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b831-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b831-134">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="3b831-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3b831-135">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="3b831-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

