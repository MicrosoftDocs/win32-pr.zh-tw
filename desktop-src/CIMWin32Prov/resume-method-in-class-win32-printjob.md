---
description: Resume WMI 類別方法會繼續進行暫停的列印工作。
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Resume Win32_PrintJob 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970709"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="59549-103">Win32 PrintJob 類別的 Resume 方法 \_</span><span class="sxs-lookup"><span data-stu-id="59549-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="59549-104">**Resume** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會繼續進行暫停的列印工作。</span><span class="sxs-lookup"><span data-stu-id="59549-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="59549-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="59549-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59549-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="59549-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59549-107">語法</span><span class="sxs-lookup"><span data-stu-id="59549-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="59549-108">參數</span><span class="sxs-lookup"><span data-stu-id="59549-108">Parameters</span></span>

<span data-ttu-id="59549-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="59549-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59549-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="59549-110">Return value</span></span>

<span data-ttu-id="59549-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="59549-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="59549-112">**0**</span><span class="sxs-lookup"><span data-stu-id="59549-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="59549-113">Success</span><span class="sxs-lookup"><span data-stu-id="59549-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="59549-114">**5**</span><span class="sxs-lookup"><span data-stu-id="59549-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="59549-115">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="59549-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="59549-116">範例</span><span class="sxs-lookup"><span data-stu-id="59549-116">Examples</span></span>

<span data-ttu-id="59549-117">下列 VBScript 程式碼範例會繼續電腦上的所有列印工作。</span><span class="sxs-lookup"><span data-stu-id="59549-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="59549-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="59549-118">Requirements</span></span>



| <span data-ttu-id="59549-119">需求</span><span class="sxs-lookup"><span data-stu-id="59549-119">Requirement</span></span> | <span data-ttu-id="59549-120">值</span><span class="sxs-lookup"><span data-stu-id="59549-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59549-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59549-121">Minimum supported client</span></span><br/> | <span data-ttu-id="59549-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59549-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="59549-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59549-123">Minimum supported server</span></span><br/> | <span data-ttu-id="59549-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59549-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="59549-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="59549-125">Namespace</span></span><br/>                | <span data-ttu-id="59549-126">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="59549-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="59549-127">MOF</span><span class="sxs-lookup"><span data-stu-id="59549-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59549-128"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="59549-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="59549-129">DLL</span><span class="sxs-lookup"><span data-stu-id="59549-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59549-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59549-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="59549-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59549-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59549-132">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="59549-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="59549-133">**Win32 \_ PrintJob**</span><span class="sxs-lookup"><span data-stu-id="59549-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

