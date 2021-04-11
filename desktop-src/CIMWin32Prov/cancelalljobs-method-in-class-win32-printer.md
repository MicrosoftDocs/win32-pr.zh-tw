---
description: 移除所有工作，包括目前從佇列中列印的工作。
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Win32_Printer 類別的 CancelAllJobs 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847115"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="aa494-103">Win32 Printer 類別的 CancelAllJobs 方法 \_</span><span class="sxs-lookup"><span data-stu-id="aa494-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="aa494-104">**CancelAllJobs** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會移除所有的工作，包括目前從佇列中列印的工作。</span><span class="sxs-lookup"><span data-stu-id="aa494-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="aa494-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="aa494-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aa494-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="aa494-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa494-107">語法</span><span class="sxs-lookup"><span data-stu-id="aa494-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="aa494-108">參數</span><span class="sxs-lookup"><span data-stu-id="aa494-108">Parameters</span></span>

<span data-ttu-id="aa494-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="aa494-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa494-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa494-110">Return value</span></span>

<span data-ttu-id="aa494-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="aa494-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="aa494-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="aa494-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="aa494-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="aa494-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="aa494-114">**0**</span><span class="sxs-lookup"><span data-stu-id="aa494-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="aa494-115">Success</span><span class="sxs-lookup"><span data-stu-id="aa494-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="aa494-116">**5**</span><span class="sxs-lookup"><span data-stu-id="aa494-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="aa494-117">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="aa494-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="aa494-118">範例</span><span class="sxs-lookup"><span data-stu-id="aa494-118">Examples</span></span>

<span data-ttu-id="aa494-119">[ [當列印佇列清除時通知使用者] 會](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) 使用 Msg.exe 將網路警示傳送給任何在列印佇列中有檔要清除的使用者。</span><span class="sxs-lookup"><span data-stu-id="aa494-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="aa494-120">傳送警示之後，腳本會清除列印佇列。</span><span class="sxs-lookup"><span data-stu-id="aa494-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="aa494-121">[ [刪除所有列印工作](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) ] VBScript 程式碼範例會刪除本機電腦上的所有列印工作。</span><span class="sxs-lookup"><span data-stu-id="aa494-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="aa494-122">下列 VBScript 範例會刪除名為 HP QuietJet 之印表機的所有列印工作。</span><span class="sxs-lookup"><span data-stu-id="aa494-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="aa494-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa494-123">Requirements</span></span>



| <span data-ttu-id="aa494-124">需求</span><span class="sxs-lookup"><span data-stu-id="aa494-124">Requirement</span></span> | <span data-ttu-id="aa494-125">值</span><span class="sxs-lookup"><span data-stu-id="aa494-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa494-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa494-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aa494-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa494-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="aa494-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa494-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aa494-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa494-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="aa494-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa494-130">Namespace</span></span><br/>                | <span data-ttu-id="aa494-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aa494-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="aa494-132">MOF</span><span class="sxs-lookup"><span data-stu-id="aa494-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa494-133"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa494-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa494-134">DLL</span><span class="sxs-lookup"><span data-stu-id="aa494-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa494-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa494-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="aa494-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa494-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa494-137">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="aa494-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="aa494-138">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="aa494-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

