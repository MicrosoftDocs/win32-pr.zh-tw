---
description: 繼續暫停的列印佇列。
ms.assetid: 6d6d21e9-f469-4e2c-9a89-3e9febe229fc
ms.tgt_platform: multiple
title: Resume Win32_Printer 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3eca8849fd1c5c449261dac1a9530f4da42e9482
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970909"
---
# <a name="resume-method-of-the-win32_printer-class"></a><span data-ttu-id="633e0-103">Win32 Printer 類別的 Resume 方法 \_</span><span class="sxs-lookup"><span data-stu-id="633e0-103">Resume method of the Win32\_Printer class</span></span>

<span data-ttu-id="633e0-104">**Resume** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會繼續已暫停的列印佇列。</span><span class="sxs-lookup"><span data-stu-id="633e0-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method resumes a paused print queue.</span></span>

<span data-ttu-id="633e0-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="633e0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="633e0-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="633e0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="633e0-107">語法</span><span class="sxs-lookup"><span data-stu-id="633e0-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="633e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="633e0-108">Parameters</span></span>

<span data-ttu-id="633e0-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="633e0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="633e0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="633e0-110">Return value</span></span>

<span data-ttu-id="633e0-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="633e0-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="633e0-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="633e0-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="633e0-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="633e0-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="633e0-114">**0**</span><span class="sxs-lookup"><span data-stu-id="633e0-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="633e0-115">Success</span><span class="sxs-lookup"><span data-stu-id="633e0-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="633e0-116">**5**</span><span class="sxs-lookup"><span data-stu-id="633e0-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="633e0-117">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="633e0-117">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="633e0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="633e0-118">Requirements</span></span>



| <span data-ttu-id="633e0-119">需求</span><span class="sxs-lookup"><span data-stu-id="633e0-119">Requirement</span></span> | <span data-ttu-id="633e0-120">值</span><span class="sxs-lookup"><span data-stu-id="633e0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="633e0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="633e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="633e0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="633e0-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="633e0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="633e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="633e0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="633e0-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="633e0-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="633e0-125">Namespace</span></span><br/>                | <span data-ttu-id="633e0-126">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="633e0-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="633e0-127">MOF</span><span class="sxs-lookup"><span data-stu-id="633e0-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="633e0-128"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="633e0-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="633e0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="633e0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="633e0-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="633e0-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="633e0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="633e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633e0-132">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="633e0-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="633e0-133">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="633e0-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="633e0-134">**Pause 方法**</span><span class="sxs-lookup"><span data-stu-id="633e0-134">**Pause Method**</span></span>](pause-method-in-class-win32-printer.md)
</dt> </dl>

 

