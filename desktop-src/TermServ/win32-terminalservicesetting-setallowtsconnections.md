---
title: Win32_TerminalServiceSetting 類別的 SetAllowTSConnections 方法
description: SetAllowTSConnections 方法會允許或拒絕新的遠端桌面連線。 這個方法會據以修改類別的 AllowTSConnections 屬性。
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- SetAllowTSConnections 方法遠端桌面服務
- SetAllowTSConnections 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetAllowTSConnections 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466720"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d1eb5-107">Win32 TerminalServiceSetting 類別的 SetAllowTSConnections 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d1eb5-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d1eb5-108">**SetAllowTSConnections** 方法會允許或拒絕新的遠端桌面連線。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="d1eb5-109">這個方法會據以修改類別的 **AllowTSConnections** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1eb5-110">語法</span><span class="sxs-lookup"><span data-stu-id="d1eb5-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="d1eb5-111">參數</span><span class="sxs-lookup"><span data-stu-id="d1eb5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1eb5-112">*AllowTSConnections* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1eb5-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1eb5-113">指定是否允許新的遠端桌面連線。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="d1eb5-114">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="d1eb5-115"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="d1eb5-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="d1eb5-116">不允許新的連接。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-116">New connections are not allowed.</span></span> <span data-ttu-id="d1eb5-117">如果 *ModifyFirewallException* 參數為1，則會停用遠端桌面防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="d1eb5-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="d1eb5-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="d1eb5-119">允許新的連接。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-119">New connections are allowed.</span></span> <span data-ttu-id="d1eb5-120">如果 *ModifyFirewallException* 參數為1，則會啟用遠端桌面防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d1eb5-121">*ModifyFirewallException* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1eb5-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1eb5-122">指定是否要將遠端桌面的防火牆例外狀況設定修改為 *AllowTSConnections* 參數所指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="d1eb5-123">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="d1eb5-124"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="d1eb5-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="d1eb5-125">請勿修改防火牆例外狀況設定。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="d1eb5-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="d1eb5-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="d1eb5-127">修改防火牆例外狀況設定。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1eb5-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1eb5-128">Return value</span></span>

<span data-ttu-id="d1eb5-129">成功時傳回成功;否則，會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="d1eb5-130">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="d1eb5-131">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1eb5-132">備註</span><span class="sxs-lookup"><span data-stu-id="d1eb5-132">Remarks</span></span>

<span data-ttu-id="d1eb5-133">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d1eb5-134">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d1eb5-135">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d1eb5-136">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d1eb5-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1eb5-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1eb5-137">Requirements</span></span>



| <span data-ttu-id="d1eb5-138">需求</span><span class="sxs-lookup"><span data-stu-id="d1eb5-138">Requirement</span></span> | <span data-ttu-id="d1eb5-139">值</span><span class="sxs-lookup"><span data-stu-id="d1eb5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1eb5-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1eb5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d1eb5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1eb5-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1eb5-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1eb5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d1eb5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1eb5-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1eb5-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1eb5-144">Namespace</span></span><br/>                | <span data-ttu-id="d1eb5-145">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d1eb5-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d1eb5-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d1eb5-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1eb5-147"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1eb5-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1eb5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d1eb5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1eb5-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1eb5-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1eb5-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1eb5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1eb5-151">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="d1eb5-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

