---
description: 暫停列印佇列。
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Win32_Printer 類別的 Pause 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385996"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="7e7dc-103">Win32 Printer 類別的 Pause 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7e7dc-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="7e7dc-104">**暫停** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會暫停列印佇列。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="7e7dc-105">在繼續執行佇列之前，不會列印任何工作。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="7e7dc-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7e7dc-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7dc-108">語法</span><span class="sxs-lookup"><span data-stu-id="7e7dc-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="7e7dc-109">參數</span><span class="sxs-lookup"><span data-stu-id="7e7dc-109">Parameters</span></span>

<span data-ttu-id="7e7dc-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e7dc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e7dc-111">Return value</span></span>

<span data-ttu-id="7e7dc-112">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="7e7dc-113">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7e7dc-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="7e7dc-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7e7dc-115">**0**</span><span class="sxs-lookup"><span data-stu-id="7e7dc-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7e7dc-116">Success</span><span class="sxs-lookup"><span data-stu-id="7e7dc-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="7e7dc-117">**5**</span><span class="sxs-lookup"><span data-stu-id="7e7dc-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="7e7dc-118">拒絕存取</span><span class="sxs-lookup"><span data-stu-id="7e7dc-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e7dc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e7dc-119">Requirements</span></span>



| <span data-ttu-id="7e7dc-120">需求</span><span class="sxs-lookup"><span data-stu-id="7e7dc-120">Requirement</span></span> | <span data-ttu-id="7e7dc-121">值</span><span class="sxs-lookup"><span data-stu-id="7e7dc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7dc-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e7dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7dc-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e7dc-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7e7dc-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e7dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7dc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e7dc-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7e7dc-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="7e7dc-126">Namespace</span></span><br/>                | <span data-ttu-id="7e7dc-127">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e7dc-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7e7dc-128">MOF</span><span class="sxs-lookup"><span data-stu-id="7e7dc-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e7dc-129"><dt>Win32 \_ 印表機。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e7dc-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e7dc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7e7dc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e7dc-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7dc-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7e7dc-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e7dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7dc-133">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="7e7dc-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7e7dc-134">**Win32 \_ 印表機**</span><span class="sxs-lookup"><span data-stu-id="7e7dc-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="7e7dc-135">**Resume 方法**</span><span class="sxs-lookup"><span data-stu-id="7e7dc-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

