---
description: 啟動目前註冊此進程的偵錯工具。
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Win32_Process 類別的 AttachDebugger 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 041bdeeab634ebed5c7ec2eccffe01f7cecce709
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847116"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a><span data-ttu-id="bedd4-103">Win32 進程類別的 AttachDebugger 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bedd4-103">AttachDebugger method of the Win32\_Process class</span></span>

<span data-ttu-id="bedd4-104">**AttachDebugger** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會啟動目前已針對此進程註冊的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="bedd4-104">The **AttachDebugger** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method starts the debugger that is currently registered for this process.</span></span>

<span data-ttu-id="bedd4-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="bedd4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bedd4-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="bedd4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bedd4-107">語法</span><span class="sxs-lookup"><span data-stu-id="bedd4-107">Syntax</span></span>


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a><span data-ttu-id="bedd4-108">參數</span><span class="sxs-lookup"><span data-stu-id="bedd4-108">Parameters</span></span>

<span data-ttu-id="bedd4-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bedd4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bedd4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bedd4-110">Return value</span></span>

<span data-ttu-id="bedd4-111">傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="bedd4-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="bedd4-112">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="bedd4-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bedd4-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="bedd4-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bedd4-114">**成功完成**</span><span class="sxs-lookup"><span data-stu-id="bedd4-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-115">0</span><span class="sxs-lookup"><span data-stu-id="bedd4-115">0</span></span>

<span data-ttu-id="bedd4-116">順利完成。</span><span class="sxs-lookup"><span data-stu-id="bedd4-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="bedd4-117">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="bedd4-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-118">2</span><span class="sxs-lookup"><span data-stu-id="bedd4-118">2</span></span>

<span data-ttu-id="bedd4-119">使用者無法存取所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="bedd4-119">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="bedd4-120">**許可權不足**</span><span class="sxs-lookup"><span data-stu-id="bedd4-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-121">3</span><span class="sxs-lookup"><span data-stu-id="bedd4-121">3</span></span>

<span data-ttu-id="bedd4-122">使用者沒有足夠的許可權。</span><span class="sxs-lookup"><span data-stu-id="bedd4-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="bedd4-123">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="bedd4-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-124">8</span><span class="sxs-lookup"><span data-stu-id="bedd4-124">8</span></span>

<span data-ttu-id="bedd4-125">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="bedd4-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="bedd4-126">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="bedd4-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-127">9</span><span class="sxs-lookup"><span data-stu-id="bedd4-127">9</span></span>

<span data-ttu-id="bedd4-128">指定的路徑不存在。</span><span class="sxs-lookup"><span data-stu-id="bedd4-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="bedd4-129">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="bedd4-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-130">21</span><span class="sxs-lookup"><span data-stu-id="bedd4-130">21</span></span>

<span data-ttu-id="bedd4-131">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="bedd4-131">The specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bedd4-132">**其他**</span><span class="sxs-lookup"><span data-stu-id="bedd4-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="bedd4-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="bedd4-133">22 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bedd4-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="bedd4-134">Requirements</span></span>



| <span data-ttu-id="bedd4-135">需求</span><span class="sxs-lookup"><span data-stu-id="bedd4-135">Requirement</span></span> | <span data-ttu-id="bedd4-136">值</span><span class="sxs-lookup"><span data-stu-id="bedd4-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bedd4-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bedd4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bedd4-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bedd4-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bedd4-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bedd4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bedd4-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bedd4-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bedd4-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="bedd4-141">Namespace</span></span><br/>                | <span data-ttu-id="bedd4-142">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bedd4-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bedd4-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bedd4-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bedd4-144"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bedd4-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bedd4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bedd4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bedd4-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bedd4-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bedd4-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bedd4-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="bedd4-148">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bedd4-148">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bedd4-149">**Win32 \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="bedd4-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

