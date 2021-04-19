---
title: Win32_TerminalServiceSetting 類別的 SetTimeZoneRedirection 方法
description: SetTimeZoneRedirection 方法會設定 TimeZoneRedirection 屬性，以允許用戶端電腦將時區設定重新導向遠端桌面服務會話。
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- SetTimeZoneRedirection 方法遠端桌面服務
- SetTimeZoneRedirection 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetTimeZoneRedirection 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968344"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="ef576-106">Win32 TerminalServiceSetting 類別的 SetTimeZoneRedirection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ef576-106">SetTimeZoneRedirection method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="ef576-107">**SetTimeZoneRedirection** 方法會設定 **TimeZoneRedirection** 屬性，以允許用戶端電腦將時區設定重新導向遠端桌面服務會話。</span><span class="sxs-lookup"><span data-stu-id="ef576-107">The **SetTimeZoneRedirection** method sets the **TimeZoneRedirection** property, which allows the client computer to redirect its time zone settings to the Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef576-108">語法</span><span class="sxs-lookup"><span data-stu-id="ef576-108">Syntax</span></span>


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a><span data-ttu-id="ef576-109">參數</span><span class="sxs-lookup"><span data-stu-id="ef576-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef576-110">*TimeZoneRedirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef576-110">*TimeZoneRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef576-111">**TimeZoneRedirection** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="ef576-111">The new value for the **TimeZoneRedirection** property.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="ef576-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="ef576-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="ef576-113">停用 **TimeZoneRedirection** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ef576-113">Disables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="ef576-114">不會發生時區重新導向。</span><span class="sxs-lookup"><span data-stu-id="ef576-114">No time zone redirection occurs.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="ef576-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="ef576-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="ef576-116">啟用 **TimeZoneRedirection** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ef576-116">Enables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="ef576-117">用戶端的時區會重新導向至會話的時區。</span><span class="sxs-lookup"><span data-stu-id="ef576-117">The client's time zone is redirected to the session's time zone.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef576-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef576-118">Return value</span></span>

<span data-ttu-id="ef576-119">成功時傳回 0;否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ef576-119">Returns 0 on success; otherwise returns a WMI error code.</span></span> <span data-ttu-id="ef576-120">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef576-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef576-121">備註</span><span class="sxs-lookup"><span data-stu-id="ef576-121">Remarks</span></span>

<span data-ttu-id="ef576-122">根據預設，遠端桌面服務會話的時區與遠端桌面工作階段主機 (RD 工作階段主機) server 的時區相同。</span><span class="sxs-lookup"><span data-stu-id="ef576-122">By default, the time zone for the Remote Desktop Services session is the same as the time zone for the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="ef576-123">用戶端電腦無法重新導向時區資訊。</span><span class="sxs-lookup"><span data-stu-id="ef576-123">Client computers cannot redirect time zone information.</span></span>

<span data-ttu-id="ef576-124">如果已停用時區重新導向，則新的會話會繼承伺服器的時區。</span><span class="sxs-lookup"><span data-stu-id="ef576-124">If time zone redirection is disabled, new sessions inherit the server time zone.</span></span> <span data-ttu-id="ef576-125">當會話重新連線時，會話會保留其中斷連線之前的時區。</span><span class="sxs-lookup"><span data-stu-id="ef576-125">When a session reconnects, the session retains the time zone it had prior to disconnecting.</span></span>

<span data-ttu-id="ef576-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ef576-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ef576-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ef576-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ef576-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ef576-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ef576-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="ef576-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef576-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef576-130">Requirements</span></span>



| <span data-ttu-id="ef576-131">需求</span><span class="sxs-lookup"><span data-stu-id="ef576-131">Requirement</span></span> | <span data-ttu-id="ef576-132">值</span><span class="sxs-lookup"><span data-stu-id="ef576-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef576-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef576-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef576-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef576-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef576-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef576-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef576-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef576-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef576-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="ef576-137">Namespace</span></span><br/>                | <span data-ttu-id="ef576-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ef576-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ef576-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ef576-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef576-140"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef576-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef576-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ef576-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef576-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef576-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef576-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef576-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef576-144">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="ef576-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

