---
description: Delete&\# 8194;WMI 類別方法會刪除排程工作。
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Win32_ScheduledJob 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111644"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="6ee42-103">Win32 Register-scheduledjob 類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6ee42-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="6ee42-104">**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除排程工作。</span><span class="sxs-lookup"><span data-stu-id="6ee42-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="6ee42-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="6ee42-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6ee42-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="6ee42-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee42-107">語法</span><span class="sxs-lookup"><span data-stu-id="6ee42-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="6ee42-108">參數</span><span class="sxs-lookup"><span data-stu-id="6ee42-108">Parameters</span></span>

<span data-ttu-id="6ee42-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6ee42-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ee42-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ee42-110">Return value</span></span>

<span data-ttu-id="6ee42-111">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="6ee42-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="6ee42-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="6ee42-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6ee42-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="6ee42-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6ee42-114">**成功完成**</span><span class="sxs-lookup"><span data-stu-id="6ee42-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-115">0</span><span class="sxs-lookup"><span data-stu-id="6ee42-115">0</span></span>

<span data-ttu-id="6ee42-116">要求已被接受。</span><span class="sxs-lookup"><span data-stu-id="6ee42-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-117">**不支援**</span><span class="sxs-lookup"><span data-stu-id="6ee42-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-118">1</span><span class="sxs-lookup"><span data-stu-id="6ee42-118">1</span></span>

<span data-ttu-id="6ee42-119">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="6ee42-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-120">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="6ee42-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-121">2</span><span class="sxs-lookup"><span data-stu-id="6ee42-121">2</span></span>

<span data-ttu-id="6ee42-122">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="6ee42-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-123">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="6ee42-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-124">8</span><span class="sxs-lookup"><span data-stu-id="6ee42-124">8</span></span>

<span data-ttu-id="6ee42-125">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="6ee42-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-126">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="6ee42-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-127">9</span><span class="sxs-lookup"><span data-stu-id="6ee42-127">9</span></span>

<span data-ttu-id="6ee42-128">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="6ee42-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-129">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="6ee42-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-130">21</span><span class="sxs-lookup"><span data-stu-id="6ee42-130">21</span></span>

<span data-ttu-id="6ee42-131">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="6ee42-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-132">**服務未啟動**</span><span class="sxs-lookup"><span data-stu-id="6ee42-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-133">22</span><span class="sxs-lookup"><span data-stu-id="6ee42-133">22</span></span>

<span data-ttu-id="6ee42-134">用來執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="6ee42-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6ee42-135">**其他**</span><span class="sxs-lookup"><span data-stu-id="6ee42-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="6ee42-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="6ee42-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ee42-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ee42-137">Requirements</span></span>



| <span data-ttu-id="6ee42-138">需求</span><span class="sxs-lookup"><span data-stu-id="6ee42-138">Requirement</span></span> | <span data-ttu-id="6ee42-139">值</span><span class="sxs-lookup"><span data-stu-id="6ee42-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee42-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ee42-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee42-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ee42-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ee42-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ee42-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee42-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ee42-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ee42-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="6ee42-144">Namespace</span></span><br/>                | <span data-ttu-id="6ee42-145">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6ee42-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ee42-146">MOF</span><span class="sxs-lookup"><span data-stu-id="6ee42-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ee42-147"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ee42-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ee42-148">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee42-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee42-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ee42-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ee42-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ee42-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ee42-151">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ee42-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6ee42-152">**Win32 \_ register-scheduledjob**</span><span class="sxs-lookup"><span data-stu-id="6ee42-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

