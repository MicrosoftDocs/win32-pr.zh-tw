---
title: Win32_TSSessionSetting 類別的 TimeLimit 方法
description: 設定配置給指定之會話限制類型的時間上限。
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- TimeLimit 方法遠端桌面服務
- TimeLimit 方法遠端桌面服務，Win32_TSSessionSetting 類別
- Win32_TSSessionSetting 類別遠端桌面服務，TimeLimit 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508320"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="bd276-106">Win32 TSSessionSetting 類別的 TimeLimit 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bd276-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="bd276-107">設定配置給指定之會話限制類型的時間上限。</span><span class="sxs-lookup"><span data-stu-id="bd276-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd276-108">語法</span><span class="sxs-lookup"><span data-stu-id="bd276-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="bd276-109">參數</span><span class="sxs-lookup"><span data-stu-id="bd276-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd276-110">*SessionLimitType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd276-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd276-111">指定方法設定的會話限制屬性類型。</span><span class="sxs-lookup"><span data-stu-id="bd276-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="bd276-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="bd276-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="bd276-113">方法正在設定 **ActiveSessionLimit** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bd276-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="bd276-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="bd276-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="bd276-115">方法正在設定 **DisconnectedSessionLimit** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bd276-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="bd276-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="bd276-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="bd276-117">方法正在設定 **IdleSessionLimit** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bd276-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bd276-118">*ValueLimit* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd276-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd276-119">*SessionLimitType* 參數所指定之屬性的新最大時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd276-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="bd276-120">零值表示沒有會話限制。</span><span class="sxs-lookup"><span data-stu-id="bd276-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd276-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd276-121">Return value</span></span>

<span data-ttu-id="bd276-122">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bd276-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bd276-123">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="bd276-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="bd276-124">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bd276-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd276-125">備註</span><span class="sxs-lookup"><span data-stu-id="bd276-125">Remarks</span></span>

<span data-ttu-id="bd276-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="bd276-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bd276-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="bd276-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bd276-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="bd276-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bd276-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="bd276-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd276-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd276-130">Requirements</span></span>



| <span data-ttu-id="bd276-131">需求</span><span class="sxs-lookup"><span data-stu-id="bd276-131">Requirement</span></span> | <span data-ttu-id="bd276-132">值</span><span class="sxs-lookup"><span data-stu-id="bd276-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd276-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd276-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bd276-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd276-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd276-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd276-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bd276-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd276-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd276-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd276-137">Namespace</span></span><br/>                | <span data-ttu-id="bd276-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="bd276-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bd276-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bd276-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd276-140"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd276-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd276-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bd276-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd276-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd276-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd276-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd276-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd276-144">**Win32 \_ TSSessionSetting**</span><span class="sxs-lookup"><span data-stu-id="bd276-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

