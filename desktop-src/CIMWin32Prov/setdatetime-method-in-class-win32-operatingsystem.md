---
description: SetDateTime&\# 8194;WMI 類別方法會在電腦上設定目前的系統時間。
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 SetDateTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001322"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="bc1e3-103">Win32 作業系統類別的 SetDateTime 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bc1e3-103">SetDateTime method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="bc1e3-104">**SetDateTime** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會設定電腦上目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-104">The **SetDateTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the current system time on the computer.</span></span>

<span data-ttu-id="bc1e3-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bc1e3-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc1e3-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc1e3-107">Syntax</span></span>


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a><span data-ttu-id="bc1e3-108">參數</span><span class="sxs-lookup"><span data-stu-id="bc1e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc1e3-109">*>datetimeoffset.localdatetime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc1e3-109">*LocalDatetime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc1e3-110">目前時間的值。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-110">Value of the current time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc1e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc1e3-111">Return value</span></span>

<span data-ttu-id="bc1e3-112">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="bc1e3-113">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-113">Any other number indicates an error.</span></span> <span data-ttu-id="bc1e3-114">如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-114">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bc1e3-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bc1e3-116">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="bc1e3-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc1e3-117">**其他** (1 4294967295) </span><span class="sxs-lookup"><span data-stu-id="bc1e3-117">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bc1e3-118">備註</span><span class="sxs-lookup"><span data-stu-id="bc1e3-118">Remarks</span></span>

<span data-ttu-id="bc1e3-119">呼叫進程必須具有 SE \_ SYSTEMTIME \_ NAME 許可權。</span><span class="sxs-lookup"><span data-stu-id="bc1e3-119">The calling process must have the SE\_SYSTEMTIME\_NAME privilege.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc1e3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc1e3-120">Requirements</span></span>



| <span data-ttu-id="bc1e3-121">需求</span><span class="sxs-lookup"><span data-stu-id="bc1e3-121">Requirement</span></span> | <span data-ttu-id="bc1e3-122">值</span><span class="sxs-lookup"><span data-stu-id="bc1e3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc1e3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc1e3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc1e3-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc1e3-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc1e3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc1e3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc1e3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc1e3-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc1e3-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc1e3-127">Namespace</span></span><br/>                | <span data-ttu-id="bc1e3-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bc1e3-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bc1e3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="bc1e3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc1e3-130"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc1e3-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc1e3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bc1e3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc1e3-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc1e3-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc1e3-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc1e3-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc1e3-134">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc1e3-134">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bc1e3-135">**Win32 \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="bc1e3-135">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="bc1e3-136">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="bc1e3-136">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

