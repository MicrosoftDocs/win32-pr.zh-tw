---
description: 暫停 WMI 類別方法會暫停列印工作。
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Win32_PrintJob 類別的 Pause 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847606"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="4ef8a-103">Win32 PrintJob 類別的 Pause 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4ef8a-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="4ef8a-104">**暫停** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會暫停列印工作。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="4ef8a-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4ef8a-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef8a-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ef8a-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="4ef8a-108">參數</span><span class="sxs-lookup"><span data-stu-id="4ef8a-108">Parameters</span></span>

<span data-ttu-id="4ef8a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ef8a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ef8a-110">Return value</span></span>

<span data-ttu-id="4ef8a-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4ef8a-112">**0**</span><span class="sxs-lookup"><span data-stu-id="4ef8a-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4ef8a-113">Success</span><span class="sxs-lookup"><span data-stu-id="4ef8a-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="4ef8a-114">**5**</span><span class="sxs-lookup"><span data-stu-id="4ef8a-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4ef8a-115">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="4ef8a-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4ef8a-116">範例</span><span class="sxs-lookup"><span data-stu-id="4ef8a-116">Examples</span></span>

<span data-ttu-id="4ef8a-117">[ [暫停所有具有空白列印佇列的印表機](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) ] VBScript 程式碼範例會暫停沒有擱置列印工作的任何印表機。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="4ef8a-118">下列 VBScript 程式碼範例會暫停列印伺服器上的所有列印工作。</span><span class="sxs-lookup"><span data-stu-id="4ef8a-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="4ef8a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ef8a-119">Requirements</span></span>



| <span data-ttu-id="4ef8a-120">需求</span><span class="sxs-lookup"><span data-stu-id="4ef8a-120">Requirement</span></span> | <span data-ttu-id="4ef8a-121">值</span><span class="sxs-lookup"><span data-stu-id="4ef8a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef8a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ef8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef8a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ef8a-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4ef8a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ef8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef8a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ef8a-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4ef8a-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="4ef8a-126">Namespace</span></span><br/>                | <span data-ttu-id="4ef8a-127">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4ef8a-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="4ef8a-128">MOF</span><span class="sxs-lookup"><span data-stu-id="4ef8a-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ef8a-129"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ef8a-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ef8a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4ef8a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ef8a-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ef8a-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4ef8a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ef8a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef8a-133">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4ef8a-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4ef8a-134">**Win32 \_ PrintJob**</span><span class="sxs-lookup"><span data-stu-id="4ef8a-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

