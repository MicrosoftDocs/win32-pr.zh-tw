---
title: Win32_TerminalServiceSetting 類別的 SetDisableForcibleLogoff 方法
description: 不支援這個方法。
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- SetDisableForcibleLogoff 方法遠端桌面服務
- SetDisableForcibleLogoff 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetDisableForcibleLogoff 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465100"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="cf260-106">Win32 TerminalServiceSetting 類別的 SetDisableForcibleLogoff 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cf260-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="cf260-107">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="cf260-107">This method is not supported.</span></span>

<span data-ttu-id="cf260-108">**Windows Vista 和 Windows Server 2008：** 啟用或停用登入主控台的系統管理員是否可以強制登出。</span><span class="sxs-lookup"><span data-stu-id="cf260-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf260-109">語法</span><span class="sxs-lookup"><span data-stu-id="cf260-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="cf260-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf260-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf260-111">*DisableForcibleLogoff* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf260-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf260-112">旗標停用或啟用 **DisableForcibleLogoff** 屬性，以決定是否可以強制登出登入主控台的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="cf260-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="cf260-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="cf260-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="cf260-114">停用屬性。</span><span class="sxs-lookup"><span data-stu-id="cf260-114">Disable the property.</span></span> <span data-ttu-id="cf260-115">已連線的系統管理員可以強制登出。</span><span class="sxs-lookup"><span data-stu-id="cf260-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="cf260-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="cf260-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="cf260-117">啟用屬性。</span><span class="sxs-lookup"><span data-stu-id="cf260-117">Enable the property.</span></span> <span data-ttu-id="cf260-118">無法強制登出連線的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="cf260-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf260-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf260-119">Return value</span></span>

<span data-ttu-id="cf260-120">成功時傳回成功;否則，會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf260-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="cf260-121">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="cf260-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf260-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf260-122">Requirements</span></span>



| <span data-ttu-id="cf260-123">需求</span><span class="sxs-lookup"><span data-stu-id="cf260-123">Requirement</span></span> | <span data-ttu-id="cf260-124">值</span><span class="sxs-lookup"><span data-stu-id="cf260-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf260-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf260-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cf260-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf260-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf260-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf260-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cf260-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf260-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf260-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cf260-129">End of client support</span></span><br/>    | <span data-ttu-id="cf260-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf260-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf260-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cf260-131">End of server support</span></span><br/>    | <span data-ttu-id="cf260-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf260-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf260-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf260-133">Namespace</span></span><br/>                | <span data-ttu-id="cf260-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="cf260-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cf260-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cf260-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf260-136"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf260-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf260-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf260-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf260-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf260-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf260-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf260-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf260-140">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="cf260-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





